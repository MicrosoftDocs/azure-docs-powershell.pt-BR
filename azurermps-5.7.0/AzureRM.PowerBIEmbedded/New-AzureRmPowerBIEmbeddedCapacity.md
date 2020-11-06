---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428120"
---
# New-AzureRmPowerBIEmbeddedCapacity

## Sinopse
Cria uma nova capacidade inserida do PowerBI.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzureRmPowerBIEmbeddedCapacity cria uma nova capacidade inserida do PowerBI

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

Cria uma capacidade chamada testcapacity na região do Azure oeste centro dos EUA e na testRG do grupo de recursos. O nível de SKU para a capacidade será a1.

## OS

### -ResourceGroupName
Nome do grupo de recursos do Azure ao qual a capacidade pertence

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### -Nome
Nome da capacidade inserida do PowerBI

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### -Local
A região do Azure na qual a capacidade incorporada do PowerBI está hospedada

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### -SKU
O nome da SKU para a capacidade.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### -Administrador
Um nome de capacidade separada por vírgulas para definir como administrador na capacidade

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash definidas como marcas na capacidade.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### -Confirme
Solicita que o usuário confirme se deseja executar a operação

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
Descreve as ações que a operação atual executará sem realmente executá-las

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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmPowerBIEmbeddedCapacity](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[Remove-AzureRmPowerBIEmbeddedCapacity](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
