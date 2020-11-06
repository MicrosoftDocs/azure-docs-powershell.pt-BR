---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601698"
---
# <span data-ttu-id="54f0c-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="54f0c-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="54f0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="54f0c-103">Retorna uma lista de todas as unidades de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="54f0c-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="54f0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54f0c-104">SYNTAX</span></span>

### <span data-ttu-id="54f0c-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="54f0c-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="54f0c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="54f0c-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="54f0c-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="54f0c-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="54f0c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54f0c-108">DESCRIPTION</span></span>
<span data-ttu-id="54f0c-109">Retorna uma lista de todas as unidades de escala em um local.</span><span class="sxs-lookup"><span data-stu-id="54f0c-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="54f0c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54f0c-110">EXAMPLES</span></span>

### <span data-ttu-id="54f0c-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54f0c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="54f0c-112">Retornar uma lista de informações sobre unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="54f0c-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="54f0c-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="54f0c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="54f0c-114">Retorna informações sobre uma unidade de escala específica.</span><span class="sxs-lookup"><span data-stu-id="54f0c-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="54f0c-115">OS</span><span class="sxs-lookup"><span data-stu-id="54f0c-115">PARAMETERS</span></span>

### <span data-ttu-id="54f0c-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="54f0c-116">-Filter</span></span>
<span data-ttu-id="54f0c-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="54f0c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="54f0c-118">-Local</span><span class="sxs-lookup"><span data-stu-id="54f0c-118">-Location</span></span>
<span data-ttu-id="54f0c-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="54f0c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="54f0c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="54f0c-120">-Name</span></span>
<span data-ttu-id="54f0c-121">Nome das unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="54f0c-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="54f0c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f0c-122">-ResourceGroupName</span></span>
<span data-ttu-id="54f0c-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="54f0c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="54f0c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54f0c-124">-ResourceId</span></span>
<span data-ttu-id="54f0c-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="54f0c-125">The resource id.</span></span>

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

### <span data-ttu-id="54f0c-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="54f0c-126">-Skip</span></span>
<span data-ttu-id="54f0c-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="54f0c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="54f0c-128">-Início</span><span class="sxs-lookup"><span data-stu-id="54f0c-128">-Top</span></span>
<span data-ttu-id="54f0c-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="54f0c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="54f0c-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="54f0c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="54f0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f0c-131">CommonParameters</span></span>
<span data-ttu-id="54f0c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f0c-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f0c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f0c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54f0c-134">INPUTS</span></span>

## <span data-ttu-id="54f0c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54f0c-135">OUTPUTS</span></span>

### <span data-ttu-id="54f0c-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="54f0c-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="54f0c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54f0c-137">NOTES</span></span>

## <span data-ttu-id="54f0c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54f0c-138">RELATED LINKS</span></span>

