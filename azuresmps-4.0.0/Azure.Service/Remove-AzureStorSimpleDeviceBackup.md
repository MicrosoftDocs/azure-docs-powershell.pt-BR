---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946467"
---
# Remove-AzureStorSimpleDeviceBackup

## Sinopse
Exclui um objeto de backup.

## SYNTAX

### IdentifyById (padrão)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureStorSimpleDeviceBackup** exclui um único objeto de backup.
Se você tentar excluir um backup que já foi excluído, esse cmdlet retornará um erro.

## EXEMPLOS

### Exemplo 1: remover um backup de um dispositivo
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

Esse comando Remove o backup com a ID especificada para o dispositivo chamado Contoso63-AppVm.
O comando inicia a operação que remove o objeto **backup** e, em seguida, retorna um objeto **TaskResponse** .
Para ver o status da tarefa, use o cmdlet **Get-AzureStorSimpleTask** .

### Exemplo 2: remover o primeiro backup de um dispositivo usando sua ID
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

O primeiro comando obtém os backups do dispositivo chamado Contoso63-AppVm e, em seguida, os armazena na variável $Backup.

O segundo comando exclui um backup do dispositivo chamado Contoso63-AppVm.
O comando usa a notação de ponto padrão para se referir à propriedade **InstanceId** do primeiro elemento da matriz de $backup.
Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .

### Exemplo 3: remover o primeiro backup de um dispositivo usando o pipeline
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

O primeiro comando obtém os backups do dispositivo chamado Contoso63-AppVm e, em seguida, os armazena na variável $Backup.

O segundo comando passa o primeiro objeto armazenado na matriz $Backup para o cmdlet atual.
Esse cmdlet exclui o backup do dispositivo chamado Contoso63-AppVm.
Esse comando especifica o parâmetro *WaitForComplete* e, portanto, o comando aguarda até que a operação seja concluída e, em seguida, retorna um objeto **TaskStatusInfo** .

## OS

### -Backup
Especifica o objeto de **backup** a ser excluído.
Para obter um objeto de **backup** , use o cmdlet **Get-AzureStorSimpleDeviceBackup** .

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupId
Especifica a ID de instância de um backup a ser excluído.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Especifica o nome do dispositivo StorSimple no qual excluir um backup.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### Fazer

## EXIBE

### TaskStatusInfo, TaskResponse
Esse cmdlet retorna um objeto **TaskStatusInfo** se você especificar o parâmetro *WaitForComplete* se você não especificar esse parâmetro, ele retornará um objeto **TaskResponse** .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


