---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774445"
---
# <span data-ttu-id="b03e8-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="b03e8-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="b03e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b03e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b03e8-103">Retorna uma lista de status de integridade da região.</span><span class="sxs-lookup"><span data-stu-id="b03e8-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="b03e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b03e8-104">SYNTAX</span></span>

### <span data-ttu-id="b03e8-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b03e8-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="b03e8-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b03e8-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b03e8-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="b03e8-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b03e8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b03e8-108">DESCRIPTION</span></span>
<span data-ttu-id="b03e8-109">Retorna uma lista de status de integridade da região.</span><span class="sxs-lookup"><span data-stu-id="b03e8-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="b03e8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b03e8-110">EXAMPLES</span></span>

### <span data-ttu-id="b03e8-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b03e8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="b03e8-112">Retorna uma lista de status de integridade da região.</span><span class="sxs-lookup"><span data-stu-id="b03e8-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="b03e8-113">OS</span><span class="sxs-lookup"><span data-stu-id="b03e8-113">PARAMETERS</span></span>

### <span data-ttu-id="b03e8-114">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b03e8-114">-Filter</span></span>
<span data-ttu-id="b03e8-115">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="b03e8-115">OData filter parameter.</span></span>

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

### <span data-ttu-id="b03e8-116">-Local</span><span class="sxs-lookup"><span data-stu-id="b03e8-116">-Location</span></span>
<span data-ttu-id="b03e8-117">Nome da região</span><span class="sxs-lookup"><span data-stu-id="b03e8-117">Name of the region</span></span>

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

### <span data-ttu-id="b03e8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b03e8-118">-ResourceGroupName</span></span>
<span data-ttu-id="b03e8-119">Nome do grupo de recursos do qual o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="b03e8-119">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="b03e8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b03e8-120">-ResourceId</span></span>
<span data-ttu-id="b03e8-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b03e8-121">The resource id.</span></span>

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

### <span data-ttu-id="b03e8-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="b03e8-122">-Skip</span></span>
<span data-ttu-id="b03e8-123">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b03e8-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b03e8-124">-Início</span><span class="sxs-lookup"><span data-stu-id="b03e8-124">-Top</span></span>
<span data-ttu-id="b03e8-125">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b03e8-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b03e8-126">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="b03e8-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b03e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03e8-127">CommonParameters</span></span>
<span data-ttu-id="b03e8-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03e8-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03e8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03e8-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b03e8-130">INPUTS</span></span>

## <span data-ttu-id="b03e8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b03e8-131">OUTPUTS</span></span>

### <span data-ttu-id="b03e8-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="b03e8-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="b03e8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b03e8-133">NOTES</span></span>

## <span data-ttu-id="b03e8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b03e8-134">RELATED LINKS</span></span>
