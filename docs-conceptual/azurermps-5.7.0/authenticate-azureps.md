---
title: Entrar com o Azure PowerShell
description: Como entrar com o Azure PowerShell como um usuário, a entidade de serviço, ou com o MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: af39fec226492c9ccf251c996b57e274de783178
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100266"
---
# <a name="sign-in-with-azure-powershell"></a>Entrar com o Azure PowerShell

O Azure PowerShell dá suporte a vários métodos de autenticação. É a maneira mais simples para entrar interativamente na linha de comando.

## <a name="sign-in-interactively"></a>Entrar no modo interativo

Para entrar no modo interativo, use o cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell
Connect-AzureRmAccount
```

Quando executado, esse cmdlet exibirá uma caixa de diálogo solicitando seu endereço de email e a senha associados à sua conta do Azure. Quando você autenticar, essas informações são salvas para a sessão atual do PowerShell, a caixa de diálogo é fechada e você tem acesso a todos os cmdlets do Azure PowerShell.

> [!IMPORTANT]
> Essa entrada é _somente_ para a sessão atual do PowerShell. Para manter a autenticação em várias sessões, consulte o artigo sobre [Credenciais Persistentes](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Entrar com uma entidade de serviço

As entidades de serviço oferecem uma maneira de criar contas não interativas para manipular recursos. As entidades de serviço são como as contas de usuário às quais você pode aplicar regras usando o Azure Active Directory. Ao conceder as permissões mínimas necessárias para uma entidade de serviço, você pode garantir que seus scripts de automação fiquem ainda mais seguros.

Se precisar criar uma entidade de serviço para usar com o Azure PowerShell, confira [Criar uma entidade de serviço do Azure com o Azure PowerShell](create-azure-service-principal-azureps.md).

Para entrar com uma entidade de serviço, use o cmdlet `-ServicePrincipal`argumento com o `Connect-AzureRmAccount`. Você também precisará da ID do aplicativo da entidade de serviço, credenciais de entrada e da ID de locatário associada à entidade de serviço. Para obter as credenciais da entidade de serviço como o objeto apropriado, use o cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Esse cmdlet exibirá uma caixa de diálogo para inserir a ID de usuário da entidade de serviço e a senha.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>Entre usando uma Identidade de Serviço Gerenciada da VM do Azure

A Identidade do Serviço Gerenciado (MSI) é a versão prévia de um recurso para o Azure Active Directory. Você pode usar uma entidade de serviço do MSI para conexão e adquirir um token de acesso somente de aplicativo para acessar outros recursos. A MSI só está disponível em máquinas virtuais em execução em uma nuvem do Azure.

Para obter mais informações sobre o MSI, consulte [Como usar uma Identidade de Serviço Gerenciado (MSI) da VM do Azure para conexão e aquisição de token](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="sign-in-to-another-cloud"></a>Entre em outra Nuvem

Os serviços de nuvem do Azure oferecem ambientes diferentes que estão de acordo com as regulamentações de manipulação de dados de diversas regiões. Caso sua conta do Azure esteja em uma nuvem associada a uma dessas regiões, será necessário especificar o ambiente ao se conectar. Por exemplo, se sua conta está na nuvem da China, faça logon usando o seguinte comando:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Use o seguinte comando para obter uma lista de ambientes disponíveis:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Saiba mais sobre como gerenciar o acesso baseado em função do Azure

Para obter mais informações sobre o gerenciamento de autenticação e assinatura no Azure, consulte [Gerenciar contas, assinaturas e funções administrativas](/azure/active-directory/role-based-access-control-configure) (a página pode estar em inglês).

Cmdlets do Azure PowerShell para gerenciamento de função:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
