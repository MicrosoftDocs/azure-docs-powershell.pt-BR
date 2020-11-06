---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425993"
---
# <span data-ttu-id="55415-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="55415-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="55415-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55415-102">SYNOPSIS</span></span>
<span data-ttu-id="55415-103">Retorna uma lista de todos os volumes de armazenamento em um local.</span><span class="sxs-lookup"><span data-stu-id="55415-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="55415-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55415-104">SYNTAX</span></span>

### <span data-ttu-id="55415-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="55415-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="55415-106">Obter</span><span class="sxs-lookup"><span data-stu-id="55415-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="55415-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="55415-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="55415-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55415-108">DESCRIPTION</span></span>
<span data-ttu-id="55415-109">Retorna uma lista de todos os volumes de armazenamento em um local.</span><span class="sxs-lookup"><span data-stu-id="55415-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="55415-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55415-110">EXAMPLES</span></span>

### <span data-ttu-id="55415-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="55415-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="55415-112">Obter uma lista de todos os volumes de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="55415-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="55415-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="55415-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="55415-114">Obter um volume de armazenamento por nome em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="55415-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="55415-115">OS</span><span class="sxs-lookup"><span data-stu-id="55415-115">PARAMETERS</span></span>

### <span data-ttu-id="55415-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="55415-116">-Filter</span></span>
<span data-ttu-id="55415-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="55415-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="55415-118">-Local</span><span class="sxs-lookup"><span data-stu-id="55415-118">-Location</span></span>
<span data-ttu-id="55415-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="55415-119">Location of the resource.</span></span>

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

### <span data-ttu-id="55415-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="55415-120">-Name</span></span>
<span data-ttu-id="55415-121">Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="55415-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="55415-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55415-122">-ResourceGroupName</span></span>
<span data-ttu-id="55415-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="55415-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="55415-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55415-124">-ResourceId</span></span>
<span data-ttu-id="55415-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="55415-125">The resource id.</span></span>

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

### <span data-ttu-id="55415-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="55415-126">-Skip</span></span>
<span data-ttu-id="55415-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="55415-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="55415-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="55415-128">-StoragePool</span></span>
<span data-ttu-id="55415-129">Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="55415-129">Storage pool name.</span></span>

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

### <span data-ttu-id="55415-130">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="55415-130">-StorageSystem</span></span>
<span data-ttu-id="55415-131">Sistema de armazenamento no qual o volume de infraestrutura está localizado.</span><span class="sxs-lookup"><span data-stu-id="55415-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="55415-132">-Início</span><span class="sxs-lookup"><span data-stu-id="55415-132">-Top</span></span>
<span data-ttu-id="55415-133">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="55415-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="55415-134">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="55415-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="55415-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55415-135">CommonParameters</span></span>
<span data-ttu-id="55415-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55415-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55415-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55415-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55415-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55415-138">INPUTS</span></span>

## <span data-ttu-id="55415-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55415-139">OUTPUTS</span></span>

### <span data-ttu-id="55415-140">Microsoft. AzureStack. Management. Fabric. admin. Models. volume</span><span class="sxs-lookup"><span data-stu-id="55415-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="55415-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55415-141">NOTES</span></span>

## <span data-ttu-id="55415-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55415-142">RELATED LINKS</span></span>

