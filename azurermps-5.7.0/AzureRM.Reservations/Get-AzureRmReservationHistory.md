---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432416"
---
# Get-AzureRmReservationHistory

## Sinopse
Obter `Reservation` histórico de revisão.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Linha de comando (padrão)
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### Pipeobject
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## DESCRITIVO
Lista de todas as revisões para o `Reservation` .

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

Obter o histórico de revisão da reserva específica

## OS

### -Reserva
Parâmetro do objeto pipe para `Reservation` s

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Reservaid
Reservaid do `Reservation` do qual o histórico deve ser mostrado

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrderId
ReservationOrderId para o `ReservationOrder` que contém o `Reservation`

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String
Microsoft. Azure. Commands. reservas. Models. PSReservation

## EXIBE

### Microsoft. Azure. Commands. reservas. Models. PSReservationPage

## INFORMA

## LINKS RELACIONADOS

