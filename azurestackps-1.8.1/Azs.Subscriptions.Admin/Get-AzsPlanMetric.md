---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774924"
---
# <span data-ttu-id="a5382-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="a5382-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="a5382-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5382-102">SYNOPSIS</span></span>
<span data-ttu-id="a5382-103">Obter as métricas do plano.</span><span class="sxs-lookup"><span data-stu-id="a5382-103">Get the plan metrics.</span></span>

## <span data-ttu-id="a5382-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5382-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="a5382-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5382-105">DESCRIPTION</span></span>
<span data-ttu-id="a5382-106">Obter as métricas do plano.</span><span class="sxs-lookup"><span data-stu-id="a5382-106">Get the plan metrics.</span></span>

## <span data-ttu-id="a5382-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5382-107">EXAMPLES</span></span>

### <span data-ttu-id="a5382-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a5382-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="a5382-109">Obter as métricas de um plano.</span><span class="sxs-lookup"><span data-stu-id="a5382-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="a5382-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5382-110">PARAMETERS</span></span>

### <span data-ttu-id="a5382-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="a5382-111">-PlanName</span></span>
<span data-ttu-id="a5382-112">Nome do plano.</span><span class="sxs-lookup"><span data-stu-id="a5382-112">Name of the plan.</span></span>

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

### <span data-ttu-id="a5382-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5382-113">-ResourceGroupName</span></span>
<span data-ttu-id="a5382-114">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="a5382-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a5382-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5382-115">CommonParameters</span></span>
<span data-ttu-id="a5382-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5382-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5382-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5382-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5382-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5382-118">INPUTS</span></span>

## <span data-ttu-id="a5382-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5382-119">OUTPUTS</span></span>

### <span data-ttu-id="a5382-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="a5382-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="a5382-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5382-121">NOTES</span></span>

## <span data-ttu-id="a5382-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5382-122">RELATED LINKS</span></span>

