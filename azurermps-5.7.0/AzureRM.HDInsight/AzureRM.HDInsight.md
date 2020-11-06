---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: ed52eb21cfa5d192e4d7d0d79a2dc0847a5fd3ee
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425280"
---
# Módulo AzureRM. HDInsight
## Descritivo
Os tópicos desta seção documentam os cmdlets do PowerShell do Azure para o Microsoft Azure HDInsight na estrutura ARM (Azure Resource Manager). Esses cmdlets são usados para gerenciar clusters HDInsight e os trabalhos que são executados neles. Os cmdlets existem no namespace Microsoft. Azure. Commands. HDInsight.

## Cmdlets do AzureRM. HDInsight
### [Add-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
Adiciona uma identidade de cluster a um objeto de configuração de cluster.

### [Add-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
Adiciona uma versão de um serviço em execução em um cluster a um objeto de configuração de cluster.

### [Add-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
Adiciona uma personalização de valor de configuração Hadoop e/ou uma personalização de biblioteca compartilhada de Hive a um objeto de configuração de cluster.

### [Add-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Adiciona um banco de dados SQL para servir como Hive ou Oozie metastore para um objeto de configuração de cluster.

### [Add-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Adiciona uma ação de script a um objeto de configuração de cluster.

### [Add-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Adiciona um objeto de segurança de um objeto de configuração de cluster.

### [Add-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Adiciona uma chave de armazenamento do Azure a um objeto de configuração de cluster.

### [Disable-AzureRmHDInsightOperationsManagementSuite](Disable-AzureRmHDInsightOperationsManagementSuite.md)
Desabilita o OMS (Operations Management Suite) em um cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho do OMS especificado durante a ativação.

### [Enable-AzureRmHDInsightOperationsManagementSuite](Enable-AzureRmHDInsightOperationsManagementSuite.md)
Habilita o OMS (Operations Management Suite) em um cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho do OMS especificado durante a ativação.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
Obtém e lista todos os clusters do Azure HDInsight associados à assinatura atual ou um grupo de recursos especificado ou recupera um cluster específico.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Obtém a lista de trabalhos de um cluster e os lista em ordem cronológica inversa ou recupera um trabalho específico.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
Obtém a saída do log para um trabalho da conta de armazenamento associada a um cluster especificado.

### [Get-AzureRmHDInsightOperationsManagementSuite](Get-AzureRmHDInsightOperationsManagementSuite.md)
Obtém o status da instalação do Operations Management Suite (OMS) no cluster.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Obtém as ações de script persistente para um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificado.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
Obtém as propriedades sobre o serviço HDInsight, como locais e capacidade disponíveis.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Obtém o histórico de ação de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.

### [Grant AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
Concede acesso HTTP ao cluster.

### [Grant AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
Concede acesso RDP ao cluster do Windows.

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
Envia uma consulta Hive para um cluster HDInsight e recupera resultados de consulta em uma operação.

### [New-AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Cria um cluster do Azure HDInsight no grupo de recursos especificado para a assinatura atual.

### [New-AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.

### [New-AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Cria um objeto de trabalho Hive.

### [New-AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
Cria um objeto de trabalho MapReduce.

### [New-AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Cria um objeto de trabalho porco.

### [New-AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Cria um objeto de trabalho Sqoop.

### [New-AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Cria um objeto de trabalho de MapReduce de fluxo contínuo.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Remove o cluster HDInsight especificado da assinatura atual.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Remove uma ação de script persistente de um cluster HDInsight.

### [REVOKE-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Desabilita o acesso HTTP ao cluster.

### [REVOKE-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Desabilita o acesso do RDP a um cluster do Windows.

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
Define o número de nós de trabalho em um cluster especificado.

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Define a configuração da conta de armazenamento padrão em um objeto de configuração de cluster.

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Define uma ação de script executada anteriormente para ser uma ação de script persistente.

### [Start-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Inicia um trabalho do Azure HDInsight definido em um cluster especificado.

### [Parar-AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Interrompe um trabalho em execução especificado em um cluster.

### [Enviar-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Envia uma nova ação de script para um cluster do Azure HDInsight.

### [Use-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Seleciona um cluster para ser usado com o cmdlet Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
Aguarda a conclusão ou a falha de um trabalho especificado.

