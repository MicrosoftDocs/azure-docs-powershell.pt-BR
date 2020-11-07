---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775008"
---
# <span data-ttu-id="0e7f6-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0e7f6-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="0e7f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7f6-103">Retorna a lista de trabalhos de migração de disco gerenciados.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="0e7f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e7f6-104">SYNTAX</span></span>

### <span data-ttu-id="0e7f6-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="0e7f6-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="0e7f6-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="0e7f6-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="0e7f6-107">Obter</span><span class="sxs-lookup"><span data-stu-id="0e7f6-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="0e7f6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e7f6-108">DESCRIPTION</span></span>
<span data-ttu-id="0e7f6-109">Retorna uma lista de trabalhos de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="0e7f6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e7f6-110">EXAMPLES</span></span>

### <span data-ttu-id="0e7f6-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0e7f6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="0e7f6-112">Obtenha um trabalho específico de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="0e7f6-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0e7f6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="0e7f6-114">Retorna uma lista de trabalhos de migração de disco gerenciados no local local.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="0e7f6-115">OS</span><span class="sxs-lookup"><span data-stu-id="0e7f6-115">PARAMETERS</span></span>

### <span data-ttu-id="0e7f6-116">-Local</span><span class="sxs-lookup"><span data-stu-id="0e7f6-116">-Location</span></span>
<span data-ttu-id="0e7f6-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-117">Location of the resource.</span></span>

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

### <span data-ttu-id="0e7f6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e7f6-118">-Name</span></span>
<span data-ttu-id="0e7f6-119">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="0e7f6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e7f6-120">-ResourceId</span></span>
<span data-ttu-id="0e7f6-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-121">The resource id.</span></span>

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

### <span data-ttu-id="0e7f6-122">-Status</span><span class="sxs-lookup"><span data-stu-id="0e7f6-122">-Status</span></span>
<span data-ttu-id="0e7f6-123">Os parâmetros do status do trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="0e7f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7f6-124">CommonParameters</span></span>
<span data-ttu-id="0e7f6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e7f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7f6-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e7f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7f6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e7f6-127">INPUTS</span></span>

## <span data-ttu-id="0e7f6-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e7f6-128">OUTPUTS</span></span>

### <span data-ttu-id="0e7f6-129">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0e7f6-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="0e7f6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e7f6-130">NOTES</span></span>

## <span data-ttu-id="0e7f6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e7f6-131">RELATED LINKS</span></span>

