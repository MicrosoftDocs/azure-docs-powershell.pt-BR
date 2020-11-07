---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774107"
---
# <span data-ttu-id="2a0af-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="2a0af-101">Get-AzsVolume</span></span>

## <span data-ttu-id="2a0af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a0af-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0af-103">Retorna uma lista de todos os volumes de armazenamento em um local.</span><span class="sxs-lookup"><span data-stu-id="2a0af-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="2a0af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a0af-104">SYNTAX</span></span>

### <span data-ttu-id="2a0af-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a0af-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2a0af-106">Obter</span><span class="sxs-lookup"><span data-stu-id="2a0af-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2a0af-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="2a0af-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2a0af-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a0af-108">DESCRIPTION</span></span>
<span data-ttu-id="2a0af-109">Retorna uma lista de todos os volumes de armazenamento em um local.</span><span class="sxs-lookup"><span data-stu-id="2a0af-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="2a0af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a0af-110">EXAMPLES</span></span>

### <span data-ttu-id="2a0af-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2a0af-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="2a0af-112">Obter uma lista de todos os volumes de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="2a0af-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="2a0af-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2a0af-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="2a0af-114">Obter um volume de armazenamento por nome em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="2a0af-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="2a0af-115">OS</span><span class="sxs-lookup"><span data-stu-id="2a0af-115">PARAMETERS</span></span>

### <span data-ttu-id="2a0af-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2a0af-116">-Filter</span></span>
<span data-ttu-id="2a0af-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="2a0af-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="2a0af-118">-Local</span><span class="sxs-lookup"><span data-stu-id="2a0af-118">-Location</span></span>
<span data-ttu-id="2a0af-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a0af-119">Location of the resource.</span></span>

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

### <span data-ttu-id="2a0af-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a0af-120">-Name</span></span>
<span data-ttu-id="2a0af-121">Nome do volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2a0af-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="2a0af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a0af-122">-ResourceGroupName</span></span>
<span data-ttu-id="2a0af-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="2a0af-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2a0af-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a0af-124">-ResourceId</span></span>
<span data-ttu-id="2a0af-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a0af-125">The resource id.</span></span>

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

### <span data-ttu-id="2a0af-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="2a0af-126">-ScaleUnit</span></span>
<span data-ttu-id="2a0af-127">Nome da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="2a0af-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="2a0af-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="2a0af-128">-StorageSubSystem</span></span>
<span data-ttu-id="2a0af-129">Subsistema de armazenamento no qual o volume está localizado.</span><span class="sxs-lookup"><span data-stu-id="2a0af-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="2a0af-130">-Início</span><span class="sxs-lookup"><span data-stu-id="2a0af-130">-Top</span></span>
<span data-ttu-id="2a0af-131">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2a0af-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2a0af-132">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="2a0af-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2a0af-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="2a0af-133">-Skip</span></span>
<span data-ttu-id="2a0af-134">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2a0af-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2a0af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0af-135">CommonParameters</span></span>
<span data-ttu-id="2a0af-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0af-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a0af-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0af-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a0af-138">INPUTS</span></span>

## <span data-ttu-id="2a0af-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a0af-139">OUTPUTS</span></span>

### <span data-ttu-id="2a0af-140">Microsoft. AzureStack. Management. Fabric. admin. Models. volume</span><span class="sxs-lookup"><span data-stu-id="2a0af-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="2a0af-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a0af-141">NOTES</span></span>

## <span data-ttu-id="2a0af-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a0af-142">RELATED LINKS</span></span>
