---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945575"
---
# Get-AzureSiteRecoveryStorageMapping

## Sinopse
Obtém mapeamentos de objetos de armazenamento de recuperação de site para um cofre.

## SYNTAX

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSiteRecoveryStorageMapping** Obtém mapeamentos dos objetos de armazenamento do Azure site Recovery para o cofre do Azure site Recovery atual.

## EXEMPLOS

### Exemplo 1: obter o mapeamento entre um objeto de armazenamento e um objeto de armazenamento de recuperação
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .
O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.

O segundo comando obtém o mapeamento entre dois objetos de armazenamento do Azure.
O comando especifica o servidor primário para o mapeamento do objeto de armazenamento como o primeiro elemento de $Servers.
O comando especifica o servidor para o objeto de armazenamento de recuperação como o segundo elemento de $Servers.

## OS

### -PrimaryServer
Especifica o servidor primário.
Para obter um servidor, use o cmdlet **Get-AzureSiteRecoveryServer** .

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

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

### -RecoveryServer
Especifica o servidor de recuperação.
Para obter um servidor, use **Get-AzureSiteRecoveryServer**.

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)

[New-AzureSiteRecoveryStorageMapping](./New-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


