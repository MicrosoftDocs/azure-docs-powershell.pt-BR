---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtaskcount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTaskCount.md
ms.openlocfilehash: f339e315f025dff921687730d9211c5b049c0f59
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93947264"
---
# Get-AzBatchTaskCount

## Sinopse
Obtém as contagens de tarefas para o trabalho especificado.

## SYNTAX

### %
```
Get-AzBatchTaskCount [-JobId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchTaskCount [[-Job] <PSCloudJob>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzBatchTaskCount** Obtém a contagem de tarefas em lotes do Azure para um trabalho em lotes.
Especifique um trabalho pelo parâmetro *JobID* ou por meio do parâmetro *Job* .
Contagens de tarefas fornecem uma contagem das tarefas por meio do estado de tarefa ativo, em execução ou concluído, e uma contagem de tarefas que tiveram êxito ou falharam. As tarefas no estado preparação são contadas como em execução. Se o validationStatus for Unvalidated, o serviço em lotes não poderá verificar contagens de estado em relação ao estado da tarefa como relatado na API de tarefas da lista. A validationStatus pode ser desvalidada se o trabalho contiver mais de 200.000 tarefas.

## EXEMPLOS

### Exemplo 1: obter contagens de tarefas por ID
```
PS C:\> Get-AzBatchTaskCount -JobId "Job01" -Id "Task03" -BatchContext $Context
Active              : 1
Completed           : 0
Failed              : 0
Running             : 1
Succeeded           : 5
ValidationStatus    : Validated
```

Esse comando obtém a contagem de tarefas para o job Job01.
Use o cmdlet Get-AzBatchAccountKey para atribuir um contexto para a variável $Context.

## OS

### -BatchContext
A instância BatchAccountContext a ser usada ao interagir com o serviço em lotes.
Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.
Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.
Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.
Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.

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
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Trabalho
Especifica o trabalho que contém as tarefas obtidas por esse cmdlet.
Para obter um objeto **PSCloudJob** , use o cmdlet Get-AzBatchJob.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
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
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### Microsoft.Azure.Commands.Batch. Modelos. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## EXIBE

### Microsoft.Azure.Commands.Batch. Modelos. PSTaskCounts

## INFORMA

## LINKS RELACIONADOS

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Cmdlets do Azure batch](/powershell/module/az.batch)
