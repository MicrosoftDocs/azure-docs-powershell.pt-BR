---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcd5d112fea0ec68e372a5ad282b3d661f9481ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595627"
---
# <span data-ttu-id="52311-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="52311-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="52311-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52311-102">SYNOPSIS</span></span>
<span data-ttu-id="52311-103">Retorna uma lista de todos os locais de malha.</span><span class="sxs-lookup"><span data-stu-id="52311-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="52311-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52311-104">SYNTAX</span></span>

### <span data-ttu-id="52311-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="52311-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="52311-106">Obter</span><span class="sxs-lookup"><span data-stu-id="52311-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="52311-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="52311-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="52311-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52311-108">DESCRIPTION</span></span>
<span data-ttu-id="52311-109">Retorna uma lista de todos os locais de malha.</span><span class="sxs-lookup"><span data-stu-id="52311-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="52311-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52311-110">EXAMPLES</span></span>

### <span data-ttu-id="52311-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="52311-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="52311-112">Retorne uma lista de todos os locais de malha.</span><span class="sxs-lookup"><span data-stu-id="52311-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="52311-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="52311-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="52311-114">Retorne um local com base no nome.</span><span class="sxs-lookup"><span data-stu-id="52311-114">Return a location based on the name.</span></span>

## <span data-ttu-id="52311-115">OS</span><span class="sxs-lookup"><span data-stu-id="52311-115">PARAMETERS</span></span>

### <span data-ttu-id="52311-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="52311-116">-Filter</span></span>
<span data-ttu-id="52311-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="52311-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="52311-118">-Local</span><span class="sxs-lookup"><span data-stu-id="52311-118">-Location</span></span>
<span data-ttu-id="52311-119">Localização do tecido.</span><span class="sxs-lookup"><span data-stu-id="52311-119">Fabric location.</span></span>

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

### <span data-ttu-id="52311-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52311-120">-ResourceGroupName</span></span>
<span data-ttu-id="52311-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="52311-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="52311-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52311-122">-ResourceId</span></span>
<span data-ttu-id="52311-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="52311-123">The resource id.</span></span>

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

### <span data-ttu-id="52311-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="52311-124">-Skip</span></span>
<span data-ttu-id="52311-125">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="52311-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="52311-126">-Início</span><span class="sxs-lookup"><span data-stu-id="52311-126">-Top</span></span>
<span data-ttu-id="52311-127">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="52311-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="52311-128">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="52311-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="52311-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52311-129">CommonParameters</span></span>
<span data-ttu-id="52311-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52311-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52311-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52311-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52311-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52311-132">INPUTS</span></span>

## <span data-ttu-id="52311-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52311-133">OUTPUTS</span></span>

### <span data-ttu-id="52311-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="52311-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="52311-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52311-135">NOTES</span></span>

## <span data-ttu-id="52311-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52311-136">RELATED LINKS</span></span>

