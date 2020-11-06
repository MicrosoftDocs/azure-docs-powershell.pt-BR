---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429705"
---
# <span data-ttu-id="dfd7d-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd7d-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="dfd7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd7d-103">Modifica um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfd7d-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfd7d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfd7d-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd7d-106">O cmdlet **set-AzureRmRedisCache** modifica um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="dfd7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfd7d-107">EXAMPLES</span></span>

### <span data-ttu-id="dfd7d-108">Exemplo 1: modificar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="dfd7d-108">Example 1: Modify a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="dfd7d-109">Esse comando atualiza a política MaxMemory do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="dfd7d-110">OS</span><span class="sxs-lookup"><span data-stu-id="dfd7d-110">PARAMETERS</span></span>

### <span data-ttu-id="dfd7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd7d-111">-DefaultProfile</span></span>
<span data-ttu-id="dfd7d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfd7d-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="dfd7d-113">-EnableNonSslPort</span></span>
<span data-ttu-id="dfd7d-114">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="dfd7d-115">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="dfd7d-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="dfd7d-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="dfd7d-117">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="dfd7d-118">Use o parâmetro *RedisConfiguration* para definir MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="dfd7d-119">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dfd7d-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="dfd7d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfd7d-120">-Name</span></span>
<span data-ttu-id="dfd7d-121">Especifica o nome do cache do Redis a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfd7d-122">-RedisConfiguration</span></span>
<span data-ttu-id="dfd7d-123">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="dfd7d-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dfd7d-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfd7d-125">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="dfd7d-126">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="dfd7d-127">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-127">Premium tier only.</span></span>
- <span data-ttu-id="dfd7d-128">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="dfd7d-129">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="dfd7d-130">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-130">Premium tier only.</span></span>
- <span data-ttu-id="dfd7d-131">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="dfd7d-132">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="dfd7d-133">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-133">Premium tier only.</span></span> 
- <span data-ttu-id="dfd7d-134">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-134">maxmemory-reserved.</span></span>
<span data-ttu-id="dfd7d-135">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="dfd7d-136">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd7d-137">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-137">maxmemory-policy.</span></span>
<span data-ttu-id="dfd7d-138">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="dfd7d-139">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-139">All pricing tiers.</span></span> 
- <span data-ttu-id="dfd7d-140">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-140">notify-keyspace-events.</span></span>
<span data-ttu-id="dfd7d-141">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="dfd7d-142">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="dfd7d-143">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="dfd7d-144">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd7d-145">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd7d-146">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="dfd7d-147">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd7d-148">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd7d-149">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-149">set-max-intset-entries.</span></span>
<span data-ttu-id="dfd7d-150">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd7d-151">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd7d-152">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="dfd7d-153">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd7d-154">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd7d-155">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="dfd7d-156">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfd7d-157">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfd7d-158">bancos.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-158">databases.</span></span>
<span data-ttu-id="dfd7d-159">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-159">Configures the number of databases.</span></span>
<span data-ttu-id="dfd7d-160">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="dfd7d-161">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="dfd7d-162">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="dfd7d-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd7d-163">-ResourceGroupName</span></span>
<span data-ttu-id="dfd7d-164">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="dfd7d-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="dfd7d-165">-ShardCount</span></span>
<span data-ttu-id="dfd7d-166">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-167">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="dfd7d-167">-Size</span></span>
<span data-ttu-id="dfd7d-168">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="dfd7d-169">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dfd7d-169">Valid values are:</span></span> 

