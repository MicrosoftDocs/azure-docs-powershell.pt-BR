---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: c969d24a894165e23628b91cda640f676ec3f3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599472"
---
# <span data-ttu-id="e5754-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="e5754-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="e5754-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5754-102">SYNOPSIS</span></span>
<span data-ttu-id="e5754-103">Obtenha a lista de `ReservationOrder` IDs aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="e5754-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="e5754-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5754-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5754-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5754-105">DESCRIPTION</span></span>
<span data-ttu-id="e5754-106">Obter IDs dos `ReservationOrder` s aplicáveis que podem ser aplicados a essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="e5754-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="e5754-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5754-107">EXAMPLES</span></span>

### <span data-ttu-id="e5754-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5754-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="e5754-109">Ser aplicado `ReservationOrder` para assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="e5754-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="e5754-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e5754-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="e5754-111">Ser aplicado `ReservationOrder` para a assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="e5754-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="e5754-112">OS</span><span class="sxs-lookup"><span data-stu-id="e5754-112">PARAMETERS</span></span>

### <span data-ttu-id="e5754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5754-113">-DefaultProfile</span></span>
<span data-ttu-id="e5754-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5754-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5754-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5754-115">-SubscriptionId</span></span>
<span data-ttu-id="e5754-116">ID da assinatura para obter a s aplicada `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="e5754-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="e5754-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5754-117">CommonParameters</span></span>
<span data-ttu-id="e5754-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5754-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5754-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5754-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5754-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5754-120">INPUTS</span></span>

### <span data-ttu-id="e5754-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e5754-121">None</span></span>

## <span data-ttu-id="e5754-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5754-122">OUTPUTS</span></span>

### <span data-ttu-id="e5754-123">Microsoft. Azure. Management. reservas. Models. AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="e5754-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="e5754-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5754-124">NOTES</span></span>

## <span data-ttu-id="e5754-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5754-125">RELATED LINKS</span></span>
