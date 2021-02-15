---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118774"
---
# <span data-ttu-id="99f2f-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="99f2f-101">Get-AzReservation</span></span>

## <span data-ttu-id="99f2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="99f2f-103">Obter `Reservation` s em um pedido de reserva determinado</span><span class="sxs-lookup"><span data-stu-id="99f2f-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="99f2f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99f2f-104">SYNTAX</span></span>

### <span data-ttu-id="99f2f-105">CommandLine (Padrão)</span><span class="sxs-lookup"><span data-stu-id="99f2f-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99f2f-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="99f2f-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99f2f-107">PageBject</span><span class="sxs-lookup"><span data-stu-id="99f2f-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99f2f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="99f2f-108">DESCRIPTION</span></span>
<span data-ttu-id="99f2f-109">Lista `Reservation` s dentro de um único `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="99f2f-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="99f2f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="99f2f-110">EXAMPLES</span></span>

### <span data-ttu-id="99f2f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99f2f-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="99f2f-112">Lista `Reservation` s dentro do `ReservationOrder` especificado.</span><span class="sxs-lookup"><span data-stu-id="99f2f-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="99f2f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="99f2f-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="99f2f-114">Obter detalhes `Reservation` específicos.</span><span class="sxs-lookup"><span data-stu-id="99f2f-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="99f2f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99f2f-115">PARAMETERS</span></span>

### <span data-ttu-id="99f2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f2f-116">-DefaultProfile</span></span>
<span data-ttu-id="99f2f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99f2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f2f-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="99f2f-118">-ReservationId</span></span>
<span data-ttu-id="99f2f-119">ID do `Reservation` que procurar</span><span class="sxs-lookup"><span data-stu-id="99f2f-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="99f2f-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="99f2f-120">-ReservationOrder</span></span>
<span data-ttu-id="99f2f-121">Parâmetro de objeto de cano para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="99f2f-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="99f2f-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="99f2f-122">-ReservationOrderId</span></span>
<span data-ttu-id="99f2f-123">ID do `ReservationOrder` que contém o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="99f2f-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="99f2f-124">Necessário.</span><span class="sxs-lookup"><span data-stu-id="99f2f-124">Required.</span></span>

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

### <span data-ttu-id="99f2f-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="99f2f-125">-ReservationOrderPage</span></span>
<span data-ttu-id="99f2f-126">Parâmetro de objeto de cano para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="99f2f-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="99f2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f2f-127">CommonParameters</span></span>
<span data-ttu-id="99f2f-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f2f-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99f2f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f2f-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="99f2f-130">INPUTS</span></span>

### <span data-ttu-id="99f2f-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="99f2f-131">System.Guid</span></span>

### <span data-ttu-id="99f2f-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="99f2f-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="99f2f-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="99f2f-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="99f2f-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="99f2f-134">OUTPUTS</span></span>

### <span data-ttu-id="99f2f-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="99f2f-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="99f2f-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="99f2f-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="99f2f-137">Notas</span><span class="sxs-lookup"><span data-stu-id="99f2f-137">NOTES</span></span>

## <span data-ttu-id="99f2f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99f2f-138">RELATED LINKS</span></span>
