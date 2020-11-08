---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112762"
---
# Módulo AZ. HDInsight
## Descritivo
Os tópicos desta seção documentam os cmdlets do PowerShell do Azure para o Microsoft Azure HDInsight na estrutura ARM (Azure Resource Manager). Esses cmdlets são usados para gerenciar clusters HDInsight e os trabalhos que são executados neles. Os cmdlets existem no namespace Microsoft. Azure. Commands. HDInsight.

## Cmdlets AZ. HDInsight
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Adiciona uma identidade de cluster a um objeto de configuração de cluster.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Adiciona uma versão de um serviço em execução em um cluster a um objeto de configuração de cluster.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Adiciona uma personalização de valor de configuração Hadoop e/ou uma personalização de biblioteca compartilhada de Hive a um objeto de configuração de cluster.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Adiciona um banco de dados SQL para servir como Hive ou Oozie metastore para um objeto de configuração de cluster.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Adiciona uma ação de script a um objeto de configuração de cluster.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Adiciona um perfil de segurança a um objeto de configuração de cluster.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Adiciona uma chave de armazenamento do Azure a um objeto de configuração de cluster.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Desabilita o monitoramento em um cluster HDInsight e os logs relevantes deixarão de fluir para o espaço de trabalho de monitoramento especificado durante a ativação.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Habilita o monitoramento em um cluster HDInsight e os logs relevantes serão enviados para o espaço de trabalho monitoramento especificado durante a ativação.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Obtém e lista todos os clusters do Azure HDInsight associados à assinatura atual ou um grupo de recursos especificado ou recupera um cluster específico.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Obtém a configuração de autoescala do cluster HDInsight.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Lista os hosts do cluster HDInsight.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Obtém a lista de trabalhos de um cluster e os lista em ordem cronológica inversa ou recupera um trabalho específico.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Obtém a saída do log para um trabalho da conta de armazenamento associada a um cluster especificado.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Obtém o status da instalação do monitoramento no cluster.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Obtém as ações de script persistente para um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificado.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Obtém as propriedades sobre o serviço HDInsight, como locais e capacidade disponíveis.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Obtém o histórico de ação de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Envia uma consulta Hive para um cluster HDInsight e recupera resultados de consulta em uma operação.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Cria um cluster do Azure HDInsight no grupo de recursos especificado para a assinatura atual.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Cria um objeto não persistente que descreve a configuração de autoescala de um cluster do Azure HDInsight.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Cria uma condição de autoescala baseada em cronograma.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Cria um objeto de trabalho Hive.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Cria um objeto de trabalho MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Cria um objeto de trabalho porco.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Cria um objeto de trabalho Sqoop.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Cria um objeto de trabalho de MapReduce de fluxo contínuo.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Remove o cluster HDInsight especificado da assinatura atual.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Remove a configuração de autoescala do cluster HDInsight.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Remove uma ação de script persistente de um cluster HDInsight.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Reinicia os hosts específicos do cluster HDInsight.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Define a configuração de autoescala de um cluster do Azure HDInsight.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Gira a chave de criptografia do disco do cluster HDInsight especificado.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Define o número de nós de trabalho em um cluster especificado.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Define a configuração da conta de armazenamento padrão em um objeto de configuração de cluster.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Define as credenciais HTTP do gateway de um cluster do Azure HDInsight.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Define uma ação de script executada anteriormente para ser uma ação de script persistente.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Inicia um trabalho do Azure HDInsight definido em um cluster especificado.

### [Parar-AzHDInsightJob](Stop-AzHDInsightJob.md)
Interrompe um trabalho em execução especificado em um cluster.

### [Enviar-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Envia uma nova ação de script para um cluster do Azure HDInsight.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Seleciona um cluster para ser usado com o cmdlet Invoke-RmAzureHDInsightHiveJob.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Aguarda a conclusão ou a falha de um trabalho especificado.

