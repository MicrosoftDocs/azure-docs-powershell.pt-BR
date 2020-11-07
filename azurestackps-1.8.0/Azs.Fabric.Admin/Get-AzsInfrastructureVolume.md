---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774633"
---
# <span data-ttu-id="eec25-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="eec25-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="eec25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eec25-102">SYNOPSIS</span></span>
<span data-ttu-id="eec25-103">Retorna uma lista de todos os volumes de armazenamento em um local.</span><span class="sxs-lookup"><span data-stu-id="eec25-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="eec25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eec25-104">SYNTAX</span></span>

### <span data-ttu-id="eec25-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="eec25-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eec25-106">Obter</span><span class="sxs-lookup"><span data-stu-id="eec25-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="eec25-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="eec25-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="eec25-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eec25-108">DESCRIPTION</span></span>
<span data-ttu-id="eec25-109">Retorna uma lista de todos os volumes de armazenamento em um local.</span><span class="sxs-lookup"><span data-stu-id="eec25-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="eec25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eec25-110">EXAMPLES</span></span>

### <span data-ttu-id="eec25-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="eec25-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="eec25-112">Obter uma lista de todos os volumes de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="eec25-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="eec25-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="eec25-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="eec25-114">Obter um volume de armazenamento por nome em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="eec25-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="eec25-115">OS</span><span class="sxs-lookup"><span data-stu-id="eec25-115">PARAMETERS</span></span>

### <span data-ttu-id="eec25-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eec25-116">-Name</span></span>
<span data-ttu-id="eec25-117">Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eec25-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="eec25-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="eec25-118">-StoragePool</span></span>
<span data-ttu-id="eec25-119">Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eec25-119">Storage pool name.</span></span>

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

### <span data-ttu-id="eec25-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="eec25-120">-StorageSystem</span></span>
<span data-ttu-id="eec25-121">Representação de um recurso do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eec25-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="eec25-122">-Local</span><span class="sxs-lookup"><span data-stu-id="eec25-122">-Location</span></span>
<span data-ttu-id="eec25-123">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="eec25-123">Location of the resource.</span></span>

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

### <span data-ttu-id="eec25-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec25-124">-ResourceGroupName</span></span>
<span data-ttu-id="eec25-125">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="eec25-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="eec25-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eec25-126">-ResourceId</span></span>
<span data-ttu-id="eec25-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="eec25-127">The resource id.</span></span>

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

### <span data-ttu-id="eec25-128">-Filtro</span><span class="sxs-lookup"><span data-stu-id="eec25-128">-Filter</span></span>
<span data-ttu-id="eec25-129">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="eec25-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="eec25-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="eec25-130">-Skip</span></span>
<span data-ttu-id="eec25-131">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eec25-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="eec25-132">-Início</span><span class="sxs-lookup"><span data-stu-id="eec25-132">-Top</span></span>
<span data-ttu-id="eec25-133">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eec25-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eec25-134">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="eec25-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="eec25-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec25-135">CommonParameters</span></span>
<span data-ttu-id="eec25-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec25-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec25-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec25-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec25-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eec25-138">INPUTS</span></span>

## <span data-ttu-id="eec25-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eec25-139">OUTPUTS</span></span>

### <span data-ttu-id="eec25-140">Microsoft. AzureStack. Management. Fabric. admin. Models. volume</span><span class="sxs-lookup"><span data-stu-id="eec25-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="eec25-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eec25-141">NOTES</span></span>

## <span data-ttu-id="eec25-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eec25-142">RELATED LINKS</span></span>