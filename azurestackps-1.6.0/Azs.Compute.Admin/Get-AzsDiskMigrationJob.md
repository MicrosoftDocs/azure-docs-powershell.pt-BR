---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425639"
---
# <span data-ttu-id="24a0d-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="24a0d-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="24a0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="24a0d-103">Retorna a lista de trabalhos de migração de disco gerenciados.</span><span class="sxs-lookup"><span data-stu-id="24a0d-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="24a0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24a0d-104">SYNTAX</span></span>

### <span data-ttu-id="24a0d-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="24a0d-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="24a0d-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="24a0d-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="24a0d-107">Obter</span><span class="sxs-lookup"><span data-stu-id="24a0d-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="24a0d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24a0d-108">DESCRIPTION</span></span>
<span data-ttu-id="24a0d-109">Retorna uma lista de trabalhos de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="24a0d-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="24a0d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24a0d-110">EXAMPLES</span></span>

### <span data-ttu-id="24a0d-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24a0d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="24a0d-112">Obtenha um trabalho específico de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="24a0d-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="24a0d-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="24a0d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="24a0d-114">Retorna uma lista de trabalhos de migração de disco gerenciados no local local.</span><span class="sxs-lookup"><span data-stu-id="24a0d-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="24a0d-115">OS</span><span class="sxs-lookup"><span data-stu-id="24a0d-115">PARAMETERS</span></span>

### <span data-ttu-id="24a0d-116">-Local</span><span class="sxs-lookup"><span data-stu-id="24a0d-116">-Location</span></span>
<span data-ttu-id="24a0d-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="24a0d-117">Location of the resource.</span></span>

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

### <span data-ttu-id="24a0d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="24a0d-118">-Name</span></span>
<span data-ttu-id="24a0d-119">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="24a0d-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a0d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a0d-120">-ResourceId</span></span>
<span data-ttu-id="24a0d-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="24a0d-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0d-122">-Status</span><span class="sxs-lookup"><span data-stu-id="24a0d-122">-Status</span></span>
<span data-ttu-id="24a0d-123">Os parâmetros do status do trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="24a0d-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="24a0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a0d-124">CommonParameters</span></span>
<span data-ttu-id="24a0d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a0d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a0d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a0d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24a0d-127">INPUTS</span></span>

## <span data-ttu-id="24a0d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24a0d-128">OUTPUTS</span></span>

### <span data-ttu-id="24a0d-129">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="24a0d-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="24a0d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24a0d-130">NOTES</span></span>

## <span data-ttu-id="24a0d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24a0d-131">RELATED LINKS</span></span>
