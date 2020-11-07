---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772941"
---
# <span data-ttu-id="55155-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="55155-101">New-AzRedisCache</span></span>

## <span data-ttu-id="55155-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55155-102">SYNOPSIS</span></span>
<span data-ttu-id="55155-103">Cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="55155-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55155-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55155-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55155-105">DESCRIPTION</span></span>
<span data-ttu-id="55155-106">O cmdlet **New-AzRedisCache** cria um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="55155-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55155-107">EXAMPLES</span></span>

### <span data-ttu-id="55155-108">Exemplo 1: criar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="55155-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="55155-109">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="55155-110">Exemplo 2: criar um cache de Redis de SKU padrão</span><span class="sxs-lookup"><span data-stu-id="55155-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="55155-111">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="55155-112">OS</span><span class="sxs-lookup"><span data-stu-id="55155-112">PARAMETERS</span></span>

### <span data-ttu-id="55155-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55155-113">-DefaultProfile</span></span>
<span data-ttu-id="55155-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55155-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55155-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="55155-115">-EnableNonSslPort</span></span>
<span data-ttu-id="55155-116">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="55155-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="55155-117">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="55155-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="55155-118">-Local</span><span class="sxs-lookup"><span data-stu-id="55155-118">-Location</span></span>
<span data-ttu-id="55155-119">Especifica o local no qual criar um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="55155-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="55155-120">Valid values are:</span></span> 
- <span data-ttu-id="55155-121">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="55155-121">North Central US</span></span>
- <span data-ttu-id="55155-122">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="55155-122">South Central US</span></span>
- <span data-ttu-id="55155-123">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="55155-123">Central US</span></span>
- <span data-ttu-id="55155-124">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="55155-124">West Europe</span></span>
- <span data-ttu-id="55155-125">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="55155-125">North Europe</span></span>
- <span data-ttu-id="55155-126">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="55155-126">West US</span></span>
- <span data-ttu-id="55155-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="55155-127">East US</span></span>
- <span data-ttu-id="55155-128">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="55155-128">East US 2</span></span>
- <span data-ttu-id="55155-129">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="55155-129">Japan East</span></span>
- <span data-ttu-id="55155-130">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="55155-130">Japan West</span></span>
- <span data-ttu-id="55155-131">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="55155-131">Brazil South</span></span>
- <span data-ttu-id="55155-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="55155-132">Southeast Asia</span></span>
- <span data-ttu-id="55155-133">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="55155-133">East Asia</span></span>
- <span data-ttu-id="55155-134">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="55155-134">Australia East</span></span>
- <span data-ttu-id="55155-135">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="55155-135">Australia Southeast</span></span>

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

### <span data-ttu-id="55155-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="55155-136">-Name</span></span>
<span data-ttu-id="55155-137">Especifica o nome do cache de Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="55155-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="55155-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="55155-138">-RedisConfiguration</span></span>
<span data-ttu-id="55155-139">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="55155-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="55155-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55155-141">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="55155-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="55155-142">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="55155-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="55155-143">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-143">Premium tier only.</span></span>
- <span data-ttu-id="55155-144">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="55155-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="55155-145">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="55155-146">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-146">Premium tier only.</span></span>
- <span data-ttu-id="55155-147">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="55155-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="55155-148">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="55155-149">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-149">Premium tier only.</span></span> 
- <span data-ttu-id="55155-150">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="55155-150">maxmemory-reserved.</span></span>
<span data-ttu-id="55155-151">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="55155-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="55155-152">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="55155-153">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="55155-153">maxmemory-policy.</span></span>
<span data-ttu-id="55155-154">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="55155-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="55155-155">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="55155-155">All pricing tiers.</span></span> 
- <span data-ttu-id="55155-156">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="55155-156">notify-keyspace-events.</span></span>
<span data-ttu-id="55155-157">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="55155-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="55155-158">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="55155-159">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="55155-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="55155-160">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="55155-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="55155-161">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="55155-162">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="55155-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="55155-163">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="55155-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="55155-164">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="55155-165">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="55155-165">set-max-intset-entries.</span></span>
<span data-ttu-id="55155-166">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="55155-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="55155-167">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="55155-168">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="55155-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="55155-169">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="55155-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="55155-170">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="55155-171">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="55155-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="55155-172">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="55155-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="55155-173">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="55155-174">bancos.</span><span class="sxs-lookup"><span data-stu-id="55155-174">databases.</span></span>
<span data-ttu-id="55155-175">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="55155-175">Configures the number of databases.</span></span>
<span data-ttu-id="55155-176">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="55155-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="55155-177">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="55155-178">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="55155-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="55155-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55155-179">-ResourceGroupName</span></span>
<span data-ttu-id="55155-180">Especifica o nome do grupo de recursos no qual criar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="55155-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="55155-181">-ShardCount</span></span>
<span data-ttu-id="55155-182">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="55155-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="55155-183">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="55155-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55155-184">um</span><span class="sxs-lookup"><span data-stu-id="55155-184">1</span></span>
- <span data-ttu-id="55155-185">2</span><span class="sxs-lookup"><span data-stu-id="55155-185">2</span></span>
- <span data-ttu-id="55155-186">3D</span><span class="sxs-lookup"><span data-stu-id="55155-186">3</span></span>
- <span data-ttu-id="55155-187">4</span><span class="sxs-lookup"><span data-stu-id="55155-187">4</span></span>
- <span data-ttu-id="55155-188">5</span><span class="sxs-lookup"><span data-stu-id="55155-188">5</span></span>
- <span data-ttu-id="55155-189">5</span><span class="sxs-lookup"><span data-stu-id="55155-189">6</span></span>
- <span data-ttu-id="55155-190">7</span><span class="sxs-lookup"><span data-stu-id="55155-190">7</span></span>
- <span data-ttu-id="55155-191">08</span><span class="sxs-lookup"><span data-stu-id="55155-191">8</span></span>
- <span data-ttu-id="55155-192">222</span><span class="sxs-lookup"><span data-stu-id="55155-192">9</span></span> 
- <span data-ttu-id="55155-193">254</span><span class="sxs-lookup"><span data-stu-id="55155-193">10</span></span>

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

