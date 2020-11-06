---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602420"
---
# <span data-ttu-id="08d33-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="08d33-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="08d33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08d33-102">SYNOPSIS</span></span>
<span data-ttu-id="08d33-103">Cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08d33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08d33-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08d33-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08d33-105">DESCRIPTION</span></span>
<span data-ttu-id="08d33-106">O cmdlet **New-AzureRmRedisCache** cria um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="08d33-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08d33-107">EXAMPLES</span></span>

### <span data-ttu-id="08d33-108">Exemplo 1: criar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="08d33-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

<span data-ttu-id="08d33-109">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="08d33-110">Exemplo 2: criar um cache de Redis de SKU padrão</span><span class="sxs-lookup"><span data-stu-id="08d33-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

<span data-ttu-id="08d33-111">Esse comando cria um cache Redis ou atualiza o cache do Redis caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="08d33-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="08d33-112">OS</span><span class="sxs-lookup"><span data-stu-id="08d33-112">PARAMETERS</span></span>

### <span data-ttu-id="08d33-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="08d33-113">-EnableNonSslPort</span></span>
<span data-ttu-id="08d33-114">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="08d33-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="08d33-115">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="08d33-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="08d33-116">-Local</span><span class="sxs-lookup"><span data-stu-id="08d33-116">-Location</span></span>
<span data-ttu-id="08d33-117">Especifica o local no qual criar um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="08d33-118">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="08d33-118">Valid values are:</span></span> 

- <span data-ttu-id="08d33-119">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="08d33-119">North Central US</span></span>
- <span data-ttu-id="08d33-120">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="08d33-120">South Central US</span></span>
- <span data-ttu-id="08d33-121">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="08d33-121">Central US</span></span>
- <span data-ttu-id="08d33-122">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="08d33-122">West Europe</span></span>
- <span data-ttu-id="08d33-123">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="08d33-123">North Europe</span></span>
- <span data-ttu-id="08d33-124">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="08d33-124">West US</span></span>
- <span data-ttu-id="08d33-125">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="08d33-125">East US</span></span>
- <span data-ttu-id="08d33-126">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="08d33-126">East US 2</span></span>
- <span data-ttu-id="08d33-127">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="08d33-127">Japan East</span></span>
- <span data-ttu-id="08d33-128">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="08d33-128">Japan West</span></span>
- <span data-ttu-id="08d33-129">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="08d33-129">Brazil South</span></span>
- <span data-ttu-id="08d33-130">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="08d33-130">Southeast Asia</span></span>
- <span data-ttu-id="08d33-131">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="08d33-131">East Asia</span></span>
- <span data-ttu-id="08d33-132">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="08d33-132">Australia East</span></span>
- <span data-ttu-id="08d33-133">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="08d33-133">Australia Southeast</span></span>

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

### <span data-ttu-id="08d33-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="08d33-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="08d33-135">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="08d33-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="08d33-136">Use o parâmetro *RedisConfiguration* para definir MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="08d33-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="08d33-137">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="08d33-137">For example:</span></span> 

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

