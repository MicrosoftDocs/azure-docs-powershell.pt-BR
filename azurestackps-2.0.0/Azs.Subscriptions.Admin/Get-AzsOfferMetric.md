---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945117"
---
# <span data-ttu-id="13476-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="13476-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="13476-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13476-102">SYNOPSIS</span></span>
<span data-ttu-id="13476-103">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="13476-103">Get the offer metrics.</span></span>

## <span data-ttu-id="13476-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13476-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="13476-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13476-105">DESCRIPTION</span></span>
<span data-ttu-id="13476-106">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="13476-106">Get the offer metrics.</span></span>

## <span data-ttu-id="13476-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13476-107">EXAMPLES</span></span>

### <span data-ttu-id="13476-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13476-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="13476-109">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="13476-109">Get the offer metrics.</span></span>

## <span data-ttu-id="13476-110">OS</span><span class="sxs-lookup"><span data-stu-id="13476-110">PARAMETERS</span></span>

### <span data-ttu-id="13476-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13476-111">-DefaultProfile</span></span>
<span data-ttu-id="13476-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13476-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13476-113">-Offername</span><span class="sxs-lookup"><span data-stu-id="13476-113">-OfferName</span></span>
<span data-ttu-id="13476-114">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="13476-114">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13476-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13476-115">-ResourceGroupName</span></span>
<span data-ttu-id="13476-116">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="13476-116">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13476-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13476-117">-SubscriptionId</span></span>
<span data-ttu-id="13476-118">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="13476-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="13476-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13476-119">CommonParameters</span></span>
<span data-ttu-id="13476-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13476-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13476-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13476-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13476-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13476-122">INPUTS</span></span>

## <span data-ttu-id="13476-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13476-123">OUTPUTS</span></span>

### <span data-ttu-id="13476-124">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="13476-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="13476-125">ALIASES</span><span class="sxs-lookup"><span data-stu-id="13476-125">ALIASES</span></span>

## <span data-ttu-id="13476-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13476-126">NOTES</span></span>

## <span data-ttu-id="13476-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13476-127">RELATED LINKS</span></span>

