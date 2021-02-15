---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112666"
---
# <span data-ttu-id="f0893-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f0893-101">New-AzRedisCache</span></span>

## <span data-ttu-id="f0893-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0893-102">SYNOPSIS</span></span>
<span data-ttu-id="f0893-103">Cria um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="f0893-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0893-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0893-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0893-105">DESCRIPTION</span></span>
<span data-ttu-id="f0893-106">O **cmdlet New-AzRedisCache** cria um Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0893-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="f0893-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0893-107">EXAMPLES</span></span>

### <span data-ttu-id="f0893-108">Exemplo 1: Criar um Cache de Redis</span><span class="sxs-lookup"><span data-stu-id="f0893-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="f0893-109">Esse comando cria um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="f0893-110">Exemplo 2: Criar um Cache de Redis de SKU Padrão</span><span class="sxs-lookup"><span data-stu-id="f0893-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="f0893-111">Esse comando cria um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="f0893-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0893-112">PARAMETERS</span></span>

### <span data-ttu-id="f0893-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0893-113">-DefaultProfile</span></span>
<span data-ttu-id="f0893-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f0893-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0893-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="f0893-115">-EnableNonSslPort</span></span>
<span data-ttu-id="f0893-116">Indica se a porta que não é SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f0893-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="f0893-117">O valor padrão é $False (a porta que não é SSL está desabilitada).</span><span class="sxs-lookup"><span data-stu-id="f0893-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="f0893-118">-Local</span><span class="sxs-lookup"><span data-stu-id="f0893-118">-Location</span></span>
<span data-ttu-id="f0893-119">Especifica o local no qual criar um Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="f0893-120">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f0893-120">Valid values are:</span></span> 
- <span data-ttu-id="f0893-121">North Central US</span><span class="sxs-lookup"><span data-stu-id="f0893-121">North Central US</span></span>
- <span data-ttu-id="f0893-122">Centro Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="f0893-122">South Central US</span></span>
- <span data-ttu-id="f0893-123">Central dos EUA</span><span class="sxs-lookup"><span data-stu-id="f0893-123">Central US</span></span>
- <span data-ttu-id="f0893-124">Europa Ocidental</span><span class="sxs-lookup"><span data-stu-id="f0893-124">West Europe</span></span>
- <span data-ttu-id="f0893-125">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="f0893-125">North Europe</span></span>
- <span data-ttu-id="f0893-126">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f0893-126">West US</span></span>
- <span data-ttu-id="f0893-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f0893-127">East US</span></span>
- <span data-ttu-id="f0893-128">Leste dos EUA 2</span><span class="sxs-lookup"><span data-stu-id="f0893-128">East US 2</span></span>
- <span data-ttu-id="f0893-129">Leste do Japão</span><span class="sxs-lookup"><span data-stu-id="f0893-129">Japan East</span></span>
- <span data-ttu-id="f0893-130">Oeste do Japão</span><span class="sxs-lookup"><span data-stu-id="f0893-130">Japan West</span></span>
- <span data-ttu-id="f0893-131">Sul do Brasil</span><span class="sxs-lookup"><span data-stu-id="f0893-131">Brazil South</span></span>
- <span data-ttu-id="f0893-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="f0893-132">Southeast Asia</span></span>
- <span data-ttu-id="f0893-133">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="f0893-133">East Asia</span></span>
- <span data-ttu-id="f0893-134">Leste da Austrália</span><span class="sxs-lookup"><span data-stu-id="f0893-134">Australia East</span></span>
- <span data-ttu-id="f0893-135">Sudeste da Austrália</span><span class="sxs-lookup"><span data-stu-id="f0893-135">Australia Southeast</span></span>

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

