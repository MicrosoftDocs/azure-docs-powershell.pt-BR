---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114688"
---
# <span data-ttu-id="2ce7e-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="2ce7e-101">Get-AzReservation</span></span>

## <span data-ttu-id="2ce7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ce7e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce7e-103">Obter `Reservation` s em uma determinada ordem de reserva</span><span class="sxs-lookup"><span data-stu-id="2ce7e-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="2ce7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ce7e-104">SYNTAX</span></span>

### <span data-ttu-id="2ce7e-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ce7e-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ce7e-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="2ce7e-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ce7e-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="2ce7e-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ce7e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ce7e-108">DESCRIPTION</span></span>
<span data-ttu-id="2ce7e-109">Lista `Reservation` s dentro de um único `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="2ce7e-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="2ce7e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ce7e-110">EXAMPLES</span></span>

### <span data-ttu-id="2ce7e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ce7e-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="2ce7e-112">Lista `Reservation` s dentro do especificado `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="2ce7e-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="2ce7e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2ce7e-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="2ce7e-114">Obter `Reservation` detalhes específicos.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="2ce7e-115">OS</span><span class="sxs-lookup"><span data-stu-id="2ce7e-115">PARAMETERS</span></span>

### <span data-ttu-id="2ce7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce7e-116">-DefaultProfile</span></span>
<span data-ttu-id="2ce7e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce7e-118">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="2ce7e-118">-ReservationId</span></span>
<span data-ttu-id="2ce7e-119">ID do `Reservation` para ver</span><span class="sxs-lookup"><span data-stu-id="2ce7e-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="2ce7e-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="2ce7e-120">-ReservationOrder</span></span>
<span data-ttu-id="2ce7e-121">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="2ce7e-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="2ce7e-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="2ce7e-122">-ReservationOrderId</span></span>
<span data-ttu-id="2ce7e-123">ID do `ReservationOrder` que contém o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="2ce7e-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="2ce7e-124">Necessário.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-124">Required.</span></span>

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

### <span data-ttu-id="2ce7e-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="2ce7e-125">-ReservationOrderPage</span></span>
<span data-ttu-id="2ce7e-126">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="2ce7e-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="2ce7e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce7e-127">CommonParameters</span></span>
<span data-ttu-id="2ce7e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce7e-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ce7e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce7e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ce7e-130">INPUTS</span></span>

### <span data-ttu-id="2ce7e-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2ce7e-131">System.Guid</span></span>

### <span data-ttu-id="2ce7e-132">Microsoft. Azure. Commands. reservas. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="2ce7e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="2ce7e-133">Microsoft. Azure. Commands. reservas. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="2ce7e-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="2ce7e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ce7e-134">OUTPUTS</span></span>

### <span data-ttu-id="2ce7e-135">Microsoft. Azure. Commands. reservas. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="2ce7e-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="2ce7e-136">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="2ce7e-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="2ce7e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ce7e-137">NOTES</span></span>

## <span data-ttu-id="2ce7e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ce7e-138">RELATED LINKS</span></span>
