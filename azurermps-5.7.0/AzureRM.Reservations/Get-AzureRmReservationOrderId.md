---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: ce6132c7c9b782969b78094de4a055415f3f30ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429697"
---
# <span data-ttu-id="a1c01-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a1c01-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="a1c01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1c01-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c01-103">Obtenha a lista de `ReservationOrder` IDs aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="a1c01-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1c01-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a1c01-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1c01-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c01-106">Obter IDs dos `ReservationOrder` s aplicáveis que podem ser aplicados a essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="a1c01-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="a1c01-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1c01-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c01-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1c01-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="a1c01-109">Ser aplicado `ReservationOrder` para assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="a1c01-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="a1c01-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a1c01-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="a1c01-111">Ser aplicado `ReservationOrder` para a assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="a1c01-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="a1c01-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1c01-112">PARAMETERS</span></span>

### <span data-ttu-id="a1c01-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1c01-113">-SubscriptionId</span></span>
<span data-ttu-id="a1c01-114">ID da assinatura para obter a s aplicada `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="a1c01-114">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c01-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c01-115">CommonParameters</span></span>
<span data-ttu-id="a1c01-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c01-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c01-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c01-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c01-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1c01-118">INPUTS</span></span>

### <span data-ttu-id="a1c01-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a1c01-119">None</span></span>

## <span data-ttu-id="a1c01-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1c01-120">OUTPUTS</span></span>

### <span data-ttu-id="a1c01-121">Microsoft. Azure. Commands. reservas. Models. PSAppliedReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a1c01-121">Microsoft.Azure.Commands.Reservations.Models.PSAppliedReservationOrderId</span></span>

## <span data-ttu-id="a1c01-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1c01-122">NOTES</span></span>

## <span data-ttu-id="a1c01-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1c01-123">RELATED LINKS</span></span>

