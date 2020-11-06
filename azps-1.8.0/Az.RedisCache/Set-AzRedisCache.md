---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599525"
---
# <span data-ttu-id="36fcf-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="36fcf-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="36fcf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="36fcf-103">Modifica um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="36fcf-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="36fcf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36fcf-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36fcf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="36fcf-106">O cmdlet **set-AzRedisCache** modifica um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="36fcf-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="36fcf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36fcf-107">EXAMPLES</span></span>

### <span data-ttu-id="36fcf-108">Exemplo 1: modificar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="36fcf-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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

<span data-ttu-id="36fcf-109">Esse comando atualiza a política MaxMemory do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="36fcf-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="36fcf-110">OS</span><span class="sxs-lookup"><span data-stu-id="36fcf-110">PARAMETERS</span></span>

### <span data-ttu-id="36fcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fcf-111">-DefaultProfile</span></span>
<span data-ttu-id="36fcf-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36fcf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36fcf-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="36fcf-113">-EnableNonSslPort</span></span>
<span data-ttu-id="36fcf-114">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="36fcf-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="36fcf-115">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="36fcf-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="36fcf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="36fcf-116">-Name</span></span>
<span data-ttu-id="36fcf-117">Especifica o nome do cache do Redis a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="36fcf-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="36fcf-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="36fcf-118">-RedisConfiguration</span></span>
<span data-ttu-id="36fcf-119">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="36fcf-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="36fcf-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="36fcf-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36fcf-121">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="36fcf-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="36fcf-122">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="36fcf-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="36fcf-123">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-123">Premium tier only.</span></span>
- <span data-ttu-id="36fcf-124">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="36fcf-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="36fcf-125">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="36fcf-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="36fcf-126">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-126">Premium tier only.</span></span>
- <span data-ttu-id="36fcf-127">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="36fcf-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="36fcf-128">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="36fcf-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="36fcf-129">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-129">Premium tier only.</span></span> 
- <span data-ttu-id="36fcf-130">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="36fcf-130">maxmemory-reserved.</span></span>
<span data-ttu-id="36fcf-131">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="36fcf-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="36fcf-132">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="36fcf-133">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="36fcf-133">maxmemory-policy.</span></span>
<span data-ttu-id="36fcf-134">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="36fcf-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="36fcf-135">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="36fcf-135">All pricing tiers.</span></span> 
- <span data-ttu-id="36fcf-136">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="36fcf-136">notify-keyspace-events.</span></span>
<span data-ttu-id="36fcf-137">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="36fcf-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="36fcf-138">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="36fcf-139">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="36fcf-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="36fcf-140">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="36fcf-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="36fcf-141">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="36fcf-142">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="36fcf-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="36fcf-143">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="36fcf-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="36fcf-144">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="36fcf-145">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="36fcf-145">set-max-intset-entries.</span></span>
<span data-ttu-id="36fcf-146">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="36fcf-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="36fcf-147">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="36fcf-148">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="36fcf-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="36fcf-149">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="36fcf-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="36fcf-150">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="36fcf-151">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="36fcf-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="36fcf-152">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="36fcf-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="36fcf-153">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="36fcf-154">bancos.</span><span class="sxs-lookup"><span data-stu-id="36fcf-154">databases.</span></span>
<span data-ttu-id="36fcf-155">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="36fcf-155">Configures the number of databases.</span></span>
<span data-ttu-id="36fcf-156">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="36fcf-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="36fcf-157">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="36fcf-158">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="36fcf-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="36fcf-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36fcf-159">-ResourceGroupName</span></span>
<span data-ttu-id="36fcf-160">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="36fcf-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="36fcf-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="36fcf-161">-ShardCount</span></span>
<span data-ttu-id="36fcf-162">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="36fcf-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="36fcf-163">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="36fcf-163">-Size</span></span>
<span data-ttu-id="36fcf-164">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="36fcf-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="36fcf-165">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="36fcf-165">Valid values are:</span></span> 
- <span data-ttu-id="36fcf-166">P1</span><span class="sxs-lookup"><span data-stu-id="36fcf-166">P1</span></span>
- <span data-ttu-id="36fcf-167">P2</span><span class="sxs-lookup"><span data-stu-id="36fcf-167">P2</span></span>
- <span data-ttu-id="36fcf-168">P3</span><span class="sxs-lookup"><span data-stu-id="36fcf-168">P3</span></span>
- <span data-ttu-id="36fcf-169">P4</span><span class="sxs-lookup"><span data-stu-id="36fcf-169">P4</span></span>
- <span data-ttu-id="36fcf-170">C0</span><span class="sxs-lookup"><span data-stu-id="36fcf-170">C0</span></span>
- <span data-ttu-id="36fcf-171">C1</span><span class="sxs-lookup"><span data-stu-id="36fcf-171">C1</span></span>
- <span data-ttu-id="36fcf-172">C2</span><span class="sxs-lookup"><span data-stu-id="36fcf-172">C2</span></span>
- <span data-ttu-id="36fcf-173">C3</span><span class="sxs-lookup"><span data-stu-id="36fcf-173">C3</span></span>
- <span data-ttu-id="36fcf-174">C4</span><span class="sxs-lookup"><span data-stu-id="36fcf-174">C4</span></span>
- <span data-ttu-id="36fcf-175">C5</span><span class="sxs-lookup"><span data-stu-id="36fcf-175">C5</span></span>
- <span data-ttu-id="36fcf-176">C6</span><span class="sxs-lookup"><span data-stu-id="36fcf-176">C6</span></span>
- <span data-ttu-id="36fcf-177">250MB</span><span class="sxs-lookup"><span data-stu-id="36fcf-177">250MB</span></span>
- <span data-ttu-id="36fcf-178">1 GB</span><span class="sxs-lookup"><span data-stu-id="36fcf-178">1GB</span></span>
- <span data-ttu-id="36fcf-179">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="36fcf-179">2.5GB</span></span>
- <span data-ttu-id="36fcf-180">6GB</span><span class="sxs-lookup"><span data-stu-id="36fcf-180">6GB</span></span>
- <span data-ttu-id="36fcf-181">13GB</span><span class="sxs-lookup"><span data-stu-id="36fcf-181">13GB</span></span>
- <span data-ttu-id="36fcf-182">26GB</span><span class="sxs-lookup"><span data-stu-id="36fcf-182">26GB</span></span>
- <span data-ttu-id="36fcf-183">53GB o valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="36fcf-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="36fcf-184">-SKU</span><span class="sxs-lookup"><span data-stu-id="36fcf-184">-Sku</span></span>
<span data-ttu-id="36fcf-185">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="36fcf-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="36fcf-186">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="36fcf-186">Valid values are:</span></span> 
- <span data-ttu-id="36fcf-187">Basic</span><span class="sxs-lookup"><span data-stu-id="36fcf-187">Basic</span></span>
- <span data-ttu-id="36fcf-188">Oficial</span><span class="sxs-lookup"><span data-stu-id="36fcf-188">Standard</span></span>
- <span data-ttu-id="36fcf-189">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="36fcf-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="36fcf-190">-Marca</span><span class="sxs-lookup"><span data-stu-id="36fcf-190">-Tag</span></span>
<span data-ttu-id="36fcf-191">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="36fcf-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="36fcf-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="36fcf-192">-TenantSettings</span></span>
<span data-ttu-id="36fcf-193">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="36fcf-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="36fcf-194">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36fcf-194">-Confirm</span></span>
<span data-ttu-id="36fcf-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36fcf-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36fcf-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36fcf-196">-WhatIf</span></span>
<span data-ttu-id="36fcf-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36fcf-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36fcf-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36fcf-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36fcf-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fcf-199">CommonParameters</span></span>
<span data-ttu-id="36fcf-200">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36fcf-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fcf-201">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36fcf-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fcf-202">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36fcf-202">INPUTS</span></span>

### <span data-ttu-id="36fcf-203">System. String</span><span class="sxs-lookup"><span data-stu-id="36fcf-203">System.String</span></span>

### <span data-ttu-id="36fcf-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="36fcf-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="36fcf-205">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36fcf-205">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36fcf-206">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36fcf-206">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="36fcf-207">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36fcf-207">OUTPUTS</span></span>

### <span data-ttu-id="36fcf-208">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="36fcf-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="36fcf-209">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36fcf-209">NOTES</span></span>

## <span data-ttu-id="36fcf-210">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36fcf-210">RELATED LINKS</span></span>

[<span data-ttu-id="36fcf-211">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="36fcf-211">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="36fcf-212">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="36fcf-212">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="36fcf-213">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="36fcf-213">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


