---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440566"
---
# <span data-ttu-id="60a91-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="60a91-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="60a91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60a91-102">SYNOPSIS</span></span>
<span data-ttu-id="60a91-103">Obtém um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="60a91-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60a91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60a91-104">SYNTAX</span></span>

### <span data-ttu-id="60a91-105">Todos na assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="60a91-105">All In Subscription (Default)</span></span>
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60a91-106">Tudo no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="60a91-106">All In Resource Group</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60a91-107">Cache Redis específico</span><span class="sxs-lookup"><span data-stu-id="60a91-107">Specific Redis Cache</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60a91-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60a91-108">DESCRIPTION</span></span>
<span data-ttu-id="60a91-109">O cmdlet **Get-AzureRmRedisCache** Obtém o cache do Azure Redis especificado.</span><span class="sxs-lookup"><span data-stu-id="60a91-109">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="60a91-110">Se você especificar nenhum parâmetro, essa operação obterá cada cache Redis para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="60a91-110">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="60a91-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60a91-111">EXAMPLES</span></span>

### <span data-ttu-id="60a91-112">Exemplo 1: obter um cache Redis por nome</span><span class="sxs-lookup"><span data-stu-id="60a91-112">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

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
```

<span data-ttu-id="60a91-113">Este comando obtém o cache Redis chamado myexists.</span><span class="sxs-lookup"><span data-stu-id="60a91-113">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="60a91-114">Exemplo 2: obter todos os Redis cache em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="60a91-114">Example 2: Get every Redis Cache in a resource group</span></span>
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
```

<span data-ttu-id="60a91-115">Esse comando obtém todos os Redis cache do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="60a91-115">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="60a91-116">Exemplo 3: obter todos os Redis cache na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="60a91-116">Example 3: Get every Redis Cache in the current subscription</span></span>
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
```

<span data-ttu-id="60a91-117">Esse comando obtém todos os Redis cache na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="60a91-117">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="60a91-118">OS</span><span class="sxs-lookup"><span data-stu-id="60a91-118">PARAMETERS</span></span>

### <span data-ttu-id="60a91-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="60a91-119">-Name</span></span>
<span data-ttu-id="60a91-120">Especifica o nome do cache de Redis a obter.</span><span class="sxs-lookup"><span data-stu-id="60a91-120">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="60a91-121">Use com o parâmetro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="60a91-121">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a91-122">-ResourceGroupName</span></span>
<span data-ttu-id="60a91-123">Especifica o nome do grupo de recursos que contém o cache de Redis a obter.</span><span class="sxs-lookup"><span data-stu-id="60a91-123">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="60a91-124">Se você especificar somente o parâmetro *ResourceGroupName* , essa operação obterá cada cache Redis no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="60a91-124">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a91-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a91-125">-DefaultProfile</span></span>
<span data-ttu-id="60a91-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60a91-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60a91-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a91-127">CommonParameters</span></span>
<span data-ttu-id="60a91-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a91-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a91-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a91-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a91-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60a91-130">INPUTS</span></span>

### <span data-ttu-id="60a91-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="60a91-131">None</span></span>
<span data-ttu-id="60a91-132">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="60a91-132">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="60a91-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60a91-133">OUTPUTS</span></span>

### <span data-ttu-id="60a91-134">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="60a91-134">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="60a91-135">Retorna uma matriz de objetos **RedisCacheAttributes** .</span><span class="sxs-lookup"><span data-stu-id="60a91-135">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="60a91-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60a91-136">NOTES</span></span>

## <span data-ttu-id="60a91-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60a91-137">RELATED LINKS</span></span>

[<span data-ttu-id="60a91-138">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="60a91-138">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="60a91-139">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="60a91-139">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="60a91-140">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="60a91-140">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


