---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945083"
---
# <span data-ttu-id="9cf6d-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="9cf6d-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="9cf6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cf6d-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf6d-103">Obter as métricas do plano especificado.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="9cf6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cf6d-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9cf6d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cf6d-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf6d-106">Obter as métricas do plano especificado.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="9cf6d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cf6d-107">EXAMPLES</span></span>

### <span data-ttu-id="9cf6d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9cf6d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="9cf6d-109">Obter as métricas de um plano.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="9cf6d-110">OS</span><span class="sxs-lookup"><span data-stu-id="9cf6d-110">PARAMETERS</span></span>

### <span data-ttu-id="9cf6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf6d-111">-DefaultProfile</span></span>
<span data-ttu-id="9cf6d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cf6d-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9cf6d-113">-PlanName</span></span>
<span data-ttu-id="9cf6d-114">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-114">Name of the plan.</span></span>

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

### <span data-ttu-id="9cf6d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf6d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9cf6d-116">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9cf6d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cf6d-117">-SubscriptionId</span></span>
<span data-ttu-id="9cf6d-118">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9cf6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf6d-119">CommonParameters</span></span>
<span data-ttu-id="9cf6d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf6d-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cf6d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf6d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cf6d-122">INPUTS</span></span>

## <span data-ttu-id="9cf6d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cf6d-123">OUTPUTS</span></span>

### <span data-ttu-id="9cf6d-124">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="9cf6d-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="9cf6d-125">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9cf6d-125">ALIASES</span></span>

## <span data-ttu-id="9cf6d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cf6d-126">NOTES</span></span>

## <span data-ttu-id="9cf6d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cf6d-127">RELATED LINKS</span></span>

