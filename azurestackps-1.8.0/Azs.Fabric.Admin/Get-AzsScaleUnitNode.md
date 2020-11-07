---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774620"
---
# <span data-ttu-id="c0d16-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c0d16-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c0d16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0d16-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d16-103">Retorna uma lista de todos os nós de unidade de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="c0d16-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="c0d16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0d16-104">SYNTAX</span></span>

### <span data-ttu-id="c0d16-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0d16-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c0d16-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c0d16-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c0d16-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="c0d16-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c0d16-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0d16-108">DESCRIPTION</span></span>
<span data-ttu-id="c0d16-109">Retorna uma lista de todos os nós de unidade de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="c0d16-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="c0d16-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0d16-110">EXAMPLES</span></span>

### <span data-ttu-id="c0d16-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="c0d16-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="c0d16-112">Obter todos os nós de unidade de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="c0d16-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="c0d16-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="c0d16-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="c0d16-114">Obtenha um nó de unidade de escala específico em um local com um nome.</span><span class="sxs-lookup"><span data-stu-id="c0d16-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="c0d16-115">OS</span><span class="sxs-lookup"><span data-stu-id="c0d16-115">PARAMETERS</span></span>

### <span data-ttu-id="c0d16-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0d16-116">-Name</span></span>
<span data-ttu-id="c0d16-117">Nome do nó da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="c0d16-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="c0d16-118">-Local</span><span class="sxs-lookup"><span data-stu-id="c0d16-118">-Location</span></span>
<span data-ttu-id="c0d16-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c0d16-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c0d16-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d16-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0d16-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="c0d16-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c0d16-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d16-122">-ResourceId</span></span>
<span data-ttu-id="c0d16-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c0d16-123">The resource id.</span></span>

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

### <span data-ttu-id="c0d16-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c0d16-124">-Filter</span></span>
<span data-ttu-id="c0d16-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c0d16-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="c0d16-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="c0d16-126">-Skip</span></span>
<span data-ttu-id="c0d16-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c0d16-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c0d16-128">-Início</span><span class="sxs-lookup"><span data-stu-id="c0d16-128">-Top</span></span>
<span data-ttu-id="c0d16-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c0d16-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c0d16-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="c0d16-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c0d16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d16-131">CommonParameters</span></span>
<span data-ttu-id="c0d16-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d16-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d16-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d16-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0d16-134">INPUTS</span></span>

## <span data-ttu-id="c0d16-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0d16-135">OUTPUTS</span></span>

### <span data-ttu-id="c0d16-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c0d16-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="c0d16-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0d16-137">NOTES</span></span>

## <span data-ttu-id="c0d16-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0d16-138">RELATED LINKS</span></span>
