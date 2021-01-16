---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258788"
---
# <span data-ttu-id="bb43e-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb43e-101">New-AzRedisCache</span></span>

## <span data-ttu-id="bb43e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb43e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb43e-103">Cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="bb43e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb43e-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb43e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb43e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb43e-106">O cmdlet **New-AzRedisCache** cria um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="bb43e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb43e-107">EXAMPLES</span></span>

### <span data-ttu-id="bb43e-108">Exemplo 1: criar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="bb43e-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="bb43e-109">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="bb43e-110">Exemplo 2: criar um cache de Redis de SKU padrão</span><span class="sxs-lookup"><span data-stu-id="bb43e-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="bb43e-111">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="bb43e-112">OS</span><span class="sxs-lookup"><span data-stu-id="bb43e-112">PARAMETERS</span></span>

### <span data-ttu-id="bb43e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb43e-113">-DefaultProfile</span></span>
<span data-ttu-id="bb43e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb43e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb43e-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="bb43e-115">-EnableNonSslPort</span></span>
<span data-ttu-id="bb43e-116">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bb43e-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="bb43e-117">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="bb43e-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="bb43e-118">-Local</span><span class="sxs-lookup"><span data-stu-id="bb43e-118">-Location</span></span>
<span data-ttu-id="bb43e-119">Especifica o local no qual criar um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="bb43e-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bb43e-120">Valid values are:</span></span> 
- <span data-ttu-id="bb43e-121">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="bb43e-121">North Central US</span></span>
- <span data-ttu-id="bb43e-122">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="bb43e-122">South Central US</span></span>
- <span data-ttu-id="bb43e-123">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="bb43e-123">Central US</span></span>
- <span data-ttu-id="bb43e-124">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="bb43e-124">West Europe</span></span>
- <span data-ttu-id="bb43e-125">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="bb43e-125">North Europe</span></span>
- <span data-ttu-id="bb43e-126">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="bb43e-126">West US</span></span>
- <span data-ttu-id="bb43e-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="bb43e-127">East US</span></span>
- <span data-ttu-id="bb43e-128">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="bb43e-128">East US 2</span></span>
- <span data-ttu-id="bb43e-129">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="bb43e-129">Japan East</span></span>
- <span data-ttu-id="bb43e-130">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="bb43e-130">Japan West</span></span>
- <span data-ttu-id="bb43e-131">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="bb43e-131">Brazil South</span></span>
- <span data-ttu-id="bb43e-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="bb43e-132">Southeast Asia</span></span>
- <span data-ttu-id="bb43e-133">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="bb43e-133">East Asia</span></span>
- <span data-ttu-id="bb43e-134">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="bb43e-134">Australia East</span></span>
- <span data-ttu-id="bb43e-135">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="bb43e-135">Australia Southeast</span></span>

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