### <span data-ttu-id="08d33-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="08d33-138">-Name</span></span>
<span data-ttu-id="08d33-139">Especifica o nome do cache de Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="08d33-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="08d33-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d33-140">-RedisConfiguration</span></span>
<span data-ttu-id="08d33-141">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="08d33-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08d33-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08d33-143">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="08d33-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="08d33-144">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="08d33-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="08d33-145">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-145">Premium tier only.</span></span>
- <span data-ttu-id="08d33-146">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="08d33-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="08d33-147">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="08d33-148">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-148">Premium tier only.</span></span>
- <span data-ttu-id="08d33-149">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="08d33-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="08d33-150">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="08d33-151">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-151">Premium tier only.</span></span> 
- <span data-ttu-id="08d33-152">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="08d33-152">maxmemory-reserved.</span></span>
<span data-ttu-id="08d33-153">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="08d33-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="08d33-154">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="08d33-155">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="08d33-155">maxmemory-policy.</span></span>
<span data-ttu-id="08d33-156">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="08d33-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="08d33-157">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="08d33-157">All pricing tiers.</span></span> 
- <span data-ttu-id="08d33-158">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="08d33-158">notify-keyspace-events.</span></span>
<span data-ttu-id="08d33-159">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="08d33-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="08d33-160">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="08d33-161">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="08d33-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="08d33-162">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="08d33-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="08d33-163">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="08d33-164">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="08d33-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="08d33-165">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="08d33-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="08d33-166">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="08d33-167">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="08d33-167">set-max-intset-entries.</span></span>
<span data-ttu-id="08d33-168">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="08d33-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="08d33-169">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="08d33-170">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="08d33-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="08d33-171">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="08d33-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="08d33-172">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="08d33-173">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="08d33-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="08d33-174">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="08d33-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="08d33-175">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="08d33-176">bancos.</span><span class="sxs-lookup"><span data-stu-id="08d33-176">databases.</span></span>
<span data-ttu-id="08d33-177">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="08d33-177">Configures the number of databases.</span></span>
<span data-ttu-id="08d33-178">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="08d33-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="08d33-179">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="08d33-180">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="08d33-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="08d33-181">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="08d33-181">-RedisVersion</span></span>
<span data-ttu-id="08d33-182">Esse parâmetro é preterido e será removido de versões futuras.</span><span class="sxs-lookup"><span data-stu-id="08d33-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="08d33-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08d33-183">-ResourceGroupName</span></span>
<span data-ttu-id="08d33-184">Especifica o nome do grupo de recursos no qual criar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="08d33-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="08d33-185">-ShardCount</span></span>
<span data-ttu-id="08d33-186">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="08d33-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="08d33-187">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08d33-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08d33-188">um</span><span class="sxs-lookup"><span data-stu-id="08d33-188">1</span></span>
- <span data-ttu-id="08d33-189">2</span><span class="sxs-lookup"><span data-stu-id="08d33-189">2</span></span>
- <span data-ttu-id="08d33-190">3D</span><span class="sxs-lookup"><span data-stu-id="08d33-190">3</span></span>
- <span data-ttu-id="08d33-191">4</span><span class="sxs-lookup"><span data-stu-id="08d33-191">4</span></span>
- <span data-ttu-id="08d33-192">5</span><span class="sxs-lookup"><span data-stu-id="08d33-192">5</span></span>
- <span data-ttu-id="08d33-193">5</span><span class="sxs-lookup"><span data-stu-id="08d33-193">6</span></span>
- <span data-ttu-id="08d33-194">7</span><span class="sxs-lookup"><span data-stu-id="08d33-194">7</span></span>
- <span data-ttu-id="08d33-195">08</span><span class="sxs-lookup"><span data-stu-id="08d33-195">8</span></span>
- <span data-ttu-id="08d33-196">222</span><span class="sxs-lookup"><span data-stu-id="08d33-196">9</span></span> 
- <span data-ttu-id="08d33-197">254</span><span class="sxs-lookup"><span data-stu-id="08d33-197">10</span></span>

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

### <span data-ttu-id="08d33-198">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="08d33-198">-Size</span></span>
<span data-ttu-id="08d33-199">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="08d33-200">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="08d33-200">Valid values are:</span></span> 

