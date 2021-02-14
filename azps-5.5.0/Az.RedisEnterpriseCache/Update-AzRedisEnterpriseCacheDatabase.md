---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117204"
---
# <span data-ttu-id="956aa-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="956aa-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="956aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="956aa-102">SYNOPSIS</span></span>
<span data-ttu-id="956aa-103">Atualiza um banco de dados</span><span class="sxs-lookup"><span data-stu-id="956aa-103">Updates a database</span></span>

## <span data-ttu-id="956aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="956aa-104">SYNTAX</span></span>

### <span data-ttu-id="956aa-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="956aa-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="956aa-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="956aa-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="956aa-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="956aa-107">DESCRIPTION</span></span>
<span data-ttu-id="956aa-108">Atualiza um banco de dados</span><span class="sxs-lookup"><span data-stu-id="956aa-108">Updates a database</span></span>

## <span data-ttu-id="956aa-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="956aa-109">EXAMPLES</span></span>

### <span data-ttu-id="956aa-110">Exemplo 1: Atualizar protocolo do cliente</span><span class="sxs-lookup"><span data-stu-id="956aa-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="956aa-111">Esse comando atualiza o protocolo de cliente do banco de dados do Cache Corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="956aa-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="956aa-112">Exemplo 2: Atualizar o protocolo do cliente e a política de desapropriação</span><span class="sxs-lookup"><span data-stu-id="956aa-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="956aa-113">Este comando atualiza o protocolo do cliente e a política de desapropriação do banco de dados do Cache Corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="956aa-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="956aa-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="956aa-114">PARAMETERS</span></span>

### <span data-ttu-id="956aa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="956aa-115">-AsJob</span></span>
<span data-ttu-id="956aa-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="956aa-116">Run the command as a job</span></span>

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

### <span data-ttu-id="956aa-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="956aa-117">-ClientProtocol</span></span>
<span data-ttu-id="956aa-118">Especifica se os clientes redis podem se conectar usando protocolos TLS-encrypted ou plaintext redis.</span><span class="sxs-lookup"><span data-stu-id="956aa-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="956aa-119">O padrão é criptografado por TLS.</span><span class="sxs-lookup"><span data-stu-id="956aa-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="956aa-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="956aa-120">-ClusteringPolicy</span></span>
<span data-ttu-id="956aa-121">Política de agrupamento – o padrão é o OSSCluster.</span><span class="sxs-lookup"><span data-stu-id="956aa-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="956aa-122">Especificado no momento de criação.</span><span class="sxs-lookup"><span data-stu-id="956aa-122">Specified at create time.</span></span>

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

### <span data-ttu-id="956aa-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="956aa-123">-ClusterName</span></span>
<span data-ttu-id="956aa-124">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="956aa-124">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="956aa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956aa-125">-DefaultProfile</span></span>
<span data-ttu-id="956aa-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="956aa-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="956aa-127">-EsporáciaPolicy</span><span class="sxs-lookup"><span data-stu-id="956aa-127">-EvictionPolicy</span></span>
<span data-ttu-id="956aa-128">Política de desapropriação de vermelhos - padrão é VolátilLRU</span><span class="sxs-lookup"><span data-stu-id="956aa-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="956aa-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="956aa-129">-InputObject</span></span>
<span data-ttu-id="956aa-130">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="956aa-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="956aa-131">-Module</span><span class="sxs-lookup"><span data-stu-id="956aa-131">-Module</span></span>
<span data-ttu-id="956aa-132">Conjunto opcional de módulos de redis para habilitar neste banco de dados: módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="956aa-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="956aa-133">Para construir, consulte a seção ANOTAÇÕES para propriedades MODULE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="956aa-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="956aa-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="956aa-134">-NoWait</span></span>
<span data-ttu-id="956aa-135">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="956aa-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="956aa-136">-Porta</span><span class="sxs-lookup"><span data-stu-id="956aa-136">-Port</span></span>
<span data-ttu-id="956aa-137">Porta TCP do ponto de extremidade do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="956aa-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="956aa-138">Especificado no momento de criação.</span><span class="sxs-lookup"><span data-stu-id="956aa-138">Specified at create time.</span></span>
<span data-ttu-id="956aa-139">Padrões para uma porta disponível.</span><span class="sxs-lookup"><span data-stu-id="956aa-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="956aa-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="956aa-140">-ResourceGroupName</span></span>
<span data-ttu-id="956aa-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="956aa-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="956aa-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="956aa-142">-SubscriptionId</span></span>
<span data-ttu-id="956aa-143">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="956aa-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="956aa-144">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="956aa-144">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="956aa-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="956aa-145">-Confirm</span></span>
<span data-ttu-id="956aa-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="956aa-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956aa-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956aa-147">-WhatIf</span></span>
<span data-ttu-id="956aa-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="956aa-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="956aa-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="956aa-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956aa-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956aa-150">CommonParameters</span></span>
<span data-ttu-id="956aa-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956aa-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956aa-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="956aa-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956aa-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="956aa-153">INPUTS</span></span>

### <span data-ttu-id="956aa-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="956aa-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="956aa-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="956aa-155">OUTPUTS</span></span>

### <span data-ttu-id="956aa-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="956aa-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="956aa-157">Notas</span><span class="sxs-lookup"><span data-stu-id="956aa-157">NOTES</span></span>

<span data-ttu-id="956aa-158">Aliases</span><span class="sxs-lookup"><span data-stu-id="956aa-158">ALIASES</span></span>

<span data-ttu-id="956aa-159">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="956aa-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="956aa-160">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="956aa-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="956aa-161">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="956aa-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="956aa-162">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="956aa-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="956aa-163">`[ClusterName <String>]`: o nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="956aa-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="956aa-164">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="956aa-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="956aa-165">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="956aa-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="956aa-166">`[Location <String>]`: a região em que a operação está.</span><span class="sxs-lookup"><span data-stu-id="956aa-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="956aa-167">`[OperationId <String>]`: identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="956aa-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="956aa-168">`[PrivateEndpointConnectionName <String>]`: o nome da conexão de ponto de extremidade particular associada ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="956aa-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="956aa-169">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="956aa-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="956aa-170">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="956aa-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="956aa-171">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="956aa-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="956aa-172">MODULE <IModule[]>: Conjunto opcional de módulos de redis para habilitar neste banco de dados: os módulos só podem ser adicionados no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="956aa-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="956aa-173">`Name <String>`: o nome do módulo, por exemplo, 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span><span class="sxs-lookup"><span data-stu-id="956aa-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="956aa-174">`[Arg <String>]`: Opções de configuração para o módulo, por exemplo, "ERROR_RATE 0,00 INITIAL_SIZE 400".</span><span class="sxs-lookup"><span data-stu-id="956aa-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="956aa-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="956aa-175">RELATED LINKS</span></span>

