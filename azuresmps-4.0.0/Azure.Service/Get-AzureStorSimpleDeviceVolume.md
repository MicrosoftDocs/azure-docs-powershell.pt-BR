---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945566"
---
# Get-AzureStorSimpleDeviceVolume

## Sinopse
Obtém volumes em um dispositivo.

## SYNTAX

### IdentifyByParentObject
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorSimpleDeviceVolume** Obtém uma lista de volumes para um contêiner de volume especificado ou um volume que tem o nome especificado.
O objeto retornado contém as seguintes propriedades: 

- **AccessType**
- **AcrList**
- **AppType**
- **DataContainer**
- **Datacontainerid**
- **Instância**
- **IsBackupEnabled**
- **IsDefaultBackupEnabled**
- **IsMonitoringEnabled**
- **Sobrenome**
- **Internet**
- **OperationInProgress**
- **SizeInBytes**
- **VSN**

## EXEMPLOS

### Exemplo 1: obter volumes em um contêiner especificado
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

Esse comando obtém o contêiner de volume chamado Container03 no dispositivo chamado Contoso63-AppVm usando o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .
O comando usa o operador pipeline para passar esse contêiner para o cmdlet atual.
Esse cmdlet obtém todos os volumes nesse contêiner para o dispositivo chamado Contoso63-AppVm.

### Exemplo 2: obter um volume usando seu nome
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

Esse comando obtém o volume chamado Volume18 no dispositivo chamado Contoso63-AppVm.

## OS

### -DeviceName
Especifica o nome do dispositivo StorSimple do qual obter volumes.

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

### -VolumeContainer
Especifica o contêiner de volume, como um objeto **DataContainer** , que inclui os volumes a serem obtidos.
Para obter um **DataContainer** , use o cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VolumeName
Especifica o nome do volume a ser obtido.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### DataContainer
Esse cmdlet aceita um objeto **DataContainer** que contém o volume a obter.

## EXIBE

### VirtualDisk, IList\<VirtualDisk\>
Esse cmdlet retorna um objeto **VirtualDisk** se você especificar o parâmetro *VolumeName* .
Se você especificar o *VolumeContainer* , este cmdlet retornará um **objeto \<VirtualDisk\> IList** .

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorSimpleDeviceVolume](./New-AzureStorSimpleDeviceVolume.md)

[Remove-AzureStorSimpleDeviceVolume](./Remove-AzureStorSimpleDeviceVolume.md)

[Set-AzureStorSimpleDeviceVolume](./Set-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


