---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93947015"
---
# <span data-ttu-id="7f0e0-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="7f0e0-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="7f0e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0e0-103">Retorna uma lista de todos os pools de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="7f0e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f0e0-104">SYNTAX</span></span>

### <span data-ttu-id="7f0e0-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f0e0-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7f0e0-106">Obter</span><span class="sxs-lookup"><span data-stu-id="7f0e0-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f0e0-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="7f0e0-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7f0e0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f0e0-108">DESCRIPTION</span></span>
<span data-ttu-id="7f0e0-109">Retorna uma lista de todos os pools de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="7f0e0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f0e0-110">EXAMPLES</span></span>

### <span data-ttu-id="7f0e0-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="7f0e0-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="7f0e0-112">Obter todos os pools de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="7f0e0-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="7f0e0-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="7f0e0-114">Obtenha um pool de armazenamento em um determinado local, dado um nome de pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="7f0e0-115">OS</span><span class="sxs-lookup"><span data-stu-id="7f0e0-115">PARAMETERS</span></span>

### <span data-ttu-id="7f0e0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f0e0-116">-Name</span></span>
<span data-ttu-id="7f0e0-117">Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-117">Storage pool name.</span></span>

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

### <span data-ttu-id="7f0e0-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="7f0e0-118">-StorageSystem</span></span>
<span data-ttu-id="7f0e0-119">Nome do subsistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="7f0e0-120">-Local</span><span class="sxs-lookup"><span data-stu-id="7f0e0-120">-Location</span></span>
<span data-ttu-id="7f0e0-121">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-121">Location of the resource.</span></span>

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

### <span data-ttu-id="7f0e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f0e0-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7f0e0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f0e0-124">-ResourceId</span></span>
<span data-ttu-id="7f0e0-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-125">The resource id.</span></span>

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

### <span data-ttu-id="7f0e0-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="7f0e0-126">-Filter</span></span>
<span data-ttu-id="7f0e0-127">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="7f0e0-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="7f0e0-128">-Skip</span></span>
<span data-ttu-id="7f0e0-129">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7f0e0-130">-Início</span><span class="sxs-lookup"><span data-stu-id="7f0e0-130">-Top</span></span>
<span data-ttu-id="7f0e0-131">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7f0e0-132">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7f0e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0e0-133">CommonParameters</span></span>
<span data-ttu-id="7f0e0-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0e0-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0e0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0e0-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f0e0-136">INPUTS</span></span>

## <span data-ttu-id="7f0e0-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f0e0-137">OUTPUTS</span></span>

### <span data-ttu-id="7f0e0-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="7f0e0-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="7f0e0-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f0e0-139">NOTES</span></span>

## <span data-ttu-id="7f0e0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f0e0-140">RELATED LINKS</span></span>
