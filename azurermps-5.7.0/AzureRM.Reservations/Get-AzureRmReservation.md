---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426624"
---
# <span data-ttu-id="a47ba-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="a47ba-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="a47ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a47ba-102">SYNOPSIS</span></span>
<span data-ttu-id="a47ba-103">Obter `Reservation` s em uma determinada ordem de reserva</span><span class="sxs-lookup"><span data-stu-id="a47ba-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a47ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a47ba-104">SYNTAX</span></span>

### <span data-ttu-id="a47ba-105">Linha de comando (padrão)</span><span class="sxs-lookup"><span data-stu-id="a47ba-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### <span data-ttu-id="a47ba-106">Pipeobject</span><span class="sxs-lookup"><span data-stu-id="a47ba-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## <span data-ttu-id="a47ba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a47ba-107">DESCRIPTION</span></span>
<span data-ttu-id="a47ba-108">Lista `Reservation` s dentro de um único `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="a47ba-108">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="a47ba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a47ba-109">EXAMPLES</span></span>

### <span data-ttu-id="a47ba-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a47ba-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="a47ba-111">Lista `Reservation` s dentro do especificado `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="a47ba-111">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="a47ba-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a47ba-112">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="a47ba-113">Obter `Reservation` detalhes específicos.</span><span class="sxs-lookup"><span data-stu-id="a47ba-113">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="a47ba-114">OS</span><span class="sxs-lookup"><span data-stu-id="a47ba-114">PARAMETERS</span></span>

### <span data-ttu-id="a47ba-115">-Reservaid</span><span class="sxs-lookup"><span data-stu-id="a47ba-115">-ReservationId</span></span>
<span data-ttu-id="a47ba-116">ID do `Reservation` para ver</span><span class="sxs-lookup"><span data-stu-id="a47ba-116">Id of the `Reservation` to look at</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ba-117">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="a47ba-117">-ReservationOrder</span></span>
<span data-ttu-id="a47ba-118">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="a47ba-118">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ba-119">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a47ba-119">-ReservationOrderId</span></span>
<span data-ttu-id="a47ba-120">ID do `ReservationOrder` que contém o `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a47ba-120">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="a47ba-121">Necessário.</span><span class="sxs-lookup"><span data-stu-id="a47ba-121">Required.</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ba-122">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="a47ba-122">-ReservationOrderPage</span></span>
<span data-ttu-id="a47ba-123">Parâmetro do objeto pipe para `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="a47ba-123">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a47ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47ba-124">CommonParameters</span></span>
<span data-ttu-id="a47ba-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a47ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47ba-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a47ba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47ba-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a47ba-127">INPUTS</span></span>

### <span data-ttu-id="a47ba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a47ba-128">System.String</span></span>
<span data-ttu-id="a47ba-129">Microsoft. Azure. Commands. reservas. Models. PSReservationOrder Microsoft. Azure. Commands. reservas. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="a47ba-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="a47ba-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a47ba-130">OUTPUTS</span></span>

### <span data-ttu-id="a47ba-131">Microsoft. Azure. Commands. reservas. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="a47ba-131">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>
<span data-ttu-id="a47ba-132">Microsoft. Azure. Commands. reservas. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="a47ba-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a47ba-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a47ba-133">NOTES</span></span>

## <span data-ttu-id="a47ba-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a47ba-134">RELATED LINKS</span></span>

