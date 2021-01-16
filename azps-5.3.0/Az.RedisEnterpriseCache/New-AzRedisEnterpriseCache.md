---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: f2f996bc212772b3b44202796e270ec345898a11
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271610"
---
# <span data-ttu-id="3b94b-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="3b94b-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="3b94b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b94b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b94b-103">Cria um cluster de cache da Redis da empresa e um banco de dados associado</span><span class="sxs-lookup"><span data-stu-id="3b94b-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="3b94b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b94b-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b94b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b94b-105">DESCRIPTION</span></span>
<span data-ttu-id="3b94b-106">Cria ou atualiza um cluster de cache existente (substituir/recriar, com o possível tempo de inatividade) e um banco de dados associado chamado ' default '</span><span class="sxs-lookup"><span data-stu-id="3b94b-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="3b94b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b94b-107">EXAMPLES</span></span>

### <span data-ttu-id="3b94b-108">Exemplo 1: criar um cache corporativo Redis</span><span class="sxs-lookup"><span data-stu-id="3b94b-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="3b94b-109">Esse comando cria um cache corporativo Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="3b94b-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="3b94b-110">Exemplo 2: criar um cache corporativo do Redis usando alguns parâmetros opcionais</span><span class="sxs-lookup"><span data-stu-id="3b94b-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="3b94b-111">Esse comando cria um cache corporativo Redis chamado myCache usando alguns parâmetros opcionais.</span><span class="sxs-lookup"><span data-stu-id="3b94b-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="3b94b-112">OS</span><span class="sxs-lookup"><span data-stu-id="3b94b-112">PARAMETERS</span></span>

### <span data-ttu-id="3b94b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b94b-113">-AsJob</span></span>
<span data-ttu-id="3b94b-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3b94b-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-115">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="3b94b-115">-Capacity</span></span>
<span data-ttu-id="3b94b-116">O tamanho do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3b94b-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="3b94b-117">O padrão é 2 ou 3, dependendo da SKU.</span><span class="sxs-lookup"><span data-stu-id="3b94b-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="3b94b-118">Os valores válidos são (2, 4, 6,...) para SKUs empresariais e (3, 9, 15,...) para SKUs flash.</span><span class="sxs-lookup"><span data-stu-id="3b94b-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3b94b-119">-ClientProtocol</span></span>
<span data-ttu-id="3b94b-120">Especifica se os clientes do Redis podem se conectar usando protocolos criptografados por TLS ou texto sem formatação do Redis.</span><span class="sxs-lookup"><span data-stu-id="3b94b-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="3b94b-121">O padrão é criptografado por TLS.</span><span class="sxs-lookup"><span data-stu-id="3b94b-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="3b94b-122">-ClusteringPolicy</span></span>
<span data-ttu-id="3b94b-123">Política de cluster-o padrão é OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="3b94b-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="3b94b-124">Especificado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="3b94b-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3b94b-125">-ClusterName</span></span>
<span data-ttu-id="3b94b-126">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="3b94b-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b94b-127">-DefaultProfile</span></span>
<span data-ttu-id="3b94b-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b94b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="3b94b-129">-EvictionPolicy</span></span>
<span data-ttu-id="3b94b-130">Política de remoção de Redis-o padrão é VolatileLRU.</span><span class="sxs-lookup"><span data-stu-id="3b94b-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-131">-Local</span><span class="sxs-lookup"><span data-stu-id="3b94b-131">-Location</span></span>
<span data-ttu-id="3b94b-132">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="3b94b-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3b94b-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="3b94b-134">A versão de TLS mínima para a qual o cluster oferece suporte, por exemplo, 1,2</span><span class="sxs-lookup"><span data-stu-id="3b94b-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-135">-Módulo</span><span class="sxs-lookup"><span data-stu-id="3b94b-135">-Module</span></span>
<span data-ttu-id="3b94b-136">Conjunto opcional de módulos Redis para habilitar nesse banco de dados-os módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="3b94b-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="3b94b-137">Para construir, consulte a seção de notas para propriedades do módulo e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3b94b-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3b94b-138">-NoWait</span></span>
<span data-ttu-id="3b94b-139">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3b94b-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-140">-Porta</span><span class="sxs-lookup"><span data-stu-id="3b94b-140">-Port</span></span>
<span data-ttu-id="3b94b-141">Porta TCP do ponto de extremidade do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3b94b-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="3b94b-142">Especificado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="3b94b-142">Specified at create time.</span></span>
<span data-ttu-id="3b94b-143">O padrão é uma porta disponível.</span><span class="sxs-lookup"><span data-stu-id="3b94b-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b94b-144">-ResourceGroupName</span></span>
<span data-ttu-id="3b94b-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b94b-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="3b94b-146">-Sku</span></span>
<span data-ttu-id="3b94b-147">O tipo de cluster RedisEnterprise a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="3b94b-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="3b94b-148">Valores possíveis: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span><span class="sxs-lookup"><span data-stu-id="3b94b-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b94b-149">-SubscriptionId</span></span>
<span data-ttu-id="3b94b-150">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b94b-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b94b-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3b94b-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-152">-Marca</span><span class="sxs-lookup"><span data-stu-id="3b94b-152">-Tag</span></span>
<span data-ttu-id="3b94b-153">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="3b94b-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="3b94b-154">-Zone</span></span>
<span data-ttu-id="3b94b-155">As zonas em que este cluster será implantado.</span><span class="sxs-lookup"><span data-stu-id="3b94b-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b94b-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b94b-156">-Confirm</span></span>
<span data-ttu-id="3b94b-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b94b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b94b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b94b-158">-WhatIf</span></span>
<span data-ttu-id="3b94b-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b94b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b94b-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b94b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b94b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b94b-161">CommonParameters</span></span>
<span data-ttu-id="3b94b-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b94b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b94b-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b94b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b94b-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b94b-164">INPUTS</span></span>

## <span data-ttu-id="3b94b-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b94b-165">OUTPUTS</span></span>

### <span data-ttu-id="3b94b-166">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="3b94b-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="3b94b-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b94b-167">NOTES</span></span>

<span data-ttu-id="3b94b-168">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3b94b-168">ALIASES</span></span>

<span data-ttu-id="3b94b-169">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3b94b-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b94b-170">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3b94b-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b94b-171">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b94b-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b94b-172">MODULE <IModule [] >: conjunto opcional de módulos Redis para habilitar nesse banco de dados-os módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="3b94b-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="3b94b-173">`Name <String>`: O nome do módulo, por exemplo, ' RedisBloom ', ' RediSearch ', ' RedisTimeSeries '</span><span class="sxs-lookup"><span data-stu-id="3b94b-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="3b94b-174">`[Arg <String>]`: Opções de configuração do módulo, por exemplo, ' ERROR_RATE 0, 0 INITIAL_SIZE 400 '.</span><span class="sxs-lookup"><span data-stu-id="3b94b-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="3b94b-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b94b-175">RELATED LINKS</span></span>

