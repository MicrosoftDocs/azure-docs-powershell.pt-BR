---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945552"
---
# Get-AzureStorSimpleTask

## Sinopse
Obtém o status de uma tarefa em um dispositivo StorSimple.

## SYNTAX

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorSimpleTask** recupera o status de uma tarefa que é executada assincronamente em um dispositivo Azure StorSimple.

Embora você gerencie um dispositivo StorSimple, a maioria das ações criar, ler, atualizar e excluir pode ser executada de forma assíncrona.
O Windows PowerShell retorna uma **TaskId**.
Use a ID para obter o status atual da tarefa.

## EXEMPLOS

### Exemplo 1: obter o status de uma tarefa
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

Esse comando obtém o status da tarefa com a ID especificada.
Os resultados mostram que a tarefa tem o status concluído e um resultado de êxito.

## OS

### -InstanceId
Especifica a ID da tarefa para a qual esse cmdlet rastreia o status.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### JobStatusInfo
Esse cmdlet retorna um objeto **TaskStatusInfo** que contém os seguintes campos: 

- **Erro**.
**ErrorDetails** , que contém **código** e **mensagem**.
- **TaskId**.
**Cadeia de caracteres**.
A ID da tarefa para a qual o status é retornado.
- **TaskSteps**.
**IList \<TaskStep\>**.
Cada objeto **TaskStep** contém **detalhe** , **ErrorCode** , **mensagem** , **resultado** e **status**.
- **Resultado**.
**TaskResult** , que contém o resultado geral da tarefa.
Os valores válidos são: falha, êxito, PartialSuccess, cancelado e inválido.
- **Status**.
**TaskStatus** , que contém o status geral de execução da tarefa.
Os valores válidos são: InProgress, invalide e Completed.
- **TaskResult**.
**TaskResult** , um valor calculado com base em **resultado** e **status**.
Os valores válidos são: falha, êxito, InProgress, PartialSuccess, cancelado e inválido.

## INFORMA

## LINKS RELACIONADOS

