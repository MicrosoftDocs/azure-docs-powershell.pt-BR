---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429281"
---
# <span data-ttu-id="d22bc-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="d22bc-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="d22bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d22bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d22bc-103">Obter destino (s) de armazenamento em cache de HPC.</span><span class="sxs-lookup"><span data-stu-id="d22bc-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="d22bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d22bc-104">SYNTAX</span></span>

### <span data-ttu-id="d22bc-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d22bc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d22bc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22bc-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d22bc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d22bc-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d22bc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d22bc-108">DESCRIPTION</span></span>
<span data-ttu-id="d22bc-109">O cmdlet **Get-AzHpcCacheStorageTarget** tem destino (s) de armazenamento que existem no cache.</span><span class="sxs-lookup"><span data-stu-id="d22bc-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="d22bc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d22bc-110">EXAMPLES</span></span>

### <span data-ttu-id="d22bc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d22bc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="d22bc-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d22bc-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="d22bc-113">OS</span><span class="sxs-lookup"><span data-stu-id="d22bc-113">PARAMETERS</span></span>

### <span data-ttu-id="d22bc-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="d22bc-114">-CacheId</span></span>
<span data-ttu-id="d22bc-115">A ID do recurso do cache</span><span class="sxs-lookup"><span data-stu-id="d22bc-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="d22bc-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="d22bc-116">-CacheName</span></span>
<span data-ttu-id="d22bc-117">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="d22bc-117">Name of cache.</span></span>

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

### <span data-ttu-id="d22bc-118">-Cacheobject</span><span class="sxs-lookup"><span data-stu-id="d22bc-118">-CacheObject</span></span>
<span data-ttu-id="d22bc-119">O objeto de cache para iniciar.</span><span class="sxs-lookup"><span data-stu-id="d22bc-119">The cache object to start.</span></span>

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

### <span data-ttu-id="d22bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22bc-120">-DefaultProfile</span></span>
<span data-ttu-id="d22bc-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d22bc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22bc-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d22bc-122">-Name</span></span>
<span data-ttu-id="d22bc-123">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d22bc-123">Name of storage target.</span></span>

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

### <span data-ttu-id="d22bc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22bc-124">-ResourceGroupName</span></span>
<span data-ttu-id="d22bc-125">O nome do cache do grupo de recursos está em.</span><span class="sxs-lookup"><span data-stu-id="d22bc-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="d22bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22bc-126">CommonParameters</span></span>
<span data-ttu-id="d22bc-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22bc-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d22bc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22bc-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d22bc-129">INPUTS</span></span>

### <span data-ttu-id="d22bc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d22bc-130">System.String</span></span>

## <span data-ttu-id="d22bc-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d22bc-131">OUTPUTS</span></span>

### <span data-ttu-id="d22bc-132">Microsoft. Azure. PowerShell. cmdlets. HPCCache. Models. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="d22bc-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="d22bc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d22bc-133">NOTES</span></span>

## <span data-ttu-id="d22bc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d22bc-134">RELATED LINKS</span></span>
