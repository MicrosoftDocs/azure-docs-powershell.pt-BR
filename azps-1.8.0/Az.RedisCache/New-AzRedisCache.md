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
ms.locfileid: "93599547"
---
# <span data-ttu-id="19f5a-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19f5a-101">New-AzRedisCache</span></span>

## <span data-ttu-id="19f5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="19f5a-103">Cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="19f5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19f5a-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19f5a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="19f5a-106">O cmdlet **New-AzRedisCache** cria um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="19f5a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19f5a-107">EXAMPLES</span></span>

### <span data-ttu-id="19f5a-108">Exemplo 1: criar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="19f5a-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="19f5a-109">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="19f5a-110">Exemplo 2: criar um cache de Redis de SKU padrão</span><span class="sxs-lookup"><span data-stu-id="19f5a-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="19f5a-111">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="19f5a-112">OS</span><span class="sxs-lookup"><span data-stu-id="19f5a-112">PARAMETERS</span></span>

### <span data-ttu-id="19f5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f5a-113">-DefaultProfile</span></span>
<span data-ttu-id="19f5a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19f5a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19f5a-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="19f5a-115">-EnableNonSslPort</span></span>
<span data-ttu-id="19f5a-116">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="19f5a-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="19f5a-117">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="19f5a-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="19f5a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="19f5a-118">-Location</span></span>
<span data-ttu-id="19f5a-119">Especifica o local no qual criar um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="19f5a-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="19f5a-120">Valid values are:</span></span> 
- <span data-ttu-id="19f5a-121">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="19f5a-121">North Central US</span></span>
- <span data-ttu-id="19f5a-122">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="19f5a-122">South Central US</span></span>
- <span data-ttu-id="19f5a-123">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="19f5a-123">Central US</span></span>
- <span data-ttu-id="19f5a-124">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="19f5a-124">West Europe</span></span>
- <span data-ttu-id="19f5a-125">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="19f5a-125">North Europe</span></span>
- <span data-ttu-id="19f5a-126">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="19f5a-126">West US</span></span>
- <span data-ttu-id="19f5a-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="19f5a-127">East US</span></span>
- <span data-ttu-id="19f5a-128">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="19f5a-128">East US 2</span></span>
- <span data-ttu-id="19f5a-129">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="19f5a-129">Japan East</span></span>
- <span data-ttu-id="19f5a-130">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="19f5a-130">Japan West</span></span>
- <span data-ttu-id="19f5a-131">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="19f5a-131">Brazil South</span></span>
- <span data-ttu-id="19f5a-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="19f5a-132">Southeast Asia</span></span>
- <span data-ttu-id="19f5a-133">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="19f5a-133">East Asia</span></span>
- <span data-ttu-id="19f5a-134">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="19f5a-134">Australia East</span></span>
- <span data-ttu-id="19f5a-135">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="19f5a-135">Australia Southeast</span></span>

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

