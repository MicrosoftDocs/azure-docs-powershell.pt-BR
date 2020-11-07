---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947110"
---
# <span data-ttu-id="bded1-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="bded1-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="bded1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bded1-102">SYNOPSIS</span></span>
<span data-ttu-id="bded1-103">Retorna uma lista de status de integridade da região.</span><span class="sxs-lookup"><span data-stu-id="bded1-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="bded1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bded1-104">SYNTAX</span></span>

### <span data-ttu-id="bded1-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="bded1-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="bded1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="bded1-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bded1-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="bded1-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bded1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bded1-108">DESCRIPTION</span></span>
<span data-ttu-id="bded1-109">Retorna uma lista de status de integridade da região.</span><span class="sxs-lookup"><span data-stu-id="bded1-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="bded1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bded1-110">EXAMPLES</span></span>

### <span data-ttu-id="bded1-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="bded1-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="bded1-112">Retorna uma lista de status de integridade da região.</span><span class="sxs-lookup"><span data-stu-id="bded1-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="bded1-113">OS</span><span class="sxs-lookup"><span data-stu-id="bded1-113">PARAMETERS</span></span>

### <span data-ttu-id="bded1-114">-Local</span><span class="sxs-lookup"><span data-stu-id="bded1-114">-Location</span></span>
<span data-ttu-id="bded1-115">Nome da região</span><span class="sxs-lookup"><span data-stu-id="bded1-115">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bded1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bded1-116">-ResourceGroupName</span></span>
<span data-ttu-id="bded1-117">Nome do grupo de recursos, opcional.</span><span class="sxs-lookup"><span data-stu-id="bded1-117">Resource group name, optional.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bded1-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bded1-118">-ResourceId</span></span>
<span data-ttu-id="bded1-119">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bded1-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bded1-120">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bded1-120">-Filter</span></span>
<span data-ttu-id="bded1-121">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="bded1-121">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bded1-122">-Início</span><span class="sxs-lookup"><span data-stu-id="bded1-122">-Top</span></span>
<span data-ttu-id="bded1-123">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bded1-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bded1-124">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="bded1-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bded1-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="bded1-125">-Skip</span></span>
<span data-ttu-id="bded1-126">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bded1-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bded1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bded1-127">CommonParameters</span></span>
<span data-ttu-id="bded1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bded1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bded1-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bded1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bded1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bded1-130">INPUTS</span></span>

## <span data-ttu-id="bded1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bded1-131">OUTPUTS</span></span>

### <span data-ttu-id="bded1-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="bded1-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="bded1-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bded1-133">NOTES</span></span>

## <span data-ttu-id="bded1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bded1-134">RELATED LINKS</span></span>