- <span data-ttu-id="dfd7d-170">P1</span><span class="sxs-lookup"><span data-stu-id="dfd7d-170">P1</span></span>
- <span data-ttu-id="dfd7d-171">P2</span><span class="sxs-lookup"><span data-stu-id="dfd7d-171">P2</span></span>
- <span data-ttu-id="dfd7d-172">P3</span><span class="sxs-lookup"><span data-stu-id="dfd7d-172">P3</span></span>
- <span data-ttu-id="dfd7d-173">P4</span><span class="sxs-lookup"><span data-stu-id="dfd7d-173">P4</span></span>
- <span data-ttu-id="dfd7d-174">C0</span><span class="sxs-lookup"><span data-stu-id="dfd7d-174">C0</span></span>
- <span data-ttu-id="dfd7d-175">C1</span><span class="sxs-lookup"><span data-stu-id="dfd7d-175">C1</span></span>
- <span data-ttu-id="dfd7d-176">C2</span><span class="sxs-lookup"><span data-stu-id="dfd7d-176">C2</span></span>
- <span data-ttu-id="dfd7d-177">C3</span><span class="sxs-lookup"><span data-stu-id="dfd7d-177">C3</span></span>
- <span data-ttu-id="dfd7d-178">C4</span><span class="sxs-lookup"><span data-stu-id="dfd7d-178">C4</span></span>
- <span data-ttu-id="dfd7d-179">C5</span><span class="sxs-lookup"><span data-stu-id="dfd7d-179">C5</span></span>
- <span data-ttu-id="dfd7d-180">C6</span><span class="sxs-lookup"><span data-stu-id="dfd7d-180">C6</span></span>
- <span data-ttu-id="dfd7d-181">250MB</span><span class="sxs-lookup"><span data-stu-id="dfd7d-181">250MB</span></span>
- <span data-ttu-id="dfd7d-182">1 GB</span><span class="sxs-lookup"><span data-stu-id="dfd7d-182">1GB</span></span>
- <span data-ttu-id="dfd7d-183">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="dfd7d-183">2.5GB</span></span>
- <span data-ttu-id="dfd7d-184">6GB</span><span class="sxs-lookup"><span data-stu-id="dfd7d-184">6GB</span></span>
- <span data-ttu-id="dfd7d-185">13GB</span><span class="sxs-lookup"><span data-stu-id="dfd7d-185">13GB</span></span>
- <span data-ttu-id="dfd7d-186">26GB</span><span class="sxs-lookup"><span data-stu-id="dfd7d-186">26GB</span></span>
- <span data-ttu-id="dfd7d-187">53GB</span><span class="sxs-lookup"><span data-stu-id="dfd7d-187">53GB</span></span>

<span data-ttu-id="dfd7d-188">O valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-189">-SKU</span><span class="sxs-lookup"><span data-stu-id="dfd7d-189">-Sku</span></span>
<span data-ttu-id="dfd7d-190">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="dfd7d-191">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dfd7d-191">Valid values are:</span></span> 

- <span data-ttu-id="dfd7d-192">Basic</span><span class="sxs-lookup"><span data-stu-id="dfd7d-192">Basic</span></span>
- <span data-ttu-id="dfd7d-193">Oficial</span><span class="sxs-lookup"><span data-stu-id="dfd7d-193">Standard</span></span>
- <span data-ttu-id="dfd7d-194">Gratifica</span><span class="sxs-lookup"><span data-stu-id="dfd7d-194">Premium</span></span>

<span data-ttu-id="dfd7d-195">O valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-196">-Marca</span><span class="sxs-lookup"><span data-stu-id="dfd7d-196">-Tag</span></span>
<span data-ttu-id="dfd7d-197">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="dfd7d-198">-TenantSettings</span></span>
<span data-ttu-id="dfd7d-199">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-200">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfd7d-200">-Confirm</span></span>
<span data-ttu-id="dfd7d-201">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd7d-202">-WhatIf</span></span>
<span data-ttu-id="dfd7d-203">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfd7d-204">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-204">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd7d-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd7d-205">CommonParameters</span></span>
<span data-ttu-id="dfd7d-206">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd7d-207">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd7d-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd7d-208">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfd7d-208">INPUTS</span></span>

### <span data-ttu-id="dfd7d-209">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dfd7d-209">None</span></span>
<span data-ttu-id="dfd7d-210">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="dfd7d-211">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfd7d-211">OUTPUTS</span></span>

### <span data-ttu-id="dfd7d-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dfd7d-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="dfd7d-213">Retorna todos os atributos de um cache Redis, incluindo as chaves de acesso primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="dfd7d-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="dfd7d-214">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfd7d-214">NOTES</span></span>

## <span data-ttu-id="dfd7d-215">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfd7d-215">RELATED LINKS</span></span>

[<span data-ttu-id="dfd7d-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd7d-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="dfd7d-217">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd7d-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="dfd7d-218">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfd7d-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


