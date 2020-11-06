---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431061"
---
# Get-AzureRmVMSize

## Sinopse
Obtém tamanhos de máquina virtual disponíveis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ListVirtualMachineSizeParamSet (padrão)
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### ListAvailableSizesForAvailabilitySet
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmVMSize** Obtém os tamanhos das máquinas virtuais disponíveis.

## EXEMPLOS

### Exemplo 1: obter tamanhos de máquina virtual para um local
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

Esse comando obtém os tamanhos disponíveis para máquinas virtuais no local especificado.

### Exemplo 2: obter tamanhos para um conjunto de disponibilidade
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Esse comando obtém tamanhos disponíveis para máquinas virtuais que você pode implantar no conjunto de disponibilidade chamado AvailabilitySet17.

### Exemplo 3: obter os tamanhos de uma máquina virtual existente
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

Esse comando obtém os tamanhos disponíveis para a máquina virtual existente chamada VirtualMachine12.
Você pode redimensionar essa máquina virtual para os tamanhos que esse comando obtém.

## OS

### -AvailabilitySetName
Especifica o nome do conjunto de disponibilidade para o qual este cmdlet obtém os tamanhos da máquina virtual disponível.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica o local para o qual esse cmdlet obtém os tamanhos da máquina virtual disponível.

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos da máquina virtual.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Especifica o nome da máquina virtual em que este cmdlet obtém os tamanhos da máquina virtual disponível para redimensionamento.

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
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

[Get-AzureRmVM](./Get-AzureRmVM.md)


