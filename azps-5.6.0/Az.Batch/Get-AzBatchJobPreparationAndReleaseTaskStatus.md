---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: e85976b4d4b5de508e1a4f25338b21abdb0c097f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889319"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## SYNOPSIS
Obtém o status da tarefa de preparação e lançamento do trabalho em lotes.

## SINTAXE

### ID (Padrão)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** obtém o status da tarefa de preparação e liberação do trabalho em lote do Azure Batch.
Você deve fornecer o *parâmetro Id* ou uma **instância do PSCloudJob** a este cmdlet.

## EXEMPLOS

### Exemplo 1: Obter o status de preparação e versão do trabalho
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Este comando obtém o status da tarefa de preparação e liberação do trabalho "Test".
Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto à variável $Context.

### Exemplo 2: Obter o status de preparação e versão do trabalho com Filter e Select especificados
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Este comando obtém o status da tarefa de preparação e liberação do trabalho "Test" no nó "tvm-2316545714_1-20170613t201733z" e usa a cláusula Select para especificar apenas retornar as informações JobPreparationTaskExecutionInformation

## PARÂMETROS

### -BatchContext
A instância BatchAccountContext a ser usada ao interagir com o serviço Batch.
Use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.

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
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

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

### -Expand
Especifica uma cláusula de expansão do Protocolo de Dados Abertos (OData).
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

### -Filter
Especifica uma cláusula de filtro OData.
Se você não especificar um filtro, este cmdlet retornará toda a preparação do trabalho e o status da tarefa de versão do trabalho.

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

### -Id
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
Especifica um **objeto PSCloudJob** que representa o trabalho para obter o status da tarefa de preparação e lançamento.
Para obter um **objeto PSCloudJob,** use Get-AzBatchJob cmdlet.

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
Especifica o número máximo de trabalhos de preparação e liberação de status da tarefa' a ser retornada.
Se você especificar um valor zero (0) ou menor, o cmdlet não usará um limite superior.
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

### -Select
Especifica uma cláusula de seleção OData.
Especifique um valor para que esse parâmetro receba propriedades específicas, em vez de todas as propriedades do objeto.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## SAÍDAS

### Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation

## NOTES

## LINKS RELACIONADOS

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlets do Lote do Azure](/powershell/module/Az.Batch/)
