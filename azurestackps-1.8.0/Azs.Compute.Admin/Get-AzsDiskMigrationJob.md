---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93774673"
---
# <span data-ttu-id="9123b-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9123b-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="9123b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9123b-102">SYNOPSIS</span></span>
<span data-ttu-id="9123b-103">Retorna a lista de trabalhos de migração de disco gerenciados.</span><span class="sxs-lookup"><span data-stu-id="9123b-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="9123b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9123b-104">SYNTAX</span></span>

### <span data-ttu-id="9123b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="9123b-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="9123b-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="9123b-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="9123b-107">Obter</span><span class="sxs-lookup"><span data-stu-id="9123b-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="9123b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9123b-108">DESCRIPTION</span></span>
<span data-ttu-id="9123b-109">Retorna uma lista de trabalhos de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="9123b-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="9123b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9123b-110">EXAMPLES</span></span>

### <span data-ttu-id="9123b-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9123b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="9123b-112">Obtenha um trabalho específico de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9123b-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="9123b-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9123b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="9123b-114">Retorna uma lista de trabalhos de migração de disco gerenciados no local local.</span><span class="sxs-lookup"><span data-stu-id="9123b-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="9123b-115">OS</span><span class="sxs-lookup"><span data-stu-id="9123b-115">PARAMETERS</span></span>

### <span data-ttu-id="9123b-116">-Local</span><span class="sxs-lookup"><span data-stu-id="9123b-116">-Location</span></span>
<span data-ttu-id="9123b-117">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9123b-117">Location of the resource.</span></span>

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

### <span data-ttu-id="9123b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9123b-118">-Name</span></span>
<span data-ttu-id="9123b-119">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="9123b-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="9123b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9123b-120">-ResourceId</span></span>
<span data-ttu-id="9123b-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9123b-121">The resource id.</span></span>

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

### <span data-ttu-id="9123b-122">-Status</span><span class="sxs-lookup"><span data-stu-id="9123b-122">-Status</span></span>
<span data-ttu-id="9123b-123">Os parâmetros do status do trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="9123b-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="9123b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9123b-124">CommonParameters</span></span>
<span data-ttu-id="9123b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9123b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9123b-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9123b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9123b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9123b-127">INPUTS</span></span>

## <span data-ttu-id="9123b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9123b-128">OUTPUTS</span></span>

### <span data-ttu-id="9123b-129">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="9123b-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="9123b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9123b-130">NOTES</span></span>

## <span data-ttu-id="9123b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9123b-131">RELATED LINKS</span></span>

