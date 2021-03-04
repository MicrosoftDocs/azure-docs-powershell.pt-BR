---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 0c8773066f39d11e6985bbe4bd1f1e69cd9142f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890327"
---
# Módulo Az.Accounts
## Descrição
Gerencia credenciais e configurações comuns para todos os módulos do Azure.

## Az.Accounts Cmdlets
### [Add-AzEnvironment](Add-AzEnvironment.md)
Adiciona pontos de extremidade e metadados para uma instância do Gerenciador de Recursos do Azure.

### [Clear-AzContext](Clear-AzContext.md)
Remova todas as credenciais, contas e informações de assinatura do Azure.

### [Clear-AzDefault](Clear-AzDefault.md)
Limpa os padrões definidos pelo usuário no contexto atual.

### [Connect-AzAccount](Connect-AzAccount.md)
Conecte-se ao Azure com uma conta autenticada para uso com cmdlets dos módulos do Az PowerShell.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Desativar a autosaving credenciais do Azure.  Suas informações de logon serão esquecidas na próxima vez que você abrir uma janela do PowerShell

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Opta por não coletar dados para melhorar os cmdlets do Azure PowerShell. Os dados são coletados por padrão, a menos que você opte explicitamente.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Desabilita aliases de prefixo do AzureRm para módulos do Az.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Desconecta uma conta do Azure conectada e remove todas as credenciais e contextos associados a essa conta.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
Os contextos do Azure são objetos do PowerShell que representam sua assinatura ativa para executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure. Com os contextos do Azure, o Azure PowerShell não precisa reauthenticar sua conta sempre que você trocar de assinatura. Para obter mais informações, consulte [objetos de contexto do Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).

Esse cmdlet permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente ao iniciar um processo do PowerShell. Por exemplo, ao abrir uma nova janela.

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com os cmdlets do Azure PowerShell. A execução desse cmdlet opta pela coleta de dados para o usuário atual no computador atual. Os dados são coletados por padrão, a menos que você opte explicitamente.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Habilita aliases de prefixo do AzureRm para módulos do Az.

### [Get-AzAccessToken](Get-AzAccessToken.md)
Obter token de acesso bruto. Ao usar -ResourceUrl, verifique se o valor corresponderá ao ambiente atual do Azure. Você pode se referir ao valor de `(Get-AzContext).Environment` .

### [Get-AzContext](Get-AzContext.md)
Obtém os metadados usados para autenticar solicitações do Gerenciador de Recursos do Azure.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
Exibe metadados sobre o recurso de autosave de contexto, incluindo se o contexto é salvo automaticamente e onde as informações de contexto e credencial salvas podem ser encontradas.

### [Get-AzDefault](Get-AzDefault.md)
Obter os padrões definidos pelo usuário no contexto atual.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Obter pontos de extremidade e metadados para uma instância dos serviços do Azure.

### [Get-AzSubscription](Get-AzSubscription.md)
Obter assinaturas que a conta atual pode acessar.

### [Get-AzTenant](Get-AzTenant.md)
Obtém locatários autorizados para o usuário atual.

### [Import-AzContext](Import-AzContext.md)
Carrega informações de autenticação do Azure de um arquivo.

### [Invoke-AzRestMethod](Invoke-AzRestMethod.md)
Construir e executar solicitação HTTP somente para o ponto de extremidade de gerenciamento de recursos do Azure

### [Register-AzModule](Register-AzModule.md)
SOMENTE PARA USO INTERNO - Fornecer suporte ao tempo de execução para cmdlets Gerados pelo AutoRest

### [Remove-AzContext](Remove-AzContext.md)
Remover um contexto do conjunto de contextos disponíveis

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Remove pontos de extremidade e metadados para se conectar a uma determinada instância do Azure.

### [Renomear-AzContext](Rename-AzContext.md)
Renomeie um contexto do Azure.  Por padrão, os contextos são nomeados por conta de usuário e assinatura.

### [Resolve-AzError](Resolve-AzError.md)
Exibir informações detalhadas sobre erros do PowerShell, com detalhes estendidos para erros do Azure PowerShell.

### [Save-AzContext](Save-AzContext.md)
Salva as informações de autenticação atuais para uso em outras sessões do PowerShell.

### [Select-AzContext](Select-AzContext.md)
Selecione uma assinatura e uma conta para direcionar nos cmdlets do Azure PowerShell

### [Send-Feedback](Send-Feedback.md)
Envia comentários para a equipe do Azure PowerShell por meio de um conjunto de prompts guiados.

### [Set-AzContext](Set-AzContext.md)
Define o locatário, a assinatura e o ambiente para cmdlets a usar na sessão atual.

### [Set-AzDefault](Set-AzDefault.md)
Define um padrão no contexto atual

### [Set-AzEnvironment](Set-AzEnvironment.md)
Define propriedades para um ambiente do Azure.

### [Uninstall-AzureRm](Uninstall-AzureRm.md)
Remove todos os módulos do AzureRm de um computador.

