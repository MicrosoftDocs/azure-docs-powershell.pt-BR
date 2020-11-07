---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774624"
---
# <span data-ttu-id="0b11c-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="0b11c-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="0b11c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b11c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b11c-103">Retorna uma lista de todas as unidades de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="0b11c-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="0b11c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b11c-104">SYNTAX</span></span>

### <span data-ttu-id="0b11c-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b11c-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0b11c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="0b11c-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0b11c-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="0b11c-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0b11c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b11c-108">DESCRIPTION</span></span>
<span data-ttu-id="0b11c-109">Retorna uma lista de todas as unidades de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="0b11c-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="0b11c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b11c-110">EXAMPLES</span></span>

### <span data-ttu-id="0b11c-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="0b11c-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="0b11c-112">Retornar uma lista de informações sobre unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="0b11c-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="0b11c-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="0b11c-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="0b11c-114">Retorna informações sobre uma unidade de escala específica.</span><span class="sxs-lookup"><span data-stu-id="0b11c-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="0b11c-115">OS</span><span class="sxs-lookup"><span data-stu-id="0b11c-115">PARAMETERS</span></span>

### <span data-ttu-id="0b11c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b11c-116">-Name</span></span>
<span data-ttu-id="0b11c-117">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="0b11c-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="0b11c-118">-Local</span><span class="sxs-lookup"><span data-stu-id="0b11c-118">-Location</span></span>
<span data-ttu-id="0b11c-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b11c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0b11c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b11c-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b11c-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="0b11c-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0b11c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b11c-122">-ResourceId</span></span>
<span data-ttu-id="0b11c-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b11c-123">The resource id.</span></span>

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

### <span data-ttu-id="0b11c-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="0b11c-124">-Filter</span></span>
<span data-ttu-id="0b11c-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="0b11c-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="0b11c-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="0b11c-126">-Skip</span></span>
<span data-ttu-id="0b11c-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b11c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0b11c-128">-Início</span><span class="sxs-lookup"><span data-stu-id="0b11c-128">-Top</span></span>
<span data-ttu-id="0b11c-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b11c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0b11c-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="0b11c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0b11c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b11c-131">CommonParameters</span></span>
<span data-ttu-id="0b11c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b11c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b11c-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b11c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b11c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b11c-134">INPUTS</span></span>

## <span data-ttu-id="0b11c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b11c-135">OUTPUTS</span></span>

### <span data-ttu-id="0b11c-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="0b11c-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="0b11c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b11c-137">NOTES</span></span>

## <span data-ttu-id="0b11c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b11c-138">RELATED LINKS</span></span>
