---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425618"
---
# <span data-ttu-id="0a99a-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="0a99a-101">Get-AzsDrive</span></span>

## <span data-ttu-id="0a99a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a99a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a99a-103">Retorna uma lista de todas as unidades de armazenamento de um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="0a99a-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="0a99a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a99a-104">SYNTAX</span></span>

### <span data-ttu-id="0a99a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a99a-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0a99a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="0a99a-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0a99a-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="0a99a-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0a99a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a99a-108">DESCRIPTION</span></span>
<span data-ttu-id="0a99a-109">Retorna uma lista de todas as unidades de armazenamento de um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="0a99a-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="0a99a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a99a-110">EXAMPLES</span></span>

### <span data-ttu-id="0a99a-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a99a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="0a99a-112">Obter uma lista de todos os drives de armazenamento de um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="0a99a-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="0a99a-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a99a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="0a99a-114">Obter uma unidade de armazenamento por nome para um determinado cluster.</span><span class="sxs-lookup"><span data-stu-id="0a99a-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="0a99a-115">OS</span><span class="sxs-lookup"><span data-stu-id="0a99a-115">PARAMETERS</span></span>

### <span data-ttu-id="0a99a-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="0a99a-116">-Filter</span></span>
<span data-ttu-id="0a99a-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="0a99a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="0a99a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="0a99a-118">-Location</span></span>
<span data-ttu-id="0a99a-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="0a99a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0a99a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a99a-120">-Name</span></span>
<span data-ttu-id="0a99a-121">Nome do drive de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0a99a-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="0a99a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a99a-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a99a-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="0a99a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0a99a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a99a-124">-ResourceId</span></span>
<span data-ttu-id="0a99a-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0a99a-125">The resource id.</span></span>

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

### <span data-ttu-id="0a99a-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="0a99a-126">-ScaleUnit</span></span>
<span data-ttu-id="0a99a-127">Nome da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="0a99a-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="0a99a-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="0a99a-128">-StorageSubSystem</span></span>
<span data-ttu-id="0a99a-129">Subsistema de armazenamento no qual a unidade está localizada.</span><span class="sxs-lookup"><span data-stu-id="0a99a-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="0a99a-130">-Início</span><span class="sxs-lookup"><span data-stu-id="0a99a-130">-Top</span></span>
<span data-ttu-id="0a99a-131">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0a99a-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0a99a-132">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="0a99a-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0a99a-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="0a99a-133">-Skip</span></span>
<span data-ttu-id="0a99a-134">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0a99a-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0a99a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a99a-135">CommonParameters</span></span>
<span data-ttu-id="0a99a-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a99a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a99a-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a99a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a99a-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a99a-138">INPUTS</span></span>

## <span data-ttu-id="0a99a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a99a-139">OUTPUTS</span></span>

### <span data-ttu-id="0a99a-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Drive</span><span class="sxs-lookup"><span data-stu-id="0a99a-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="0a99a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a99a-141">NOTES</span></span>

## <span data-ttu-id="0a99a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a99a-142">RELATED LINKS</span></span>