### <span data-ttu-id="bb43e-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="bb43e-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="bb43e-137">Especifique a versão de TLS exigida pelos clientes para se conectar ao cache.</span><span class="sxs-lookup"><span data-stu-id="bb43e-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="bb43e-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb43e-138">-Name</span></span>
<span data-ttu-id="bb43e-139">Especifica o nome do cache de Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="bb43e-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="bb43e-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb43e-140">-RedisConfiguration</span></span>
<span data-ttu-id="bb43e-141">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="bb43e-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bb43e-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb43e-143">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="bb43e-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="bb43e-144">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bb43e-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="bb43e-145">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-145">Premium tier only.</span></span>
- <span data-ttu-id="bb43e-146">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb43e-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="bb43e-147">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="bb43e-148">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-148">Premium tier only.</span></span>
- <span data-ttu-id="bb43e-149">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="bb43e-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="bb43e-150">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="bb43e-151">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-151">Premium tier only.</span></span> 
- <span data-ttu-id="bb43e-152">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="bb43e-152">maxmemory-reserved.</span></span>
<span data-ttu-id="bb43e-153">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="bb43e-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="bb43e-154">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="bb43e-155">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="bb43e-155">maxmemory-policy.</span></span>
<span data-ttu-id="bb43e-156">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="bb43e-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="bb43e-157">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="bb43e-157">All pricing tiers.</span></span> 
- <span data-ttu-id="bb43e-158">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="bb43e-158">notify-keyspace-events.</span></span>
<span data-ttu-id="bb43e-159">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="bb43e-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="bb43e-160">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="bb43e-161">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="bb43e-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="bb43e-162">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="bb43e-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="bb43e-163">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="bb43e-164">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="bb43e-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="bb43e-165">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="bb43e-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="bb43e-166">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="bb43e-167">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="bb43e-167">set-max-intset-entries.</span></span>
<span data-ttu-id="bb43e-168">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="bb43e-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="bb43e-169">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="bb43e-170">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="bb43e-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="bb43e-171">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="bb43e-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="bb43e-172">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="bb43e-173">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="bb43e-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="bb43e-174">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="bb43e-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="bb43e-175">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="bb43e-176">bancos.</span><span class="sxs-lookup"><span data-stu-id="bb43e-176">databases.</span></span>
<span data-ttu-id="bb43e-177">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="bb43e-177">Configures the number of databases.</span></span>
<span data-ttu-id="bb43e-178">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="bb43e-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="bb43e-179">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="bb43e-180">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="bb43e-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="bb43e-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb43e-181">-ResourceGroupName</span></span>
<span data-ttu-id="bb43e-182">Especifica o nome do grupo de recursos no qual criar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="bb43e-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="bb43e-183">-ShardCount</span></span>
<span data-ttu-id="bb43e-184">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="bb43e-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="bb43e-185">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bb43e-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb43e-186">um</span><span class="sxs-lookup"><span data-stu-id="bb43e-186">1</span></span>
- <span data-ttu-id="bb43e-187">2</span><span class="sxs-lookup"><span data-stu-id="bb43e-187">2</span></span>
- <span data-ttu-id="bb43e-188">3D</span><span class="sxs-lookup"><span data-stu-id="bb43e-188">3</span></span>
- <span data-ttu-id="bb43e-189">4</span><span class="sxs-lookup"><span data-stu-id="bb43e-189">4</span></span>
- <span data-ttu-id="bb43e-190">5</span><span class="sxs-lookup"><span data-stu-id="bb43e-190">5</span></span>
- <span data-ttu-id="bb43e-191">5</span><span class="sxs-lookup"><span data-stu-id="bb43e-191">6</span></span>
- <span data-ttu-id="bb43e-192">7</span><span class="sxs-lookup"><span data-stu-id="bb43e-192">7</span></span>
- <span data-ttu-id="bb43e-193">08</span><span class="sxs-lookup"><span data-stu-id="bb43e-193">8</span></span>
- <span data-ttu-id="bb43e-194">222</span><span class="sxs-lookup"><span data-stu-id="bb43e-194">9</span></span> 
- <span data-ttu-id="bb43e-195">254</span><span class="sxs-lookup"><span data-stu-id="bb43e-195">10</span></span>

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

