---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 882bbb9f45720114fe3ca12e8094e1464b895881
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891737"
---
# <span data-ttu-id="53f2c-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="53f2c-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="53f2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="53f2c-103">Atualiza um banco de dados</span><span class="sxs-lookup"><span data-stu-id="53f2c-103">Updates a database</span></span>

## <span data-ttu-id="53f2c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="53f2c-104">SYNTAX</span></span>

### <span data-ttu-id="53f2c-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="53f2c-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53f2c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53f2c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="53f2c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="53f2c-107">DESCRIPTION</span></span>
<span data-ttu-id="53f2c-108">Atualiza um banco de dados</span><span class="sxs-lookup"><span data-stu-id="53f2c-108">Updates a database</span></span>

## <span data-ttu-id="53f2c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53f2c-109">EXAMPLES</span></span>

### <span data-ttu-id="53f2c-110">Exemplo 1: atualizar o protocolo do cliente</span><span class="sxs-lookup"><span data-stu-id="53f2c-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="53f2c-111">Este comando atualiza o protocolo de cliente do banco de dados para o Cache da Empresa Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="53f2c-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="53f2c-112">Exemplo 2: atualizar o protocolo do cliente e a política de despejo</span><span class="sxs-lookup"><span data-stu-id="53f2c-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="53f2c-113">Este comando atualiza o protocolo de cliente e a política de despejo do banco de dados do Cache Corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="53f2c-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="53f2c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="53f2c-114">PARAMETERS</span></span>

### <span data-ttu-id="53f2c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53f2c-115">-AsJob</span></span>
<span data-ttu-id="53f2c-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="53f2c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="53f2c-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="53f2c-117">-ClientProtocol</span></span>
<span data-ttu-id="53f2c-118">Especifica se os clientes redis podem se conectar usando protocolos de redis criptografados por TLS ou plaintext.</span><span class="sxs-lookup"><span data-stu-id="53f2c-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="53f2c-119">O padrão é criptografado por TLS.</span><span class="sxs-lookup"><span data-stu-id="53f2c-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="53f2c-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="53f2c-120">-ClusteringPolicy</span></span>
<span data-ttu-id="53f2c-121">Política de clustering - o padrão é OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="53f2c-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="53f2c-122">Especificado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="53f2c-122">Specified at create time.</span></span>

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

### <span data-ttu-id="53f2c-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="53f2c-123">-ClusterName</span></span>
<span data-ttu-id="53f2c-124">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="53f2c-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="53f2c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f2c-125">-DefaultProfile</span></span>
<span data-ttu-id="53f2c-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53f2c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f2c-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="53f2c-127">-EvictionPolicy</span></span>
<span data-ttu-id="53f2c-128">Política de despejo de redis - o padrão é VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="53f2c-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="53f2c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53f2c-129">-InputObject</span></span>
<span data-ttu-id="53f2c-130">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="53f2c-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="53f2c-131">-Module</span><span class="sxs-lookup"><span data-stu-id="53f2c-131">-Module</span></span>
<span data-ttu-id="53f2c-132">Conjunto opcional de módulos redis para habilitar neste banco de dados - os módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="53f2c-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="53f2c-133">Para construir, consulte a seção NOTES para propriedades MODULE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="53f2c-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="53f2c-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="53f2c-134">-NoWait</span></span>
<span data-ttu-id="53f2c-135">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="53f2c-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="53f2c-136">-Port</span><span class="sxs-lookup"><span data-stu-id="53f2c-136">-Port</span></span>
<span data-ttu-id="53f2c-137">Porta TCP do ponto de extremidade do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="53f2c-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="53f2c-138">Especificado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="53f2c-138">Specified at create time.</span></span>
<span data-ttu-id="53f2c-139">Padrão para uma porta disponível.</span><span class="sxs-lookup"><span data-stu-id="53f2c-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="53f2c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f2c-140">-ResourceGroupName</span></span>
<span data-ttu-id="53f2c-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53f2c-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="53f2c-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53f2c-142">-SubscriptionId</span></span>
<span data-ttu-id="53f2c-143">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53f2c-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="53f2c-144">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="53f2c-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="53f2c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53f2c-145">-Confirm</span></span>
<span data-ttu-id="53f2c-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53f2c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f2c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f2c-147">-WhatIf</span></span>
<span data-ttu-id="53f2c-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53f2c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f2c-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53f2c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f2c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f2c-150">CommonParameters</span></span>
<span data-ttu-id="53f2c-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f2c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f2c-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53f2c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f2c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53f2c-153">INPUTS</span></span>

### <span data-ttu-id="53f2c-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="53f2c-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="53f2c-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="53f2c-155">OUTPUTS</span></span>

### <span data-ttu-id="53f2c-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="53f2c-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="53f2c-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="53f2c-157">NOTES</span></span>

<span data-ttu-id="53f2c-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="53f2c-158">ALIASES</span></span>

<span data-ttu-id="53f2c-159">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="53f2c-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53f2c-160">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="53f2c-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53f2c-161">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53f2c-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53f2c-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="53f2c-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53f2c-163">`[ClusterName <String>]`: O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="53f2c-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="53f2c-164">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="53f2c-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="53f2c-165">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="53f2c-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53f2c-166">`[Location <String>]`: A região em que a operação está.</span><span class="sxs-lookup"><span data-stu-id="53f2c-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="53f2c-167">`[OperationId <String>]`: Identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="53f2c-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="53f2c-168">`[PrivateEndpointConnectionName <String>]`: O nome da conexão de ponto de extremidade privada associada ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="53f2c-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="53f2c-169">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53f2c-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="53f2c-170">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53f2c-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="53f2c-171">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="53f2c-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="53f2c-172">MODULE <IModule[]>: conjunto opcional de módulos redis para habilitar neste banco de dados - os módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="53f2c-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="53f2c-173">`Name <String>`: O nome do módulo, por exemplo, 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="53f2c-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="53f2c-174">`[Arg <String>]`: Opções de configuração para o módulo, por exemplo, 'ERROR_RATE 0,00 INITIAL_SIZE 400'.</span><span class="sxs-lookup"><span data-stu-id="53f2c-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="53f2c-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53f2c-175">RELATED LINKS</span></span>

