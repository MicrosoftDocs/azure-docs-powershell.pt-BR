---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774615"
---
# <span data-ttu-id="3862a-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="3862a-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="3862a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3862a-102">SYNOPSIS</span></span>
<span data-ttu-id="3862a-103">Retorna uma lista de todos os pools de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="3862a-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="3862a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3862a-104">SYNTAX</span></span>

### <span data-ttu-id="3862a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="3862a-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3862a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3862a-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3862a-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="3862a-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3862a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3862a-108">DESCRIPTION</span></span>
<span data-ttu-id="3862a-109">Retorna uma lista de todos os pools de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="3862a-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="3862a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3862a-110">EXAMPLES</span></span>

### <span data-ttu-id="3862a-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="3862a-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="3862a-112">Obter todos os pools de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="3862a-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="3862a-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="3862a-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="3862a-114">Obtenha um pool de armazenamento em um determinado local, dado um nome de pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3862a-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="3862a-115">OS</span><span class="sxs-lookup"><span data-stu-id="3862a-115">PARAMETERS</span></span>

### <span data-ttu-id="3862a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3862a-116">-Name</span></span>
<span data-ttu-id="3862a-117">Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3862a-117">Storage pool name.</span></span>

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

### <span data-ttu-id="3862a-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="3862a-118">-StorageSystem</span></span>
<span data-ttu-id="3862a-119">Nome do subsistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3862a-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="3862a-120">-Local</span><span class="sxs-lookup"><span data-stu-id="3862a-120">-Location</span></span>
<span data-ttu-id="3862a-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="3862a-121">Location of the resource.</span></span>

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

### <span data-ttu-id="3862a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3862a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3862a-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="3862a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3862a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3862a-124">-ResourceId</span></span>
<span data-ttu-id="3862a-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3862a-125">The resource id.</span></span>

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

### <span data-ttu-id="3862a-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3862a-126">-Filter</span></span>
<span data-ttu-id="3862a-127">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="3862a-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="3862a-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="3862a-128">-Skip</span></span>
<span data-ttu-id="3862a-129">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3862a-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3862a-130">-Início</span><span class="sxs-lookup"><span data-stu-id="3862a-130">-Top</span></span>
<span data-ttu-id="3862a-131">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3862a-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3862a-132">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="3862a-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3862a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3862a-133">CommonParameters</span></span>
<span data-ttu-id="3862a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3862a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3862a-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3862a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3862a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3862a-136">INPUTS</span></span>

## <span data-ttu-id="3862a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3862a-137">OUTPUTS</span></span>

### <span data-ttu-id="3862a-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="3862a-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="3862a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3862a-139">NOTES</span></span>

## <span data-ttu-id="3862a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3862a-140">RELATED LINKS</span></span>
