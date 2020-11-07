---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2abc9073b9e7bcbcd4644150ada4c19cd351f660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774108"
---
# <span data-ttu-id="12e1a-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="12e1a-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="12e1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="12e1a-103">Retorna uma lista de todos os subsistemas de armazenamento para uma unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="12e1a-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="12e1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e1a-104">SYNTAX</span></span>

### <span data-ttu-id="12e1a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="12e1a-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="12e1a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="12e1a-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="12e1a-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="12e1a-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="12e1a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12e1a-108">DESCRIPTION</span></span>
<span data-ttu-id="12e1a-109">Retorna uma lista de todos os subsistemas de armazenamento para uma unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="12e1a-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="12e1a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12e1a-110">EXAMPLES</span></span>

### <span data-ttu-id="12e1a-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="12e1a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="12e1a-112">Obter todos os subsistemas de armazenamento a partir de uma unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="12e1a-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="12e1a-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="12e1a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="12e1a-114">Obtenha um subsistema de armazenamento de acordo com uma unidade de escala e um nome.</span><span class="sxs-lookup"><span data-stu-id="12e1a-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="12e1a-115">OS</span><span class="sxs-lookup"><span data-stu-id="12e1a-115">PARAMETERS</span></span>

### <span data-ttu-id="12e1a-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="12e1a-116">-Filter</span></span>
<span data-ttu-id="12e1a-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="12e1a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="12e1a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="12e1a-118">-Location</span></span>
<span data-ttu-id="12e1a-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="12e1a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="12e1a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="12e1a-120">-Name</span></span>
<span data-ttu-id="12e1a-121">Nome do subsistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12e1a-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="12e1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="12e1a-123">Grupo de recursos no qual o provedor de recursos foi registrado.</span><span class="sxs-lookup"><span data-stu-id="12e1a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="12e1a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e1a-124">-ResourceId</span></span>
<span data-ttu-id="12e1a-125">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="12e1a-125">The resource id.</span></span>

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

### <span data-ttu-id="12e1a-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="12e1a-126">-ScaleUnit</span></span>
<span data-ttu-id="12e1a-127">Nome da unidade de escala.</span><span class="sxs-lookup"><span data-stu-id="12e1a-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="12e1a-128">-Início</span><span class="sxs-lookup"><span data-stu-id="12e1a-128">-Top</span></span>
<span data-ttu-id="12e1a-129">Retorne os N principais itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="12e1a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="12e1a-130">Aplica-se após o parâmetro-Skip.</span><span class="sxs-lookup"><span data-stu-id="12e1a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="12e1a-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="12e1a-131">-Skip</span></span>
<span data-ttu-id="12e1a-132">Ignorar os primeiros N itens conforme especificado pelo valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="12e1a-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="12e1a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e1a-133">CommonParameters</span></span>
<span data-ttu-id="12e1a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e1a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e1a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e1a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e1a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12e1a-136">INPUTS</span></span>

## <span data-ttu-id="12e1a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12e1a-137">OUTPUTS</span></span>

### <span data-ttu-id="12e1a-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="12e1a-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="12e1a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12e1a-139">NOTES</span></span>

## <span data-ttu-id="12e1a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12e1a-140">RELATED LINKS</span></span>
