---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271602"
---
# <span data-ttu-id="1ad3e-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="1ad3e-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="1ad3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ad3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad3e-103">Atualiza um cluster existente do RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="1ad3e-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="1ad3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ad3e-104">SYNTAX</span></span>

### <span data-ttu-id="1ad3e-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ad3e-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ad3e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ad3e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ad3e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ad3e-107">DESCRIPTION</span></span>
<span data-ttu-id="1ad3e-108">Atualiza um cluster existente do RedisEnterprise</span><span class="sxs-lookup"><span data-stu-id="1ad3e-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="1ad3e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ad3e-109">EXAMPLES</span></span>

### <span data-ttu-id="1ad3e-110">Exemplo 1: atualizar o cache corporativo do Redis</span><span class="sxs-lookup"><span data-stu-id="1ad3e-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="1ad3e-111">Esse comando atualiza a versão mínima do TLS e adiciona uma marca ao cache corporativo do Redis chamado myCache.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="1ad3e-112">OS</span><span class="sxs-lookup"><span data-stu-id="1ad3e-112">PARAMETERS</span></span>

### <span data-ttu-id="1ad3e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ad3e-113">-AsJob</span></span>
<span data-ttu-id="1ad3e-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="1ad3e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1ad3e-115">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="1ad3e-115">-Capacity</span></span>
<span data-ttu-id="1ad3e-116">O tamanho do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="1ad3e-117">O padrão é 2 ou 3, dependendo da SKU.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="1ad3e-118">Os valores válidos são (2, 4, 6,...) para SKUs empresariais e (3, 9, 15,...) para SKUs flash.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="1ad3e-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1ad3e-119">-ClusterName</span></span>
<span data-ttu-id="1ad3e-120">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="1ad3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad3e-121">-DefaultProfile</span></span>
<span data-ttu-id="1ad3e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ad3e-123">-InputObject</span></span>
<span data-ttu-id="1ad3e-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ad3e-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1ad3e-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="1ad3e-126">A versão de TLS mínima para o cluster dar suporte, por exemplo, ' 1,2 '</span><span class="sxs-lookup"><span data-stu-id="1ad3e-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="1ad3e-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1ad3e-127">-NoWait</span></span>
<span data-ttu-id="1ad3e-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="1ad3e-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ad3e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad3e-129">-ResourceGroupName</span></span>
<span data-ttu-id="1ad3e-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ad3e-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="1ad3e-131">-Sku</span></span>
<span data-ttu-id="1ad3e-132">O tipo de cluster RedisEnterprise a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="1ad3e-133">Valores possíveis: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span><span class="sxs-lookup"><span data-stu-id="1ad3e-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad3e-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ad3e-134">-SubscriptionId</span></span>
<span data-ttu-id="1ad3e-135">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ad3e-136">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1ad3e-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="1ad3e-137">-Tag</span></span>
<span data-ttu-id="1ad3e-138">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-138">Resource tags.</span></span>

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

### <span data-ttu-id="1ad3e-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ad3e-139">-Confirm</span></span>
<span data-ttu-id="1ad3e-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad3e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad3e-141">-WhatIf</span></span>
<span data-ttu-id="1ad3e-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad3e-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad3e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad3e-144">CommonParameters</span></span>
<span data-ttu-id="1ad3e-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad3e-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ad3e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad3e-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ad3e-147">INPUTS</span></span>

### <span data-ttu-id="1ad3e-148">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="1ad3e-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="1ad3e-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ad3e-149">OUTPUTS</span></span>

### <span data-ttu-id="1ad3e-150">Microsoft. Azure. PowerShell. cmdlets. RedisEnterpriseCache. Models. Api20201001Preview. ICluster</span><span class="sxs-lookup"><span data-stu-id="1ad3e-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="1ad3e-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ad3e-151">NOTES</span></span>

<span data-ttu-id="1ad3e-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1ad3e-152">ALIASES</span></span>

<span data-ttu-id="1ad3e-153">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="1ad3e-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ad3e-154">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ad3e-155">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ad3e-156">INPUTobject <IRedisEnterpriseCacheIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="1ad3e-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ad3e-157">`[ClusterName <String>]`: O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="1ad3e-158">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1ad3e-159">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1ad3e-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ad3e-160">`[Location <String>]`: A região em que a operação se encontra.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="1ad3e-161">`[OperationId <String>]`: O identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="1ad3e-162">`[PrivateEndpointConnectionName <String>]`: O nome da conexão de ponto de extremidade particular associado ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="1ad3e-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="1ad3e-163">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1ad3e-164">`[SubscriptionId <String>]`: Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1ad3e-165">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="1ad3e-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1ad3e-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ad3e-166">RELATED LINKS</span></span>

