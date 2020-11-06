---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429698"
---
# <span data-ttu-id="6d341-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="6d341-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="6d341-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d341-102">SYNOPSIS</span></span>
<span data-ttu-id="6d341-103">Combina dois `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="6d341-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d341-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d341-104">SYNTAX</span></span>

### <span data-ttu-id="6d341-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d341-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d341-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="6d341-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d341-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d341-107">DESCRIPTION</span></span>
<span data-ttu-id="6d341-108">Mescle o `Reservation` s especificado em um novo `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="6d341-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="6d341-109">Os dois `Reservation` s sendo mesclados devem ter as mesmas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6d341-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="6d341-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d341-110">EXAMPLES</span></span>

### <span data-ttu-id="6d341-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d341-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="6d341-112">Mesclar os dois `Reservation` s especificados em um `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6d341-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="6d341-113">OS</span><span class="sxs-lookup"><span data-stu-id="6d341-113">PARAMETERS</span></span>

### <span data-ttu-id="6d341-114">-Reserva</span><span class="sxs-lookup"><span data-stu-id="6d341-114">-Reservation</span></span>
<span data-ttu-id="6d341-115">Cadeias de caracteres separadas por vírgula de dois ReservationIds para mesclar</span><span class="sxs-lookup"><span data-stu-id="6d341-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d341-116">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="6d341-116">-ReservationId</span></span>
<span data-ttu-id="6d341-117">ReservationOrderId para o `ReservationOrder` que contém os dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="6d341-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d341-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6d341-118">-ReservationOrderId</span></span>
<span data-ttu-id="6d341-119">{{Fill ReservationOrderId descrição}}</span><span class="sxs-lookup"><span data-stu-id="6d341-119">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d341-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d341-120">-Confirm</span></span>
<span data-ttu-id="6d341-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d341-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d341-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d341-122">-WhatIf</span></span>
<span data-ttu-id="6d341-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d341-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d341-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d341-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d341-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d341-125">CommonParameters</span></span>
<span data-ttu-id="6d341-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d341-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d341-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d341-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d341-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d341-128">INPUTS</span></span>

### <span data-ttu-id="6d341-129">Microsoft. Azure. Commands. reservas. Models. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="6d341-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="6d341-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d341-130">OUTPUTS</span></span>

### <span data-ttu-id="6d341-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. reservas. Models. PSReservation, Microsoft. Azure. Commands. reservas, Version = 1.0.0.0, Culture = neutro, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6d341-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6d341-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d341-132">NOTES</span></span>

## <span data-ttu-id="6d341-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d341-133">RELATED LINKS</span></span>

