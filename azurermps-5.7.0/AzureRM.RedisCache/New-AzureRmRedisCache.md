---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428817"
---
# <span data-ttu-id="b43d2-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b43d2-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="b43d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b43d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b43d2-103">Cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b43d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b43d2-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b43d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b43d2-105">DESCRIPTION</span></span>
<span data-ttu-id="b43d2-106">O cmdlet **New-AzureRmRedisCache** cria um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="b43d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b43d2-107">EXAMPLES</span></span>

### <span data-ttu-id="b43d2-108">Exemplo 1: criar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="b43d2-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="b43d2-109">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="b43d2-110">Exemplo 2: criar um cache de Redis de SKU padrão</span><span class="sxs-lookup"><span data-stu-id="b43d2-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="b43d2-111">Esse comando cria um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="b43d2-112">OS</span><span class="sxs-lookup"><span data-stu-id="b43d2-112">PARAMETERS</span></span>

### <span data-ttu-id="b43d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43d2-113">-DefaultProfile</span></span>
<span data-ttu-id="b43d2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b43d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b43d2-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="b43d2-115">-EnableNonSslPort</span></span>
<span data-ttu-id="b43d2-116">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b43d2-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="b43d2-117">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="b43d2-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="b43d2-118">-Local</span><span class="sxs-lookup"><span data-stu-id="b43d2-118">-Location</span></span>
<span data-ttu-id="b43d2-119">Especifica o local no qual criar um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="b43d2-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b43d2-120">Valid values are:</span></span> 

- <span data-ttu-id="b43d2-121">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="b43d2-121">North Central US</span></span>
- <span data-ttu-id="b43d2-122">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="b43d2-122">South Central US</span></span>
- <span data-ttu-id="b43d2-123">Centro dos EUA</span><span class="sxs-lookup"><span data-stu-id="b43d2-123">Central US</span></span>
- <span data-ttu-id="b43d2-124">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="b43d2-124">West Europe</span></span>
- <span data-ttu-id="b43d2-125">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="b43d2-125">North Europe</span></span>
- <span data-ttu-id="b43d2-126">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="b43d2-126">West US</span></span>
- <span data-ttu-id="b43d2-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="b43d2-127">East US</span></span>
- <span data-ttu-id="b43d2-128">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="b43d2-128">East US 2</span></span>
- <span data-ttu-id="b43d2-129">Japão oriental</span><span class="sxs-lookup"><span data-stu-id="b43d2-129">Japan East</span></span>
- <span data-ttu-id="b43d2-130">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="b43d2-130">Japan West</span></span>
- <span data-ttu-id="b43d2-131">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="b43d2-131">Brazil South</span></span>
- <span data-ttu-id="b43d2-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="b43d2-132">Southeast Asia</span></span>
- <span data-ttu-id="b43d2-133">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="b43d2-133">East Asia</span></span>
- <span data-ttu-id="b43d2-134">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="b43d2-134">Australia East</span></span>
- <span data-ttu-id="b43d2-135">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="b43d2-135">Australia Southeast</span></span>

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

### <span data-ttu-id="b43d2-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="b43d2-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="b43d2-137">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="b43d2-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="b43d2-138">Use o parâmetro *RedisConfiguration* para definir MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="b43d2-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="b43d2-139">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b43d2-139">For example:</span></span> 

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

