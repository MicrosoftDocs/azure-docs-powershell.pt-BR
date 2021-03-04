---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891766"
---
# <span data-ttu-id="f7945-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f7945-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="f7945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7945-102">SYNOPSIS</span></span>
<span data-ttu-id="f7945-103">Modifica um Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f7945-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="f7945-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7945-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7945-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7945-105">DESCRIPTION</span></span>
<span data-ttu-id="f7945-106">O cmdlet **Set-AzRedisCache** modifica um Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="f7945-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="f7945-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7945-107">EXAMPLES</span></span>

### <span data-ttu-id="f7945-108">Exemplo 1: Modificar um Cache Redis</span><span class="sxs-lookup"><span data-stu-id="f7945-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="f7945-109">Este comando atualiza a política maxmemory para o Cache Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="f7945-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="f7945-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7945-110">PARAMETERS</span></span>

### <span data-ttu-id="f7945-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7945-111">-DefaultProfile</span></span>
<span data-ttu-id="f7945-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f7945-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7945-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="f7945-113">-EnableNonSslPort</span></span>
<span data-ttu-id="f7945-114">Indica se a porta não SSL está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f7945-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="f7945-115">O valor padrão é $False (a porta não SSL está desabilitada).</span><span class="sxs-lookup"><span data-stu-id="f7945-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="f7945-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f7945-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="f7945-117">Especifique a versão TLS necessária para que os clientes se conectem ao cache.</span><span class="sxs-lookup"><span data-stu-id="f7945-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="f7945-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f7945-118">-Name</span></span>
<span data-ttu-id="f7945-119">Especifica o nome do Cache Redis a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f7945-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="f7945-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7945-120">-RedisConfiguration</span></span>
<span data-ttu-id="f7945-121">Especifica as configurações redis.</span><span class="sxs-lookup"><span data-stu-id="f7945-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="f7945-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f7945-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7945-123">rdb-backup habilitado.</span><span class="sxs-lookup"><span data-stu-id="f7945-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="f7945-124">Especifica que a persistência de dados Redis está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f7945-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="f7945-125">Somente camada premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-125">Premium tier only.</span></span>
- <span data-ttu-id="f7945-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="f7945-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="f7945-127">Especifica a cadeia de conexão com a conta de armazenamento para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="f7945-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="f7945-128">Somente camada premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-128">Premium tier only.</span></span>
- <span data-ttu-id="f7945-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="f7945-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="f7945-130">Especifica a frequência de backup para persistência de dados Redis.</span><span class="sxs-lookup"><span data-stu-id="f7945-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="f7945-131">Somente camada premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-131">Premium tier only.</span></span> 
- <span data-ttu-id="f7945-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="f7945-132">maxmemory-reserved.</span></span>
<span data-ttu-id="f7945-133">Configura a memória reservada para processos que não são de cache.</span><span class="sxs-lookup"><span data-stu-id="f7945-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="f7945-134">Camadas Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f7945-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="f7945-135">maxmemory-policy.</span></span>
<span data-ttu-id="f7945-136">Configura a política de despejo do cache.</span><span class="sxs-lookup"><span data-stu-id="f7945-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="f7945-137">Todas as camadas de preços.</span><span class="sxs-lookup"><span data-stu-id="f7945-137">All pricing tiers.</span></span> 
- <span data-ttu-id="f7945-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="f7945-138">notify-keyspace-events.</span></span>
<span data-ttu-id="f7945-139">Configura notificações de espaço-chave.</span><span class="sxs-lookup"><span data-stu-id="f7945-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="f7945-140">Camadas padrão e premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="f7945-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="f7945-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="f7945-142">Configura a otimização de memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f7945-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f7945-143">Camadas Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f7945-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="f7945-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="f7945-145">Configura a otimização de memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f7945-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f7945-146">Camadas Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f7945-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="f7945-147">set-max-intset-entries.</span></span>
<span data-ttu-id="f7945-148">Configura a otimização de memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f7945-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f7945-149">Camadas Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f7945-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="f7945-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="f7945-151">Configura a otimização de memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f7945-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f7945-152">Camadas Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f7945-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="f7945-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="f7945-154">Configura a otimização de memória para pequenos tipos de dados agregados.</span><span class="sxs-lookup"><span data-stu-id="f7945-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="f7945-155">Camadas Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="f7945-156">databases.</span><span class="sxs-lookup"><span data-stu-id="f7945-156">databases.</span></span>
<span data-ttu-id="f7945-157">Configura o número de bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="f7945-157">Configures the number of databases.</span></span>
<span data-ttu-id="f7945-158">Essa propriedade só pode ser configurada na criação de cache.</span><span class="sxs-lookup"><span data-stu-id="f7945-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="f7945-159">Camadas Padrão e Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="f7945-160">Para obter mais informações, consulte Manage Azure Redis Cache with Azure PowerShell http://go.microsoft.com/fwlink/?LinkId=800051 ( http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="f7945-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="f7945-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7945-161">-ResourceGroupName</span></span>
<span data-ttu-id="f7945-162">Especifica o nome do grupo de recursos que contém o Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f7945-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="f7945-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="f7945-163">-ShardCount</span></span>
<span data-ttu-id="f7945-164">Especifica o número de fragmentos a ser criado em um cache de cluster Premium.</span><span class="sxs-lookup"><span data-stu-id="f7945-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="f7945-165">-Size</span><span class="sxs-lookup"><span data-stu-id="f7945-165">-Size</span></span>
<span data-ttu-id="f7945-166">Especifica o tamanho do Cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f7945-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="f7945-167">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f7945-167">Valid values are:</span></span> 
- <span data-ttu-id="f7945-168">P1</span><span class="sxs-lookup"><span data-stu-id="f7945-168">P1</span></span>
- <span data-ttu-id="f7945-169">P2</span><span class="sxs-lookup"><span data-stu-id="f7945-169">P2</span></span>
- <span data-ttu-id="f7945-170">P3</span><span class="sxs-lookup"><span data-stu-id="f7945-170">P3</span></span>
- <span data-ttu-id="f7945-171">P4</span><span class="sxs-lookup"><span data-stu-id="f7945-171">P4</span></span>
- <span data-ttu-id="f7945-172">P5</span><span class="sxs-lookup"><span data-stu-id="f7945-172">P5</span></span>
- <span data-ttu-id="f7945-173">C0</span><span class="sxs-lookup"><span data-stu-id="f7945-173">C0</span></span>
- <span data-ttu-id="f7945-174">C1</span><span class="sxs-lookup"><span data-stu-id="f7945-174">C1</span></span>
- <span data-ttu-id="f7945-175">C2</span><span class="sxs-lookup"><span data-stu-id="f7945-175">C2</span></span>
- <span data-ttu-id="f7945-176">C3</span><span class="sxs-lookup"><span data-stu-id="f7945-176">C3</span></span>
- <span data-ttu-id="f7945-177">C4</span><span class="sxs-lookup"><span data-stu-id="f7945-177">C4</span></span>
- <span data-ttu-id="f7945-178">C5</span><span class="sxs-lookup"><span data-stu-id="f7945-178">C5</span></span>
- <span data-ttu-id="f7945-179">C6</span><span class="sxs-lookup"><span data-stu-id="f7945-179">C6</span></span>
- <span data-ttu-id="f7945-180">250 MB</span><span class="sxs-lookup"><span data-stu-id="f7945-180">250MB</span></span>
- <span data-ttu-id="f7945-181">1 GB</span><span class="sxs-lookup"><span data-stu-id="f7945-181">1GB</span></span>
- <span data-ttu-id="f7945-182">2,5 GB</span><span class="sxs-lookup"><span data-stu-id="f7945-182">2.5GB</span></span>
- <span data-ttu-id="f7945-183">6 GB</span><span class="sxs-lookup"><span data-stu-id="f7945-183">6GB</span></span>
- <span data-ttu-id="f7945-184">13 GB</span><span class="sxs-lookup"><span data-stu-id="f7945-184">13GB</span></span>
- <span data-ttu-id="f7945-185">26 GB</span><span class="sxs-lookup"><span data-stu-id="f7945-185">26GB</span></span>
- <span data-ttu-id="f7945-186">53 GB</span><span class="sxs-lookup"><span data-stu-id="f7945-186">53GB</span></span>
- <span data-ttu-id="f7945-187">120 GB O valor padrão é 1 GB ou C1.</span><span class="sxs-lookup"><span data-stu-id="f7945-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="f7945-188">-Sku</span><span class="sxs-lookup"><span data-stu-id="f7945-188">-Sku</span></span>
<span data-ttu-id="f7945-189">Especifica a SKU do Cache Redis a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f7945-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="f7945-190">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f7945-190">Valid values are:</span></span> 
- <span data-ttu-id="f7945-191">Básico</span><span class="sxs-lookup"><span data-stu-id="f7945-191">Basic</span></span>
- <span data-ttu-id="f7945-192">Standard</span><span class="sxs-lookup"><span data-stu-id="f7945-192">Standard</span></span>
- <span data-ttu-id="f7945-193">Premium O valor padrão é Standard.</span><span class="sxs-lookup"><span data-stu-id="f7945-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="f7945-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7945-194">-Tag</span></span>
<span data-ttu-id="f7945-195">Uma tabela de hash que representa marcas.</span><span class="sxs-lookup"><span data-stu-id="f7945-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="f7945-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="f7945-196">-TenantSettings</span></span>
<span data-ttu-id="f7945-197">Esse parâmetro foi preterido.</span><span class="sxs-lookup"><span data-stu-id="f7945-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="f7945-198">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7945-198">-Confirm</span></span>
<span data-ttu-id="f7945-199">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7945-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7945-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7945-200">-WhatIf</span></span>
<span data-ttu-id="f7945-201">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7945-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7945-202">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7945-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7945-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7945-203">CommonParameters</span></span>
<span data-ttu-id="f7945-204">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7945-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7945-205">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7945-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7945-206">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7945-206">INPUTS</span></span>

### <span data-ttu-id="f7945-207">System.String</span><span class="sxs-lookup"><span data-stu-id="f7945-207">System.String</span></span>

### <span data-ttu-id="f7945-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7945-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f7945-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7945-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f7945-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7945-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f7945-211">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7945-211">OUTPUTS</span></span>

### <span data-ttu-id="f7945-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f7945-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="f7945-213">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7945-213">NOTES</span></span>

## <span data-ttu-id="f7945-214">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7945-214">RELATED LINKS</span></span>

[<span data-ttu-id="f7945-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f7945-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="f7945-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f7945-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f7945-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f7945-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


