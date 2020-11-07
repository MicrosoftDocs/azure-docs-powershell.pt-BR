---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2867f0c438f1f8752137f680365ecade255d291
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774488"
---
# <span data-ttu-id="a7296-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a7296-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="a7296-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7296-102">SYNOPSIS</span></span>
<span data-ttu-id="a7296-103">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="a7296-103">Create or update a quota.</span></span>

## <span data-ttu-id="a7296-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7296-104">SYNTAX</span></span>

### <span data-ttu-id="a7296-105">Cotas (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7296-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7296-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="a7296-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7296-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7296-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7296-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7296-108">DESCRIPTION</span></span>
<span data-ttu-id="a7296-109">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="a7296-109">Create or update a quota.</span></span>

## <span data-ttu-id="a7296-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7296-110">EXAMPLES</span></span>

### <span data-ttu-id="a7296-111">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7296-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="a7296-112">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="a7296-112">Update a network quota by name.</span></span>

### <span data-ttu-id="a7296-113">--------------------------EXEMPLO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7296-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="a7296-114">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="a7296-114">Update a network quota by name.</span></span>

## <span data-ttu-id="a7296-115">OS</span><span class="sxs-lookup"><span data-stu-id="a7296-115">PARAMETERS</span></span>

### <span data-ttu-id="a7296-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7296-116">-InputObject</span></span>
<span data-ttu-id="a7296-117">Posbbily cota de rede modificada retornada por Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a7296-117">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-118">-Local</span><span class="sxs-lookup"><span data-stu-id="a7296-118">-Location</span></span>
<span data-ttu-id="a7296-119">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7296-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-120">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7296-120">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="a7296-121">O número máximo de balanceadores de carga permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7296-121">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-122">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7296-122">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="a7296-123">O máximo de NICs permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7296-123">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-124">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7296-124">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="a7296-125">O máximo de endereços IP públicos permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7296-125">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-126">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7296-126">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="a7296-127">O número máximo de grupos de segurança permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7296-127">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7296-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="a7296-129">O número máximo de conexões de gateway virtual de rede permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7296-129">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-130">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7296-130">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="a7296-131">O número máximo de gateways de rede virtual permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7296-131">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-132">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a7296-132">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="a7296-133">O número máximo de redes virtuais permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="a7296-133">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7296-134">-Name</span></span>
<span data-ttu-id="a7296-135">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7296-135">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7296-136">-ResourceId</span></span>
<span data-ttu-id="a7296-137">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7296-137">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7296-138">-Confirm</span></span>
<span data-ttu-id="a7296-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7296-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7296-140">-WhatIf</span></span>
<span data-ttu-id="a7296-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7296-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7296-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7296-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7296-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7296-143">CommonParameters</span></span>
<span data-ttu-id="a7296-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7296-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7296-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7296-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7296-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7296-146">INPUTS</span></span>

## <span data-ttu-id="a7296-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7296-147">OUTPUTS</span></span>

### <span data-ttu-id="a7296-148">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="a7296-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="a7296-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7296-149">NOTES</span></span>

## <span data-ttu-id="a7296-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7296-150">RELATED LINKS</span></span>

