---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427180"
---
# <span data-ttu-id="37a7c-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="37a7c-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="37a7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="37a7c-103">Obter `Reservation` s em uma determinada ordem de reserva</span><span class="sxs-lookup"><span data-stu-id="37a7c-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37a7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37a7c-104">SYNTAX</span></span>

### <span data-ttu-id="37a7c-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="37a7c-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37a7c-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="37a7c-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37a7c-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="37a7c-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a7c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37a7c-108">DESCRIPTION</span></span>
<span data-ttu-id="37a7c-109">Lista `Reservation` s dentro de um único `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="37a7c-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="37a7c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37a7c-110">EXAMPLES</span></span>

### <span data-ttu-id="37a7c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37a7c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="37a7c-112">Lista `Reservation` s dentro do especificado `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="37a7c-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="37a7c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="37a7c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="37a7c-114">Obter `Reservation` detalhes específicos.</span><span class="sxs-lookup"><span data-stu-id="37a7c-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="37a7c-115">OS</span><span class="sxs-lookup"><span data-stu-id="37a7c-115">PARAMETERS</span></span>

### <span data-ttu-id="37a7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a7c-116">-DefaultProfile</span></span>
<span data-ttu-id="37a7c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37a7c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37a7c-118">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="37a7c-118">-ReservationId</span></span>
<span data-ttu-id="37a7c-119">ID do `Reservation` para ver</span><span class="sxs-lookup"><span data-stu-id="37a7c-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="37a7c-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="37a7c-120">-ReservationOrder</span></span>
<span data-ttu-id="37a7c-121">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="37a7c-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="37a7c-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="37a7c-122">-ReservationOrderId</span></span>
<span data-ttu-id="37a7c-123">ID do `ReservationOrder` que contém o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="37a7c-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="37a7c-124">Necessário.</span><span class="sxs-lookup"><span data-stu-id="37a7c-124">Required.</span></span>

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

### <span data-ttu-id="37a7c-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="37a7c-125">-ReservationOrderPage</span></span>
<span data-ttu-id="37a7c-126">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="37a7c-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="37a7c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a7c-127">CommonParameters</span></span>
<span data-ttu-id="37a7c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a7c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a7c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a7c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a7c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37a7c-130">INPUTS</span></span>

### <span data-ttu-id="37a7c-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="37a7c-131">System.Guid</span></span>

### <span data-ttu-id="37a7c-132">Microsoft. Azure. Commands. reservas. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="37a7c-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="37a7c-133">Parâmetros: ReservationOrder (ByValue)</span><span class="sxs-lookup"><span data-stu-id="37a7c-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="37a7c-134">Microsoft. Azure. Commands. reservas. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="37a7c-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="37a7c-135">Parâmetros: ReservationOrderPage (ByValue)</span><span class="sxs-lookup"><span data-stu-id="37a7c-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="37a7c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37a7c-136">OUTPUTS</span></span>

### <span data-ttu-id="37a7c-137">Microsoft. Azure. Commands. reservas. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="37a7c-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="37a7c-138">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="37a7c-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="37a7c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37a7c-139">NOTES</span></span>

## <span data-ttu-id="37a7c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37a7c-140">RELATED LINKS</span></span>
