---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426132"
---
# <span data-ttu-id="d8644-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="d8644-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="d8644-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8644-102">SYNOPSIS</span></span>
<span data-ttu-id="d8644-103">Retorna uma lista de todas as sub-redes lógicas.</span><span class="sxs-lookup"><span data-stu-id="d8644-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="d8644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8644-104">SYNTAX</span></span>

### <span data-ttu-id="d8644-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8644-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d8644-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d8644-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8644-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="d8644-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d8644-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8644-108">DESCRIPTION</span></span>
<span data-ttu-id="d8644-109">Retorna uma lista de todas as sub-redes lógicas.</span><span class="sxs-lookup"><span data-stu-id="d8644-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="d8644-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8644-110">EXAMPLES</span></span>

### <span data-ttu-id="d8644-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8644-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="d8644-112">Obter uma lista de todas as sub-redes lógicas para uma determinada rede lógica e local.</span><span class="sxs-lookup"><span data-stu-id="d8644-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="d8644-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8644-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="d8644-114">Obter uma sub-rede lógica específica para uma determinada rede lógica e localização com base no nome.</span><span class="sxs-lookup"><span data-stu-id="d8644-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="d8644-115">OS</span><span class="sxs-lookup"><span data-stu-id="d8644-115">PARAMETERS</span></span>

### <span data-ttu-id="d8644-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d8644-116">-Filter</span></span>
<span data-ttu-id="d8644-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d8644-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="d8644-118">-Local</span><span class="sxs-lookup"><span data-stu-id="d8644-118">-Location</span></span>
<span data-ttu-id="d8644-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8644-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d8644-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="d8644-120">-LogicalNetwork</span></span>
<span data-ttu-id="d8644-121">Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="d8644-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8644-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8644-122">-Name</span></span>
<span data-ttu-id="d8644-123">Nome da sub-rede lógica.</span><span class="sxs-lookup"><span data-stu-id="d8644-123">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8644-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8644-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8644-125">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="d8644-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d8644-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8644-126">-ResourceId</span></span>
<span data-ttu-id="d8644-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8644-127">The resource id.</span></span>

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

### <span data-ttu-id="d8644-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="d8644-128">-Skip</span></span>
<span data-ttu-id="d8644-129">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d8644-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d8644-130">-Início</span><span class="sxs-lookup"><span data-stu-id="d8644-130">-Top</span></span>
<span data-ttu-id="d8644-131">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d8644-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d8644-132">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d8644-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d8644-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8644-133">CommonParameters</span></span>
<span data-ttu-id="d8644-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8644-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8644-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8644-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8644-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8644-136">INPUTS</span></span>

## <span data-ttu-id="d8644-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8644-137">OUTPUTS</span></span>

### <span data-ttu-id="d8644-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="d8644-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="d8644-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8644-139">NOTES</span></span>

## <span data-ttu-id="d8644-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8644-140">RELATED LINKS</span></span>

