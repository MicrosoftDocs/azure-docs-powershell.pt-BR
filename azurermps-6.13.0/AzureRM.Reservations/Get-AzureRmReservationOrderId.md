---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrderId.md
ms.openlocfilehash: 1e60ca2ce1a845fa460e14a4e99b921fa4c085ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428390"
---
# <span data-ttu-id="3562e-101">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="3562e-101">Get-AzureRmReservationOrderId</span></span>

## <span data-ttu-id="3562e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3562e-102">SYNOPSIS</span></span>
<span data-ttu-id="3562e-103">Obtenha a lista de `ReservationOrder` IDs aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="3562e-103">Get list of applicable `ReservationOrder` Ids.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3562e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3562e-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3562e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3562e-105">DESCRIPTION</span></span>
<span data-ttu-id="3562e-106">Obter IDs dos `ReservationOrder` s aplicáveis que podem ser aplicados a essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="3562e-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="3562e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3562e-107">EXAMPLES</span></span>

### <span data-ttu-id="3562e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3562e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrderId
```

<span data-ttu-id="3562e-109">Ser aplicado `ReservationOrder` para assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="3562e-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="3562e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3562e-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="3562e-111">Ser aplicado `ReservationOrder` para a assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="3562e-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="3562e-112">OS</span><span class="sxs-lookup"><span data-stu-id="3562e-112">PARAMETERS</span></span>

### <span data-ttu-id="3562e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3562e-113">-DefaultProfile</span></span>
<span data-ttu-id="3562e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3562e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3562e-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3562e-115">-SubscriptionId</span></span>
<span data-ttu-id="3562e-116">ID da assinatura para obter a s aplicada `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="3562e-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3562e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3562e-117">CommonParameters</span></span>
<span data-ttu-id="3562e-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3562e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3562e-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3562e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3562e-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3562e-120">INPUTS</span></span>

### <span data-ttu-id="3562e-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3562e-121">None</span></span>

## <span data-ttu-id="3562e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3562e-122">OUTPUTS</span></span>

### <span data-ttu-id="3562e-123">Microsoft. Azure. Management. reservas. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="3562e-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="3562e-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3562e-124">NOTES</span></span>

## <span data-ttu-id="3562e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3562e-125">RELATED LINKS</span></span>
