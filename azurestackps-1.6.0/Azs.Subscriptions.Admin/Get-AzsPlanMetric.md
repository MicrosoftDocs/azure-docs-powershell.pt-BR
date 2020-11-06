---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426020"
---
# <span data-ttu-id="2e130-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="2e130-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="2e130-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e130-102">SYNOPSIS</span></span>
<span data-ttu-id="2e130-103">Obter as métricas do plano.</span><span class="sxs-lookup"><span data-stu-id="2e130-103">Get the plan metrics.</span></span>

## <span data-ttu-id="2e130-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e130-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="2e130-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e130-105">DESCRIPTION</span></span>
<span data-ttu-id="2e130-106">Obter as métricas do plano.</span><span class="sxs-lookup"><span data-stu-id="2e130-106">Get the plan metrics.</span></span>

## <span data-ttu-id="2e130-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e130-107">EXAMPLES</span></span>

### <span data-ttu-id="2e130-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e130-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="2e130-109">Obter as métricas de um plano.</span><span class="sxs-lookup"><span data-stu-id="2e130-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="2e130-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e130-110">PARAMETERS</span></span>

### <span data-ttu-id="2e130-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2e130-111">-PlanName</span></span>
<span data-ttu-id="2e130-112">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="2e130-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e130-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e130-113">-ResourceGroupName</span></span>
<span data-ttu-id="2e130-114">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="2e130-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e130-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e130-115">CommonParameters</span></span>
<span data-ttu-id="2e130-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e130-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e130-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e130-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e130-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e130-118">INPUTS</span></span>

## <span data-ttu-id="2e130-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e130-119">OUTPUTS</span></span>

### <span data-ttu-id="2e130-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="2e130-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="2e130-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e130-121">NOTES</span></span>

## <span data-ttu-id="2e130-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e130-122">RELATED LINKS</span></span>

