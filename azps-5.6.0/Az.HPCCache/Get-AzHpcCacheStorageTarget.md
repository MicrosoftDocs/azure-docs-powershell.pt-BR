---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 6fb1e00f74bcd170d8117e4e37655da6c275a62f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889983"
---
# <span data-ttu-id="a785d-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a785d-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="a785d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a785d-102">SYNOPSIS</span></span>
<span data-ttu-id="a785d-103">Obter destinos de armazenamento de cache HPC.</span><span class="sxs-lookup"><span data-stu-id="a785d-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="a785d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a785d-104">SYNTAX</span></span>

### <span data-ttu-id="a785d-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a785d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a785d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a785d-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a785d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a785d-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a785d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a785d-108">DESCRIPTION</span></span>
<span data-ttu-id="a785d-109">O cmdlet **Get-AzHpcCacheStorageTarget** obtém destinos de armazenamento existentes no cache.</span><span class="sxs-lookup"><span data-stu-id="a785d-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="a785d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a785d-110">EXAMPLES</span></span>

### <span data-ttu-id="a785d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a785d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="a785d-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a785d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="a785d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a785d-113">PARAMETERS</span></span>

### <span data-ttu-id="a785d-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a785d-114">-CacheId</span></span>
<span data-ttu-id="a785d-115">A id de recurso do Cache</span><span class="sxs-lookup"><span data-stu-id="a785d-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a785d-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="a785d-116">-CacheName</span></span>
<span data-ttu-id="a785d-117">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="a785d-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a785d-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="a785d-118">-CacheObject</span></span>
<span data-ttu-id="a785d-119">O objeto cache a ser inicial.</span><span class="sxs-lookup"><span data-stu-id="a785d-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a785d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a785d-120">-DefaultProfile</span></span>
<span data-ttu-id="a785d-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a785d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a785d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a785d-122">-Name</span></span>
<span data-ttu-id="a785d-123">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a785d-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a785d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a785d-124">-ResourceGroupName</span></span>
<span data-ttu-id="a785d-125">O nome do cache do grupo de recursos está.</span><span class="sxs-lookup"><span data-stu-id="a785d-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a785d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a785d-126">CommonParameters</span></span>
<span data-ttu-id="a785d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a785d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a785d-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a785d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a785d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a785d-129">INPUTS</span></span>

### <span data-ttu-id="a785d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a785d-130">System.String</span></span>

## <span data-ttu-id="a785d-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a785d-131">OUTPUTS</span></span>

### <span data-ttu-id="a785d-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a785d-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="a785d-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="a785d-133">NOTES</span></span>

## <span data-ttu-id="a785d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a785d-134">RELATED LINKS</span></span>
