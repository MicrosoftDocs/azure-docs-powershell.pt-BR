---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d5870624b6d39b3e821ed6a7fb76d87c8422ab2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601730"
---
# <span data-ttu-id="63ddf-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="63ddf-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="63ddf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="63ddf-103">Retorna uma lista de todos os nós de unidade de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="63ddf-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="63ddf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63ddf-104">SYNTAX</span></span>

### <span data-ttu-id="63ddf-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="63ddf-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="63ddf-106">Obter</span><span class="sxs-lookup"><span data-stu-id="63ddf-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="63ddf-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="63ddf-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="63ddf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63ddf-108">DESCRIPTION</span></span>
<span data-ttu-id="63ddf-109">Retorna uma lista de todos os nós de unidade de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="63ddf-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="63ddf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63ddf-110">EXAMPLES</span></span>

### <span data-ttu-id="63ddf-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="63ddf-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="63ddf-112">Obter todos os nós de unidade de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="63ddf-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="63ddf-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="63ddf-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="63ddf-114">Obtenha um nó de unidade de escala específico em um local com um nome.</span><span class="sxs-lookup"><span data-stu-id="63ddf-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="63ddf-115">OS</span><span class="sxs-lookup"><span data-stu-id="63ddf-115">PARAMETERS</span></span>

### <span data-ttu-id="63ddf-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="63ddf-116">-Filter</span></span>
<span data-ttu-id="63ddf-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="63ddf-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="63ddf-118">-Local</span><span class="sxs-lookup"><span data-stu-id="63ddf-118">-Location</span></span>
<span data-ttu-id="63ddf-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="63ddf-119">Location of the resource.</span></span>

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

### <span data-ttu-id="63ddf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="63ddf-120">-Name</span></span>
<span data-ttu-id="63ddf-121">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="63ddf-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="63ddf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ddf-122">-ResourceGroupName</span></span>
<span data-ttu-id="63ddf-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="63ddf-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="63ddf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63ddf-124">-ResourceId</span></span>
<span data-ttu-id="63ddf-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="63ddf-125">The resource id.</span></span>

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

### <span data-ttu-id="63ddf-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="63ddf-126">-Skip</span></span>
<span data-ttu-id="63ddf-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="63ddf-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="63ddf-128">-Início</span><span class="sxs-lookup"><span data-stu-id="63ddf-128">-Top</span></span>
<span data-ttu-id="63ddf-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="63ddf-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="63ddf-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="63ddf-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="63ddf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ddf-131">CommonParameters</span></span>
<span data-ttu-id="63ddf-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63ddf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ddf-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ddf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ddf-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63ddf-134">INPUTS</span></span>

## <span data-ttu-id="63ddf-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63ddf-135">OUTPUTS</span></span>

### <span data-ttu-id="63ddf-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="63ddf-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="63ddf-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63ddf-137">NOTES</span></span>

## <span data-ttu-id="63ddf-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63ddf-138">RELATED LINKS</span></span>

