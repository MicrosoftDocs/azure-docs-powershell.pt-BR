---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426664"
---
# Test-AzureRmPowerBIEmbeddedCapacity

## Sinopse
Testa a existência de uma instância da capacidade inserida do PowerBI.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Test-AzureRmPowerBIEmbeddedCapacity testa a existência de uma instância da capacidade inserida do PowerBI

## EXEMPLOS

### Exemplo 1
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

Esse comando testará se há uma capacidade chamada testcapacity

## OS

### -Nome
Nome da capacidade inserida do PowerBI

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmPowerBIEmbeddedCapacity](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[Remove-AzureRmPowerBIEmbeddedCapacity](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