### <span data-ttu-id="19f5a-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="19f5a-136">-Name</span></span>
<span data-ttu-id="19f5a-137">Especifica o nome do cache de Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="19f5a-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="19f5a-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f5a-138">-RedisConfiguration</span></span>
<span data-ttu-id="19f5a-139">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="19f5a-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="19f5a-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19f5a-141">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="19f5a-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="19f5a-142">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="19f5a-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="19f5a-143">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-143">Premium tier only.</span></span>
- <span data-ttu-id="19f5a-144">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="19f5a-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="19f5a-145">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="19f5a-146">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-146">Premium tier only.</span></span>
- <span data-ttu-id="19f5a-147">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="19f5a-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="19f5a-148">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="19f5a-149">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-149">Premium tier only.</span></span> 
- <span data-ttu-id="19f5a-150">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="19f5a-150">maxmemory-reserved.</span></span>
<span data-ttu-id="19f5a-151">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="19f5a-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="19f5a-152">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19f5a-153">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="19f5a-153">maxmemory-policy.</span></span>
<span data-ttu-id="19f5a-154">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="19f5a-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="19f5a-155">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="19f5a-155">All pricing tiers.</span></span> 
- <span data-ttu-id="19f5a-156">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="19f5a-156">notify-keyspace-events.</span></span>
<span data-ttu-id="19f5a-157">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="19f5a-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="19f5a-158">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="19f5a-159">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="19f5a-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="19f5a-160">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="19f5a-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19f5a-161">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19f5a-162">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="19f5a-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="19f5a-163">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="19f5a-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19f5a-164">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19f5a-165">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="19f5a-165">set-max-intset-entries.</span></span>
<span data-ttu-id="19f5a-166">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="19f5a-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19f5a-167">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19f5a-168">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="19f5a-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="19f5a-169">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="19f5a-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19f5a-170">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19f5a-171">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="19f5a-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="19f5a-172">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="19f5a-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="19f5a-173">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="19f5a-174">bancos.</span><span class="sxs-lookup"><span data-stu-id="19f5a-174">databases.</span></span>
<span data-ttu-id="19f5a-175">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="19f5a-175">Configures the number of databases.</span></span>
<span data-ttu-id="19f5a-176">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="19f5a-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="19f5a-177">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="19f5a-178">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="19f5a-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="19f5a-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f5a-179">-ResourceGroupName</span></span>
<span data-ttu-id="19f5a-180">Especifica o nome do grupo de recursos no qual criar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="19f5a-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="19f5a-181">-ShardCount</span></span>
<span data-ttu-id="19f5a-182">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="19f5a-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="19f5a-183">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="19f5a-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19f5a-184">um</span><span class="sxs-lookup"><span data-stu-id="19f5a-184">1</span></span>
- <span data-ttu-id="19f5a-185">2</span><span class="sxs-lookup"><span data-stu-id="19f5a-185">2</span></span>
- <span data-ttu-id="19f5a-186">3D</span><span class="sxs-lookup"><span data-stu-id="19f5a-186">3</span></span>
- <span data-ttu-id="19f5a-187">4</span><span class="sxs-lookup"><span data-stu-id="19f5a-187">4</span></span>
- <span data-ttu-id="19f5a-188">5</span><span class="sxs-lookup"><span data-stu-id="19f5a-188">5</span></span>
- <span data-ttu-id="19f5a-189">5</span><span class="sxs-lookup"><span data-stu-id="19f5a-189">6</span></span>
- <span data-ttu-id="19f5a-190">7</span><span class="sxs-lookup"><span data-stu-id="19f5a-190">7</span></span>
- <span data-ttu-id="19f5a-191">08</span><span class="sxs-lookup"><span data-stu-id="19f5a-191">8</span></span>
- <span data-ttu-id="19f5a-192">222</span><span class="sxs-lookup"><span data-stu-id="19f5a-192">9</span></span> 
- <span data-ttu-id="19f5a-193">254</span><span class="sxs-lookup"><span data-stu-id="19f5a-193">10</span></span>

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

