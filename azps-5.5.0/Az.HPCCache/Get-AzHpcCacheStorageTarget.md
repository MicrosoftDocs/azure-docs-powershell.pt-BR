---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118989"
---
# <span data-ttu-id="10a58-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="10a58-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="10a58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10a58-102">SYNOPSIS</span></span>
<span data-ttu-id="10a58-103">Obter destinos de armazenamento em cache HPC.</span><span class="sxs-lookup"><span data-stu-id="10a58-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="10a58-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10a58-104">SYNTAX</span></span>

### <span data-ttu-id="10a58-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10a58-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10a58-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a58-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10a58-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a58-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10a58-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="10a58-108">DESCRIPTION</span></span>
<span data-ttu-id="10a58-109">O cmdlet **Get-AzHpcCacheStorageTarget** obtém os destinos de armazenamento existentes no cache.</span><span class="sxs-lookup"><span data-stu-id="10a58-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="10a58-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10a58-110">EXAMPLES</span></span>

### <span data-ttu-id="10a58-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10a58-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="10a58-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="10a58-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="10a58-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10a58-113">PARAMETERS</span></span>

### <span data-ttu-id="10a58-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="10a58-114">-CacheId</span></span>
<span data-ttu-id="10a58-115">A ID do recurso do Cache</span><span class="sxs-lookup"><span data-stu-id="10a58-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="10a58-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="10a58-116">-CacheName</span></span>
<span data-ttu-id="10a58-117">Nome do cache.</span><span class="sxs-lookup"><span data-stu-id="10a58-117">Name of cache.</span></span>

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

### <span data-ttu-id="10a58-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="10a58-118">-CacheObject</span></span>
<span data-ttu-id="10a58-119">O objeto de cache para iniciar.</span><span class="sxs-lookup"><span data-stu-id="10a58-119">The cache object to start.</span></span>

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

### <span data-ttu-id="10a58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a58-120">-DefaultProfile</span></span>
<span data-ttu-id="10a58-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10a58-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10a58-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="10a58-122">-Name</span></span>
<span data-ttu-id="10a58-123">Nome do destino de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10a58-123">Name of storage target.</span></span>

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

### <span data-ttu-id="10a58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a58-124">-ResourceGroupName</span></span>
<span data-ttu-id="10a58-125">O nome do cache do grupo de recursos está.</span><span class="sxs-lookup"><span data-stu-id="10a58-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="10a58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a58-126">CommonParameters</span></span>
<span data-ttu-id="10a58-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a58-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10a58-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a58-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="10a58-129">INPUTS</span></span>

### <span data-ttu-id="10a58-130">System.String</span><span class="sxs-lookup"><span data-stu-id="10a58-130">System.String</span></span>

## <span data-ttu-id="10a58-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="10a58-131">OUTPUTS</span></span>

### <span data-ttu-id="10a58-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="10a58-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="10a58-133">Notas</span><span class="sxs-lookup"><span data-stu-id="10a58-133">NOTES</span></span>

## <span data-ttu-id="10a58-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10a58-134">RELATED LINKS</span></span>
