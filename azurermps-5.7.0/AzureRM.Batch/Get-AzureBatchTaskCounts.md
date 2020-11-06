---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtaskcounts
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTaskCounts.md
ms.openlocfilehash: d0b98081675cd11d8d3eb60a6495ac87a1111034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427687"
---
# Get-AzureBatchTaskCounts

## Sinopse
Obtém as contagens de tarefas para o trabalho especificado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### %
```
Get-AzureBatchTaskCounts [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

### ParentObject
```
Get-AzureBatchTaskCounts [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>]
```

## DESCRITIVO
O cmdlet **Get-AzureBatchTaskCounts** Obtém a contagem de tarefas em lotes do Azure para um trabalho em lotes.
Especifique um trabalho pelo parâmetro *JobID* ou por meio do parâmetro *Job* .
Contagens de tarefas fornecem uma contagem das tarefas por meio do estado de tarefa ativo, em execução ou concluído, e uma contagem de tarefas que tiveram êxito ou falharam. As tarefas no estado preparação são contadas como em execução. Se o validationStatus for Unvalidated, o serviço em lotes não poderá verificar contagens de estado em relação ao estado da tarefa como relatado na API de tarefas da lista. A validationStatus pode ser desvalidada se o trabalho contiver mais de 200.000 tarefas.

## EXEMPLOS

### Exemplo 1: obter contagens de tarefas por ID
```
PS C:\> Get-AzureBatchTaskCounts -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Esse comando obtém a contagem de tarefas para o job Job01.
Use o cmdlet Get-AzureRmBatchAccountKeys para atribuir um contexto para a variável $Context.

## OS

### -BatchContext
A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.
Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.
Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.
Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.
Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trabalho
Especifica o trabalho que contém as tarefas obtidas por esse cmdlet.
Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzureBatchJob.

```yaml
Type: PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
A ID do trabalho para o qual obter contagens de tarefas.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## SENSORES

### System. String
Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext


## EXIBE

### Microsoft.Azure.Commands.Batch. Modelos. PSTaskCounts


## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchJob](./Get-AzureBatchJob.md)

[Cmdlets do Azure batch](./AzureRM.Batch.md)
