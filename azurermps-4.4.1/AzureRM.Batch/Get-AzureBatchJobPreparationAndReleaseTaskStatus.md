---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 6c44688bcd11b624738c299dc04c1a0cb0da9494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610843"
---
# Get-AzureBatchJobPreparationAndReleaseTaskStatus

## Sinopse
Obtém o status da tarefa de liberação e preparação do trabalho em lotes.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ID (padrão)
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureBatchJobPreparationAndReleaseTaskStatus** Obtém a preparação do trabalho em lotes do Azure e o status da tarefa de liberação para um trabalho em lotes.
Você deve fornecer o parâmetro *ID* ou uma instância **PSCloudJob** para esse cmdlet.

## EXEMPLOS

### Exemplo 1: obter a preparação do trabalho e o status de lançamento de um trabalho
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Esse comando obtém a preparação do trabalho e o status da tarefa de liberação do trabalho "teste".
Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.

### Exemplo 2: obter a preparação do trabalho e o status de lançamento de um trabalho com filtro e selecionar especificado
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Este comando obtém a preparação do trabalho e o status da tarefa de liberação para o trabalho "Test" no nó "TVM-2316545714_1-20170613t201733z" e usa a cláusula SELECT para especificar a reutilização das informações do JobPreparationTaskExecutionInformation

## OS

### -BatchContext
A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.
Use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.

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

### -Expandir
Especifica uma cláusula de expansão do Open Data Protocol (OData).
Especifique um valor para esse parâmetro para obter entidades associadas da entidade principal que você obtém.

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
Se você não especificar um filtro, esse cmdlet retornará toda a preparação do trabalho e liberar o status da tarefa para o trabalho.

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
Especifica a ID do trabalho cujas tarefas de preparação e liberação devem ser recuperadas.
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
Especifica um objeto **PSCloudJob** que representa o trabalho para obter o status da tarefa de lançamento e preparação de.
Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzureBatchJob.

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
Especifica o número máximo de preparação de trabalhos e o status da tarefa de liberação ' a ser retornado.
Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.
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

### -Selecione
Especifica uma cláusula de seleção OData.
Especifique um valor para esse parâmetro para obter propriedades específicas em vez de todas as propriedades do objeto.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String
Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext

## EXIBE

### Microsoft.Azure.Commands.Batch. Modelos. PSJobPreparationAndReleaseTaskExecutionInformation

## INFORMA

## LINKS RELACIONADOS

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Cmdlets do Azure batch](./AzureRM.Batch.md)
