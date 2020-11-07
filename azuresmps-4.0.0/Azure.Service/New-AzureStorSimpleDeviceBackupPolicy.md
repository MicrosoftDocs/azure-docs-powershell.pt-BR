---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946208"
---
# New-AzureStorSimpleDeviceBackupPolicy

## Sinopse
Cria uma política de backup.

## SYNTAX

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorSimpleDeviceBackupPolicy** cria uma política de backup.
Uma política de backup contém uma ou mais agendas de backup que podem ser executadas em um ou mais volumes.
Para criar um agendamento de backup, use o cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

## EXEMPLOS

### Exemplo 1: criar uma política de backup
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

O primeiro comando cria um objeto de configuração de agendamento de backup usando o cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** e, em seguida, armazena esse objeto na variável $Schedule 01.

O segundo comando cria outro objeto de configuração de backup usando **New-AzureStorSimpleDeviceBackupScheduleAddConfig** e, em seguida, armazena esse objeto na variável $Schedule 02.

O terceiro comando cria uma variável de matriz vazia, chamada $ScheduleArray.
Os próximos dois comandos adicionam os objetos criados nos dois primeiros comandos para $ScheduleArray.

O sexto comando obtém um contêiner de volume para o dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** e armazena esse objeto de contêiner na variável $DeviceContainer.

O sétimo comando obtém um volume do contêiner de volume armazenado no primeiro membro de $DeviceContainer usando o cmdlet **Get-AzureStorSimpleDeviceVolume** e, em seguida, armazena esse volume na variável $volume.

O oitavo comando cria uma variável de matriz vazia, chamada $VolumeArray.
O próximo comando adiciona uma ID de volume a $VolumeArray.
Esse valor identifica o volume, armazenado em $Volume, no qual a política de backup é executada.
Você pode adicionar IDs de volume adicionais a $VolumeArray.

O comando final cria a política de backup chamada GeneralPolicy07 para o dispositivo chamado Contoso63-AppVm.
O comando especifica os objetos de configuração de agendamento armazenados em $ScheduleArray.
O comando especifica o volume ou os volumes aos quais aplicar a política em $VolumeArray.
Você pode verificar a política de backup usando o cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .

## OS

### -BackupPolicyName
Especifica o nome da política de backup.

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

### -BackupSchedulesToAdd
Especifica uma matriz de objetos **BackupScheduleBase** para adicionar à política.
Cada objeto representa um cronograma.
Uma política de backup contém um ou mais cronogramas.
Para obter um objeto **BackupScheduleBase** , use o cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Especifica o nome do dispositivo StorSimple no qual criar a política de backup.

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

### -VolumeIdsToAdd
Especifica uma matriz das IDs dos volumes a serem adicionados à política de backup.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
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

### Nenhuma

## EXIBE

### BackupPolicy
Esse cmdlet retorna um objeto **BackupPolicy** que contém os novos cronogramas e volumes.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[New-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


