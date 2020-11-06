---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8228a8605462b71fce598c7dc44454a16e1d7c90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601696"
---
# <span data-ttu-id="9c9ec-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="9c9ec-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="9c9ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9ec-103">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-103">Get the offer metrics.</span></span>

## <span data-ttu-id="9c9ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c9ec-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="9c9ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="9c9ec-106">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-106">Get the offer metrics.</span></span>

## <span data-ttu-id="9c9ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="9c9ec-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9c9ec-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="9c9ec-109">Obter as métricas da oferta.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-109">Get the offer metrics.</span></span>

## <span data-ttu-id="9c9ec-110">OS</span><span class="sxs-lookup"><span data-stu-id="9c9ec-110">PARAMETERS</span></span>

### <span data-ttu-id="9c9ec-111">-Offername</span><span class="sxs-lookup"><span data-stu-id="9c9ec-111">-OfferName</span></span>
<span data-ttu-id="9c9ec-112">Nome de uma oferta.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-112">Name of an offer.</span></span>

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

### <span data-ttu-id="9c9ec-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c9ec-113">-ResourceGroupName</span></span>
<span data-ttu-id="9c9ec-114">O grupo de recursos no qual o recurso está localizado.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9c9ec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9ec-115">CommonParameters</span></span>
<span data-ttu-id="9c9ec-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9ec-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c9ec-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9ec-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c9ec-118">INPUTS</span></span>

## <span data-ttu-id="9c9ec-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c9ec-119">OUTPUTS</span></span>

### <span data-ttu-id="9c9ec-120">Microsoft. AzureStack. Management. subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="9c9ec-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="9c9ec-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c9ec-121">NOTES</span></span>

## <span data-ttu-id="9c9ec-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c9ec-122">RELATED LINKS</span></span>

