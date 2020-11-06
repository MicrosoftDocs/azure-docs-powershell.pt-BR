---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426050"
---
# <span data-ttu-id="37072-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="37072-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="37072-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37072-102">SYNOPSIS</span></span>
<span data-ttu-id="37072-103">Retorna uma lista de todos os pools de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="37072-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="37072-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37072-104">SYNTAX</span></span>

### <span data-ttu-id="37072-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="37072-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="37072-106">Obter</span><span class="sxs-lookup"><span data-stu-id="37072-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="37072-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="37072-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="37072-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37072-108">DESCRIPTION</span></span>
<span data-ttu-id="37072-109">Retorna uma lista de todos os pools de armazenamento de um local.</span><span class="sxs-lookup"><span data-stu-id="37072-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="37072-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37072-110">EXAMPLES</span></span>

### <span data-ttu-id="37072-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="37072-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="37072-112">Obter todos os pools de armazenamento em um determinado local.</span><span class="sxs-lookup"><span data-stu-id="37072-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="37072-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="37072-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="37072-114">Obtenha um pool de armazenamento em um determinado local, dado um nome de pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37072-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="37072-115">OS</span><span class="sxs-lookup"><span data-stu-id="37072-115">PARAMETERS</span></span>

### <span data-ttu-id="37072-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="37072-116">-Filter</span></span>
<span data-ttu-id="37072-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="37072-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="37072-118">-Local</span><span class="sxs-lookup"><span data-stu-id="37072-118">-Location</span></span>
<span data-ttu-id="37072-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="37072-119">Location of the resource.</span></span>

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

### <span data-ttu-id="37072-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="37072-120">-Name</span></span>
<span data-ttu-id="37072-121">Nome do pool de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37072-121">Storage pool name.</span></span>

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

### <span data-ttu-id="37072-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37072-122">-ResourceGroupName</span></span>
<span data-ttu-id="37072-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="37072-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="37072-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37072-124">-ResourceId</span></span>
<span data-ttu-id="37072-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="37072-125">The resource id.</span></span>

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

### <span data-ttu-id="37072-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="37072-126">-Skip</span></span>
<span data-ttu-id="37072-127">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="37072-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="37072-128">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="37072-128">-StorageSystem</span></span>
<span data-ttu-id="37072-129">Sistema de armazenamento no qual o pool de armazenamento está localizado.</span><span class="sxs-lookup"><span data-stu-id="37072-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="37072-130">-Início</span><span class="sxs-lookup"><span data-stu-id="37072-130">-Top</span></span>
<span data-ttu-id="37072-131">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="37072-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="37072-132">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="37072-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="37072-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37072-133">CommonParameters</span></span>
<span data-ttu-id="37072-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37072-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37072-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37072-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37072-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37072-136">INPUTS</span></span>

## <span data-ttu-id="37072-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37072-137">OUTPUTS</span></span>

### <span data-ttu-id="37072-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="37072-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="37072-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37072-139">NOTES</span></span>

## <span data-ttu-id="37072-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37072-140">RELATED LINKS</span></span>

