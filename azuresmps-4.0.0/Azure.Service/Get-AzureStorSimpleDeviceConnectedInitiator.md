---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946291"
---
# Get-AzureStorSimpleDeviceConnectedInitiator

## Sinopse
Obtém as conexões iSCSI disponíveis para um dispositivo StorSimple.

## SYNTAX

### IdentifyById
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorSimpleDeviceConnectedInitiator** Obtém uma lista das conexões iSCSI disponíveis para um dispositivo StorSimple.
Os objetos de conexão iSCSI que este cmdlet retorna contêm as seguintes propriedades:

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Classes**
- **Iqn**
- **IscsiConnectionId**

Este cmdlet obtém o objeto Connection apenas se as conexões iSCSI estiverem ativadas para o dispositivo.
Por padrão, as conexões estão desativadas.

## EXEMPLOS

### Exemplo 1: obter todas as conexões de um dispositivo
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

Esse comando obtém todas as conexões iSCSI para o dispositivo chamado Contoso63-AppVm.
Esse comando retornará as conexões somente se as conexões estiverem ativadas para o dispositivo.

## OS

### -DeviceID
Especifica a ID de instância do dispositivo StorSimple do qual obter iniciadores iSCSI.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Especifica o nome do dispositivo StorSimple do qual obter iniciadores iSCSI.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Programação\<IscsiConnection\>
Esse cmdlet retorna um objeto de conexão iSCSI que contém as seguintes propriedades: 

- **AcrInstanceId**
- **AcrName**
- **AllowedVolumeNames**
- **InitiatorAddress**
- **Classes**
- **Iqn**
- **IscsiConnectionId**

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


