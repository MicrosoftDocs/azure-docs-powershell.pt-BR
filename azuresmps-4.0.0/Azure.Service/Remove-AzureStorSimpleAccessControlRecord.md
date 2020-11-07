---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946096"
---
# Remove-AzureStorSimpleAccessControlRecord

## Sinopse
Exclui um registro de controle de acesso da configuração do serviço.

## SYNTAX

### IdentifyByName
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureStorSimpleAccessControlRecord** exclui um registro de controle de acesso da configuração do serviço.

## EXEMPLOS

### Exemplo 1: remover um controle de recordaccess de controle de Controlaccess de acesso
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

Esse comando exclui o registro de controle de acesso chamado Acr10.
Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .

### Exemplo 2: remover um registro de controle de Controlaccess de acesso usando o controle Controlaccess Controlaccess de pipelineAccess
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

Esse comando usa **Get-AzureStorSimpleAccessControlRecord** para obter o **AccessControlRecord** chamado Acr10 e, em seguida, passa o objeto para o cmdlet atual usando o operador pipeline.
O comando inicia a operação que remove o objeto **AccessControlRecord** e, em seguida, retorna um objeto **TaskResponse** .
Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .

## OS

### -ACR
Especifica um objeto **AccessControlRecord** a ser excluído.
Para obter um objeto **AccessControlRecord** , use o cmdlet **Get-AzureStorSimpleAccessControlRecord** .

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ACRName
Especifica um nome do registro de controle de acesso a ser excluído.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indica que esse cmdlet não solicita confirmação.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica um perfil do Azure.

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

### -WaitForComplete
Indica que esse cmdlet aguarda a conclusão da operação antes de retornar o controle ao console do Windows PowerShell.

```yaml
Type: SwitchParameter
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

### AccessControlRecord
Esse cmdlet aceita um objeto **AccessControlRecord** .
Um objeto **AccessControlRecord** contém os seguintes campos: 

- **GlobalId** ( **cadeia** ) 
- **Initiatorname** ( **cadeia de caracteres** ) 
- **InstanceId** ( **cadeia** ) 
- **Name** ( **cadeia** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## EXIBE

### TaskStatusInfo, TaskResponse
Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* .
Se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[New-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


