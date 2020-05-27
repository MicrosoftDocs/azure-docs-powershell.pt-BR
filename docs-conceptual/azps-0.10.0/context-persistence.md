---
title: Contextos e credenciais de entrada do Azure
description: Aprenda a reutilizar as credenciais do Azure e outras informações em várias sessões do PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: c79d1d634d5b76b2c6ab6b6ab309c2d49f9f7678
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83385194"
---
# <a name="azure-powershell-context-objects"></a>Objetos de contexto do Azure PowerShell

O Azure PowerShell usa _objetos de contexto do Azure PowerShell_ (contextos do Azure) para armazenar as informações de assinatura e autenticação. Se tiver mais de uma assinatura, os contextos do Azure permitirão que você selecione a assinatura na qual executar os cmdlets do Azure PowerShell. Os contextos do Azure também são usados para armazenar informações de conexão em várias sessões do PowerShell e executar tarefas em segundo plano.

Este artigo aborda o gerenciamento de contextos do Azure, não o gerenciamento de assinaturas ou contas. Se você estiver procurando gerenciar usuários, assinaturas, locatários ou outras informações de conta, confira a documentação do [Azure Active Directory](/azure/active-directory). Para saber mais sobre como usar contextos para executar tarefas em segundo plano ou em paralelo, confira [Usar cmdlets do Azure PowerShell em trabalhos do PowerShell](using-psjobs.md) depois de se familiarizar com os contextos do Azure.

## <a name="overview-of-azure-context-objects"></a>Visão geral de objetos de contexto do Azure

Os contextos do Azure são objetos do PowerShell que representam sua assinatura ativa na qual executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure. Com os contextos do Azure, o Azure PowerShell não precisa autenticar novamente sua conta sempre que você mudar de assinaturas. Um contexto do Azure é composto:

* Pela _conta_ que foi usada para entrar no Azure com [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). Os contextos do Azure tratam usuários, IDs de aplicativo e entidades de serviço da mesma maneira de uma perspectiva de conta.
* Pela _assinatura_ ativa, um contrato de serviço com a Microsoft para criar e executar recursos do Azure, que estão associados a um _locatário_. Os locatários costumam ser chamados de _organizações_ na documentação ou ao trabalhar com o Active Directory.
* Por uma referência a um _cache de token_, um token de autenticação armazenado para acessar uma nuvem do Azure. O local em que esse token é armazenado e por quanto tempo ele persiste é determinado pelas [configurações de salvamento automático de contexto](#save-azure-contexts-across-powershell-sessions).

Para obter mais informações sobre esses termos, confira [Terminologia do Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Os tokens de autenticação usados por contextos do Azure são os mesmos que outros tokens armazenados que fazem parte de uma sessão persistente. 

Quando você entra com `Connect-AzAccount`, pelo menos um contexto do Azure é criado para sua assinatura padrão. O objeto retornado por `Connect-AzAccount` é o contexto padrão do Azure usado para o restante da sessão do PowerShell.

## <a name="get-azure-contexts"></a>Obter contextos do Azure

Os contextos do Azure disponíveis são recuperados com o cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext). Liste todos os contextos disponíveis com `-ListAvailable`:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Ou obtenha um contexto por nome:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

Os nomes de contexto podem ser diferentes do nome da assinatura associada.

> [!IMPORTANT]
> Os contextos do Azure disponíveis __nem__ sempre são suas assinaturas disponíveis. Os contextos do Azure representam apenas informações armazenadas localmente. Você pode obter suas assinaturas com o cmdlet [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).

## <a name="create-a-new-azure-context-from-subscription-information"></a>Criar um contexto do Azure com base em informações de assinatura

O cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) é usado para criar contextos do Azure e defini-los como o contexto ativo.
A maneira mais fácil de criar um contexto do Azure é usar informações de assinatura existentes. O cmdlet é criado para usar o objeto de saída de `Get-AzSubscription` como um valor de pipe e configurar um novo contexto do Azure:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

Ou forneça o nome ou a ID da assinatura e a ID de locatário, se necessário:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Se o argumento `-Name` for omitido, o nome e a ID da assinatura serão usados como o nome do contexto no formato `Subscription Name (subscription-id)`.

## <a name="change-the-active-azure-context"></a>Alterar o contexto do Azure ativo

