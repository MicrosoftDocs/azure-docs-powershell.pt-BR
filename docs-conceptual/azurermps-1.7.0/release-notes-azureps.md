---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c821153db7fb2c337e936abbd8ebb8c848069415
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

## <a name="version-170"></a>Versão 1.7.0

* **Alteração de comportamento para os parâmetros -Force, -Confirm e $ConfirmPreference de todos os cmdlets. Estamos alterando essa implementação para estar alinhada com as diretrizes do PowerShell. Para a maioria dos cmdlets, isso significa remover o parâmetro Force e ignorar o prompt ShouldProcess. Os usuários precisarão incluir o parâmetro ‘-Confirm:$false’ em seus scripts do PowerShell.** Essas alterações estão abordando os seguintes problemas:
  - implementação correta da funcionalidade –WhatIf, que permite ao usuário determinar os efeitos de um cmdlet ou script sem fazer nenhuma alteração real
  - controle sobre a solicitação usando um $ConfirmPreference de toda a sessão, para que o usuário seja solicitado com base no impacto de uma alteração em potencial (conforme relatado na configuração ConfirmImpact no cmdlet)
  - controle específico do cmdlet sobre as solicitações de confirmação usando o parâmetro –Confirm
  - uso consistente de ShouldContinue e do parâmetro –Force nos cmdlets, apenas para as ações que exigem solicitar ao usuário devido à natureza especial das alterações (por exemplo, exclusão de arquivos ocultos)
  - consistência com outros cmdlets do PowerShell, para que esse conhecimento de script do PowerShell em relação a outros cmdlets seja imediatamente aplicável aos cmdlets do Azure PowerShell.

**Observe que agora para ignorar *automaticamente todas as Solicitações em todas as Circunstâncias*, os cmdlets do Azure PowerShell exigem que o usuário forneça dois parâmetros:**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Computação do Azure
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Parâmetro -Redeploy de Restart-AzureVM
  - Parâmetro -Validate para Move-AzureService, Move-AzureStorageAccount, e Move-AzureVirtualNetwork
  - Os parâmetros name e version dos cmdlets de extensão são opcionais como antes.
  - New-AzureVM pode obter um tipo de licença no objeto de VM.
* Armazenamento do Azure
  - Alterar o Parâmetro Tags para Tag e adicionar as Marcas de alias do parâmetro
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Rede do Azure
  - Novo cmdlet adicionado para emparelhamento da Rede Virtual
* Cache Redis do Azure
  - Novo cmdlet adicionado para Reset-AzureRmRedisCache
  - Novo cmdlet adicionado para Export-AzureRmRedisCache
  - Novo cmdlet adicionado para Import-AzureRmRedisCache
  - Cmdlet New-AzureRmRedisCache modificado para incluir a alteração do parâmetro para vNet
* Backup/Restauração do Banco de Dados SQL Azure
  - Cmdlets para o recurso de backup LTR (Retenção de Longo Prazo)
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Restore-AzureRmSqlDatabase agora oferece suporte à restauração pontual de um banco de dados excluído
  - Restore-AzureRmSqlDatabase agora oferece suporte à restauração de um backup de Retenção de Longo Prazo
* LogicApp do Azure
  - Cmdlets adicionados das contas de Integração do LogicApp.
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Repositório Azure Data Lake
  - Melhore drasticamente o desempenho do arquivo, o carregamento e o download da pasta.
  - Isso inclui uma pequena mudança nos nomes do parâmetro para download e a inclusão de dois parâmetros novos para carregar:
    + NumThreads -> PerFileThreadCount, usados para indicar o número de threads a usar em um único arquivo
    + ConcurrentFileCount, usado para indicar o número de arquivos para carregar/baixar em paralelo para o upload/download de uma pasta.
  - Os valores de threading padrão agora são projetados para oferecer uma melhor taxa de transferência para a maioria dos tamanhos de arquivo. Se o desempenho não for o desejado, os valores acima poderão ser modificados para atender aos requisitos.
* Análise Azure Data Lake
  - Get-AzureRMDataLakeAnalyticsDataSource agora retorna todas as fontes de dados quando chamado sem argumentos.
  - Essa alteração também remove do cmdlet o parâmetro do tipo da fonte de dados.
  - Essa alteração resulta em um novo objeto sendo retornado para a operação de lista com as seguintes propriedades:
    + Type, o tipo da fonte de dados
    + Name, o nome da fonte de dados
    + IsDefault, definido para true se esta for a fonte de dados padrão da conta
  - Get-AzureRMDataLakeAnalyticsJob corrigido para a lista de certos valores de deslocamento de data e hora ao filtrar em submittedBefore e submittedAfter.
* Aplicativos Web
  - Adicionar o cmdlet Swap-AzureRmWebAppSlot de troca regular e trocar pela visualização
  - Estender o cmdlet Set-AzureRmWebAppSlot para oferecer suporte à troca automática
* Gerenciamento de API do Azure
  - Cmdlets de Implantação do Gerenciamento de Api do Azure corrigidos para o AzureChinaCloud.
  - O cmdlet Set-AzureRmApiManagementTenantGitAccess removido como Acesso ao Git é habilitado por Padrão.
* Backup dos Serviços de Recuperação do Azure
  - Suporte adicionado para a carga de trabalho do SQL Azure
  - Suporte adicionado para o backup e a restauração das VMs criptografadas do Azure
  - Backup-AzureRmRecoveryServicesBackupItem - recurso do tempo de retenção opcional adicionado para os pontos de recuperação
  - Correções menores do bug relacionado ao filtro nos cmdlets Get-AzureRmRecoveryServicesBackupContainer e Get-AzureRmRecoveryServicesBackupItem
* Automação do Azure
  - Get-AzureRmAutomationHybridWorkerGroup adicionado