### <span data-ttu-id="55155-194">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="55155-194">-Size</span></span>
<span data-ttu-id="55155-195">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="55155-196">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="55155-196">Valid values are:</span></span> 
- <span data-ttu-id="55155-197">P1</span><span class="sxs-lookup"><span data-stu-id="55155-197">P1</span></span>
- <span data-ttu-id="55155-198">P2</span><span class="sxs-lookup"><span data-stu-id="55155-198">P2</span></span>
- <span data-ttu-id="55155-199">P3</span><span class="sxs-lookup"><span data-stu-id="55155-199">P3</span></span>
- <span data-ttu-id="55155-200">P4</span><span class="sxs-lookup"><span data-stu-id="55155-200">P4</span></span>
- <span data-ttu-id="55155-201">C0</span><span class="sxs-lookup"><span data-stu-id="55155-201">C0</span></span>
- <span data-ttu-id="55155-202">C1</span><span class="sxs-lookup"><span data-stu-id="55155-202">C1</span></span>
- <span data-ttu-id="55155-203">C2</span><span class="sxs-lookup"><span data-stu-id="55155-203">C2</span></span>
- <span data-ttu-id="55155-204">C3</span><span class="sxs-lookup"><span data-stu-id="55155-204">C3</span></span>
- <span data-ttu-id="55155-205">C4</span><span class="sxs-lookup"><span data-stu-id="55155-205">C4</span></span>
- <span data-ttu-id="55155-206">C5</span><span class="sxs-lookup"><span data-stu-id="55155-206">C5</span></span>
- <span data-ttu-id="55155-207">C6</span><span class="sxs-lookup"><span data-stu-id="55155-207">C6</span></span>
- <span data-ttu-id="55155-208">250MB</span><span class="sxs-lookup"><span data-stu-id="55155-208">250MB</span></span>
- <span data-ttu-id="55155-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="55155-209">1GB</span></span>
- <span data-ttu-id="55155-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="55155-210">2.5GB</span></span>
- <span data-ttu-id="55155-211">6GB</span><span class="sxs-lookup"><span data-stu-id="55155-211">6GB</span></span>
- <span data-ttu-id="55155-212">13GB</span><span class="sxs-lookup"><span data-stu-id="55155-212">13GB</span></span>
- <span data-ttu-id="55155-213">26GB</span><span class="sxs-lookup"><span data-stu-id="55155-213">26GB</span></span>
- <span data-ttu-id="55155-214">53GB o valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="55155-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="55155-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="55155-215">-Sku</span></span>
<span data-ttu-id="55155-216">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="55155-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="55155-217">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="55155-217">Valid values are:</span></span> 
- <span data-ttu-id="55155-218">Basic</span><span class="sxs-lookup"><span data-stu-id="55155-218">Basic</span></span>
- <span data-ttu-id="55155-219">Oficial</span><span class="sxs-lookup"><span data-stu-id="55155-219">Standard</span></span>
- <span data-ttu-id="55155-220">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="55155-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="55155-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="55155-221">-StaticIP</span></span>
<span data-ttu-id="55155-222">Especifica um endereço IP exclusivo na sub-rede para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="55155-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="55155-223">Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="55155-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="55155-224">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="55155-224">-SubnetId</span></span>
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

### <span data-ttu-id="55155-225">-Marca</span><span class="sxs-lookup"><span data-stu-id="55155-225">-Tag</span></span>
<span data-ttu-id="55155-226">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="55155-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="55155-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="55155-227">-TenantSettings</span></span>
<span data-ttu-id="55155-228">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="55155-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="55155-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="55155-229">-Zone</span></span>
<span data-ttu-id="55155-230">Lista de zonas.</span><span class="sxs-lookup"><span data-stu-id="55155-230">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55155-231">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55155-231">-Confirm</span></span>
<span data-ttu-id="55155-232">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55155-232">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55155-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55155-233">-WhatIf</span></span>
<span data-ttu-id="55155-234">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55155-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55155-235">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55155-235">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55155-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55155-236">CommonParameters</span></span>
<span data-ttu-id="55155-237">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55155-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55155-238">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55155-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55155-239">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55155-239">INPUTS</span></span>

### <span data-ttu-id="55155-240">System. String</span><span class="sxs-lookup"><span data-stu-id="55155-240">System.String</span></span>

### <span data-ttu-id="55155-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55155-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="55155-242">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="55155-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="55155-243">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="55155-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="55155-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="55155-244">System.String[]</span></span>

## <span data-ttu-id="55155-245">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55155-245">OUTPUTS</span></span>

### <span data-ttu-id="55155-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="55155-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="55155-247">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55155-247">NOTES</span></span>

## <span data-ttu-id="55155-248">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55155-248">RELATED LINKS</span></span>

[<span data-ttu-id="55155-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="55155-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="55155-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="55155-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="55155-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="55155-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


