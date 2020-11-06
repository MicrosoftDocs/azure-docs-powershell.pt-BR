---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 3a28545958e353c5a5523e24baf20ac6bff21ef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609603"
---
# Get-AzureRmRecoveryServicesAsrNetwork

## Sinopse
Obtém informações sobre as redes gerenciadas pela recuperação de site para o cofre atual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByFabricObject (padrão)
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmRecoveryServicesAsrNetwork** Obtém informações sobre as redes de recuperação de site do Azure para o cofre do Azure site Recovery atual.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

Obtém todas as redes conhecidas na malha especificada.

## OS

### -Fabric
Objeto de malha ASR

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
Nome amigável do objeto ASR de rede.

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
Nome do objeto ASR de rede.

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

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMA

## LINKS RELACIONADOS

