---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429699"
---
# <span data-ttu-id="72ad6-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="72ad6-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="72ad6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="72ad6-103">Dividir a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="72ad6-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72ad6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72ad6-104">SYNTAX</span></span>

### <span data-ttu-id="72ad6-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="72ad6-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ad6-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="72ad6-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72ad6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72ad6-107">DESCRIPTION</span></span>
<span data-ttu-id="72ad6-108">Dividir um `Reservation` em dois `Reservation` s com distribuição de quantidade especificada.</span><span class="sxs-lookup"><span data-stu-id="72ad6-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="72ad6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72ad6-109">EXAMPLES</span></span>

### <span data-ttu-id="72ad6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="72ad6-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="72ad6-111">Dividir o especificado `Reservation` em dois `Reservation` s com as quantidades correspondentes</span><span class="sxs-lookup"><span data-stu-id="72ad6-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="72ad6-112">OS</span><span class="sxs-lookup"><span data-stu-id="72ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="72ad6-113">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="72ad6-113">-Quantity</span></span>
<span data-ttu-id="72ad6-114">Inteiros separados por vírgula para o campo quantidade dos dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="72ad6-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ad6-115">-Reserva</span><span class="sxs-lookup"><span data-stu-id="72ad6-115">-Reservation</span></span>
<span data-ttu-id="72ad6-116">Parâmetro do objeto pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="72ad6-116">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="72ad6-117">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="72ad6-117">-ReservationId</span></span>
<span data-ttu-id="72ad6-118">ID do `Reservation` a ser dividida</span><span class="sxs-lookup"><span data-stu-id="72ad6-118">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="72ad6-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="72ad6-119">-ReservationOrderId</span></span>
<span data-ttu-id="72ad6-120">ID do `ReservationOrder` que contém o `Reservation` usuário que deseja dividir</span><span class="sxs-lookup"><span data-stu-id="72ad6-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="72ad6-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72ad6-121">-Confirm</span></span>
<span data-ttu-id="72ad6-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72ad6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ad6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ad6-123">-WhatIf</span></span>
<span data-ttu-id="72ad6-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72ad6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72ad6-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72ad6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ad6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ad6-126">CommonParameters</span></span>
<span data-ttu-id="72ad6-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ad6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ad6-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ad6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ad6-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72ad6-129">INPUTS</span></span>

### <span data-ttu-id="72ad6-130">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="72ad6-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="72ad6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72ad6-131">OUTPUTS</span></span>

### <span data-ttu-id="72ad6-132">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. reservas. Models. PSReservation, Microsoft. Azure. Commands. reservas, Version = 1.0.0.0, Culture = neutro, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="72ad6-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="72ad6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72ad6-133">NOTES</span></span>

## <span data-ttu-id="72ad6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72ad6-134">RELATED LINKS</span></span>