### <span data-ttu-id="f0893-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f0893-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="f0893-137">Especifique a versão TLS necessária para que os clientes se conectem ao cache.</span><span class="sxs-lookup"><span data-stu-id="f0893-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="f0893-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0893-138">-Name</span></span>
<span data-ttu-id="f0893-139">Especifica o nome do Cache de Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f0893-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="f0893-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0893-140">-RedisConfiguration</span></span>
<span data-ttu-id="f0893-141">Especifica as configurações de redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="f0893-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f0893-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f0893-143">RDB habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="f0893-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="f0893-144">Especifica que a persistência de dados Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f0893-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="f0893-145">Somente camada premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-145">Premium tier only.</span></span>
- <span data-ttu-id="f0893-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="f0893-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="f0893-147">Especifica a cadeia de conexão com a conta de Armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="f0893-148">Somente camada premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-148">Premium tier only.</span></span>
- <span data-ttu-id="f0893-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="f0893-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="f0893-150">Especifica a frequência de backup para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="f0893-151">Somente camada premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-151">Premium tier only.</span></span> 
- <span data-ttu-id="f0893-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="f0893-152">maxmemory-reserved.</span></span>
<span data-ttu-id="f0893-153">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="f0893-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="f0893-154">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f0893-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="f0893-155">maxmemory-policy.</span></span>
<span data-ttu-id="f0893-156">Configura a política de desapropriação do cache.</span><span class="sxs-lookup"><span data-stu-id="f0893-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="f0893-157">Todos os níveis de preços.</span><span class="sxs-lookup"><span data-stu-id="f0893-157">All pricing tiers.</span></span> 
- <span data-ttu-id="f0893-158">notificar eventos de espaço-chave.</span><span class="sxs-lookup"><span data-stu-id="f0893-158">notify-keyspace-events.</span></span>
<span data-ttu-id="f0893-159">Configura notificações de espaço de tecla.</span><span class="sxs-lookup"><span data-stu-id="f0893-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="f0893-160">Camadas padrão e premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="f0893-161">entradas hash-max-ziplist.</span><span class="sxs-lookup"><span data-stu-id="f0893-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="f0893-162">Configura a otimização da memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f0893-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f0893-163">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f0893-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="f0893-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="f0893-165">Configura a otimização da memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f0893-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f0893-166">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f0893-167">entradas set-max-intset.</span><span class="sxs-lookup"><span data-stu-id="f0893-167">set-max-intset-entries.</span></span>
<span data-ttu-id="f0893-168">Configura a otimização da memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f0893-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f0893-169">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f0893-170">entradas zset-max-ziplist.</span><span class="sxs-lookup"><span data-stu-id="f0893-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="f0893-171">Configura a otimização da memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f0893-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f0893-172">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f0893-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="f0893-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="f0893-174">Configura a otimização da memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f0893-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f0893-175">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f0893-176">Bancos.</span><span class="sxs-lookup"><span data-stu-id="f0893-176">databases.</span></span>
<span data-ttu-id="f0893-177">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="f0893-177">Configures the number of databases.</span></span>
<span data-ttu-id="f0893-178">Essa propriedade só pode ser configurada na criação de cache.</span><span class="sxs-lookup"><span data-stu-id="f0893-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="f0893-179">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="f0893-180">Para obter mais informações, consulte Gerenciar Cache de Redis do Azure com o PowerShell do Azure http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="f0893-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="f0893-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0893-181">-ResourceGroupName</span></span>
<span data-ttu-id="f0893-182">Especifica o nome do grupo de recursos no qual criar o Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="f0893-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="f0893-183">-ShardCount</span></span>
<span data-ttu-id="f0893-184">Especifica o número de fragmentos a ser criado em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="f0893-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="f0893-185">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f0893-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f0893-186">1</span><span class="sxs-lookup"><span data-stu-id="f0893-186">1</span></span>
- <span data-ttu-id="f0893-187">2</span><span class="sxs-lookup"><span data-stu-id="f0893-187">2</span></span>
- <span data-ttu-id="f0893-188">3</span><span class="sxs-lookup"><span data-stu-id="f0893-188">3</span></span>
- <span data-ttu-id="f0893-189">4</span><span class="sxs-lookup"><span data-stu-id="f0893-189">4</span></span>
- <span data-ttu-id="f0893-190">5</span><span class="sxs-lookup"><span data-stu-id="f0893-190">5</span></span>
- <span data-ttu-id="f0893-191">6</span><span class="sxs-lookup"><span data-stu-id="f0893-191">6</span></span>
- <span data-ttu-id="f0893-192">7</span><span class="sxs-lookup"><span data-stu-id="f0893-192">7</span></span>
- <span data-ttu-id="f0893-193">8</span><span class="sxs-lookup"><span data-stu-id="f0893-193">8</span></span>
- <span data-ttu-id="f0893-194">9</span><span class="sxs-lookup"><span data-stu-id="f0893-194">9</span></span> 
- <span data-ttu-id="f0893-195">10</span><span class="sxs-lookup"><span data-stu-id="f0893-195">10</span></span>

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

