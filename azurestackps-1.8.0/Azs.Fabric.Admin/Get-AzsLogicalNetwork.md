---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774628"
---
# <span data-ttu-id="2bfd4-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="2bfd4-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="2bfd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bfd4-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfd4-103">Retorna uma lista de todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="2bfd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bfd4-104">SYNTAX</span></span>

### <span data-ttu-id="2bfd4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="2bfd4-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2bfd4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="2bfd4-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2bfd4-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="2bfd4-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2bfd4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bfd4-108">DESCRIPTION</span></span>
<span data-ttu-id="2bfd4-109">Retorna uma lista de todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="2bfd4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bfd4-110">EXAMPLES</span></span>

### <span data-ttu-id="2bfd4-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="2bfd4-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="2bfd4-112">Obter todas as redes lógicas em um local.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="2bfd4-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="2bfd4-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="2bfd4-114">Obter redes lógicas específicas em um local com base em um nome.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="2bfd4-115">OS</span><span class="sxs-lookup"><span data-stu-id="2bfd4-115">PARAMETERS</span></span>

### <span data-ttu-id="2bfd4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bfd4-116">-Name</span></span>
<span data-ttu-id="2bfd4-117">Nome da rede lógica.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="2bfd4-118">-Local</span><span class="sxs-lookup"><span data-stu-id="2bfd4-118">-Location</span></span>
<span data-ttu-id="2bfd4-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-119">Location of the resource.</span></span>

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

### <span data-ttu-id="2bfd4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bfd4-120">-ResourceGroupName</span></span>
<span data-ttu-id="2bfd4-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2bfd4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bfd4-122">-ResourceId</span></span>
<span data-ttu-id="2bfd4-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-123">The resource id.</span></span>

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

### <span data-ttu-id="2bfd4-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2bfd4-124">-Filter</span></span>
<span data-ttu-id="2bfd4-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="2bfd4-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="2bfd4-126">-Skip</span></span>
<span data-ttu-id="2bfd4-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2bfd4-128">-Início</span><span class="sxs-lookup"><span data-stu-id="2bfd4-128">-Top</span></span>
<span data-ttu-id="2bfd4-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2bfd4-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2bfd4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfd4-131">CommonParameters</span></span>
<span data-ttu-id="2bfd4-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bfd4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfd4-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfd4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfd4-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bfd4-134">INPUTS</span></span>

## <span data-ttu-id="2bfd4-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bfd4-135">OUTPUTS</span></span>

### <span data-ttu-id="2bfd4-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="2bfd4-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="2bfd4-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bfd4-137">NOTES</span></span>

## <span data-ttu-id="2bfd4-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bfd4-138">RELATED LINKS</span></span>
