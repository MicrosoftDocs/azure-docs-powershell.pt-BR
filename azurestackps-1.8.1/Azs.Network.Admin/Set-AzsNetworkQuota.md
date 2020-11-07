---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93775082"
---
# <span data-ttu-id="b6fa9-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b6fa9-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="b6fa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6fa9-103">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-103">Create or update a quota.</span></span>

## <span data-ttu-id="b6fa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6fa9-104">SYNTAX</span></span>

### <span data-ttu-id="b6fa9-105">Cotas (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6fa9-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6fa9-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="b6fa9-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6fa9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6fa9-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6fa9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6fa9-108">DESCRIPTION</span></span>
<span data-ttu-id="b6fa9-109">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-109">Create or update a quota.</span></span>

## <span data-ttu-id="b6fa9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6fa9-110">EXAMPLES</span></span>

### <span data-ttu-id="b6fa9-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="b6fa9-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="b6fa9-112">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-112">Update a network quota by name.</span></span>

### <span data-ttu-id="b6fa9-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="b6fa9-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="b6fa9-114">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-114">Update a network quota by name.</span></span>

## <span data-ttu-id="b6fa9-115">OS</span><span class="sxs-lookup"><span data-stu-id="b6fa9-115">PARAMETERS</span></span>

### <span data-ttu-id="b6fa9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6fa9-116">-Name</span></span>
<span data-ttu-id="b6fa9-117">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-117">Name of the resource.</span></span>

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

### <span data-ttu-id="b6fa9-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fa9-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="b6fa9-119">O máximo de NICs permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-119">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="b6fa9-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fa9-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="b6fa9-121">O máximo de endereços IP públicos permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-121">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="b6fa9-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fa9-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="b6fa9-123">O número máximo de conexões de gateway virtual de rede permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="b6fa9-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fa9-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="b6fa9-125">O número máximo de redes virtuais permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-125">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="b6fa9-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fa9-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="b6fa9-127">O número máximo de gateways de rede virtual permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="b6fa9-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fa9-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="b6fa9-129">O número máximo de grupos de segurança permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-129">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="b6fa9-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b6fa9-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="b6fa9-131">O número máximo de balanceadores de carga permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-131">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="b6fa9-132">-Local</span><span class="sxs-lookup"><span data-stu-id="b6fa9-132">-Location</span></span>
<span data-ttu-id="b6fa9-133">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-133">Location of the resource.</span></span>

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

### <span data-ttu-id="b6fa9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6fa9-134">-ResourceId</span></span>
<span data-ttu-id="b6fa9-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-135">The resource id.</span></span>

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

### <span data-ttu-id="b6fa9-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6fa9-136">-InputObject</span></span>
<span data-ttu-id="b6fa9-137">Posbbily cota de rede modificada retornada por Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b6fa9-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

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

### <span data-ttu-id="b6fa9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6fa9-138">-WhatIf</span></span>
<span data-ttu-id="b6fa9-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6fa9-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6fa9-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6fa9-141">-Confirm</span></span>
<span data-ttu-id="b6fa9-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6fa9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6fa9-143">CommonParameters</span></span>
<span data-ttu-id="b6fa9-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6fa9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6fa9-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6fa9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6fa9-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6fa9-146">INPUTS</span></span>

## <span data-ttu-id="b6fa9-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6fa9-147">OUTPUTS</span></span>

### <span data-ttu-id="b6fa9-148">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="b6fa9-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="b6fa9-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6fa9-149">NOTES</span></span>

## <span data-ttu-id="b6fa9-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6fa9-150">RELATED LINKS</span></span>
