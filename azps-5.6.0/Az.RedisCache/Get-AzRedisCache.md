---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 8423c098542a621ec66a5de3255ccf62c3e8ec94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885259"
---
# <span data-ttu-id="c4663-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c4663-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="c4663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4663-102">SYNOPSIS</span></span>
<span data-ttu-id="c4663-103">Obtém um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="c4663-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="c4663-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c4663-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4663-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c4663-105">DESCRIPTION</span></span>
<span data-ttu-id="c4663-106">O cmdlet **Get-AzRedisCache** obtém o Cache redis do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="c4663-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="c4663-107">Se você especificar nenhum parâmetro, essa operação obtém cada Cache Redis para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c4663-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="c4663-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4663-108">EXAMPLES</span></span>

### <span data-ttu-id="c4663-109">Exemplo 1: Obter um Cache Redis pelo nome</span><span class="sxs-lookup"><span data-stu-id="c4663-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

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

<span data-ttu-id="c4663-110">Este comando obtém o Cache Redis chamado myexists.</span><span class="sxs-lookup"><span data-stu-id="c4663-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="c4663-111">Exemplo 2: Obter todos os Redis Cache em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c4663-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="c4663-112">Esse comando obtém cada Cache Redis no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c4663-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="c4663-113">Exemplo 3: Obter todos os Redis Cache na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="c4663-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

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

<span data-ttu-id="c4663-114">Este comando obtém cada Cache Redis na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c4663-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="c4663-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c4663-115">PARAMETERS</span></span>

### <span data-ttu-id="c4663-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4663-116">-DefaultProfile</span></span>
<span data-ttu-id="c4663-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c4663-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4663-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c4663-118">-Name</span></span>
<span data-ttu-id="c4663-119">Especifica o nome do Cache Redis a ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="c4663-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="c4663-120">Use com o *parâmetro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="c4663-120">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4663-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4663-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4663-122">Especifica o nome do grupo de recursos que contém o Cache Redis a ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="c4663-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="c4663-123">Se você especificar apenas o *parâmetro ResourceGroupName,* essa operação obtém cada Cache Redis no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c4663-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4663-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4663-124">CommonParameters</span></span>
<span data-ttu-id="c4663-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4663-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4663-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4663-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4663-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4663-127">INPUTS</span></span>

### <span data-ttu-id="c4663-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c4663-128">System.String</span></span>

## <span data-ttu-id="c4663-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c4663-129">OUTPUTS</span></span>

### <span data-ttu-id="c4663-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="c4663-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="c4663-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="c4663-131">NOTES</span></span>

## <span data-ttu-id="c4663-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4663-132">RELATED LINKS</span></span>

[<span data-ttu-id="c4663-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c4663-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c4663-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c4663-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="c4663-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c4663-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


