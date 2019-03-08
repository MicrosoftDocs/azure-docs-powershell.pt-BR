---
title: Manter credenciais do usuário entre as sessões do PowerShell
description: Aprenda a reutilizar as credenciais do Azure e outras informações em várias sessões do PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8702de48429482748939fb1a43ff911bed15f6c0
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837224"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a>Manter credenciais do usuário entre as sessões do PowerShell

O Azure PowerShell oferece um recurso chamado **Salvamento Automático do contexto do Azure**, que oferece os seguintes recursos:

- Retenção das informações de conexão para a reutilização em novas sessões do PowerShell.
- Facilitar o uso de tarefas em segundo plano para executar os cmdlets de execução longa.
- Alterne contas, assinaturas e ambientes sem usar credenciais separadas.
- Execução de tarefas usando credenciais e assinaturas diferentes, simultaneamente, a partir da mesma sessão do PowerShell.

## <a name="azure-contexts-defined"></a>Contextos do Azure definidos

Um *contexto do Azure* é um conjunto de informações que define o destino de cmdlets do Azure PowerShell. O contexto consiste em cinco partes:

- Uma *Conta* - a entidade de serviço ou o nome de usuário usado para autenticar a comunicação com o Azure
- Uma *Assinatura* - a assinatura do Azure com os recursos que estão sendo tratados.
- Um *Locatário* - o locatário do Azure Active Directory que contém sua assinatura. Os Locatários são mais importantes para a autenticação ServicePrincipal.
- Um *Ambiente* - a nuvem de destino específica do Azure, normalmente a nuvem global do Azure.
  No entanto, a configuração do ambiente também permite usar nuvens nacionais, governamentais e locais (Azure Stack) como destino.
- *Credenciais* - as informações usadas pelo Azure para verificar sua identidade e confirmar sua autorização para acessar recursos no Azure

Com a versão mais recente do Azure PowerShell, os Contextos do Azure podem ser salvos automaticamente sempre que uma nova sessão do PowerShell for aberta.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>Salvar automaticamente o contexto para a próxima conexão

O Azure PowerShell retém suas informações do contexto automaticamente entre as sessões. Para configurar o PowerShell para esquecer o contexto e as credenciais, use `Disable-AzContextAutoSave`. Com o salvamento de contexto desabilitado, você precisará entrar no Azure sempre que abrir uma sessão do PowerShell.

Para permitir que o Azure PowerShell se lembre do seu contexto depois que a sessão do PowerShell for fechada, use `Enable-AzContextAutosave`. As informações de contexto e as credenciais são salvas automaticamente em uma pasta oculta especial no diretório de usuário (`$env:USERPROFILE\.Azure` no Windows e `$HOME/.Azure` em outras plataformas). Cada nova sessão do PowerShell terá como alvo o contexto usado na última sessão.

