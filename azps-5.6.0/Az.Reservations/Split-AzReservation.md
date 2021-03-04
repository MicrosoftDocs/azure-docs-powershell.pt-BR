---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 9ea53203bc07cca5ca5a8b7909f9fbab558e3c5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891673"
---
# <span data-ttu-id="e3901-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="e3901-101">Split-AzReservation</span></span>

## <span data-ttu-id="e3901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3901-102">SYNOPSIS</span></span>
<span data-ttu-id="e3901-103">Dividir um `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e3901-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="e3901-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3901-104">SYNTAX</span></span>

### <span data-ttu-id="e3901-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3901-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3901-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e3901-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3901-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3901-107">DESCRIPTION</span></span>
<span data-ttu-id="e3901-108">Divida um `Reservation` em dois s com distribuição de quantidade `Reservation` especificada.</span><span class="sxs-lookup"><span data-stu-id="e3901-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="e3901-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3901-109">EXAMPLES</span></span>

### <span data-ttu-id="e3901-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3901-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="e3901-111">Divida o especificado `Reservation` em dois s com as quantidades `Reservation` correspondentes</span><span class="sxs-lookup"><span data-stu-id="e3901-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="e3901-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3901-112">PARAMETERS</span></span>

### <span data-ttu-id="e3901-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3901-113">-DefaultProfile</span></span>
<span data-ttu-id="e3901-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3901-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3901-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="e3901-115">-Quantity</span></span>
<span data-ttu-id="e3901-116">Inteiros separados por vírgulas para o campo de quantidade dos dois `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="e3901-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="e3901-117">-Reservation</span><span class="sxs-lookup"><span data-stu-id="e3901-117">-Reservation</span></span>
<span data-ttu-id="e3901-118">Parâmetro do objeto Pipe para `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e3901-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="e3901-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="e3901-119">-ReservationId</span></span>
<span data-ttu-id="e3901-120">ID do `Reservation` para dividir</span><span class="sxs-lookup"><span data-stu-id="e3901-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="e3901-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e3901-121">-ReservationOrderId</span></span>
<span data-ttu-id="e3901-122">ID do `ReservationOrder` que contém o que o usuário deseja `Reservation` dividir</span><span class="sxs-lookup"><span data-stu-id="e3901-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="e3901-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3901-123">-Confirm</span></span>
<span data-ttu-id="e3901-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3901-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3901-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3901-125">-WhatIf</span></span>
<span data-ttu-id="e3901-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3901-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3901-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3901-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3901-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3901-128">CommonParameters</span></span>
<span data-ttu-id="e3901-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3901-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3901-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3901-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3901-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3901-131">INPUTS</span></span>

### <span data-ttu-id="e3901-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="e3901-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e3901-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3901-133">OUTPUTS</span></span>

### <span data-ttu-id="e3901-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="e3901-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e3901-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3901-135">NOTES</span></span>

## <span data-ttu-id="e3901-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3901-136">RELATED LINKS</span></span>
