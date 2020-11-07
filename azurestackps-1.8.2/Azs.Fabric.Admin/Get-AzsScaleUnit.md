---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947060"
---
# <span data-ttu-id="a916f-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a916f-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="a916f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a916f-102">SYNOPSIS</span></span>
<span data-ttu-id="a916f-103">Retorna uma lista de todas as unidades de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="a916f-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="a916f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a916f-104">SYNTAX</span></span>

### <span data-ttu-id="a916f-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="a916f-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a916f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a916f-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a916f-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="a916f-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a916f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a916f-108">DESCRIPTION</span></span>
<span data-ttu-id="a916f-109">Retorna uma lista de todas as unidades de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="a916f-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="a916f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a916f-110">EXAMPLES</span></span>

### <span data-ttu-id="a916f-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="a916f-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="a916f-112">Retornar uma lista de informações sobre unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="a916f-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="a916f-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="a916f-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="a916f-114">Retorna informações sobre uma unidade de escala específica.</span><span class="sxs-lookup"><span data-stu-id="a916f-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="a916f-115">OS</span><span class="sxs-lookup"><span data-stu-id="a916f-115">PARAMETERS</span></span>

### <span data-ttu-id="a916f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a916f-116">-Name</span></span>
<span data-ttu-id="a916f-117">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="a916f-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="a916f-118">-Local</span><span class="sxs-lookup"><span data-stu-id="a916f-118">-Location</span></span>
<span data-ttu-id="a916f-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="a916f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a916f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a916f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a916f-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="a916f-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a916f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a916f-122">-ResourceId</span></span>
<span data-ttu-id="a916f-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a916f-123">The resource id.</span></span>

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

### <span data-ttu-id="a916f-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a916f-124">-Filter</span></span>
<span data-ttu-id="a916f-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a916f-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="a916f-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="a916f-126">-Skip</span></span>
<span data-ttu-id="a916f-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a916f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a916f-128">-Início</span><span class="sxs-lookup"><span data-stu-id="a916f-128">-Top</span></span>
<span data-ttu-id="a916f-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a916f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a916f-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a916f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a916f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a916f-131">CommonParameters</span></span>
<span data-ttu-id="a916f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a916f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a916f-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a916f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a916f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a916f-134">INPUTS</span></span>

## <span data-ttu-id="a916f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a916f-135">OUTPUTS</span></span>

### <span data-ttu-id="a916f-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a916f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="a916f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a916f-137">NOTES</span></span>

## <span data-ttu-id="a916f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a916f-138">RELATED LINKS</span></span>
