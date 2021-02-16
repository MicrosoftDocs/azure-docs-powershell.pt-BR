---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117965"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## Sinopse
Obtém o status de preparação e liberação de tarefas em lotes.

## Sintaxe

### ID (Padrão)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Inputobject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzBatch JobPreparationAndReleaseTaskStatus** obtém o status de tarefa de preparação e lançamento de tarefas em lote do Azure Batch.
Você deve fornecer o parâmetro *ID* ou uma **instância do PSCloudCloudCloud para** este cmdlet.

## Exemplos

### Exemplo 1: Obter o status de preparação e liberação de um trabalho
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Esse comando obtém o status de preparação e liberação da tarefa para o trabalho "Teste".
Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context dados.

### Exemplo 2: Obter o status de preparação e liberação de um trabalho com Filtrar e Selecionar especificado
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Este comando obtém o status da tarefa de preparação e liberação do trabalho "Teste" no nó "tvm-2316545714_1-20170613t201733z" e usa a cláusula Select para especificar apenas as informações jobPreparationTaskExecutionInformation

## Parâmetros

### -BatchContext
A instância BatchAccountContext a ser usada ao interagir com o serviço Lote.
Use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expandir
Especifica uma cláusula de expansão do Open Data Protocol (OData).
Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtro
Especifica uma cláusula de filtro OData.
Se você não especificar um filtro, esse cmdlet retornará toda a preparação do trabalho e liberará o status da tarefa para o trabalho.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Especifica a ID do trabalho cujas tarefas de preparação e lançamento devem ser recuperadas.
Não é possível especificar caracteres curinga.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Especifica um objeto **PSCloudCloud Que** representa o trabalho para obter o status da tarefa de preparação e lançamento.
Para obter um **objeto PSCloudCloud,** use Get-AzBatchJob cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Especifica o número máximo de trabalhos de preparação e liberação do status da tarefa' a ser retornado.
Se você especificar um valor zero (0) ou menos, o cmdlet não usará um limite superior.
O valor padrão é 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Selecionar
Especifica uma cláusula de seleção OData.
Especifique um valor para esse parâmetro para obter propriedades específicas, em vez de todas as propriedades do objeto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.Batch. Models.PSCloudCloud

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## Saídas

### Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation

## Notas

## LINKS RELACIONADOS

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlets de lote do Azure](/powershell/module/Az.Batch/)
