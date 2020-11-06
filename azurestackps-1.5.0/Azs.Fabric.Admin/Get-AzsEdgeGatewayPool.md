---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67a49abc82ba1ec8d9411141d456b8f71f75600f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425610"
---
# <span data-ttu-id="de6ed-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="de6ed-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="de6ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="de6ed-103">Retorna objetos do pool de gateway em um local.</span><span class="sxs-lookup"><span data-stu-id="de6ed-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="de6ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de6ed-104">SYNTAX</span></span>

### <span data-ttu-id="de6ed-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="de6ed-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="de6ed-106">Obter</span><span class="sxs-lookup"><span data-stu-id="de6ed-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="de6ed-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="de6ed-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="de6ed-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de6ed-108">DESCRIPTION</span></span>
<span data-ttu-id="de6ed-109">Retorna objetos do pool do gateway de borda em um local.</span><span class="sxs-lookup"><span data-stu-id="de6ed-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="de6ed-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de6ed-110">EXAMPLES</span></span>

### <span data-ttu-id="de6ed-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="de6ed-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="de6ed-112">Obter uma lista de todos os pools de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="de6ed-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="de6ed-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="de6ed-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="de6ed-114">Obter um pool específico do gateway de borda.</span><span class="sxs-lookup"><span data-stu-id="de6ed-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="de6ed-115">OS</span><span class="sxs-lookup"><span data-stu-id="de6ed-115">PARAMETERS</span></span>

### <span data-ttu-id="de6ed-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="de6ed-116">-Filter</span></span>
<span data-ttu-id="de6ed-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="de6ed-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="de6ed-118">-Local</span><span class="sxs-lookup"><span data-stu-id="de6ed-118">-Location</span></span>
<span data-ttu-id="de6ed-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="de6ed-119">Location of the resource.</span></span>

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

### <span data-ttu-id="de6ed-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="de6ed-120">-Name</span></span>
<span data-ttu-id="de6ed-121">Nome do pool de gateways de borda.</span><span class="sxs-lookup"><span data-stu-id="de6ed-121">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="de6ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="de6ed-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="de6ed-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="de6ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de6ed-124">-ResourceId</span></span>
<span data-ttu-id="de6ed-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="de6ed-125">The resource id.</span></span>

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

### <span data-ttu-id="de6ed-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="de6ed-126">-Skip</span></span>
<span data-ttu-id="de6ed-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de6ed-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="de6ed-128">-Início</span><span class="sxs-lookup"><span data-stu-id="de6ed-128">-Top</span></span>
<span data-ttu-id="de6ed-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de6ed-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="de6ed-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="de6ed-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="de6ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6ed-131">CommonParameters</span></span>
<span data-ttu-id="de6ed-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de6ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6ed-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de6ed-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6ed-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de6ed-134">INPUTS</span></span>

## <span data-ttu-id="de6ed-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de6ed-135">OUTPUTS</span></span>

### <span data-ttu-id="de6ed-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="de6ed-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="de6ed-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de6ed-137">NOTES</span></span>

## <span data-ttu-id="de6ed-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de6ed-138">RELATED LINKS</span></span>

