---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775982"
---
# <span data-ttu-id="d4f36-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="d4f36-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="d4f36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d4f36-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f36-103">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="d4f36-103">Create or update a quota.</span></span>

## <span data-ttu-id="d4f36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4f36-104">SYNTAX</span></span>

### <span data-ttu-id="d4f36-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="d4f36-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4f36-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="d4f36-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4f36-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d4f36-107">DESCRIPTION</span></span>
<span data-ttu-id="d4f36-108">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="d4f36-108">Create or update a quota.</span></span>

## <span data-ttu-id="d4f36-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d4f36-109">EXAMPLES</span></span>

### <span data-ttu-id="d4f36-110">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d4f36-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="d4f36-111">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="d4f36-111">Update a network quota by name.</span></span>

### <span data-ttu-id="d4f36-112">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d4f36-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="d4f36-113">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="d4f36-113">Update a network quota by name.</span></span>

## <span data-ttu-id="d4f36-114">OS</span><span class="sxs-lookup"><span data-stu-id="d4f36-114">PARAMETERS</span></span>

### <span data-ttu-id="d4f36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f36-115">-DefaultProfile</span></span>
<span data-ttu-id="d4f36-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f36-117">-Local</span><span class="sxs-lookup"><span data-stu-id="d4f36-117">-Location</span></span>
<span data-ttu-id="d4f36-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="d4f36-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f36-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="d4f36-120">Número máximo de balanceadores de carga que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f36-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="d4f36-122">Número máximo de NICs que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f36-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="d4f36-124">Número máximo de endereços IP públicos que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f36-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="d4f36-126">Número máximo de grupos de segurança que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f36-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="d4f36-128">Número máximo de conexões de gateway de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f36-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="d4f36-130">Número máximo de gateways de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d4f36-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="d4f36-132">Número máximo de redes virtuais que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4f36-133">-Name</span></span>
<span data-ttu-id="d4f36-134">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d4f36-134">Name of the resource.</span></span>

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

### <span data-ttu-id="d4f36-135">-Quota</span><span class="sxs-lookup"><span data-stu-id="d4f36-135">-Quota</span></span>
<span data-ttu-id="d4f36-136">Recurso de cota de rede.</span><span class="sxs-lookup"><span data-stu-id="d4f36-136">Network quota resource.</span></span>
<span data-ttu-id="d4f36-137">Para construir, consulte a seção de notas para propriedades de cota e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d4f36-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4f36-138">-SubscriptionId</span></span>
<span data-ttu-id="d4f36-139">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f36-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4f36-140">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d4f36-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4f36-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="d4f36-141">-Tag</span></span>
<span data-ttu-id="d4f36-142">Lista de pares de valores chave.</span><span class="sxs-lookup"><span data-stu-id="d4f36-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4f36-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d4f36-143">-Confirm</span></span>
<span data-ttu-id="d4f36-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4f36-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4f36-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4f36-145">-WhatIf</span></span>
<span data-ttu-id="d4f36-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d4f36-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4f36-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d4f36-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4f36-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f36-148">CommonParameters</span></span>
<span data-ttu-id="d4f36-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4f36-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f36-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4f36-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f36-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d4f36-151">INPUTS</span></span>

### <span data-ttu-id="d4f36-152">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="d4f36-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="d4f36-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d4f36-153">OUTPUTS</span></span>

### <span data-ttu-id="d4f36-154">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="d4f36-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="d4f36-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d4f36-155">NOTES</span></span>

<span data-ttu-id="d4f36-156">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d4f36-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4f36-157">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4f36-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d4f36-158">COTA <IQuota> : recurso de cota de rede.</span><span class="sxs-lookup"><span data-stu-id="d4f36-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="d4f36-159">`[Tag <IResourceTags>]`: Lista de pares de valores chave.</span><span class="sxs-lookup"><span data-stu-id="d4f36-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="d4f36-160">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="d4f36-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d4f36-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Número máximo de balanceadores de carga que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d4f36-162">`[MaxNicsPerSubscription <Int64?>]`: Número máximo de NICs que podem ser provisionadas por uma assinatura de locatário.</span><span class="sxs-lookup"><span data-stu-id="d4f36-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d4f36-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Número máximo de endereços IP públicos que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d4f36-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Número máximo de grupos de segurança que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d4f36-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Número máximo de conexões de gateway de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d4f36-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Número máximo de gateways de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="d4f36-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d4f36-167">`[MaxVnetsPerSubscription <Int64?>]`: Número máximo de redes virtuais que podem ser provisionadas por uma assinatura de locatário.</span><span class="sxs-lookup"><span data-stu-id="d4f36-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="d4f36-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d4f36-168">RELATED LINKS</span></span>