### <span data-ttu-id="bb43e-196">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="bb43e-196">-Size</span></span>
<span data-ttu-id="bb43e-197">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="bb43e-198">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bb43e-198">Valid values are:</span></span> 
- <span data-ttu-id="bb43e-199">P1</span><span class="sxs-lookup"><span data-stu-id="bb43e-199">P1</span></span>
- <span data-ttu-id="bb43e-200">P2</span><span class="sxs-lookup"><span data-stu-id="bb43e-200">P2</span></span>
- <span data-ttu-id="bb43e-201">P3</span><span class="sxs-lookup"><span data-stu-id="bb43e-201">P3</span></span>
- <span data-ttu-id="bb43e-202">P4</span><span class="sxs-lookup"><span data-stu-id="bb43e-202">P4</span></span>
- <span data-ttu-id="bb43e-203">P5</span><span class="sxs-lookup"><span data-stu-id="bb43e-203">P5</span></span>
- <span data-ttu-id="bb43e-204">C0</span><span class="sxs-lookup"><span data-stu-id="bb43e-204">C0</span></span>
- <span data-ttu-id="bb43e-205">C1</span><span class="sxs-lookup"><span data-stu-id="bb43e-205">C1</span></span>
- <span data-ttu-id="bb43e-206">C2</span><span class="sxs-lookup"><span data-stu-id="bb43e-206">C2</span></span>
- <span data-ttu-id="bb43e-207">C3</span><span class="sxs-lookup"><span data-stu-id="bb43e-207">C3</span></span>
- <span data-ttu-id="bb43e-208">C4</span><span class="sxs-lookup"><span data-stu-id="bb43e-208">C4</span></span>
- <span data-ttu-id="bb43e-209">C5</span><span class="sxs-lookup"><span data-stu-id="bb43e-209">C5</span></span>
- <span data-ttu-id="bb43e-210">C6</span><span class="sxs-lookup"><span data-stu-id="bb43e-210">C6</span></span>
- <span data-ttu-id="bb43e-211">250MB</span><span class="sxs-lookup"><span data-stu-id="bb43e-211">250MB</span></span>
- <span data-ttu-id="bb43e-212">1 GB</span><span class="sxs-lookup"><span data-stu-id="bb43e-212">1GB</span></span>
- <span data-ttu-id="bb43e-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="bb43e-213">2.5GB</span></span>
- <span data-ttu-id="bb43e-214">6GB</span><span class="sxs-lookup"><span data-stu-id="bb43e-214">6GB</span></span>
- <span data-ttu-id="bb43e-215">13GB</span><span class="sxs-lookup"><span data-stu-id="bb43e-215">13GB</span></span>
- <span data-ttu-id="bb43e-216">26GB</span><span class="sxs-lookup"><span data-stu-id="bb43e-216">26GB</span></span>
- <span data-ttu-id="bb43e-217">53GB o valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="bb43e-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="bb43e-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="bb43e-218">-Sku</span></span>
<span data-ttu-id="bb43e-219">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="bb43e-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="bb43e-220">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bb43e-220">Valid values are:</span></span> 
- <span data-ttu-id="bb43e-221">Basic</span><span class="sxs-lookup"><span data-stu-id="bb43e-221">Basic</span></span>
- <span data-ttu-id="bb43e-222">Oficial</span><span class="sxs-lookup"><span data-stu-id="bb43e-222">Standard</span></span>
- <span data-ttu-id="bb43e-223">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="bb43e-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="bb43e-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="bb43e-224">-StaticIP</span></span>
<span data-ttu-id="bb43e-225">Especifica um endereço IP exclusivo na sub-rede para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="bb43e-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="bb43e-226">Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="bb43e-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="bb43e-227">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="bb43e-227">-SubnetId</span></span>
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

### <span data-ttu-id="bb43e-228">-Marca</span><span class="sxs-lookup"><span data-stu-id="bb43e-228">-Tag</span></span>
<span data-ttu-id="bb43e-229">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="bb43e-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="bb43e-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="bb43e-230">-TenantSettings</span></span>
<span data-ttu-id="bb43e-231">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="bb43e-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="bb43e-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="bb43e-232">-Zone</span></span>
<span data-ttu-id="bb43e-233">Lista de zonas.</span><span class="sxs-lookup"><span data-stu-id="bb43e-233">List of zones.</span></span>

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

### <span data-ttu-id="bb43e-234">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb43e-234">-Confirm</span></span>
<span data-ttu-id="bb43e-235">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb43e-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb43e-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb43e-236">-WhatIf</span></span>
<span data-ttu-id="bb43e-237">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb43e-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb43e-238">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb43e-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb43e-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb43e-239">CommonParameters</span></span>
<span data-ttu-id="bb43e-240">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb43e-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb43e-241">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb43e-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb43e-242">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb43e-242">INPUTS</span></span>

### <span data-ttu-id="bb43e-243">System. String</span><span class="sxs-lookup"><span data-stu-id="bb43e-243">System.String</span></span>

### <span data-ttu-id="bb43e-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bb43e-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bb43e-245">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb43e-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bb43e-246">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb43e-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bb43e-247">System. String []</span><span class="sxs-lookup"><span data-stu-id="bb43e-247">System.String[]</span></span>

## <span data-ttu-id="bb43e-248">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb43e-248">OUTPUTS</span></span>

### <span data-ttu-id="bb43e-249">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bb43e-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="bb43e-250">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb43e-250">NOTES</span></span>

## <span data-ttu-id="bb43e-251">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb43e-251">RELATED LINKS</span></span>

[<span data-ttu-id="bb43e-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb43e-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="bb43e-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb43e-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="bb43e-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb43e-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


