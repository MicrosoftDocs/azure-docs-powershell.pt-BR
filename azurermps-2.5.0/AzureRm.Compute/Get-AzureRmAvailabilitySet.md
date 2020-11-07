---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785374"
---
# Get-AzureRmAvailabilitySet

## Sinopse
Obtém conjuntos de disponibilidade do Azure em um grupo de recursos.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### Microsoft. Azure. Commands. COMPUTE. Models. PSAvailabilitySet

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmAvailabilitySet](./New-AzureRmAvailabilitySet.md)

[Remove-AzureRmAvailabilitySet](./Remove-AzureRmAvailabilitySet.md)