### <span data-ttu-id="19f5a-194">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="19f5a-194">-Size</span></span>
<span data-ttu-id="19f5a-195">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="19f5a-196">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="19f5a-196">Valid values are:</span></span> 
- <span data-ttu-id="19f5a-197">P1</span><span class="sxs-lookup"><span data-stu-id="19f5a-197">P1</span></span>
- <span data-ttu-id="19f5a-198">P2</span><span class="sxs-lookup"><span data-stu-id="19f5a-198">P2</span></span>
- <span data-ttu-id="19f5a-199">P3</span><span class="sxs-lookup"><span data-stu-id="19f5a-199">P3</span></span>
- <span data-ttu-id="19f5a-200">P4</span><span class="sxs-lookup"><span data-stu-id="19f5a-200">P4</span></span>
- <span data-ttu-id="19f5a-201">C0</span><span class="sxs-lookup"><span data-stu-id="19f5a-201">C0</span></span>
- <span data-ttu-id="19f5a-202">C1</span><span class="sxs-lookup"><span data-stu-id="19f5a-202">C1</span></span>
- <span data-ttu-id="19f5a-203">C2</span><span class="sxs-lookup"><span data-stu-id="19f5a-203">C2</span></span>
- <span data-ttu-id="19f5a-204">C3</span><span class="sxs-lookup"><span data-stu-id="19f5a-204">C3</span></span>
- <span data-ttu-id="19f5a-205">C4</span><span class="sxs-lookup"><span data-stu-id="19f5a-205">C4</span></span>
- <span data-ttu-id="19f5a-206">C5</span><span class="sxs-lookup"><span data-stu-id="19f5a-206">C5</span></span>
- <span data-ttu-id="19f5a-207">C6</span><span class="sxs-lookup"><span data-stu-id="19f5a-207">C6</span></span>
- <span data-ttu-id="19f5a-208">250MB</span><span class="sxs-lookup"><span data-stu-id="19f5a-208">250MB</span></span>
- <span data-ttu-id="19f5a-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="19f5a-209">1GB</span></span>
- <span data-ttu-id="19f5a-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="19f5a-210">2.5GB</span></span>
- <span data-ttu-id="19f5a-211">6GB</span><span class="sxs-lookup"><span data-stu-id="19f5a-211">6GB</span></span>
- <span data-ttu-id="19f5a-212">13GB</span><span class="sxs-lookup"><span data-stu-id="19f5a-212">13GB</span></span>
- <span data-ttu-id="19f5a-213">26GB</span><span class="sxs-lookup"><span data-stu-id="19f5a-213">26GB</span></span>
- <span data-ttu-id="19f5a-214">53GB o valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="19f5a-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="19f5a-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="19f5a-215">-Sku</span></span>
<span data-ttu-id="19f5a-216">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="19f5a-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="19f5a-217">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="19f5a-217">Valid values are:</span></span> 
- <span data-ttu-id="19f5a-218">Basic</span><span class="sxs-lookup"><span data-stu-id="19f5a-218">Basic</span></span>
- <span data-ttu-id="19f5a-219">Oficial</span><span class="sxs-lookup"><span data-stu-id="19f5a-219">Standard</span></span>
- <span data-ttu-id="19f5a-220">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="19f5a-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="19f5a-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="19f5a-221">-StaticIP</span></span>
<span data-ttu-id="19f5a-222">Especifica um endereço IP exclusivo na sub-rede para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="19f5a-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="19f5a-223">Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="19f5a-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="19f5a-224">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="19f5a-224">-SubnetId</span></span>
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

### <span data-ttu-id="19f5a-225">-Marca</span><span class="sxs-lookup"><span data-stu-id="19f5a-225">-Tag</span></span>
<span data-ttu-id="19f5a-226">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="19f5a-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="19f5a-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="19f5a-227">-TenantSettings</span></span>
<span data-ttu-id="19f5a-228">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="19f5a-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="19f5a-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="19f5a-229">-Zone</span></span>
<span data-ttu-id="19f5a-230">Lista de zonas.</span><span class="sxs-lookup"><span data-stu-id="19f5a-230">List of zones.</span></span>

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

### <span data-ttu-id="19f5a-231">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19f5a-231">-Confirm</span></span>
<span data-ttu-id="19f5a-232">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19f5a-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f5a-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f5a-233">-WhatIf</span></span>
<span data-ttu-id="19f5a-234">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19f5a-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19f5a-235">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19f5a-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f5a-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f5a-236">CommonParameters</span></span>
<span data-ttu-id="19f5a-237">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f5a-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f5a-238">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f5a-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f5a-239">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19f5a-239">INPUTS</span></span>

### <span data-ttu-id="19f5a-240">System. String</span><span class="sxs-lookup"><span data-stu-id="19f5a-240">System.String</span></span>

### <span data-ttu-id="19f5a-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19f5a-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="19f5a-242">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19f5a-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="19f5a-243">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19f5a-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="19f5a-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="19f5a-244">System.String[]</span></span>

## <span data-ttu-id="19f5a-245">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19f5a-245">OUTPUTS</span></span>

### <span data-ttu-id="19f5a-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="19f5a-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="19f5a-247">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19f5a-247">NOTES</span></span>

## <span data-ttu-id="19f5a-248">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19f5a-248">RELATED LINKS</span></span>

[<span data-ttu-id="19f5a-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19f5a-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="19f5a-250">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19f5a-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="19f5a-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="19f5a-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


