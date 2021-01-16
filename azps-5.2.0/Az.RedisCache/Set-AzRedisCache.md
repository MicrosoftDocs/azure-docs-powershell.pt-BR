---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261459"
---
# <span data-ttu-id="90901-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90901-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="90901-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90901-102">SYNOPSIS</span></span>
<span data-ttu-id="90901-103">Modifica um cache Redis.</span><span class="sxs-lookup"><span data-stu-id="90901-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="90901-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90901-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90901-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90901-105">DESCRIPTION</span></span>
<span data-ttu-id="90901-106">O cmdlet **set-AzRedisCache** modifica um cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="90901-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="90901-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90901-107">EXAMPLES</span></span>

### <span data-ttu-id="90901-108">Exemplo 1: modificar um cache Redis</span><span class="sxs-lookup"><span data-stu-id="90901-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="90901-109">Esse comando atualiza a política MaxMemory do cache Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="90901-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="90901-110">OS</span><span class="sxs-lookup"><span data-stu-id="90901-110">PARAMETERS</span></span>

### <span data-ttu-id="90901-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90901-111">-DefaultProfile</span></span>
<span data-ttu-id="90901-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90901-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90901-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="90901-113">-EnableNonSslPort</span></span>
<span data-ttu-id="90901-114">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="90901-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="90901-115">O valor padrão é $False (a porta não SSL está desativada).</span><span class="sxs-lookup"><span data-stu-id="90901-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="90901-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="90901-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="90901-117">Especifique a versão de TLS exigida pelos clientes para se conectar ao cache.</span><span class="sxs-lookup"><span data-stu-id="90901-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="90901-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="90901-118">-Name</span></span>
<span data-ttu-id="90901-119">Especifica o nome do cache do Redis a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="90901-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="90901-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="90901-120">-RedisConfiguration</span></span>
<span data-ttu-id="90901-121">Especifica as configurações de configuração do Redis.</span><span class="sxs-lookup"><span data-stu-id="90901-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="90901-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="90901-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90901-123">RDB-habilitado para backup.</span><span class="sxs-lookup"><span data-stu-id="90901-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="90901-124">Especifica que a persistência de dados do Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="90901-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="90901-125">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-125">Premium tier only.</span></span>
- <span data-ttu-id="90901-126">RDB-Storage-Connection-cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="90901-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="90901-127">Especifica a cadeia de conexão para a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="90901-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="90901-128">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-128">Premium tier only.</span></span>
- <span data-ttu-id="90901-129">RDB-backup-frequência.</span><span class="sxs-lookup"><span data-stu-id="90901-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="90901-130">Especifica a frequência de backup para persistência de dados do Redis.</span><span class="sxs-lookup"><span data-stu-id="90901-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="90901-131">Somente camada Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-131">Premium tier only.</span></span> 
- <span data-ttu-id="90901-132">MaxMemory-reservado.</span><span class="sxs-lookup"><span data-stu-id="90901-132">maxmemory-reserved.</span></span>
<span data-ttu-id="90901-133">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="90901-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="90901-134">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90901-135">MaxMemory-política.</span><span class="sxs-lookup"><span data-stu-id="90901-135">maxmemory-policy.</span></span>
<span data-ttu-id="90901-136">Configura a política de remoção para o cache.</span><span class="sxs-lookup"><span data-stu-id="90901-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="90901-137">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="90901-137">All pricing tiers.</span></span> 
- <span data-ttu-id="90901-138">Notify-keyspace-Events.</span><span class="sxs-lookup"><span data-stu-id="90901-138">notify-keyspace-events.</span></span>
<span data-ttu-id="90901-139">Configura notificações de espaço livre.</span><span class="sxs-lookup"><span data-stu-id="90901-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="90901-140">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="90901-141">hash-Max-ziplist-entradas.</span><span class="sxs-lookup"><span data-stu-id="90901-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="90901-142">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="90901-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90901-143">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90901-144">hash-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="90901-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="90901-145">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="90901-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90901-146">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90901-147">SET-Max-intset-entradas.</span><span class="sxs-lookup"><span data-stu-id="90901-147">set-max-intset-entries.</span></span>
<span data-ttu-id="90901-148">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="90901-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90901-149">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90901-150">zset-Max-ziplist-Entries.</span><span class="sxs-lookup"><span data-stu-id="90901-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="90901-151">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="90901-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90901-152">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90901-153">zset-Max-ziplist-Value.</span><span class="sxs-lookup"><span data-stu-id="90901-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="90901-154">Configura a otimização de memória para tipos de dados de agregação pequenos.</span><span class="sxs-lookup"><span data-stu-id="90901-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="90901-155">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="90901-156">bancos.</span><span class="sxs-lookup"><span data-stu-id="90901-156">databases.</span></span>
<span data-ttu-id="90901-157">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="90901-157">Configures the number of databases.</span></span>
<span data-ttu-id="90901-158">Essa propriedade pode ser configurada somente na criação do cache.</span><span class="sxs-lookup"><span data-stu-id="90901-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="90901-159">Camadas padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="90901-160">Para obter mais informações, consulte Gerenciar o cache do Azure Redis com o PowerShell do PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="90901-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="90901-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90901-161">-ResourceGroupName</span></span>
<span data-ttu-id="90901-162">Especifica o nome do grupo de recursos que contém o cache Redis.</span><span class="sxs-lookup"><span data-stu-id="90901-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="90901-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="90901-163">-ShardCount</span></span>
<span data-ttu-id="90901-164">Especifica o número de fragmentos a serem criados em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="90901-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="90901-165">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="90901-165">-Size</span></span>
<span data-ttu-id="90901-166">Especifica o tamanho do cache Redis.</span><span class="sxs-lookup"><span data-stu-id="90901-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="90901-167">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="90901-167">Valid values are:</span></span> 
- <span data-ttu-id="90901-168">P1</span><span class="sxs-lookup"><span data-stu-id="90901-168">P1</span></span>
- <span data-ttu-id="90901-169">P2</span><span class="sxs-lookup"><span data-stu-id="90901-169">P2</span></span>
- <span data-ttu-id="90901-170">P3</span><span class="sxs-lookup"><span data-stu-id="90901-170">P3</span></span>
- <span data-ttu-id="90901-171">P4</span><span class="sxs-lookup"><span data-stu-id="90901-171">P4</span></span>
- <span data-ttu-id="90901-172">P5</span><span class="sxs-lookup"><span data-stu-id="90901-172">P5</span></span>
- <span data-ttu-id="90901-173">C0</span><span class="sxs-lookup"><span data-stu-id="90901-173">C0</span></span>
- <span data-ttu-id="90901-174">C1</span><span class="sxs-lookup"><span data-stu-id="90901-174">C1</span></span>
- <span data-ttu-id="90901-175">C2</span><span class="sxs-lookup"><span data-stu-id="90901-175">C2</span></span>
- <span data-ttu-id="90901-176">C3</span><span class="sxs-lookup"><span data-stu-id="90901-176">C3</span></span>
- <span data-ttu-id="90901-177">C4</span><span class="sxs-lookup"><span data-stu-id="90901-177">C4</span></span>
- <span data-ttu-id="90901-178">C5</span><span class="sxs-lookup"><span data-stu-id="90901-178">C5</span></span>
- <span data-ttu-id="90901-179">C6</span><span class="sxs-lookup"><span data-stu-id="90901-179">C6</span></span>
- <span data-ttu-id="90901-180">250MB</span><span class="sxs-lookup"><span data-stu-id="90901-180">250MB</span></span>
- <span data-ttu-id="90901-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="90901-181">1GB</span></span>
- <span data-ttu-id="90901-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="90901-182">2.5GB</span></span>
- <span data-ttu-id="90901-183">6GB</span><span class="sxs-lookup"><span data-stu-id="90901-183">6GB</span></span>
- <span data-ttu-id="90901-184">13GB</span><span class="sxs-lookup"><span data-stu-id="90901-184">13GB</span></span>
- <span data-ttu-id="90901-185">26GB</span><span class="sxs-lookup"><span data-stu-id="90901-185">26GB</span></span>
- <span data-ttu-id="90901-186">53GB</span><span class="sxs-lookup"><span data-stu-id="90901-186">53GB</span></span>
- <span data-ttu-id="90901-187">120 GB o valor padrão é 1GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="90901-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="90901-188">-SKU</span><span class="sxs-lookup"><span data-stu-id="90901-188">-Sku</span></span>
<span data-ttu-id="90901-189">Especifica o SKU do cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="90901-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="90901-190">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="90901-190">Valid values are:</span></span> 
- <span data-ttu-id="90901-191">Basic</span><span class="sxs-lookup"><span data-stu-id="90901-191">Basic</span></span>
- <span data-ttu-id="90901-192">Oficial</span><span class="sxs-lookup"><span data-stu-id="90901-192">Standard</span></span>
- <span data-ttu-id="90901-193">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="90901-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="90901-194">-Marca</span><span class="sxs-lookup"><span data-stu-id="90901-194">-Tag</span></span>
<span data-ttu-id="90901-195">Uma tabela de hash que representa as marcas.</span><span class="sxs-lookup"><span data-stu-id="90901-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="90901-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="90901-196">-TenantSettings</span></span>
<span data-ttu-id="90901-197">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="90901-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="90901-198">-Confirme</span><span class="sxs-lookup"><span data-stu-id="90901-198">-Confirm</span></span>
<span data-ttu-id="90901-199">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90901-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90901-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90901-200">-WhatIf</span></span>
<span data-ttu-id="90901-201">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90901-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90901-202">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90901-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90901-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90901-203">CommonParameters</span></span>
<span data-ttu-id="90901-204">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90901-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90901-205">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90901-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90901-206">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90901-206">INPUTS</span></span>

### <span data-ttu-id="90901-207">System. String</span><span class="sxs-lookup"><span data-stu-id="90901-207">System.String</span></span>

### <span data-ttu-id="90901-208">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="90901-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="90901-209">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="90901-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="90901-210">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="90901-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="90901-211">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90901-211">OUTPUTS</span></span>

### <span data-ttu-id="90901-212">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="90901-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="90901-213">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90901-213">NOTES</span></span>

## <span data-ttu-id="90901-214">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90901-214">RELATED LINKS</span></span>

[<span data-ttu-id="90901-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90901-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="90901-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90901-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="90901-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90901-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


