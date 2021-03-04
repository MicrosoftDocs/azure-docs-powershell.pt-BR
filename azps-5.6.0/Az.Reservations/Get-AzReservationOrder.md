---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 1878237544cc1b44b5e47814f455638c168e2412
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891686"
---
# Get-AzReservationOrder

## SYNOPSIS
Obter `ReservationOrder`

## SINTAXE

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
Lista de todos os `ReservationOrder` s aos que o usuário tem acesso no locatário atual. Se o parâmetro ReservationOrderId estiver definido, obter esse ReservationOrder específico.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzReservationOrder
```

Listar `ReservationOrder` tudo o que o usuário tem acesso no locatário atual

### Exemplo 2
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

Obter `ReservationOrder` com o ReservationOrderId especificado

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservationOrderId
Id do ReservationOrder específico que o usuário deseja ver

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage

### Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder

## NOTES

## LINKS RELACIONADOS
