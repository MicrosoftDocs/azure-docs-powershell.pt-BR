---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93774952"
---
# <span data-ttu-id="bce2d-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="bce2d-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="bce2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bce2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bce2d-103">Retorna uma lista de todos os subsistemas de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="bce2d-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="bce2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bce2d-104">SYNTAX</span></span>

### <span data-ttu-id="bce2d-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="bce2d-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bce2d-106">Obter</span><span class="sxs-lookup"><span data-stu-id="bce2d-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bce2d-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="bce2d-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bce2d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bce2d-108">DESCRIPTION</span></span>
<span data-ttu-id="bce2d-109">Retorna uma lista de todos os subsistemas de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="bce2d-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="bce2d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bce2d-110">EXAMPLES</span></span>

### <span data-ttu-id="bce2d-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="bce2d-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="bce2d-112">Obter todos os subsistemas de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="bce2d-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="bce2d-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="bce2d-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="bce2d-114">Obtenha um subsistema de armazenamento de acordo com um local e um nome.</span><span class="sxs-lookup"><span data-stu-id="bce2d-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="bce2d-115">OS</span><span class="sxs-lookup"><span data-stu-id="bce2d-115">PARAMETERS</span></span>

### <span data-ttu-id="bce2d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="bce2d-116">-Name</span></span>
<span data-ttu-id="bce2d-117">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="bce2d-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bce2d-118">-Local</span><span class="sxs-lookup"><span data-stu-id="bce2d-118">-Location</span></span>
<span data-ttu-id="bce2d-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="bce2d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="bce2d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce2d-120">-ResourceGroupName</span></span>
<span data-ttu-id="bce2d-121">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="bce2d-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bce2d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bce2d-122">-ResourceId</span></span>
<span data-ttu-id="bce2d-123">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bce2d-123">The resource id.</span></span>

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

### <span data-ttu-id="bce2d-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bce2d-124">-Filter</span></span>
<span data-ttu-id="bce2d-125">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="bce2d-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="bce2d-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="bce2d-126">-Skip</span></span>
<span data-ttu-id="bce2d-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bce2d-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bce2d-128">-Início</span><span class="sxs-lookup"><span data-stu-id="bce2d-128">-Top</span></span>
<span data-ttu-id="bce2d-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bce2d-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bce2d-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="bce2d-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bce2d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce2d-131">CommonParameters</span></span>
<span data-ttu-id="bce2d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce2d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce2d-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce2d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce2d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bce2d-134">INPUTS</span></span>

## <span data-ttu-id="bce2d-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bce2d-135">OUTPUTS</span></span>

### <span data-ttu-id="bce2d-136">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="bce2d-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="bce2d-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bce2d-137">NOTES</span></span>

## <span data-ttu-id="bce2d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bce2d-138">RELATED LINKS</span></span>