### <span data-ttu-id="f0893-196">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="f0893-196">-Size</span></span>
<span data-ttu-id="f0893-197">Especifica o tamanho do Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="f0893-198">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f0893-198">Valid values are:</span></span> 
- <span data-ttu-id="f0893-199">P1</span><span class="sxs-lookup"><span data-stu-id="f0893-199">P1</span></span>
- <span data-ttu-id="f0893-200">P2</span><span class="sxs-lookup"><span data-stu-id="f0893-200">P2</span></span>
- <span data-ttu-id="f0893-201">P3</span><span class="sxs-lookup"><span data-stu-id="f0893-201">P3</span></span>
- <span data-ttu-id="f0893-202">P4</span><span class="sxs-lookup"><span data-stu-id="f0893-202">P4</span></span>
- <span data-ttu-id="f0893-203">P5</span><span class="sxs-lookup"><span data-stu-id="f0893-203">P5</span></span>
- <span data-ttu-id="f0893-204">C0</span><span class="sxs-lookup"><span data-stu-id="f0893-204">C0</span></span>
- <span data-ttu-id="f0893-205">C1</span><span class="sxs-lookup"><span data-stu-id="f0893-205">C1</span></span>
- <span data-ttu-id="f0893-206">C2</span><span class="sxs-lookup"><span data-stu-id="f0893-206">C2</span></span>
- <span data-ttu-id="f0893-207">C3</span><span class="sxs-lookup"><span data-stu-id="f0893-207">C3</span></span>
- <span data-ttu-id="f0893-208">C4</span><span class="sxs-lookup"><span data-stu-id="f0893-208">C4</span></span>
- <span data-ttu-id="f0893-209">C5</span><span class="sxs-lookup"><span data-stu-id="f0893-209">C5</span></span>
- <span data-ttu-id="f0893-210">C6</span><span class="sxs-lookup"><span data-stu-id="f0893-210">C6</span></span>
- <span data-ttu-id="f0893-211">250 MB</span><span class="sxs-lookup"><span data-stu-id="f0893-211">250MB</span></span>
- <span data-ttu-id="f0893-212">1gb</span><span class="sxs-lookup"><span data-stu-id="f0893-212">1GB</span></span>
- <span data-ttu-id="f0893-213">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="f0893-213">2.5GB</span></span>
- <span data-ttu-id="f0893-214">6 GB</span><span class="sxs-lookup"><span data-stu-id="f0893-214">6GB</span></span>
- <span data-ttu-id="f0893-215">13 GB</span><span class="sxs-lookup"><span data-stu-id="f0893-215">13GB</span></span>
- <span data-ttu-id="f0893-216">26 GB</span><span class="sxs-lookup"><span data-stu-id="f0893-216">26GB</span></span>
- <span data-ttu-id="f0893-217">53 GB O valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="f0893-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="f0893-218">-SKU</span><span class="sxs-lookup"><span data-stu-id="f0893-218">-Sku</span></span>
<span data-ttu-id="f0893-219">Especifica a SKU do Cache de Redis para criar.</span><span class="sxs-lookup"><span data-stu-id="f0893-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="f0893-220">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f0893-220">Valid values are:</span></span> 
- <span data-ttu-id="f0893-221">Basic</span><span class="sxs-lookup"><span data-stu-id="f0893-221">Basic</span></span>
- <span data-ttu-id="f0893-222">Padrão</span><span class="sxs-lookup"><span data-stu-id="f0893-222">Standard</span></span>
- <span data-ttu-id="f0893-223">Premium O valor padrão é Padrão.</span><span class="sxs-lookup"><span data-stu-id="f0893-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="f0893-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="f0893-224">-StaticIP</span></span>
<span data-ttu-id="f0893-225">Especifica um endereço IP exclusivo na sub-rede do Cache de Redis.</span><span class="sxs-lookup"><span data-stu-id="f0893-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="f0893-226">Se você não especificar um valor para esse parâmetro, esse cmdlet escolherá um endereço IP na sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f0893-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="f0893-227">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="f0893-227">-SubnetId</span></span>
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

### <span data-ttu-id="f0893-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0893-228">-Tag</span></span>
<span data-ttu-id="f0893-229">Uma tabela hash que representa marcas.</span><span class="sxs-lookup"><span data-stu-id="f0893-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="f0893-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="f0893-230">-TenantSettings</span></span>
<span data-ttu-id="f0893-231">Este parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="f0893-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="f0893-232">-Zona</span><span class="sxs-lookup"><span data-stu-id="f0893-232">-Zone</span></span>
<span data-ttu-id="f0893-233">Lista de zonas.</span><span class="sxs-lookup"><span data-stu-id="f0893-233">List of zones.</span></span>

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

### <span data-ttu-id="f0893-234">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f0893-234">-Confirm</span></span>
<span data-ttu-id="f0893-235">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0893-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0893-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0893-236">-WhatIf</span></span>
<span data-ttu-id="f0893-237">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f0893-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0893-238">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0893-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0893-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0893-239">CommonParameters</span></span>
<span data-ttu-id="f0893-240">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0893-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0893-241">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0893-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0893-242">Entradas</span><span class="sxs-lookup"><span data-stu-id="f0893-242">INPUTS</span></span>

### <span data-ttu-id="f0893-243">System.String</span><span class="sxs-lookup"><span data-stu-id="f0893-243">System.String</span></span>

### <span data-ttu-id="f0893-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f0893-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f0893-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0893-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f0893-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0893-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f0893-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f0893-247">System.String[]</span></span>

## <span data-ttu-id="f0893-248">Saídas</span><span class="sxs-lookup"><span data-stu-id="f0893-248">OUTPUTS</span></span>

### <span data-ttu-id="f0893-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f0893-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="f0893-250">Notas</span><span class="sxs-lookup"><span data-stu-id="f0893-250">NOTES</span></span>

## <span data-ttu-id="f0893-251">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0893-251">RELATED LINKS</span></span>

[<span data-ttu-id="f0893-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f0893-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="f0893-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f0893-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f0893-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f0893-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


