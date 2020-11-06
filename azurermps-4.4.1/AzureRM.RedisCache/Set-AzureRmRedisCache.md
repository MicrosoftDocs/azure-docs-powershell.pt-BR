---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429143"
---
# <span data-ttu-id="166ed-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="166ed-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="166ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="166ed-102">SYNOPSIS</span></span>
<span data-ttu-id="166ed-103">Modifica um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="166ed-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="166ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="166ed-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="166ed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="166ed-105">DESCRIPTION</span></span>
<span data-ttu-id="166ed-106">O cmdlet **set-AzureRmRedisCache** modifica um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="166ed-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="166ed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="166ed-107">EXAMPLES</span></span>

### <span data-ttu-id="166ed-108">Exemplo 1: modificar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="166ed-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
```

<span data-ttu-id="166ed-109">Esse comando atualiza a política MaxMemory do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="166ed-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="166ed-110">OS</span><span class="sxs-lookup"><span data-stu-id="166ed-110">PARAMETERS</span></span>

### <span data-ttu-id="166ed-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="166ed-111">-EnableNonSslPort</span></span>
<span data-ttu-id="166ed-112">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="166ed-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="166ed-113">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="166ed-113">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="166ed-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="166ed-115">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="166ed-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="166ed-116">Use o parâmetro *RedisConfiguration* para definir MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="166ed-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="166ed-117">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="166ed-117">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="166ed-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="166ed-118">-Name</span></span>
<span data-ttu-id="166ed-119">Especifica o nome do cache do Redis a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="166ed-119">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="166ed-120">-RedisConfiguration</span></span>
<span data-ttu-id="166ed-121">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="166ed-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="166ed-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="166ed-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="166ed-123">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="166ed-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="166ed-124">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="166ed-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="166ed-125">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-125">Premium tier only.</span></span>
- <span data-ttu-id="166ed-126">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="166ed-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="166ed-127">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="166ed-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="166ed-128">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-128">Premium tier only.</span></span>
- <span data-ttu-id="166ed-129">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="166ed-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="166ed-130">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="166ed-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="166ed-131">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-131">Premium tier only.</span></span> 
- <span data-ttu-id="166ed-132">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="166ed-132">maxmemory-reserved.</span></span>
<span data-ttu-id="166ed-133">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="166ed-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="166ed-134">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="166ed-135">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="166ed-135">maxmemory-policy.</span></span>
<span data-ttu-id="166ed-136">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="166ed-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="166ed-137">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="166ed-137">All pricing tiers.</span></span> 
- <span data-ttu-id="166ed-138">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="166ed-138">notify-keyspace-events.</span></span>
<span data-ttu-id="166ed-139">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="166ed-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="166ed-140">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="166ed-141">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="166ed-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="166ed-142">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="166ed-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="166ed-143">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="166ed-144">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="166ed-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="166ed-145">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="166ed-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="166ed-146">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="166ed-147">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="166ed-147">set-max-intset-entries.</span></span>
<span data-ttu-id="166ed-148">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="166ed-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="166ed-149">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="166ed-150">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="166ed-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="166ed-151">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="166ed-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="166ed-152">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="166ed-153">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="166ed-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="166ed-154">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="166ed-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="166ed-155">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="166ed-156">bancos.</span><span class="sxs-lookup"><span data-stu-id="166ed-156">databases.</span></span>
<span data-ttu-id="166ed-157">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="166ed-157">Configures the number of databases.</span></span>
<span data-ttu-id="166ed-158">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="166ed-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="166ed-159">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="166ed-160">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="166ed-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166ed-161">-ResourceGroupName</span></span>
<span data-ttu-id="166ed-162">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="166ed-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="166ed-163">-ShardCount</span></span>
<span data-ttu-id="166ed-164">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="166ed-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-165">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="166ed-165">-Size</span></span>
<span data-ttu-id="166ed-166">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="166ed-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="166ed-167">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="166ed-167">Valid values are:</span></span> 

- <span data-ttu-id="166ed-168">P1</span><span class="sxs-lookup"><span data-stu-id="166ed-168">P1</span></span>
- <span data-ttu-id="166ed-169">P2</span><span class="sxs-lookup"><span data-stu-id="166ed-169">P2</span></span>
- <span data-ttu-id="166ed-170">P3</span><span class="sxs-lookup"><span data-stu-id="166ed-170">P3</span></span>
- <span data-ttu-id="166ed-171">P4</span><span class="sxs-lookup"><span data-stu-id="166ed-171">P4</span></span>
- <span data-ttu-id="166ed-172">C0</span><span class="sxs-lookup"><span data-stu-id="166ed-172">C0</span></span>
- <span data-ttu-id="166ed-173">C1</span><span class="sxs-lookup"><span data-stu-id="166ed-173">C1</span></span>
- <span data-ttu-id="166ed-174">C2</span><span class="sxs-lookup"><span data-stu-id="166ed-174">C2</span></span>
- <span data-ttu-id="166ed-175">C3</span><span class="sxs-lookup"><span data-stu-id="166ed-175">C3</span></span>
- <span data-ttu-id="166ed-176">C4</span><span class="sxs-lookup"><span data-stu-id="166ed-176">C4</span></span>
- <span data-ttu-id="166ed-177">C5</span><span class="sxs-lookup"><span data-stu-id="166ed-177">C5</span></span>
- <span data-ttu-id="166ed-178">C6</span><span class="sxs-lookup"><span data-stu-id="166ed-178">C6</span></span>
- <span data-ttu-id="166ed-179">250MB</span><span class="sxs-lookup"><span data-stu-id="166ed-179">250MB</span></span>
- <span data-ttu-id="166ed-180">1 GB</span><span class="sxs-lookup"><span data-stu-id="166ed-180">1GB</span></span>
- <span data-ttu-id="166ed-181">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="166ed-181">2.5GB</span></span>
- <span data-ttu-id="166ed-182">6GB</span><span class="sxs-lookup"><span data-stu-id="166ed-182">6GB</span></span>
- <span data-ttu-id="166ed-183">13GB</span><span class="sxs-lookup"><span data-stu-id="166ed-183">13GB</span></span>
- <span data-ttu-id="166ed-184">26GB</span><span class="sxs-lookup"><span data-stu-id="166ed-184">26GB</span></span>
- <span data-ttu-id="166ed-185">53GB</span><span class="sxs-lookup"><span data-stu-id="166ed-185">53GB</span></span>

<span data-ttu-id="166ed-186">O valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="166ed-186">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-187">-SKU</span><span class="sxs-lookup"><span data-stu-id="166ed-187">-Sku</span></span>
<span data-ttu-id="166ed-188">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="166ed-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="166ed-189">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="166ed-189">Valid values are:</span></span> 

- <span data-ttu-id="166ed-190">Basic</span><span class="sxs-lookup"><span data-stu-id="166ed-190">Basic</span></span>
- <span data-ttu-id="166ed-191">Oficial</span><span class="sxs-lookup"><span data-stu-id="166ed-191">Standard</span></span>
- <span data-ttu-id="166ed-192">Gratifica</span><span class="sxs-lookup"><span data-stu-id="166ed-192">Premium</span></span>

<span data-ttu-id="166ed-193">O valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="166ed-193">The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="166ed-194">-TenantSettings</span></span>
<span data-ttu-id="166ed-195">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="166ed-195">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166ed-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166ed-196">-DefaultProfile</span></span>
<span data-ttu-id="166ed-197">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="166ed-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="166ed-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166ed-198">CommonParameters</span></span>
<span data-ttu-id="166ed-199">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="166ed-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166ed-200">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="166ed-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166ed-201">SENSORES</span><span class="sxs-lookup"><span data-stu-id="166ed-201">INPUTS</span></span>

### <span data-ttu-id="166ed-202">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="166ed-202">None</span></span>
<span data-ttu-id="166ed-203">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="166ed-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="166ed-204">EXIBE</span><span class="sxs-lookup"><span data-stu-id="166ed-204">OUTPUTS</span></span>

### <span data-ttu-id="166ed-205">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="166ed-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="166ed-206">Retorna todos os atributos de um cache Redis, incluindo as chaves de acesso primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="166ed-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="166ed-207">INFORMA</span><span class="sxs-lookup"><span data-stu-id="166ed-207">NOTES</span></span>

## <span data-ttu-id="166ed-208">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="166ed-208">RELATED LINKS</span></span>

[<span data-ttu-id="166ed-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="166ed-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="166ed-210">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="166ed-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="166ed-211">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="166ed-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


