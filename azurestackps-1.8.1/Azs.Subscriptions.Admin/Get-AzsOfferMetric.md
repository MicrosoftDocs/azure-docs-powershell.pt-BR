---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774930"
---
# <span data-ttu-id="93d31-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="93d31-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="93d31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93d31-102">SYNOPSIS</span></span>
<span data-ttu-id="93d31-103">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="93d31-103">Get the offer metrics.</span></span>

## <span data-ttu-id="93d31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93d31-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="93d31-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93d31-105">DESCRIPTION</span></span>
<span data-ttu-id="93d31-106">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="93d31-106">Get the offer metrics.</span></span>

## <span data-ttu-id="93d31-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93d31-107">EXAMPLES</span></span>

### <span data-ttu-id="93d31-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="93d31-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="93d31-109">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="93d31-109">Get the offer metrics.</span></span>

## <span data-ttu-id="93d31-110">OS</span><span class="sxs-lookup"><span data-stu-id="93d31-110">PARAMETERS</span></span>

### <span data-ttu-id="93d31-111">-Offername</span><span class="sxs-lookup"><span data-stu-id="93d31-111">-OfferName</span></span>
<span data-ttu-id="93d31-112">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="93d31-112">Name of an offer.</span></span>

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

### <span data-ttu-id="93d31-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d31-113">-ResourceGroupName</span></span>
<span data-ttu-id="93d31-114">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="93d31-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="93d31-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d31-115">CommonParameters</span></span>
<span data-ttu-id="93d31-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d31-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d31-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d31-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d31-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93d31-118">INPUTS</span></span>

## <span data-ttu-id="93d31-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93d31-119">OUTPUTS</span></span>

### <span data-ttu-id="93d31-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="93d31-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="93d31-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93d31-121">NOTES</span></span>

## <span data-ttu-id="93d31-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93d31-122">RELATED LINKS</span></span>

