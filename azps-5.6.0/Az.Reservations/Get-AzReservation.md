---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 427e715e055cd909d204f92aedd58eca9d7db0f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891691"
---
# <span data-ttu-id="28155-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="28155-101">Get-AzReservation</span></span>

## <span data-ttu-id="28155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28155-102">SYNOPSIS</span></span>
<span data-ttu-id="28155-103">Obter `Reservation` s em um determinado pedido de reserva</span><span class="sxs-lookup"><span data-stu-id="28155-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="28155-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="28155-104">SYNTAX</span></span>

### <span data-ttu-id="28155-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="28155-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28155-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="28155-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28155-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="28155-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28155-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="28155-108">DESCRIPTION</span></span>
<span data-ttu-id="28155-109">Lista `Reservation` s dentro de um único `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="28155-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="28155-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28155-110">EXAMPLES</span></span>

### <span data-ttu-id="28155-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28155-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="28155-112">Lista `Reservation` s dentro do especificado `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="28155-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="28155-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="28155-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="28155-114">Obter detalhes `Reservation` específicos.</span><span class="sxs-lookup"><span data-stu-id="28155-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="28155-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="28155-115">PARAMETERS</span></span>

### <span data-ttu-id="28155-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28155-116">-DefaultProfile</span></span>
<span data-ttu-id="28155-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28155-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28155-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="28155-118">-ReservationId</span></span>
<span data-ttu-id="28155-119">ID do `Reservation` a ser analisado</span><span class="sxs-lookup"><span data-stu-id="28155-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28155-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="28155-120">-ReservationOrder</span></span>
<span data-ttu-id="28155-121">Parâmetro do objeto Pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="28155-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28155-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="28155-122">-ReservationOrderId</span></span>
<span data-ttu-id="28155-123">ID do `ReservationOrder` que contém o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="28155-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="28155-124">Necessário.</span><span class="sxs-lookup"><span data-stu-id="28155-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28155-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="28155-125">-ReservationOrderPage</span></span>
<span data-ttu-id="28155-126">Parâmetro do objeto Pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="28155-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28155-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28155-127">CommonParameters</span></span>
<span data-ttu-id="28155-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28155-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28155-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28155-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28155-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28155-130">INPUTS</span></span>

### <span data-ttu-id="28155-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="28155-131">System.Guid</span></span>

### <span data-ttu-id="28155-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="28155-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="28155-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="28155-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="28155-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="28155-134">OUTPUTS</span></span>

### <span data-ttu-id="28155-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="28155-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="28155-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="28155-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="28155-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="28155-137">NOTES</span></span>

## <span data-ttu-id="28155-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28155-138">RELATED LINKS</span></span>
