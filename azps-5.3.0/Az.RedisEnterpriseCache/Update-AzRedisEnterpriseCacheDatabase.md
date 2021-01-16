---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271600"
---
# <span data-ttu-id="c00a2-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="c00a2-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="c00a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c00a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c00a2-103">Atualiza um banco de dados</span><span class="sxs-lookup"><span data-stu-id="c00a2-103">Updates a database</span></span>

## <span data-ttu-id="c00a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c00a2-104">SYNTAX</span></span>

### <span data-ttu-id="c00a2-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="c00a2-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c00a2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c00a2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c00a2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c00a2-107">DESCRIPTION</span></span>
<span data-ttu-id="c00a2-108">Atualiza um banco de dados</span><span class="sxs-lookup"><span data-stu-id="c00a2-108">Updates a database</span></span>

## <span data-ttu-id="c00a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c00a2-109">EXAMPLES</span></span>

### <span data-ttu-id="c00a2-110">Exemplo 1: atualizar o protocolo do cliente</span><span class="sxs-lookup"><span data-stu-id="c00a2-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="c00a2-111">Esse comando atualiza o protocolo de cliente do banco de dados para o cache corporativo Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="c00a2-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="c00a2-112">Exemplo 2: atualizar o protocolo de cliente e a política de remoção</span><span class="sxs-lookup"><span data-stu-id="c00a2-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="c00a2-113">Esse comando atualiza o protocolo de cliente e a política de remoção do banco de dados para o cache corporativo Redis nomeado como myCache.</span><span class="sxs-lookup"><span data-stu-id="c00a2-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="c00a2-114">OS</span><span class="sxs-lookup"><span data-stu-id="c00a2-114">PARAMETERS</span></span>

### <span data-ttu-id="c00a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c00a2-115">-AsJob</span></span>
<span data-ttu-id="c00a2-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c00a2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c00a2-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c00a2-117">-ClientProtocol</span></span>
<span data-ttu-id="c00a2-118">Especifica se os clientes do Redis podem se conectar usando protocolos criptografados por TLS ou texto sem formatação do Redis.</span><span class="sxs-lookup"><span data-stu-id="c00a2-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="c00a2-119">O padrão é criptografado por TLS.</span><span class="sxs-lookup"><span data-stu-id="c00a2-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="c00a2-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="c00a2-120">-ClusteringPolicy</span></span>
<span data-ttu-id="c00a2-121">Política de cluster-o padrão é OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="c00a2-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="c00a2-122">Especificado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="c00a2-122">Specified at create time.</span></span>

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

### <span data-ttu-id="c00a2-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c00a2-123">-ClusterName</span></span>
<span data-ttu-id="c00a2-124">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="c00a2-124">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00a2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00a2-125">-DefaultProfile</span></span>
<span data-ttu-id="c00a2-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c00a2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c00a2-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="c00a2-127">-EvictionPolicy</span></span>
<span data-ttu-id="c00a2-128">Política de remoção de Redis-o padrão é VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="c00a2-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="c00a2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c00a2-129">-InputObject</span></span>
<span data-ttu-id="c00a2-130">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c00a2-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c00a2-131">-Módulo</span><span class="sxs-lookup"><span data-stu-id="c00a2-131">-Module</span></span>
<span data-ttu-id="c00a2-132">Conjunto opcional de módulos Redis para habilitar nesse banco de dados-os módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="c00a2-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="c00a2-133">Para construir, consulte a seção de notas para propriedades do módulo e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c00a2-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c00a2-134">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c00a2-134">-NoWait</span></span>
<span data-ttu-id="c00a2-135">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c00a2-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c00a2-136">-Porta</span><span class="sxs-lookup"><span data-stu-id="c00a2-136">-Port</span></span>
<span data-ttu-id="c00a2-137">Porta TCP do ponto de extremidade do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c00a2-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="c00a2-138">Especificado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="c00a2-138">Specified at create time.</span></span>
<span data-ttu-id="c00a2-139">O padrão é uma porta disponível.</span><span class="sxs-lookup"><span data-stu-id="c00a2-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="c00a2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00a2-140">-ResourceGroupName</span></span>
<span data-ttu-id="c00a2-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c00a2-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00a2-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c00a2-142">-SubscriptionId</span></span>
<span data-ttu-id="c00a2-143">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c00a2-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c00a2-144">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c00a2-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00a2-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c00a2-145">-Confirm</span></span>
<span data-ttu-id="c00a2-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c00a2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c00a2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c00a2-147">-WhatIf</span></span>
<span data-ttu-id="c00a2-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c00a2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c00a2-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c00a2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c00a2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00a2-150">CommonParameters</span></span>
<span data-ttu-id="c00a2-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c00a2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00a2-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c00a2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00a2-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c00a2-153">INPUTS</span></span>

### <span data-ttu-id="c00a2-154">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="c00a2-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="c00a2-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c00a2-155">OUTPUTS</span></span>

### <span data-ttu-id="c00a2-156">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. IDatabase</span><span class="sxs-lookup"><span data-stu-id="c00a2-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="c00a2-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c00a2-157">NOTES</span></span>

<span data-ttu-id="c00a2-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c00a2-158">ALIASES</span></span>

<span data-ttu-id="c00a2-159">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c00a2-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c00a2-160">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c00a2-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c00a2-161">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c00a2-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c00a2-162">INPUTobject <IRedisEnterpriseCacheIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c00a2-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c00a2-163">`[ClusterName <String>]`: O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="c00a2-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="c00a2-164">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c00a2-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c00a2-165">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c00a2-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c00a2-166">`[Location <String>]`: A região em que a operação se encontra.</span><span class="sxs-lookup"><span data-stu-id="c00a2-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="c00a2-167">`[OperationId <String>]`: O identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="c00a2-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="c00a2-168">`[PrivateEndpointConnectionName <String>]`: O nome da conexão de ponto de extremidade particular associado ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="c00a2-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="c00a2-169">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c00a2-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c00a2-170">`[SubscriptionId <String>]`: Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c00a2-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c00a2-171">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c00a2-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="c00a2-172">MODULE <IModule [] >: conjunto opcional de módulos Redis para habilitar nesse banco de dados-os módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="c00a2-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="c00a2-173">`Name <String>`: O nome do módulo, por exemplo, ' RedisBloom ', ' RediSearch ', ' RedisTimeSeries '</span><span class="sxs-lookup"><span data-stu-id="c00a2-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="c00a2-174">`[Arg <String>]`: Opções de configuração do módulo, por exemplo, ' ERROR_RATE 0, 0 INITIAL_SIZE 400 '.</span><span class="sxs-lookup"><span data-stu-id="c00a2-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="c00a2-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c00a2-175">RELATED LINKS</span></span>

