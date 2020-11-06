---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440293"
---
# <span data-ttu-id="a5b69-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a5b69-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="a5b69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5b69-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b69-103">Modifica um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5b69-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5b69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5b69-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b69-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5b69-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b69-106">O cmdlet **set-AzureRmRedisCache** modifica um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a5b69-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="a5b69-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5b69-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b69-108">Exemplo 1: modificar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="a5b69-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="a5b69-109">Esse comando atualiza a política MaxMemory do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="a5b69-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="a5b69-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5b69-110">PARAMETERS</span></span>

### <span data-ttu-id="a5b69-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b69-111">-DefaultProfile</span></span>
<span data-ttu-id="a5b69-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b69-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5b69-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="a5b69-113">-EnableNonSslPort</span></span>
<span data-ttu-id="a5b69-114">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a5b69-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="a5b69-115">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="a5b69-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="a5b69-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5b69-116">-Name</span></span>
<span data-ttu-id="a5b69-117">Especifica o nome do cache do Redis a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="a5b69-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="a5b69-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5b69-118">-RedisConfiguration</span></span>
<span data-ttu-id="a5b69-119">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="a5b69-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="a5b69-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a5b69-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5b69-121">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="a5b69-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="a5b69-122">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a5b69-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="a5b69-123">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-123">Premium tier only.</span></span>
- <span data-ttu-id="a5b69-124">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a5b69-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="a5b69-125">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="a5b69-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="a5b69-126">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-126">Premium tier only.</span></span>
- <span data-ttu-id="a5b69-127">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="a5b69-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="a5b69-128">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="a5b69-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="a5b69-129">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-129">Premium tier only.</span></span> 
- <span data-ttu-id="a5b69-130">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="a5b69-130">maxmemory-reserved.</span></span>
<span data-ttu-id="a5b69-131">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="a5b69-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="a5b69-132">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a5b69-133">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="a5b69-133">maxmemory-policy.</span></span>
<span data-ttu-id="a5b69-134">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="a5b69-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="a5b69-135">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="a5b69-135">All pricing tiers.</span></span> 
- <span data-ttu-id="a5b69-136">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="a5b69-136">notify-keyspace-events.</span></span>
<span data-ttu-id="a5b69-137">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="a5b69-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="a5b69-138">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="a5b69-139">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="a5b69-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="a5b69-140">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="a5b69-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a5b69-141">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a5b69-142">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="a5b69-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="a5b69-143">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="a5b69-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a5b69-144">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a5b69-145">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="a5b69-145">set-max-intset-entries.</span></span>
<span data-ttu-id="a5b69-146">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="a5b69-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a5b69-147">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a5b69-148">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="a5b69-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="a5b69-149">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="a5b69-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a5b69-150">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a5b69-151">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="a5b69-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="a5b69-152">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="a5b69-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a5b69-153">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a5b69-154">bancos.</span><span class="sxs-lookup"><span data-stu-id="a5b69-154">databases.</span></span>
<span data-ttu-id="a5b69-155">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="a5b69-155">Configures the number of databases.</span></span>
<span data-ttu-id="a5b69-156">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="a5b69-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="a5b69-157">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="a5b69-158">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="a5b69-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="a5b69-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b69-159">-ResourceGroupName</span></span>
<span data-ttu-id="a5b69-160">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5b69-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="a5b69-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="a5b69-161">-ShardCount</span></span>
<span data-ttu-id="a5b69-162">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="a5b69-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="a5b69-163">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="a5b69-163">-Size</span></span>
<span data-ttu-id="a5b69-164">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a5b69-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="a5b69-165">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a5b69-165">Valid values are:</span></span> 
- <span data-ttu-id="a5b69-166">P1</span><span class="sxs-lookup"><span data-stu-id="a5b69-166">P1</span></span>
- <span data-ttu-id="a5b69-167">P2</span><span class="sxs-lookup"><span data-stu-id="a5b69-167">P2</span></span>
- <span data-ttu-id="a5b69-168">P3</span><span class="sxs-lookup"><span data-stu-id="a5b69-168">P3</span></span>
- <span data-ttu-id="a5b69-169">P4</span><span class="sxs-lookup"><span data-stu-id="a5b69-169">P4</span></span>
- <span data-ttu-id="a5b69-170">C0</span><span class="sxs-lookup"><span data-stu-id="a5b69-170">C0</span></span>
- <span data-ttu-id="a5b69-171">C1</span><span class="sxs-lookup"><span data-stu-id="a5b69-171">C1</span></span>
- <span data-ttu-id="a5b69-172">C2</span><span class="sxs-lookup"><span data-stu-id="a5b69-172">C2</span></span>
- <span data-ttu-id="a5b69-173">C3</span><span class="sxs-lookup"><span data-stu-id="a5b69-173">C3</span></span>
- <span data-ttu-id="a5b69-174">C4</span><span class="sxs-lookup"><span data-stu-id="a5b69-174">C4</span></span>
- <span data-ttu-id="a5b69-175">C5</span><span class="sxs-lookup"><span data-stu-id="a5b69-175">C5</span></span>
- <span data-ttu-id="a5b69-176">C6</span><span class="sxs-lookup"><span data-stu-id="a5b69-176">C6</span></span>
- <span data-ttu-id="a5b69-177">250MB</span><span class="sxs-lookup"><span data-stu-id="a5b69-177">250MB</span></span>
- <span data-ttu-id="a5b69-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="a5b69-178">1GB</span></span>
- <span data-ttu-id="a5b69-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="a5b69-179">2.5GB</span></span>
- <span data-ttu-id="a5b69-180">6GB</span><span class="sxs-lookup"><span data-stu-id="a5b69-180">6GB</span></span>
- <span data-ttu-id="a5b69-181">13GB</span><span class="sxs-lookup"><span data-stu-id="a5b69-181">13GB</span></span>
- <span data-ttu-id="a5b69-182">26GB</span><span class="sxs-lookup"><span data-stu-id="a5b69-182">26GB</span></span>
- <span data-ttu-id="a5b69-183">53GB o valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="a5b69-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="a5b69-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="a5b69-184">-Sku</span></span>
<span data-ttu-id="a5b69-185">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a5b69-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="a5b69-186">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a5b69-186">Valid values are:</span></span> 
- <span data-ttu-id="a5b69-187">Basic</span><span class="sxs-lookup"><span data-stu-id="a5b69-187">Basic</span></span>
- <span data-ttu-id="a5b69-188">Oficial</span><span class="sxs-lookup"><span data-stu-id="a5b69-188">Standard</span></span>
- <span data-ttu-id="a5b69-189">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="a5b69-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="a5b69-190">-Marca</span><span class="sxs-lookup"><span data-stu-id="a5b69-190">-Tag</span></span>
<span data-ttu-id="a5b69-191">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="a5b69-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="a5b69-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="a5b69-192">-TenantSettings</span></span>
<span data-ttu-id="a5b69-193">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="a5b69-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="a5b69-194">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a5b69-194">-Confirm</span></span>
<span data-ttu-id="a5b69-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b69-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b69-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b69-196">-WhatIf</span></span>
<span data-ttu-id="a5b69-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5b69-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5b69-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5b69-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b69-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b69-199">CommonParameters</span></span>
<span data-ttu-id="a5b69-200">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b69-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b69-201">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b69-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b69-202">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5b69-202">INPUTS</span></span>

### <span data-ttu-id="a5b69-203">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b69-203">System.String</span></span>

### <span data-ttu-id="a5b69-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a5b69-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a5b69-205">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a5b69-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a5b69-206">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a5b69-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a5b69-207">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5b69-207">OUTPUTS</span></span>

### <span data-ttu-id="a5b69-208">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a5b69-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="a5b69-209">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5b69-209">NOTES</span></span>

## <span data-ttu-id="a5b69-210">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5b69-210">RELATED LINKS</span></span>

[<span data-ttu-id="a5b69-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a5b69-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="a5b69-212">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a5b69-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a5b69-213">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a5b69-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


