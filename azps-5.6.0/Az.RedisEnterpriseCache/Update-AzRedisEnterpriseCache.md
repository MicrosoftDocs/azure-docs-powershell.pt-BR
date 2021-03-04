---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: 1b16f30b068eb41bf0202c65e95f55f94769ba2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891738"
---
# <span data-ttu-id="ad433-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="ad433-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="ad433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad433-102">SYNOPSIS</span></span>
<span data-ttu-id="ad433-103">Atualiza um cluster RedisEnterprise existente</span><span class="sxs-lookup"><span data-stu-id="ad433-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="ad433-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ad433-104">SYNTAX</span></span>

### <span data-ttu-id="ad433-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ad433-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ad433-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ad433-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad433-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ad433-107">DESCRIPTION</span></span>
<span data-ttu-id="ad433-108">Atualiza um cluster RedisEnterprise existente</span><span class="sxs-lookup"><span data-stu-id="ad433-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="ad433-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad433-109">EXAMPLES</span></span>

### <span data-ttu-id="ad433-110">Exemplo 1: Atualizar o Cache da Empresa Redis</span><span class="sxs-lookup"><span data-stu-id="ad433-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="ad433-111">Este comando atualiza a versão TLS mínima e adiciona uma marca ao Cache corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="ad433-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="ad433-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ad433-112">PARAMETERS</span></span>

### <span data-ttu-id="ad433-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad433-113">-AsJob</span></span>
<span data-ttu-id="ad433-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ad433-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ad433-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="ad433-115">-Capacity</span></span>
<span data-ttu-id="ad433-116">O tamanho do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ad433-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="ad433-117">O padrão é 2 ou 3, dependendo do SKU.</span><span class="sxs-lookup"><span data-stu-id="ad433-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="ad433-118">Os valores válidos são (2, 4, 6, ...) para SKUs Empresariais e (3, 9, 15, ...) para SKUs Flash.</span><span class="sxs-lookup"><span data-stu-id="ad433-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="ad433-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ad433-119">-ClusterName</span></span>
<span data-ttu-id="ad433-120">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ad433-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ad433-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad433-121">-DefaultProfile</span></span>
<span data-ttu-id="ad433-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ad433-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad433-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad433-123">-InputObject</span></span>
<span data-ttu-id="ad433-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ad433-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad433-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ad433-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="ad433-126">A versão TLS mínima para o cluster dar suporte, por exemplo, '1.2'</span><span class="sxs-lookup"><span data-stu-id="ad433-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="ad433-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad433-127">-NoWait</span></span>
<span data-ttu-id="ad433-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ad433-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad433-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad433-129">-ResourceGroupName</span></span>
<span data-ttu-id="ad433-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad433-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad433-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="ad433-131">-Sku</span></span>
<span data-ttu-id="ad433-132">O tipo de cluster RedisEnterprise a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="ad433-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="ad433-133">Valores possíveis: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span><span class="sxs-lookup"><span data-stu-id="ad433-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="ad433-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad433-134">-SubscriptionId</span></span>
<span data-ttu-id="ad433-135">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad433-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ad433-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ad433-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ad433-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad433-137">-Tag</span></span>
<span data-ttu-id="ad433-138">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ad433-138">Resource tags.</span></span>

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

### <span data-ttu-id="ad433-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad433-139">-Confirm</span></span>
<span data-ttu-id="ad433-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad433-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad433-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad433-141">-WhatIf</span></span>
<span data-ttu-id="ad433-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad433-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad433-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad433-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad433-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad433-144">CommonParameters</span></span>
<span data-ttu-id="ad433-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad433-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad433-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad433-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad433-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad433-147">INPUTS</span></span>

### <span data-ttu-id="ad433-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="ad433-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="ad433-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ad433-149">OUTPUTS</span></span>

### <span data-ttu-id="ad433-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="ad433-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="ad433-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="ad433-151">NOTES</span></span>

<span data-ttu-id="ad433-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ad433-152">ALIASES</span></span>

<span data-ttu-id="ad433-153">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ad433-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad433-154">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ad433-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad433-155">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad433-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad433-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ad433-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad433-157">`[ClusterName <String>]`: O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="ad433-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="ad433-158">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ad433-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ad433-159">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ad433-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad433-160">`[Location <String>]`: A região em que a operação está.</span><span class="sxs-lookup"><span data-stu-id="ad433-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="ad433-161">`[OperationId <String>]`: Identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="ad433-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="ad433-162">`[PrivateEndpointConnectionName <String>]`: O nome da conexão de ponto de extremidade privada associada ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="ad433-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="ad433-163">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad433-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ad433-164">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ad433-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ad433-165">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ad433-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ad433-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad433-166">RELATED LINKS</span></span>

