---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 1345978ac502d0c7d576b56f720bd16ca704e062
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599468"
---
# <span data-ttu-id="e3e0d-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="e3e0d-101">Split-AzReservation</span></span>

## <span data-ttu-id="e3e0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e0d-103">Dividir a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e3e0d-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="e3e0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3e0d-104">SYNTAX</span></span>

### <span data-ttu-id="e3e0d-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="e3e0d-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e0d-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="e3e0d-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e0d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3e0d-107">DESCRIPTION</span></span>
<span data-ttu-id="e3e0d-108">Dividir um `Reservation` em dois `Reservation` s com distribuição de quantidade especificada.</span><span class="sxs-lookup"><span data-stu-id="e3e0d-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="e3e0d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3e0d-109">EXAMPLES</span></span>

### <span data-ttu-id="e3e0d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3e0d-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="e3e0d-111">Dividir o especificado `Reservation` em dois `Reservation` s com as quantidades correspondentes</span><span class="sxs-lookup"><span data-stu-id="e3e0d-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="e3e0d-112">OS</span><span class="sxs-lookup"><span data-stu-id="e3e0d-112">PARAMETERS</span></span>

### <span data-ttu-id="e3e0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e0d-113">-DefaultProfile</span></span>
<span data-ttu-id="e3e0d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3e0d-115">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="e3e0d-115">-Quantity</span></span>
<span data-ttu-id="e3e0d-116">Inteiros separados por vírgula para o campo quantidade dos dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="e3e0d-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="e3e0d-117">-Reserva</span><span class="sxs-lookup"><span data-stu-id="e3e0d-117">-Reservation</span></span>
<span data-ttu-id="e3e0d-118">Parâmetro do objeto pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e3e0d-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="e3e0d-119">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="e3e0d-119">-ReservationId</span></span>
<span data-ttu-id="e3e0d-120">ID do `Reservation` a ser dividida</span><span class="sxs-lookup"><span data-stu-id="e3e0d-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="e3e0d-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e3e0d-121">-ReservationOrderId</span></span>
<span data-ttu-id="e3e0d-122">ID do `ReservationOrder` que contém o `Reservation` usuário que deseja dividir</span><span class="sxs-lookup"><span data-stu-id="e3e0d-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="e3e0d-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3e0d-123">-Confirm</span></span>
<span data-ttu-id="e3e0d-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3e0d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e0d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e0d-125">-WhatIf</span></span>
<span data-ttu-id="e3e0d-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3e0d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3e0d-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3e0d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e0d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e0d-128">CommonParameters</span></span>
<span data-ttu-id="e3e0d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e0d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e0d-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e0d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e0d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3e0d-131">INPUTS</span></span>

### <span data-ttu-id="e3e0d-132">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="e3e0d-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e3e0d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3e0d-133">OUTPUTS</span></span>

### <span data-ttu-id="e3e0d-134">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="e3e0d-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e3e0d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3e0d-135">NOTES</span></span>

## <span data-ttu-id="e3e0d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3e0d-136">RELATED LINKS</span></span>