- <span data-ttu-id="08d33-201">P1</span><span class="sxs-lookup"><span data-stu-id="08d33-201">P1</span></span>
- <span data-ttu-id="08d33-202">P2</span><span class="sxs-lookup"><span data-stu-id="08d33-202">P2</span></span>
- <span data-ttu-id="08d33-203">P3</span><span class="sxs-lookup"><span data-stu-id="08d33-203">P3</span></span>
- <span data-ttu-id="08d33-204">P4</span><span class="sxs-lookup"><span data-stu-id="08d33-204">P4</span></span>
- <span data-ttu-id="08d33-205">C0</span><span class="sxs-lookup"><span data-stu-id="08d33-205">C0</span></span>
- <span data-ttu-id="08d33-206">C1</span><span class="sxs-lookup"><span data-stu-id="08d33-206">C1</span></span>
- <span data-ttu-id="08d33-207">C2</span><span class="sxs-lookup"><span data-stu-id="08d33-207">C2</span></span>
- <span data-ttu-id="08d33-208">C3</span><span class="sxs-lookup"><span data-stu-id="08d33-208">C3</span></span>
- <span data-ttu-id="08d33-209">C4</span><span class="sxs-lookup"><span data-stu-id="08d33-209">C4</span></span>
- <span data-ttu-id="08d33-210">C5</span><span class="sxs-lookup"><span data-stu-id="08d33-210">C5</span></span>
- <span data-ttu-id="08d33-211">C6</span><span class="sxs-lookup"><span data-stu-id="08d33-211">C6</span></span>
- <span data-ttu-id="08d33-212">250MB</span><span class="sxs-lookup"><span data-stu-id="08d33-212">250MB</span></span>
- <span data-ttu-id="08d33-213">1 GB</span><span class="sxs-lookup"><span data-stu-id="08d33-213">1GB</span></span>
- <span data-ttu-id="08d33-214">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="08d33-214">2.5GB</span></span>
- <span data-ttu-id="08d33-215">6GB</span><span class="sxs-lookup"><span data-stu-id="08d33-215">6GB</span></span>
- <span data-ttu-id="08d33-216">13GB</span><span class="sxs-lookup"><span data-stu-id="08d33-216">13GB</span></span>
- <span data-ttu-id="08d33-217">26GB</span><span class="sxs-lookup"><span data-stu-id="08d33-217">26GB</span></span>
- <span data-ttu-id="08d33-218">53GB</span><span class="sxs-lookup"><span data-stu-id="08d33-218">53GB</span></span>

<span data-ttu-id="08d33-219">O valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="08d33-219">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="08d33-220">-SKU</span><span class="sxs-lookup"><span data-stu-id="08d33-220">-Sku</span></span>
<span data-ttu-id="08d33-221">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="08d33-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="08d33-222">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="08d33-222">Valid values are:</span></span> 

- <span data-ttu-id="08d33-223">Basic</span><span class="sxs-lookup"><span data-stu-id="08d33-223">Basic</span></span>
- <span data-ttu-id="08d33-224">Oficial</span><span class="sxs-lookup"><span data-stu-id="08d33-224">Standard</span></span>
- <span data-ttu-id="08d33-225">Gratifica</span><span class="sxs-lookup"><span data-stu-id="08d33-225">Premium</span></span>

<span data-ttu-id="08d33-226">O valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="08d33-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="08d33-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="08d33-227">-StaticIP</span></span>
<span data-ttu-id="08d33-228">Especifica um endereço IP exclusivo na sub-rede para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="08d33-229">Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="08d33-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="08d33-230">-Subnet</span><span class="sxs-lookup"><span data-stu-id="08d33-230">-Subnet</span></span>
<span data-ttu-id="08d33-231">Especifica o nome da sub-rede na qual implantar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="08d33-232">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="08d33-232">-SubnetId</span></span>
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

### <span data-ttu-id="08d33-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="08d33-233">-TenantSettings</span></span>
<span data-ttu-id="08d33-234">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="08d33-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="08d33-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08d33-235">-VirtualNetwork</span></span>
<span data-ttu-id="08d33-236">Especifica a ID do recurso da rede virtual na qual você deseja implantar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="08d33-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="08d33-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d33-237">-DefaultProfile</span></span>
<span data-ttu-id="08d33-238">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08d33-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08d33-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d33-239">CommonParameters</span></span>
<span data-ttu-id="08d33-240">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08d33-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d33-241">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08d33-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d33-242">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08d33-242">INPUTS</span></span>

### <span data-ttu-id="08d33-243">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="08d33-243">None</span></span>
<span data-ttu-id="08d33-244">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="08d33-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="08d33-245">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08d33-245">OUTPUTS</span></span>

### <span data-ttu-id="08d33-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="08d33-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="08d33-247">Esse cmdlet retorna todos os atributos de um cache Redis incluindo as chaves de acesso primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="08d33-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="08d33-248">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08d33-248">NOTES</span></span>

## <span data-ttu-id="08d33-249">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08d33-249">RELATED LINKS</span></span>

[<span data-ttu-id="08d33-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="08d33-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="08d33-251">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="08d33-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="08d33-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="08d33-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


