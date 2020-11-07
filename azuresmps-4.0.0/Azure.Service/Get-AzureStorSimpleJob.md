---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945558"
---
# Get-AzureStorSimpleJob

## Sinopse
Obtém trabalhos do StorSimple.

## SYNTAX

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorSimpleJob** Obtém trabalhos do Azure StorSimple.
Especifique uma ID de instância para obter um trabalho específico.
Especifique outros parâmetros para limitar os trabalhos que esse cmdlet obtém.

Este cmdlet retorna um máximo de 200 trabalhos.
Se houver mais de 200 trabalhos, obtenha os trabalhos restantes usando os parâmetros *First* e *Skip* .
Se você especificar um valor de 100 para *Skip* e 50 para *primeiro* , esse cmdlet não retornará os primeiros resultados de 100.
Ele retorna os próximos 50 resultados após o 100 que ele ignora.

## EXEMPLOS

### Exemplo 1: obter um trabalho usando uma ID
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

Esse comando obtém informações para o trabalho que tem a ID especificada.

### Exemplo 2: obter trabalhos usando um nome de dispositivo
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

Esse comando obtém informações para os trabalhos do dispositivo chamado 8600-bravo 001.
O comando obtém os dois primeiros trabalhos do dispositivo.

### Exemplo 3: obter trabalhos concluídos
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

Este comando obtém trabalhos concluídos.
O comando obtém apenas os dois primeiros trabalhos depois de ignorar os dez primeiros trabalhos.

### Exemplo 4: obter trabalhos de backup manuais
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

Esse comando obtém os trabalhos do tipo de backup manual.

### Exemplo 5: obter trabalhos entre horários especificados
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

Os dois primeiros comandos criam objetos **DateTime** usando o cmdlet Get-Date.
Os comandos armazenam os novos horários nas variáveis $StartTime e $EndTime.
Para obter mais informações, digite `Get-Help Get-Date` .

O comando final Obtém trabalhos para o dispositivo chamado Device07 entre os horários armazenados em $StartTime e $EndTime.

## OS

### -DeviceName
Especifica o nome de um dispositivo StorSimple.

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

### -Primeiro
Obtém apenas o número especificado de objetos.
Digite o número de objetos a serem obtidos.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -De
Especifica a data e a hora de início dos trabalhos que esse cmdlet obtém.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Especifica a ID do trabalho a ser obtido.

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

### -Skip
Ignora o número especificado de objetos e obtém os objetos restantes.
Digite o número de objetos a serem ignorados.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Especifica o status.
Os valores aceitáveis para esse parâmetro são:

- Executando
- Feito
- Cela
- Conseguiu
- Cancelamento
- CompletedWithErrors

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

### -To
Especifica a data e a hora de término dos trabalhos que este cmdlet obtém.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de trabalho.
Os valores aceitáveis para esse parâmetro são:

- Fazer
- ManualBackup
- Restaurar
- CloneWorkflow
- DeviceRestore
- Atualização
- SupportPackage
- VirtualApplianceProvisioning

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
Não é possível canalizar a entrada para este cmdlet.

## EXIBE

### IList \<DeviceJobDetails\> , DeviceJobDetails
Esse cmdlet retorna uma lista de objetos de detalhes do trabalho ou, se você especificar o parâmetro *InstanceId* , ele retornará um único objeto de detalhes do trabalho.

## INFORMA

## LINKS RELACIONADOS

[Parar-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


