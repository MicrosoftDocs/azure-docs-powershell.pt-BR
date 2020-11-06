---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426769"
---
# Update-AzureRmAvailabilitySet

## Sinopse
Atualiza um conjunto de disponibilidade.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SkuParameterSet
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedParamterSet
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureRmAvailabilitySet** atualiza um conjunto de disponibilidade.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

Esse comando atualiza o conjunto de disponibilidade chamado ' AvSet01 ' no grupo de recursos chamado ' ResourceGroup01 ' para um conjunto de disponibilidade gerenciada.

## OS

### -Availabilityset
Especifica o objeto do conjunto de disponibilidade a ser atualizado.

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### Gerenciados por
Conjunto de disponibilidade gerenciada

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
O nome do SKU

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet

## INFORMA

## LINKS RELACIONADOS