### <span data-ttu-id="b43d2-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="b43d2-140">-Name</span></span>
<span data-ttu-id="b43d2-141">Especifica o nome do cache de Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b43d2-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="b43d2-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="b43d2-142">-RedisConfiguration</span></span>
<span data-ttu-id="b43d2-143">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="b43d2-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b43d2-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b43d2-145">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="b43d2-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="b43d2-146">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b43d2-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="b43d2-147">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-147">Premium tier only.</span></span>
- <span data-ttu-id="b43d2-148">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b43d2-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="b43d2-149">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="b43d2-150">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-150">Premium tier only.</span></span>
- <span data-ttu-id="b43d2-151">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="b43d2-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="b43d2-152">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="b43d2-153">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-153">Premium tier only.</span></span> 
- <span data-ttu-id="b43d2-154">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="b43d2-154">maxmemory-reserved.</span></span>
<span data-ttu-id="b43d2-155">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="b43d2-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="b43d2-156">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b43d2-157">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="b43d2-157">maxmemory-policy.</span></span>
<span data-ttu-id="b43d2-158">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="b43d2-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="b43d2-159">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="b43d2-159">All pricing tiers.</span></span> 
- <span data-ttu-id="b43d2-160">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="b43d2-160">notify-keyspace-events.</span></span>
<span data-ttu-id="b43d2-161">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="b43d2-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="b43d2-162">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="b43d2-163">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="b43d2-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="b43d2-164">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="b43d2-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b43d2-165">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b43d2-166">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="b43d2-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="b43d2-167">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="b43d2-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b43d2-168">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b43d2-169">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="b43d2-169">set-max-intset-entries.</span></span>
<span data-ttu-id="b43d2-170">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="b43d2-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b43d2-171">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b43d2-172">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="b43d2-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="b43d2-173">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="b43d2-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b43d2-174">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b43d2-175">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="b43d2-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="b43d2-176">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="b43d2-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b43d2-177">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b43d2-178">bancos.</span><span class="sxs-lookup"><span data-stu-id="b43d2-178">databases.</span></span>
<span data-ttu-id="b43d2-179">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="b43d2-179">Configures the number of databases.</span></span>
<span data-ttu-id="b43d2-180">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="b43d2-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="b43d2-181">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="b43d2-182">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="b43d2-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="b43d2-183">-RedisVersion</span><span class="sxs-lookup"><span data-stu-id="b43d2-183">-RedisVersion</span></span>
<span data-ttu-id="b43d2-184">Esse parâmetro é preterido e será removido de versões futuras.</span><span class="sxs-lookup"><span data-stu-id="b43d2-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="b43d2-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43d2-185">-ResourceGroupName</span></span>
<span data-ttu-id="b43d2-186">Especifica o nome do grupo de recursos no qual criar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="b43d2-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="b43d2-187">-ShardCount</span></span>
<span data-ttu-id="b43d2-188">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="b43d2-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="b43d2-189">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b43d2-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b43d2-190">um</span><span class="sxs-lookup"><span data-stu-id="b43d2-190">1</span></span>
- <span data-ttu-id="b43d2-191">2</span><span class="sxs-lookup"><span data-stu-id="b43d2-191">2</span></span>
- <span data-ttu-id="b43d2-192">3D</span><span class="sxs-lookup"><span data-stu-id="b43d2-192">3</span></span>
- <span data-ttu-id="b43d2-193">4</span><span class="sxs-lookup"><span data-stu-id="b43d2-193">4</span></span>
- <span data-ttu-id="b43d2-194">5</span><span class="sxs-lookup"><span data-stu-id="b43d2-194">5</span></span>
- <span data-ttu-id="b43d2-195">5</span><span class="sxs-lookup"><span data-stu-id="b43d2-195">6</span></span>
- <span data-ttu-id="b43d2-196">7</span><span class="sxs-lookup"><span data-stu-id="b43d2-196">7</span></span>
- <span data-ttu-id="b43d2-197">08</span><span class="sxs-lookup"><span data-stu-id="b43d2-197">8</span></span>
- <span data-ttu-id="b43d2-198">222</span><span class="sxs-lookup"><span data-stu-id="b43d2-198">9</span></span> 
- <span data-ttu-id="b43d2-199">254</span><span class="sxs-lookup"><span data-stu-id="b43d2-199">10</span></span>

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

### <span data-ttu-id="b43d2-200">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="b43d2-200">-Size</span></span>
<span data-ttu-id="b43d2-201">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="b43d2-202">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b43d2-202">Valid values are:</span></span> 

- <span data-ttu-id="b43d2-203">P1</span><span class="sxs-lookup"><span data-stu-id="b43d2-203">P1</span></span>
- <span data-ttu-id="b43d2-204">P2</span><span class="sxs-lookup"><span data-stu-id="b43d2-204">P2</span></span>
- <span data-ttu-id="b43d2-205">P3</span><span class="sxs-lookup"><span data-stu-id="b43d2-205">P3</span></span>
- <span data-ttu-id="b43d2-206">P4</span><span class="sxs-lookup"><span data-stu-id="b43d2-206">P4</span></span>
- <span data-ttu-id="b43d2-207">C0</span><span class="sxs-lookup"><span data-stu-id="b43d2-207">C0</span></span>
- <span data-ttu-id="b43d2-208">C1</span><span class="sxs-lookup"><span data-stu-id="b43d2-208">C1</span></span>
- <span data-ttu-id="b43d2-209">C2</span><span class="sxs-lookup"><span data-stu-id="b43d2-209">C2</span></span>
- <span data-ttu-id="b43d2-210">C3</span><span class="sxs-lookup"><span data-stu-id="b43d2-210">C3</span></span>
- <span data-ttu-id="b43d2-211">C4</span><span class="sxs-lookup"><span data-stu-id="b43d2-211">C4</span></span>
- <span data-ttu-id="b43d2-212">C5</span><span class="sxs-lookup"><span data-stu-id="b43d2-212">C5</span></span>
- <span data-ttu-id="b43d2-213">C6</span><span class="sxs-lookup"><span data-stu-id="b43d2-213">C6</span></span>
- <span data-ttu-id="b43d2-214">250MB</span><span class="sxs-lookup"><span data-stu-id="b43d2-214">250MB</span></span>
- <span data-ttu-id="b43d2-215">1 GB</span><span class="sxs-lookup"><span data-stu-id="b43d2-215">1GB</span></span>
- <span data-ttu-id="b43d2-216">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="b43d2-216">2.5GB</span></span>
- <span data-ttu-id="b43d2-217">6GB</span><span class="sxs-lookup"><span data-stu-id="b43d2-217">6GB</span></span>
- <span data-ttu-id="b43d2-218">13GB</span><span class="sxs-lookup"><span data-stu-id="b43d2-218">13GB</span></span>
- <span data-ttu-id="b43d2-219">26GB</span><span class="sxs-lookup"><span data-stu-id="b43d2-219">26GB</span></span>
- <span data-ttu-id="b43d2-220">53GB</span><span class="sxs-lookup"><span data-stu-id="b43d2-220">53GB</span></span>

