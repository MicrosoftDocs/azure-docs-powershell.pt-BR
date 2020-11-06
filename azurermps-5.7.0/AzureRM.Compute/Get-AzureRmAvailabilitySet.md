---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431075"
---
# Get-AzureRmAvailabilitySet

## Sinopse
Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmAvailabilitySet** Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.
Você pode especificar o nome de um conjunto de disponibilidade específico para obter.

## EXEMPLOS

### Exemplo 1: obter um conjunto de disponibilidade específico
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

Esse comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11.

### Exemplo 2: obter todos os conjuntos de disponibilidade
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

Esse comando obtém todos os conjuntos de disponibilidade no grupo de recursos chamado ResourceGroup11.

## OS

### -Nome
Especifica o nome de um conjunto de disponibilidade que este cmdlet obtém.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmAvailabilitySet](./New-AzureRmAvailabilitySet.md)

[Remove-AzureRmAvailabilitySet](./Remove-AzureRmAvailabilitySet.md)


