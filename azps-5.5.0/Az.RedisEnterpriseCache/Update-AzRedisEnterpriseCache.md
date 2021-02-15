---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114525"
---
# <span data-ttu-id="083f0-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="083f0-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="083f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="083f0-102">SYNOPSIS</span></span>
<span data-ttu-id="083f0-103">Atualiza um cluster RedisEnterprise existente</span><span class="sxs-lookup"><span data-stu-id="083f0-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="083f0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="083f0-104">SYNTAX</span></span>

### <span data-ttu-id="083f0-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="083f0-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="083f0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="083f0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="083f0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="083f0-107">DESCRIPTION</span></span>
<span data-ttu-id="083f0-108">Atualiza um cluster RedisEnterprise existente</span><span class="sxs-lookup"><span data-stu-id="083f0-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="083f0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="083f0-109">EXAMPLES</span></span>

### <span data-ttu-id="083f0-110">Exemplo 1: Atualizar Redis Enterprise Cache</span><span class="sxs-lookup"><span data-stu-id="083f0-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="083f0-111">Esse comando atualiza a versão TLS mínima e adiciona uma marca ao Cache Corporativo Redis chamado MyCache.</span><span class="sxs-lookup"><span data-stu-id="083f0-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="083f0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="083f0-112">PARAMETERS</span></span>

### <span data-ttu-id="083f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="083f0-113">-AsJob</span></span>
<span data-ttu-id="083f0-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="083f0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="083f0-115">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="083f0-115">-Capacity</span></span>
<span data-ttu-id="083f0-116">O tamanho do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="083f0-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="083f0-117">O padrão é 2 ou 3, dependendo da SKU.</span><span class="sxs-lookup"><span data-stu-id="083f0-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="083f0-118">Os valores válidos são (2, 4, 6, ...) para SKUs Enterprise e (3, 9, 15, ...) para SKUs Flash.</span><span class="sxs-lookup"><span data-stu-id="083f0-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="083f0-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="083f0-119">-ClusterName</span></span>
<span data-ttu-id="083f0-120">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="083f0-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="083f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083f0-121">-DefaultProfile</span></span>
<span data-ttu-id="083f0-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="083f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="083f0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="083f0-123">-InputObject</span></span>
<span data-ttu-id="083f0-124">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="083f0-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="083f0-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="083f0-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="083f0-126">A versão TLS mínima para o cluster dar suporte, por exemplo, '1.2'</span><span class="sxs-lookup"><span data-stu-id="083f0-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="083f0-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="083f0-127">-NoWait</span></span>
<span data-ttu-id="083f0-128">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="083f0-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="083f0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="083f0-129">-ResourceGroupName</span></span>
<span data-ttu-id="083f0-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="083f0-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="083f0-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="083f0-131">-Sku</span></span>
<span data-ttu-id="083f0-132">O tipo de cluster RedisEnterprise a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="083f0-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="083f0-133">Valores possíveis: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span><span class="sxs-lookup"><span data-stu-id="083f0-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="083f0-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="083f0-134">-SubscriptionId</span></span>
<span data-ttu-id="083f0-135">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="083f0-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="083f0-136">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="083f0-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="083f0-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="083f0-137">-Tag</span></span>
<span data-ttu-id="083f0-138">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="083f0-138">Resource tags.</span></span>

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

### <span data-ttu-id="083f0-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="083f0-139">-Confirm</span></span>
<span data-ttu-id="083f0-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083f0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="083f0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="083f0-141">-WhatIf</span></span>
<span data-ttu-id="083f0-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="083f0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="083f0-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="083f0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="083f0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083f0-144">CommonParameters</span></span>
<span data-ttu-id="083f0-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083f0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083f0-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="083f0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083f0-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="083f0-147">INPUTS</span></span>

### <span data-ttu-id="083f0-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="083f0-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="083f0-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="083f0-149">OUTPUTS</span></span>

### <span data-ttu-id="083f0-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="083f0-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="083f0-151">Notas</span><span class="sxs-lookup"><span data-stu-id="083f0-151">NOTES</span></span>

<span data-ttu-id="083f0-152">Aliases</span><span class="sxs-lookup"><span data-stu-id="083f0-152">ALIASES</span></span>

<span data-ttu-id="083f0-153">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="083f0-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="083f0-154">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="083f0-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="083f0-155">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="083f0-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="083f0-156">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="083f0-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="083f0-157">`[ClusterName <String>]`: o nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="083f0-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="083f0-158">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="083f0-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="083f0-159">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="083f0-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="083f0-160">`[Location <String>]`: a região em que a operação está.</span><span class="sxs-lookup"><span data-stu-id="083f0-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="083f0-161">`[OperationId <String>]`: identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="083f0-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="083f0-162">`[PrivateEndpointConnectionName <String>]`: o nome da conexão de ponto de extremidade particular associada ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="083f0-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="083f0-163">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="083f0-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="083f0-164">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="083f0-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="083f0-165">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="083f0-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="083f0-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="083f0-166">RELATED LINKS</span></span>