<span data-ttu-id="b43d2-221">O valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="b43d2-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="b43d2-222">-SKU</span><span class="sxs-lookup"><span data-stu-id="b43d2-222">-Sku</span></span>
<span data-ttu-id="b43d2-223">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b43d2-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="b43d2-224">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="b43d2-224">Valid values are:</span></span> 

- <span data-ttu-id="b43d2-225">Basic</span><span class="sxs-lookup"><span data-stu-id="b43d2-225">Basic</span></span>
- <span data-ttu-id="b43d2-226">Oficial</span><span class="sxs-lookup"><span data-stu-id="b43d2-226">Standard</span></span>
- <span data-ttu-id="b43d2-227">Gratifica</span><span class="sxs-lookup"><span data-stu-id="b43d2-227">Premium</span></span>

<span data-ttu-id="b43d2-228">O valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="b43d2-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="b43d2-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="b43d2-229">-StaticIP</span></span>
<span data-ttu-id="b43d2-230">Especifica um endereço IP exclusivo na sub-rede para o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="b43d2-231">Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b43d2-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="b43d2-232">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b43d2-232">-Subnet</span></span>
<span data-ttu-id="b43d2-233">Especifica o nome da sub-rede na qual implantar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="b43d2-234">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="b43d2-234">-SubnetId</span></span>
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

### <span data-ttu-id="b43d2-235">-Marca</span><span class="sxs-lookup"><span data-stu-id="b43d2-235">-Tag</span></span>
<span data-ttu-id="b43d2-236">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="b43d2-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="b43d2-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="b43d2-237">-TenantSettings</span></span>
<span data-ttu-id="b43d2-238">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="b43d2-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="b43d2-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b43d2-239">-VirtualNetwork</span></span>
<span data-ttu-id="b43d2-240">Especifica a ID do recurso da rede virtual na qual você deseja implantar o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="b43d2-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="b43d2-241">-Zone</span><span class="sxs-lookup"><span data-stu-id="b43d2-241">-Zone</span></span>
<span data-ttu-id="b43d2-242">Lista de zonas.</span><span class="sxs-lookup"><span data-stu-id="b43d2-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b43d2-243">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b43d2-243">-Confirm</span></span>
<span data-ttu-id="b43d2-244">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b43d2-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b43d2-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b43d2-245">-WhatIf</span></span>
<span data-ttu-id="b43d2-246">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b43d2-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b43d2-247">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b43d2-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b43d2-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43d2-248">CommonParameters</span></span>
<span data-ttu-id="b43d2-249">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43d2-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43d2-250">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b43d2-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43d2-251">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b43d2-251">INPUTS</span></span>

### <span data-ttu-id="b43d2-252">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b43d2-252">None</span></span>
<span data-ttu-id="b43d2-253">Você pode canalizar a entrada para esse cmdlet pelo nome, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="b43d2-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="b43d2-254">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b43d2-254">OUTPUTS</span></span>

### <span data-ttu-id="b43d2-255">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b43d2-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="b43d2-256">Esse cmdlet retorna todos os atributos de um cache Redis incluindo as chaves de acesso primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="b43d2-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="b43d2-257">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b43d2-257">NOTES</span></span>

## <span data-ttu-id="b43d2-258">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b43d2-258">RELATED LINKS</span></span>

[<span data-ttu-id="b43d2-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b43d2-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b43d2-260">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b43d2-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="b43d2-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b43d2-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


