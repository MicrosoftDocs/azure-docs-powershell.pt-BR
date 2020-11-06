---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 8e3633e88bc3c0972df0d667ed1002571d5ec142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427689"
---
# Get-AzureBatchSubtask

## Sinopse
Obtém as informações de subtarefas da tarefa especificada.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ODataFilter (padrão)
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureBatchSubtask** recupera as informações de subtarefas sobre a tarefa especificada.
As subtarefas fornecem processamento paralelo para tarefas individuais e permitem o monitoramento preciso da execução e do progresso da tarefa.

## EXEMPLOS

### Exemplo 1: retornar todas as subtarefas de uma tarefa especificada
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

Esses comandos retornam todas as subtarefas da tarefa com a ID MyTask.
Para fazer isso, o primeiro comando do exemplo cria uma referência de objeto para as chaves de conta do contosobatchaccount da conta em lotes.
Essa referência de objeto é armazenada em uma variável chamada $context.

Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzureBatchSubtask** para retornar todas as subtarefas de MyTask, uma tarefa que é executada como parte do trabalho do trabalho-01.

## OS

### -BatchContext
Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.
Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes. Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas. Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão. Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.

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

### -JobId
Especifica a ID do trabalho que contém a tarefa cujas subtarefas esse cmdlet obtém.

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Especifica o número máximo de subtarefas a serem retornadas.
Se você especificar um valor igual a zero (0) ou menos, o cmdlet não usará um limite superior.
O valor padrão é 1000.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tarefa
Especifica uma referência de objeto para a tarefa que contém as subtarefas que esse cmdlet retorna.
Essa referência de objeto é criada usando-se o cmdlet Get-AzureBatchTask e armazenando o objeto retornado em uma variável.

```yaml
Type: PSCloudTask
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
Especifica a ID da tarefa cujas subtarefas esse cmdlet retorna.

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### BatchAccountContext
O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline

### PSCloudTask
O parâmetro ' Task ' aceita o valor do tipo ' PSCloudTask ' da pipeline

## EXIBE

###  
Esse cmdlet retorna instâncias do objeto **PSSubtaskInformation** .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureBatchTask](./Get-AzureBatchTask.md)


