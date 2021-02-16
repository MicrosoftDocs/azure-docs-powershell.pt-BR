---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118476"
---
# Módulo Az.HDInsight
## Descrição
Os tópicos neste documento de seção são os cmdlets do Azure PowerShell do Microsoft Azure HDInsight na estrutura do Gerenciador de Recursos do Azure (ARM). Esses cmdlets são usados para gerenciar clusters HDInsight e os trabalhos executados neles. Os cmdlets existem no namespace Microsoft.Azure.Commands.HDInsight.

## Az.HDInsight Cmdlets
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Adiciona uma identidade de cluster a um objeto de configuração de cluster.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Adiciona uma versão para um serviço em execução em um cluster a um objeto de configuração de cluster.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Adiciona uma personalização de valor de configuração hadoop e/ou uma personalização de biblioteca compartilhada de Colmeia a um objeto de configuração de cluster.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Adiciona um banco de dados SQL para servir como uma Metadados ou Metadados Oozie a um objeto de configuração de cluster.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Adiciona uma ação de script a um objeto de configuração de cluster.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Adiciona um perfil de segurança a um objeto de configuração de cluster.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Adiciona uma chave de Armazenamento do Azure a um objeto de configuração de cluster.

### [Desabilitar-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Desabilita o monitoramento em um cluster HDInsight, e logs relevantes deixarão de fluir para o espaço de trabalho de monitoramento especificado durante a habilitação.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Habilita o monitoramento em um cluster HDInsight, e logs relevantes serão enviados para o espaço de trabalho de monitoramento especificado durante a habilitação.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Obtém e lista todos os clusters HDInsight do Azure associados à assinatura atual ou a um grupo de recursos especificado, ou recupera um cluster específico.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Obtém a configuração de escala automática do cluster HDInsight.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Lista os hosts do cluster HDInsight.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Obtém a lista de trabalhos de um cluster e os lista em ordem cronológica inversa ou recupera um trabalho específico.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Obtém a saída de log de um trabalho da conta de armazenamento associada a um cluster especificado.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Obtém o status de monitoramento da instalação no cluster.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Obtém as ações de script persistentes de um cluster e as lista em ordem cronológica ou obtém detalhes de uma ação de script persistente especificada.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Obtém propriedades sobre o serviço HDInsight, como locais e capacidade disponíveis.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Obtém o histórico de ações de script para um cluster e o lista em ordem cronológica inversa ou obtém detalhes de uma ação de script executada anteriormente.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Envia uma consulta Descarrilhado a um cluster HDInsight e recupera os resultados da consulta em uma única operação.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Cria um cluster HDInsight do Azure no grupo de recursos especificado para a assinatura atual.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Cria um objeto não persistente que descreve a configuração de escala automática de um cluster HDInsight do Azure.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Cria uma condição de escala automática baseada em cronograma.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster HDInsight do Azure.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Cria um objeto de trabalho de Colmeia.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Cria um objeto de trabalho MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Cria um objeto de trabalho de leitões.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Cria um objeto de trabalho Sqoop.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Cria um objeto de trabalho Streaming MapReduce.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Remove o cluster HDInsight especificado da assinatura atual.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Remove a configuração de escala automática do cluster HDInsight.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Remove uma ação de script persistente de um cluster HDInsight.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Reinicia os hosts específicos do cluster HDInsight.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Define a configuração de escala automática de um cluster HDInsight do Azure.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Gira a chave de criptografia de disco do cluster HDInsight especificado.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Define o número de nós de Trabalhador em um cluster especificado.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Define a configuração de conta de armazenamento padrão em um objeto de configuração de cluster.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Define as credenciais HTTP do gateway de um cluster HDInsight do Azure.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Define uma ação de script executada anteriormente como uma ação de script persistente.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Inicia um trabalho HDInsight do Azure definido em um cluster especificado.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Interrompe um trabalho de execução especificado em um cluster.

### [Enviar-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Envia uma nova ação de script para um cluster HDInsight do Azure.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Seleciona um cluster a ser usado com Invoke-RmAzureHDInsightHiveJob cmdlet.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Aguarda a conclusão ou a falha de um trabalho especificado.

