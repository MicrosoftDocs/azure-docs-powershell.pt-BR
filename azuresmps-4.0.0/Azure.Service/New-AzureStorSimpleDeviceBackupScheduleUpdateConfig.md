---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945524"
---
# New-AzureStorSimpleDeviceBackupScheduleUpdateConfig

## Sinopse
Cria um objeto de configuração de atualização de agendamento de backup.

## SYNTAX

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cria um objeto de configuração **BackupScheduleUpdateRequest** .
Use este objeto de configuração para atualizar uma política de backup usando o cmdlet **set-AzureStorSimpleDeviceBackupPolicy** .

## EXEMPLOS

### Exemplo 1: criar uma solicitação de atualização de agendamento
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

Esse comando cria uma solicitação de atualização de agendamento de backup para o cronograma que tem a ID especificada.
A solicitação é fazer o cronograma de um backup de instantâneo na nuvem que se repete a cada hora.
Os backups são mantidos por 50 dias.
Este cronograma está habilitado do tempo padrão, que é a hora atual.

## OS

### -Backuptype
Especifica o tipo de backup.
Os valores válidos são: LocalSnapshot e CloudSnapshot.

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

### Habilitado para o
Indica se o agendamento de backup deve ser habilitado.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Especifica a ID da instância do agendamento de backup a ser atualizado.

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

### -RecurrenceType
Especifica o tipo de recorrência para este agendamento de backup.
Os valores válidos são: 

- Minutos
- Por hora
- Daily
- Mensal

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

### -Recorrência
Especifica com que frequência fazer um backup.
Esse parâmetro usa a unidade especificada pelo parâmetro *RecurrenceType* .

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionCount
Especifica o número de dias para manter um backup.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartFromDateTime
Especifica a data a partir da qual começar a fazer backups.
O valor padrão é a hora atual.

```yaml
Type: String
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

### BackupScheduleUpdateRequest
Esse cmdlet retorna um objeto **BackupScheduleUpdateRequest** que contém informações sobre agendas de backup atualizadas.

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)


