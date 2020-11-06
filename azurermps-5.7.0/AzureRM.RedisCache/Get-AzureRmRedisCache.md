---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 1e91aa946e89b8231ea2c58b28c686d603855ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429718"
---
# <span data-ttu-id="91a7b-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a7b-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="91a7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="91a7b-103">Obtém um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="91a7b-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91a7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91a7b-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91a7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91a7b-105">DESCRIPTION</span></span>
<span data-ttu-id="91a7b-106">O cmdlet **Get-AzureRmRedisCache** Obtém o cache do Azure Redis especificado.</span><span class="sxs-lookup"><span data-stu-id="91a7b-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="91a7b-107">Se você especificar nenhum parâmetro, essa operação obterá cada cache Redis para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="91a7b-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="91a7b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91a7b-108">EXAMPLES</span></span>

### <span data-ttu-id="91a7b-109">Exemplo 1: obter um cache Redis por nome</span><span class="sxs-lookup"><span data-stu-id="91a7b-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="91a7b-110">Este comando obtém o cache Redis chamado myexists.</span><span class="sxs-lookup"><span data-stu-id="91a7b-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="91a7b-111">Exemplo 2: obter todos os Redis cache em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="91a7b-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="91a7b-112">Esse comando obtém todos os Redis cache do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="91a7b-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="91a7b-113">Exemplo 3: obter todos os Redis cache na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="91a7b-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="91a7b-114">Esse comando obtém todos os Redis cache na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="91a7b-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="91a7b-115">OS</span><span class="sxs-lookup"><span data-stu-id="91a7b-115">PARAMETERS</span></span>

### <span data-ttu-id="91a7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a7b-116">-DefaultProfile</span></span>
<span data-ttu-id="91a7b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91a7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91a7b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="91a7b-118">-Name</span></span>
<span data-ttu-id="91a7b-119">Especifica o nome do cache de Redis a obter.</span><span class="sxs-lookup"><span data-stu-id="91a7b-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="91a7b-120">Use com o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="91a7b-120">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91a7b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a7b-121">-ResourceGroupName</span></span>
<span data-ttu-id="91a7b-122">Especifica o nome do grupo de recursos que contém o cache de Redis a obter.</span><span class="sxs-lookup"><span data-stu-id="91a7b-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="91a7b-123">Se você especificar somente o parâmetro *ResourceGroupName* , essa operação obterá cada cache Redis no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="91a7b-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91a7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a7b-124">CommonParameters</span></span>
<span data-ttu-id="91a7b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a7b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91a7b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a7b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91a7b-127">INPUTS</span></span>

### <span data-ttu-id="91a7b-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="91a7b-128">None</span></span>
<span data-ttu-id="91a7b-129">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="91a7b-129">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="91a7b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91a7b-130">OUTPUTS</span></span>

### <span data-ttu-id="91a7b-131">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="91a7b-131">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="91a7b-132">Retorna uma matriz de objetos **RedisCacheAttributes** .</span><span class="sxs-lookup"><span data-stu-id="91a7b-132">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="91a7b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91a7b-133">NOTES</span></span>

## <span data-ttu-id="91a7b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91a7b-134">RELATED LINKS</span></span>

[<span data-ttu-id="91a7b-135">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a7b-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="91a7b-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a7b-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="91a7b-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="91a7b-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


