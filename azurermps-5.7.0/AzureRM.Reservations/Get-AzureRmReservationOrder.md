---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429700"
---
# Get-AzureRmReservationOrder

## Sinopse
Obter `ReservationOrder`

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## DESCRITIVO
Lista de todos os `ReservationOrder` s aos quais o usuário tem acesso no locatário atual. Se o parâmetro ReservationOrderId estiver definido, obtenha essa ReservationOrder específica.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmReservationOrder
```

Listar todos os `ReservationOrder` usuários que o usuário tem acesso ao locatário atual

### Exemplo 2
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

Obter `ReservationOrder` com o ReservationOrderId especificado

## OS

### -ReservationOrderId
ID do ReservationOrder específico que o usuário quer ver

```yaml
Type: String
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

### Microsoft. Azure. Commands. reservas. Models. PSReservationOrderPage
Microsoft. Azure. Commands. reservas. Models. PSReservationOrder

## INFORMA

## LINKS RELACIONADOS