Tanto `Set-AzContext` quanto [Select-AzContext](/powershell/module/az.accounts/set-azcontext) podem ser usados para alterar o contexto do Azure ativo. Conforme descrito em [Criar um contexto do Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` criará um contexto do Azure para uma assinatura se não existir um e alternará para usar esse contexto como o ativo.

O `Select-AzContext` destina-se a ser usado somente com contextos existentes do Azure e funciona de forma semelhante ao uso de `Set-AzContext -Context`, mas foi projetado para uso com o redirecionamento:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Como muitos outros comandos de gerenciamento de conta e de contexto no Azure PowerShell, `Set-AzContext` e `Select-AzContext` dão suporte ao argumento `-Scope` para que você possa controlar por quanto tempo o contexto está ativo. `-Scope` permite que você altere o contexto ativo de uma única sessão sem alterar o padrão:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

Para evitar alternar contextos para uma sessão inteira do PowerShell, todos os comandos do Azure PowerShell podem ser executados em um contexto determinado com o argumento `-AzContext`:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

O outro uso principal de contextos com cmdlets do Azure PowerShell é executar comandos em segundo plano. Para saber mais sobre como executar Trabalhos do PowerShell usando o Azure PowerShell, confira [Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Salvar contextos do Azure em sessões do PowerShell

Por padrão, os contextos do Azure são salvos para uso entre sessões do PowerShell. Você muda esse comportamento das seguintes maneiras:

* Entre usando o `-Scope Process` com o `Connect-AzAccount`.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  O contexto do Azure retornado como parte dessa entrada é válido _apenas_ para a sessão atual e não será salvo automaticamente, independentemente da configuração de salvamento automático do contexto do Azure PowerShell.
* Desabilite o salvamento automático do contexto do AzurePowershell com o cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).
  Desabilitar o salvamento automático de contexto __não__ limpa os tokens armazenados. Para saber como limpar informações de contexto do Azure armazenadas, confira [Remover contextos e credenciais do Azure](#remove-azure-contexts-and-stored-credentials).
* Habilitar explicitamente o salvamento automático de contexto do Azure pode ser habilitado com o cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave). Com o salvamento automático habilitado, todos os contextos de um usuário são armazenados localmente para sessões posteriores do PowerShell.
* Salve manualmente contextos com [Save-AzContext](/powershell/module/az.accounts/save-azcontext) para serem usados em sessões futuras do PowerShell, em que eles podem ser carregados com [Import-AzContext](/powershell/module/az.accounts/import-azcontext):

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> Desabilitar o salvamento automático de contexto __não__ limpa as informações de contexto armazenadas que foram salvas. Para remover informações armazenadas, use o cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Para saber mais sobre como remover contextos salvos, confira [Remover contextos e credenciais](#remove-azure-contexts-and-stored-credentials).

Cada um desses comandos dá suporte ao parâmetro `-Scope`, que pode usar um valor de `Process` a ser aplicado apenas ao processo de execução atual. Por exemplo, para garantir que contextos recém-criados não sejam salvos após sair de uma sessão do PowerShell:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

As informações de contexto e tokens são armazenados no diretório `$env:USERPROFILE\.Azure` no Windows e no `$HOME/.Azure` em outras plataformas. Informações confidenciais, como IDs de assinatura e IDs de locatário, ainda podem ser expostas em informações armazenadas, por meio de logs ou contextos salvos. Para saber como limpar informações armazenadas, confira a seção [Remover contextos e credenciais](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Remover contextos e credenciais armazenadas do Azure

Para limpar contextos e credenciais do Azure:

* Saia de uma conta com [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).
  Você pode sair de qualquer conta por conta ou contexto:

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  A desconexão sempre remove tokens de autenticação armazenados e limpa contextos salvos associados ao usuário desconectado ou ao contexto.
* Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Esse cmdlet tem a garantia de sempre remover contextos armazenados e tokens de autenticação e também desconectará você.
* Remova um contexto com [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Se remover o contexto ativo, você será desconectado do Azure e precisará autenticar-se novamente com `Connect-AzAccount`.

## <a name="see-also"></a>Confira também

* [Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell](using-psjobs.md)
* [Terminologia do Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Referência Az.Accounts](/powershell/module/az.accounts)
