---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/get-azreservationorderid
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrderId.md
ms.openlocfilehash: 9783d1ff8d3a42d3ad6627abcaae792f966b7828
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891685"
---
# <span data-ttu-id="bb426-101">Get-AzReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="bb426-101">Get-AzReservationOrderId</span></span>

## <span data-ttu-id="bb426-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb426-102">SYNOPSIS</span></span>
<span data-ttu-id="bb426-103">Obter lista de `ReservationOrder` Ids aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="bb426-103">Get list of applicable `ReservationOrder` Ids.</span></span>

## <span data-ttu-id="bb426-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb426-104">SYNTAX</span></span>

```
Get-AzReservationOrderId [-SubscriptionId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb426-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb426-105">DESCRIPTION</span></span>
<span data-ttu-id="bb426-106">Obter Ids de `ReservationOrder` s aplicáveis que podem ser aplicadas a essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="bb426-106">Get Ids of applicable `ReservationOrder`s that can be applied to this subscription.</span></span>

## <span data-ttu-id="bb426-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb426-107">EXAMPLES</span></span>

### <span data-ttu-id="bb426-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb426-108">Example 1</span></span>
```
PS C:\> Get-AzReservationOrderId
```

<span data-ttu-id="bb426-109">Obter a aplicação `ReservationOrder` da assinatura padrão</span><span class="sxs-lookup"><span data-stu-id="bb426-109">Get applied `ReservationOrder` for default subscription</span></span>

### <span data-ttu-id="bb426-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bb426-110">Example 2</span></span>
```
PS C:\> Get-AzReservationOrderId -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="bb426-111">Obter a `ReservationOrder` aplicação para assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="bb426-111">Get applied `ReservationOrder` for specified subscription</span></span>

## <span data-ttu-id="bb426-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb426-112">PARAMETERS</span></span>

### <span data-ttu-id="bb426-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb426-113">-DefaultProfile</span></span>
<span data-ttu-id="bb426-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb426-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb426-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb426-115">-SubscriptionId</span></span>
<span data-ttu-id="bb426-116">ID da assinatura para obter os `ReservationOrder` s aplicados</span><span class="sxs-lookup"><span data-stu-id="bb426-116">Id of the subscription to get the applied `ReservationOrder`s</span></span>

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

### <span data-ttu-id="bb426-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb426-117">CommonParameters</span></span>
<span data-ttu-id="bb426-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb426-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb426-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb426-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb426-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb426-120">INPUTS</span></span>

### <span data-ttu-id="bb426-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bb426-121">None</span></span>

## <span data-ttu-id="bb426-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb426-122">OUTPUTS</span></span>

### <span data-ttu-id="bb426-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span><span class="sxs-lookup"><span data-stu-id="bb426-123">Microsoft.Azure.Management.Reservations.Models.AppliedReservations</span></span>

## <span data-ttu-id="bb426-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb426-124">NOTES</span></span>

## <span data-ttu-id="bb426-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb426-125">RELATED LINKS</span></span>
