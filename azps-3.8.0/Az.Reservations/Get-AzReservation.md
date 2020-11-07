---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778132"
---
# <span data-ttu-id="dd037-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="dd037-101">Get-AzReservation</span></span>

## <span data-ttu-id="dd037-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd037-102">SYNOPSIS</span></span>
<span data-ttu-id="dd037-103">Obter `Reservation` s em uma determinada ordem de reserva</span><span class="sxs-lookup"><span data-stu-id="dd037-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="dd037-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd037-104">SYNTAX</span></span>

### <span data-ttu-id="dd037-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd037-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd037-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="dd037-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd037-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="dd037-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd037-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd037-108">DESCRIPTION</span></span>
<span data-ttu-id="dd037-109">Lista `Reservation` s dentro de um único `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="dd037-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="dd037-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd037-110">EXAMPLES</span></span>

### <span data-ttu-id="dd037-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd037-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="dd037-112">Lista `Reservation` s dentro do especificado `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="dd037-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="dd037-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dd037-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="dd037-114">Obter `Reservation` detalhes específicos.</span><span class="sxs-lookup"><span data-stu-id="dd037-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="dd037-115">OS</span><span class="sxs-lookup"><span data-stu-id="dd037-115">PARAMETERS</span></span>

### <span data-ttu-id="dd037-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd037-116">-DefaultProfile</span></span>
<span data-ttu-id="dd037-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd037-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd037-118">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="dd037-118">-ReservationId</span></span>
<span data-ttu-id="dd037-119">ID do `Reservation` para ver</span><span class="sxs-lookup"><span data-stu-id="dd037-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="dd037-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="dd037-120">-ReservationOrder</span></span>
<span data-ttu-id="dd037-121">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="dd037-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="dd037-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="dd037-122">-ReservationOrderId</span></span>
<span data-ttu-id="dd037-123">ID do `ReservationOrder` que contém o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="dd037-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="dd037-124">Necessário.</span><span class="sxs-lookup"><span data-stu-id="dd037-124">Required.</span></span>

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

### <span data-ttu-id="dd037-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="dd037-125">-ReservationOrderPage</span></span>
<span data-ttu-id="dd037-126">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="dd037-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="dd037-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd037-127">CommonParameters</span></span>
<span data-ttu-id="dd037-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd037-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd037-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd037-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd037-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd037-130">INPUTS</span></span>

### <span data-ttu-id="dd037-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dd037-131">System.Guid</span></span>

### <span data-ttu-id="dd037-132">Microsoft. Azure. Commands. reservas. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="dd037-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="dd037-133">Microsoft. Azure. Commands. reservas. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="dd037-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="dd037-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd037-134">OUTPUTS</span></span>

### <span data-ttu-id="dd037-135">Microsoft. Azure. Commands. reservas. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="dd037-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="dd037-136">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="dd037-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="dd037-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd037-137">NOTES</span></span>

## <span data-ttu-id="dd037-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd037-138">RELATED LINKS</span></span>
