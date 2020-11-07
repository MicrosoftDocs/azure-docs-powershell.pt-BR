---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775987"
---
# <span data-ttu-id="26908-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="26908-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="26908-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26908-102">SYNOPSIS</span></span>
<span data-ttu-id="26908-103">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="26908-103">Create or update a quota.</span></span>

## <span data-ttu-id="26908-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26908-104">SYNTAX</span></span>

### <span data-ttu-id="26908-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="26908-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26908-106">Criados</span><span class="sxs-lookup"><span data-stu-id="26908-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26908-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26908-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="26908-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="26908-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26908-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26908-109">DESCRIPTION</span></span>
<span data-ttu-id="26908-110">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="26908-110">Create or update a quota.</span></span>

## <span data-ttu-id="26908-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26908-111">EXAMPLES</span></span>

### <span data-ttu-id="26908-112">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="26908-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="26908-113">Crie uma nova cota de rede com todos os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="26908-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="26908-114">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="26908-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="26908-115">Crie uma nova cota de rede com valores não padrão para a cota.</span><span class="sxs-lookup"><span data-stu-id="26908-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="26908-116">OS</span><span class="sxs-lookup"><span data-stu-id="26908-116">PARAMETERS</span></span>

### <span data-ttu-id="26908-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26908-117">-DefaultProfile</span></span>
<span data-ttu-id="26908-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26908-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26908-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26908-119">-InputObject</span></span>
<span data-ttu-id="26908-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="26908-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="26908-121">-Local</span><span class="sxs-lookup"><span data-stu-id="26908-121">-Location</span></span>
<span data-ttu-id="26908-122">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="26908-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="26908-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="26908-124">Número máximo de balanceadores de carga que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="26908-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="26908-126">Número máximo de NICs que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="26908-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="26908-128">Número máximo de endereços IP públicos que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="26908-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="26908-130">Número máximo de grupos de segurança que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="26908-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="26908-132">Número máximo de conexões de gateway de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="26908-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="26908-134">Número máximo de gateways de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="26908-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="26908-136">Número máximo de redes virtuais que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="26908-137">-Name</span></span>
<span data-ttu-id="26908-138">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="26908-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-139">-Quota</span><span class="sxs-lookup"><span data-stu-id="26908-139">-Quota</span></span>
<span data-ttu-id="26908-140">Recurso de cota de rede.</span><span class="sxs-lookup"><span data-stu-id="26908-140">Network quota resource.</span></span>
<span data-ttu-id="26908-141">Para construir, consulte a seção de notas para propriedades de cota e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="26908-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="26908-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26908-142">-SubscriptionId</span></span>
<span data-ttu-id="26908-143">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="26908-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="26908-144">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="26908-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="26908-145">-Tag</span></span>
<span data-ttu-id="26908-146">Lista de pares de valores chave.</span><span class="sxs-lookup"><span data-stu-id="26908-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="26908-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="26908-147">-Confirm</span></span>
<span data-ttu-id="26908-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26908-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26908-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26908-149">-WhatIf</span></span>
<span data-ttu-id="26908-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="26908-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26908-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="26908-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26908-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26908-152">CommonParameters</span></span>
<span data-ttu-id="26908-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26908-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26908-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26908-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26908-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26908-155">INPUTS</span></span>

### <span data-ttu-id="26908-156">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="26908-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="26908-157">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="26908-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="26908-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26908-158">OUTPUTS</span></span>

### <span data-ttu-id="26908-159">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="26908-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="26908-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26908-160">NOTES</span></span>

<span data-ttu-id="26908-161">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="26908-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26908-162">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26908-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="26908-163">INPUTobject <INetworkAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="26908-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26908-164">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="26908-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26908-165">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="26908-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="26908-166">`[ResourceName <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="26908-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="26908-167">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="26908-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="26908-168">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="26908-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="26908-169">COTA <IQuota> : recurso de cota de rede.</span><span class="sxs-lookup"><span data-stu-id="26908-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="26908-170">`[Tag <IResourceTags>]`: Lista de pares de valores chave.</span><span class="sxs-lookup"><span data-stu-id="26908-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="26908-171">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="26908-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="26908-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Número máximo de balanceadores de carga que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="26908-173">`[MaxNicsPerSubscription <Int64?>]`: Número máximo de NICs que podem ser provisionadas por uma assinatura de locatário.</span><span class="sxs-lookup"><span data-stu-id="26908-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="26908-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Número máximo de endereços IP públicos que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="26908-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Número máximo de grupos de segurança que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="26908-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Número máximo de conexões de gateway de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="26908-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Número máximo de gateways de rede virtual que uma assinatura de locatário pode provisionar.</span><span class="sxs-lookup"><span data-stu-id="26908-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="26908-178">`[MaxVnetsPerSubscription <Int64?>]`: Número máximo de redes virtuais que podem ser provisionadas por uma assinatura de locatário.</span><span class="sxs-lookup"><span data-stu-id="26908-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="26908-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26908-179">RELATED LINKS</span></span>

