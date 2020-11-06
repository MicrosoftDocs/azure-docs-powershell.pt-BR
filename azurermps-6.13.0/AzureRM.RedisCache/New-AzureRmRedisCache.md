---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 6b2239e09a35ada6b756e58cf2c3a09ed891e730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609383"
---
# <span data-ttu-id="dfa27-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfa27-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="dfa27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfa27-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa27-103">Cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfa27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfa27-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>]
 [-Sku <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfa27-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfa27-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa27-106">O cmdlet **New-AzureRmRedisCache** cria um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="dfa27-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfa27-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa27-108">Exemplo 1: criar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="dfa27-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="dfa27-109">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="dfa27-110">Exemplo 2: criar um cache de Redis de SKU padrão</span><span class="sxs-lookup"><span data-stu-id="dfa27-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="dfa27-111">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="dfa27-112">OS</span><span class="sxs-lookup"><span data-stu-id="dfa27-112">PARAMETERS</span></span>

### <span data-ttu-id="dfa27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa27-113">-DefaultProfile</span></span>
<span data-ttu-id="dfa27-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfa27-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfa27-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="dfa27-115">-EnableNonSslPort</span></span>
<span data-ttu-id="dfa27-116">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dfa27-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="dfa27-117">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="dfa27-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="dfa27-118">-Local</span><span class="sxs-lookup"><span data-stu-id="dfa27-118">-Location</span></span>
<span data-ttu-id="dfa27-119">Especifica o local no qual criar um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="dfa27-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dfa27-120">Valid values are:</span></span> 
- <span data-ttu-id="dfa27-121">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="dfa27-121">North Central US</span></span>
- <span data-ttu-id="dfa27-122">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="dfa27-122">South Central US</span></span>
- <span data-ttu-id="dfa27-123">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="dfa27-123">Central US</span></span>
- <span data-ttu-id="dfa27-124">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="dfa27-124">West Europe</span></span>
- <span data-ttu-id="dfa27-125">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="dfa27-125">North Europe</span></span>
- <span data-ttu-id="dfa27-126">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="dfa27-126">West US</span></span>
- <span data-ttu-id="dfa27-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="dfa27-127">East US</span></span>
- <span data-ttu-id="dfa27-128">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="dfa27-128">East US 2</span></span>
- <span data-ttu-id="dfa27-129">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="dfa27-129">Japan East</span></span>
- <span data-ttu-id="dfa27-130">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="dfa27-130">Japan West</span></span>
- <span data-ttu-id="dfa27-131">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="dfa27-131">Brazil South</span></span>
- <span data-ttu-id="dfa27-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="dfa27-132">Southeast Asia</span></span>
- <span data-ttu-id="dfa27-133">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="dfa27-133">East Asia</span></span>
- <span data-ttu-id="dfa27-134">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="dfa27-134">Australia East</span></span>
- <span data-ttu-id="dfa27-135">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="dfa27-135">Australia Southeast</span></span>

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

### <span data-ttu-id="dfa27-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfa27-136">-Name</span></span>
<span data-ttu-id="dfa27-137">Especifica o nome do cache de Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="dfa27-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="dfa27-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfa27-138">-RedisConfiguration</span></span>
<span data-ttu-id="dfa27-139">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="dfa27-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dfa27-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfa27-141">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="dfa27-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="dfa27-142">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dfa27-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="dfa27-143">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-143">Premium tier only.</span></span>
- <span data-ttu-id="dfa27-144">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dfa27-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="dfa27-145">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="dfa27-146">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-146">Premium tier only.</span></span>
- <span data-ttu-id="dfa27-147">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="dfa27-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="dfa27-148">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="dfa27-149">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-149">Premium tier only.</span></span> 
- <span data-ttu-id="dfa27-150">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="dfa27-150">maxmemory-reserved.</span></span>
<span data-ttu-id="dfa27-151">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="dfa27-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="dfa27-152">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfa27-153">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="dfa27-153">maxmemory-policy.</span></span>
<span data-ttu-id="dfa27-154">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="dfa27-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="dfa27-155">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="dfa27-155">All pricing tiers.</span></span> 
- <span data-ttu-id="dfa27-156">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="dfa27-156">notify-keyspace-events.</span></span>
<span data-ttu-id="dfa27-157">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="dfa27-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="dfa27-158">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="dfa27-159">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="dfa27-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="dfa27-160">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfa27-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfa27-161">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfa27-162">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="dfa27-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="dfa27-163">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfa27-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfa27-164">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfa27-165">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="dfa27-165">set-max-intset-entries.</span></span>
<span data-ttu-id="dfa27-166">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfa27-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfa27-167">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfa27-168">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="dfa27-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="dfa27-169">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfa27-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfa27-170">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfa27-171">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="dfa27-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="dfa27-172">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="dfa27-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="dfa27-173">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="dfa27-174">bancos.</span><span class="sxs-lookup"><span data-stu-id="dfa27-174">databases.</span></span>
<span data-ttu-id="dfa27-175">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="dfa27-175">Configures the number of databases.</span></span>
<span data-ttu-id="dfa27-176">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="dfa27-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="dfa27-177">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="dfa27-178">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="dfa27-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="dfa27-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa27-179">-ResourceGroupName</span></span>
<span data-ttu-id="dfa27-180">Especifica o nome do grupo de recursos no qual criar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="dfa27-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="dfa27-181">-ShardCount</span></span>
<span data-ttu-id="dfa27-182">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="dfa27-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="dfa27-183">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dfa27-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfa27-184">um</span><span class="sxs-lookup"><span data-stu-id="dfa27-184">1</span></span>
- <span data-ttu-id="dfa27-185">2</span><span class="sxs-lookup"><span data-stu-id="dfa27-185">2</span></span>
- <span data-ttu-id="dfa27-186">3D</span><span class="sxs-lookup"><span data-stu-id="dfa27-186">3</span></span>
- <span data-ttu-id="dfa27-187">4</span><span class="sxs-lookup"><span data-stu-id="dfa27-187">4</span></span>
- <span data-ttu-id="dfa27-188">5</span><span class="sxs-lookup"><span data-stu-id="dfa27-188">5</span></span>
- <span data-ttu-id="dfa27-189">5</span><span class="sxs-lookup"><span data-stu-id="dfa27-189">6</span></span>
- <span data-ttu-id="dfa27-190">7</span><span class="sxs-lookup"><span data-stu-id="dfa27-190">7</span></span>
- <span data-ttu-id="dfa27-191">08</span><span class="sxs-lookup"><span data-stu-id="dfa27-191">8</span></span>
- <span data-ttu-id="dfa27-192">222</span><span class="sxs-lookup"><span data-stu-id="dfa27-192">9</span></span> 
- <span data-ttu-id="dfa27-193">254</span><span class="sxs-lookup"><span data-stu-id="dfa27-193">10</span></span>

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

### <span data-ttu-id="dfa27-194">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="dfa27-194">-Size</span></span>
<span data-ttu-id="dfa27-195">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="dfa27-196">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dfa27-196">Valid values are:</span></span> 
- <span data-ttu-id="dfa27-197">P1</span><span class="sxs-lookup"><span data-stu-id="dfa27-197">P1</span></span>
- <span data-ttu-id="dfa27-198">P2</span><span class="sxs-lookup"><span data-stu-id="dfa27-198">P2</span></span>
- <span data-ttu-id="dfa27-199">P3</span><span class="sxs-lookup"><span data-stu-id="dfa27-199">P3</span></span>
- <span data-ttu-id="dfa27-200">P4</span><span class="sxs-lookup"><span data-stu-id="dfa27-200">P4</span></span>
- <span data-ttu-id="dfa27-201">C0</span><span class="sxs-lookup"><span data-stu-id="dfa27-201">C0</span></span>
- <span data-ttu-id="dfa27-202">C1</span><span class="sxs-lookup"><span data-stu-id="dfa27-202">C1</span></span>
- <span data-ttu-id="dfa27-203">C2</span><span class="sxs-lookup"><span data-stu-id="dfa27-203">C2</span></span>
- <span data-ttu-id="dfa27-204">C3</span><span class="sxs-lookup"><span data-stu-id="dfa27-204">C3</span></span>
- <span data-ttu-id="dfa27-205">C4</span><span class="sxs-lookup"><span data-stu-id="dfa27-205">C4</span></span>
- <span data-ttu-id="dfa27-206">C5</span><span class="sxs-lookup"><span data-stu-id="dfa27-206">C5</span></span>
- <span data-ttu-id="dfa27-207">C6</span><span class="sxs-lookup"><span data-stu-id="dfa27-207">C6</span></span>
- <span data-ttu-id="dfa27-208">250MB</span><span class="sxs-lookup"><span data-stu-id="dfa27-208">250MB</span></span>
- <span data-ttu-id="dfa27-209">1 GB</span><span class="sxs-lookup"><span data-stu-id="dfa27-209">1GB</span></span>
- <span data-ttu-id="dfa27-210">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="dfa27-210">2.5GB</span></span>
- <span data-ttu-id="dfa27-211">6GB</span><span class="sxs-lookup"><span data-stu-id="dfa27-211">6GB</span></span>
- <span data-ttu-id="dfa27-212">13GB</span><span class="sxs-lookup"><span data-stu-id="dfa27-212">13GB</span></span>
- <span data-ttu-id="dfa27-213">26GB</span><span class="sxs-lookup"><span data-stu-id="dfa27-213">26GB</span></span>
- <span data-ttu-id="dfa27-214">53GB o valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="dfa27-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="dfa27-215">-SKU</span><span class="sxs-lookup"><span data-stu-id="dfa27-215">-Sku</span></span>
<span data-ttu-id="dfa27-216">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="dfa27-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="dfa27-217">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dfa27-217">Valid values are:</span></span> 
- <span data-ttu-id="dfa27-218">Basic</span><span class="sxs-lookup"><span data-stu-id="dfa27-218">Basic</span></span>
- <span data-ttu-id="dfa27-219">Oficial</span><span class="sxs-lookup"><span data-stu-id="dfa27-219">Standard</span></span>
- <span data-ttu-id="dfa27-220">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="dfa27-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="dfa27-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="dfa27-221">-StaticIP</span></span>
<span data-ttu-id="dfa27-222">Especifica um endereço IP exclusivo na sub-rede para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="dfa27-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="dfa27-223">Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="dfa27-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="dfa27-224">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="dfa27-224">-SubnetId</span></span>
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

### <span data-ttu-id="dfa27-225">-Marca</span><span class="sxs-lookup"><span data-stu-id="dfa27-225">-Tag</span></span>
<span data-ttu-id="dfa27-226">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="dfa27-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="dfa27-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="dfa27-227">-TenantSettings</span></span>
<span data-ttu-id="dfa27-228">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="dfa27-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="dfa27-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="dfa27-229">-Zone</span></span>
<span data-ttu-id="dfa27-230">Lista de zonas.</span><span class="sxs-lookup"><span data-stu-id="dfa27-230">List of zones.</span></span>

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

### <span data-ttu-id="dfa27-231">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfa27-231">-Confirm</span></span>
<span data-ttu-id="dfa27-232">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfa27-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfa27-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfa27-233">-WhatIf</span></span>
<span data-ttu-id="dfa27-234">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfa27-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfa27-235">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfa27-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfa27-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa27-236">CommonParameters</span></span>
<span data-ttu-id="dfa27-237">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa27-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa27-238">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa27-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa27-239">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfa27-239">INPUTS</span></span>

### <span data-ttu-id="dfa27-240">System. String</span><span class="sxs-lookup"><span data-stu-id="dfa27-240">System.String</span></span>

### <span data-ttu-id="dfa27-241">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dfa27-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dfa27-242">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dfa27-242">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dfa27-243">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="dfa27-243">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="dfa27-244">System. String []</span><span class="sxs-lookup"><span data-stu-id="dfa27-244">System.String[]</span></span>

## <span data-ttu-id="dfa27-245">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfa27-245">OUTPUTS</span></span>

### <span data-ttu-id="dfa27-246">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dfa27-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="dfa27-247">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfa27-247">NOTES</span></span>

## <span data-ttu-id="dfa27-248">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfa27-248">RELATED LINKS</span></span>

[<span data-ttu-id="dfa27-249">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfa27-249">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="dfa27-250">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfa27-250">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="dfa27-251">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="dfa27-251">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


