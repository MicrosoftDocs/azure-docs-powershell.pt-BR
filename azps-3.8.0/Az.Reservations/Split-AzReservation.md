---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941857"
---
# <span data-ttu-id="636eb-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="636eb-101">Split-AzReservation</span></span>

## <span data-ttu-id="636eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="636eb-102">SYNOPSIS</span></span>
<span data-ttu-id="636eb-103">Dividir a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="636eb-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="636eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="636eb-104">SYNTAX</span></span>

### <span data-ttu-id="636eb-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="636eb-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="636eb-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="636eb-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="636eb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="636eb-107">DESCRIPTION</span></span>
<span data-ttu-id="636eb-108">Dividir um `Reservation` em dois `Reservation` s com distribuição de quantidade especificada.</span><span class="sxs-lookup"><span data-stu-id="636eb-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="636eb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="636eb-109">EXAMPLES</span></span>

### <span data-ttu-id="636eb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="636eb-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="636eb-111">Dividir o especificado `Reservation` em dois `Reservation` s com as quantidades correspondentes</span><span class="sxs-lookup"><span data-stu-id="636eb-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="636eb-112">OS</span><span class="sxs-lookup"><span data-stu-id="636eb-112">PARAMETERS</span></span>

### <span data-ttu-id="636eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="636eb-113">-DefaultProfile</span></span>
<span data-ttu-id="636eb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="636eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="636eb-115">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="636eb-115">-Quantity</span></span>
<span data-ttu-id="636eb-116">Inteiros separados por vírgula para o campo quantidade dos dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="636eb-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636eb-117">-Reserva</span><span class="sxs-lookup"><span data-stu-id="636eb-117">-Reservation</span></span>
<span data-ttu-id="636eb-118">Parâmetro do objeto pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="636eb-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="636eb-119">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="636eb-119">-ReservationId</span></span>
<span data-ttu-id="636eb-120">ID do `Reservation` a ser dividida</span><span class="sxs-lookup"><span data-stu-id="636eb-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636eb-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="636eb-121">-ReservationOrderId</span></span>
<span data-ttu-id="636eb-122">ID do `ReservationOrder` que contém o `Reservation` usuário que deseja dividir</span><span class="sxs-lookup"><span data-stu-id="636eb-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636eb-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="636eb-123">-Confirm</span></span>
<span data-ttu-id="636eb-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="636eb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636eb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="636eb-125">-WhatIf</span></span>
<span data-ttu-id="636eb-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="636eb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="636eb-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="636eb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="636eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="636eb-128">CommonParameters</span></span>
<span data-ttu-id="636eb-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="636eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="636eb-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="636eb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="636eb-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="636eb-131">INPUTS</span></span>

### <span data-ttu-id="636eb-132">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="636eb-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="636eb-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="636eb-133">OUTPUTS</span></span>

### <span data-ttu-id="636eb-134">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="636eb-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="636eb-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="636eb-135">NOTES</span></span>

## <span data-ttu-id="636eb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="636eb-136">RELATED LINKS</span></span>