Os cmdlets que permitem gerenciar contextos do Azure também permitem um controle refinado. Se quiser que as alterações sejam aplicadas somente à sessão atual do PowerShell (escopo `Process`) ou em cada sessão do PowerShell (escopo `CurrentUser`). Essas opções são analisadas com mais detalhes em [Usando Escopos de Contexto](#Using-Context-Scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Executar os cmdlets do Azure PowerShell como trabalhos em segundo plano

O recurso de **Salvamento Automático de Contexto do Azure** também permite compartilhar seu contexto com trabalhos em segundo plano do PowerShell. O PowerShell permite iniciar e monitorar tarefas de execução longa como trabalhos em segundo plano sem a necessidade de aguardar a conclusão das tarefas. Você pode compartilhar as credenciais com trabalhos em segundo plano de duas maneiras diferentes:

- Transmitir o contexto como um argumento

  A maioria dos cmdlets do AzureRM permite passar o contexto como um parâmetro para o cmdlet. Você pode passar um contexto para um trabalho em segundo plano, conforme mostrado no exemplo a seguir:

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- Usando o contexto padrão com Salvamento Automático habilitado

  Se você tiver habilitado o **Salvamento Automático de Contexto**, os trabalhos em segundo plano automaticamente usarão o contexto padrão salvo.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

Quando precisar saber o resultado da tarefa em segundo plano, use `Get-Job` para verificar o status do trabalho e `Wait-Job` para aguardar a conclusão do trabalho. Use `Receive-Job` para capturar ou exibir a saída do trabalho em segundo plano. Para obter mais informações, consulte [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Criando, selecionando, renomeando e removendo contextos

Para criar um contexto, você deve entrar no Azure. O cmdlet `Connect-AzAccount` (ou seu alias, `Login-AzAccount`) define o contexto padrão usado pelos cmdlets do Azure PowerShell e deixa que você acesse qualquer locatário ou assinatura permitida por suas credenciais.

Para adicionar um novo contexto após a conexão, use `Set-AzContext` (ou seu alias, `Select-AzSubscription`).

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

O exemplo anterior adiciona um novo contexto com 'Assinatura Contoso 1' como destino usando suas credenciais atuais. O novo contexto é denominado 'Contoso1'. Se você não fornecer um nome para o contexto, será usado um nome padrão usando a ID da conta e a ID da assinatura.

Para renomear um contexto já existente, use o cmdlet `Rename-AzContext`. Por exemplo: 

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

Este exemplo renomeia o contexto com o nome automático `[user1@contoso.org; 123456-7890-1234-564321]` por um nome simples nome 'Contoso2'. Os cmdlets que gerenciam contextos também usam o preenchimento de guia e isso permite escolher rapidamente o contexto.

E, por último, para remover um contexto, use o cmdlet `Remove-AzContext`.  Por exemplo: 

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

Você se esquece do contexto que foi nomeado 'Contoso2'. É possível recriar este contexto usando `Set-AzContext`

## <a name="removing-credentials"></a>Removendo credenciais

Você pode remover todas as credenciais e contextos associados de um usuário ou entidade de serviço usando `Disconnect-AzAccount` (também conhecido como `Logout-AzAccount`). Quando executado sem parâmetros, o cmdlet `Disconnect-AzAccount` remove todas as credenciais e contextos associados ao usuário ou entidade de serviço no contexto atual. Você pode passar um Nome de Usuário, o Nome da Entidade de Serviço ou o Contexto para uma determinada entidade de destino.

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Usando escopos de contexto

Ocasionalmente, convém selecionar, alterar ou remover um contexto em uma sessão do PowerShell sem afetar outras sessões. Para alterar o comportamento padrão dos cmdlets de contexto, use o parâmetro `Scope`. O escopo `Process` substitui o comportamento padrão aplicando-o apenas à sessão atual. Por outro lado, o escopo `CurrentUser` altera o contexto em todas as sessões, em vez de apenas a sessão atual.

Por exemplo, para alterar o contexto padrão na sessão atual do PowerShell sem afetar outras janelas ou o contexto usado na próxima vez em que uma sessão for aberta, use:

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Como a configuração de salvamento automático de contexto é lembrada

A configuração de Salvamento Automático de contexto é salva no diretório do usuário do Azure PowerShell (`$env:USERPROFILE\.Azure` no Windows e `$HOME/.Azure` em outras plataformas). Alguns tipos de contas de computador podem não ter acesso a esse diretório. Para esses cenários, você pode usar a variável de ambiente

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Quando definido como “true”, o contexto é salvo automaticamente. Se definido como “false”, o contexto não é salvo.

## <a name="context-management-cmdlets"></a>Cmdlets de gerenciamento de contexto

- [Enable-AzContextAutosave][enable]: permite salvar o contexto entre sessões do PowerShell.
  Qualquer alteração feita afetará o contexto global.
- [Disable-AzContextAutosave][disable]: desativa o salvamento automático do contexto. É necessário entrar novamente em cada nova sessão do PowerShell.
- [Select-AzContext][select]: seleciona um contexto como o padrão. Todos os cmdlets usam as credenciais neste contexto para autenticação.
- [Disconnect-AzAccount][remove-cred]: remove todas as credenciais e contextos associados a uma conta.
- [Remove-AzContext][remove-context]: remove um contexto nomeado.
- [Rename-AzContext][rename]: renomeia um contexto existente.
- [Add-AzAccount][login]: permite o escopo da conexão para o processo ou o usuário atual.
  Permite nomear o contexto padrão após a autenticação.
- [Import-AzContext][import]: permite o escopo da conexão para o processo ou o usuário atual.
- [Set-AzContext][set-context]: permite a seleção de contextos nomeados existentes e alterações no escopo do processo ou do usuário atual.

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext