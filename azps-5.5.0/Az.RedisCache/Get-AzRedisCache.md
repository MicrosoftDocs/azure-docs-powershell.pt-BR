---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: cc8d6ff7e7fb55c5ee71c82a8eca4cc661b98b07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118178"
---
# <span data-ttu-id="4009a-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4009a-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="4009a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4009a-102">SYNOPSIS</span></span>
<span data-ttu-id="4009a-103">Obtém um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="4009a-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="4009a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4009a-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4009a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4009a-105">DESCRIPTION</span></span>
<span data-ttu-id="4009a-106">O cmdlet **Get-AzRedisCache** obtém o Cache de Redis do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="4009a-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="4009a-107">Se você especificar nenhum parâmetro, essa operação obtém todos os Redis Cache da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4009a-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="4009a-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4009a-108">EXAMPLES</span></span>

### <span data-ttu-id="4009a-109">Exemplo 1: Obter um Cache de Redis por nome</span><span class="sxs-lookup"><span data-stu-id="4009a-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="4009a-110">Esse comando recebe o Cache Redis denominado myexists.</span><span class="sxs-lookup"><span data-stu-id="4009a-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="4009a-111">Exemplo 2: Obter cada Cache de Redis em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4009a-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="4009a-112">Esse comando obtém todos os Caches De Redis no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="4009a-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="4009a-113">Exemplo 3: Obter cada Cache de Redis na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="4009a-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="4009a-114">Esse comando obtém todos os Caches De Redis na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4009a-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="4009a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4009a-115">PARAMETERS</span></span>

### <span data-ttu-id="4009a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4009a-116">-DefaultProfile</span></span>
<span data-ttu-id="4009a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4009a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4009a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4009a-118">-Name</span></span>
<span data-ttu-id="4009a-119">Especifica o nome do Cache de Redis para obter.</span><span class="sxs-lookup"><span data-stu-id="4009a-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="4009a-120">Use com o parâmetro *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="4009a-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="4009a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4009a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4009a-122">Especifica o nome do grupo de recursos que contém o Cache de Redis para obter.</span><span class="sxs-lookup"><span data-stu-id="4009a-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="4009a-123">Se você especificar apenas o parâmetro *ResourceGroupName,* essa operação obtém cada Cache de Redis no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="4009a-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="4009a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4009a-124">CommonParameters</span></span>
<span data-ttu-id="4009a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4009a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4009a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4009a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4009a-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="4009a-127">INPUTS</span></span>

### <span data-ttu-id="4009a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4009a-128">System.String</span></span>

## <span data-ttu-id="4009a-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="4009a-129">OUTPUTS</span></span>

### <span data-ttu-id="4009a-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="4009a-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="4009a-131">Notas</span><span class="sxs-lookup"><span data-stu-id="4009a-131">NOTES</span></span>

## <span data-ttu-id="4009a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4009a-132">RELATED LINKS</span></span>

[<span data-ttu-id="4009a-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4009a-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4009a-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4009a-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4009a-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4009a-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


