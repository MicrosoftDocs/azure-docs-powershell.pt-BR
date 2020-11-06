---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609602"
---
# Get-AzureRmRecoveryServicesAsrServicesProvider

## Sinopse
Obtém os detalhes dos provedores de serviços de recuperação ASR registrados no cofre de serviços de recuperação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Padrão (padrão)
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRecoveryServicesAsrServicesProvider** Obtém informações sobre os provedores do Azure site Recovery no cofre.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

Liste todos os provedores de serviços de replicação ASR registrados no cofre de serviços de recuperação correspondente à malha especificada.

## OS

### -Fabric
Especifica o objeto de malha ASR.

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FriendlyName
Especifica o nome amigável do provedor de serviços de recuperação ASR para o qual obter detalhes.

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do provedor de serviços de recuperação ASR para o qual obter detalhes.

```yaml
Type: String
Parameter Sets: ByName
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

### Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric

## EXIBE

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMA

## LINKS RELACIONADOS

[Remove-AzureRmRecoveryServicesAsrServicesProvider](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[Update-AzureRmRecoveryServicesAsrServicesProvider](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
