---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946887"
---
# <span data-ttu-id="94a72-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="94a72-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="94a72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94a72-102">SYNOPSIS</span></span>
<span data-ttu-id="94a72-103">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="94a72-103">Create or update a quota.</span></span>

## <span data-ttu-id="94a72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94a72-104">SYNTAX</span></span>

### <span data-ttu-id="94a72-105">Cotas (padrão)</span><span class="sxs-lookup"><span data-stu-id="94a72-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94a72-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="94a72-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94a72-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="94a72-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a72-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94a72-108">DESCRIPTION</span></span>
<span data-ttu-id="94a72-109">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="94a72-109">Create or update a quota.</span></span>

## <span data-ttu-id="94a72-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94a72-110">EXAMPLES</span></span>

### <span data-ttu-id="94a72-111">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="94a72-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="94a72-112">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="94a72-112">Update a network quota by name.</span></span>

### <span data-ttu-id="94a72-113">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="94a72-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="94a72-114">Atualize uma cota de rede por nome.</span><span class="sxs-lookup"><span data-stu-id="94a72-114">Update a network quota by name.</span></span>

## <span data-ttu-id="94a72-115">OS</span><span class="sxs-lookup"><span data-stu-id="94a72-115">PARAMETERS</span></span>

### <span data-ttu-id="94a72-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="94a72-116">-Name</span></span>
<span data-ttu-id="94a72-117">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="94a72-117">Name of the resource.</span></span>

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

### <span data-ttu-id="94a72-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="94a72-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="94a72-119">O máximo de NICs permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="94a72-119">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="94a72-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="94a72-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="94a72-121">O máximo de endereços IP públicos permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="94a72-121">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="94a72-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="94a72-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="94a72-123">O número máximo de conexões de gateway virtual de rede permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="94a72-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="94a72-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="94a72-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="94a72-125">O número máximo de redes virtuais permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="94a72-125">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="94a72-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="94a72-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="94a72-127">O número máximo de gateways de rede virtual permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="94a72-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="94a72-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="94a72-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="94a72-129">O número máximo de grupos de segurança permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="94a72-129">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="94a72-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="94a72-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="94a72-131">O número máximo de balanceadores de carga permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="94a72-131">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="94a72-132">-Local</span><span class="sxs-lookup"><span data-stu-id="94a72-132">-Location</span></span>
<span data-ttu-id="94a72-133">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="94a72-133">Location of the resource.</span></span>

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

### <span data-ttu-id="94a72-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a72-134">-ResourceId</span></span>
<span data-ttu-id="94a72-135">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="94a72-135">The resource id.</span></span>

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

### <span data-ttu-id="94a72-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94a72-136">-InputObject</span></span>
<span data-ttu-id="94a72-137">Posbbily cota de rede modificada retornada por Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="94a72-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

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

### <span data-ttu-id="94a72-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a72-138">-WhatIf</span></span>
<span data-ttu-id="94a72-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94a72-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a72-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94a72-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a72-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94a72-141">-Confirm</span></span>
<span data-ttu-id="94a72-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94a72-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a72-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a72-143">CommonParameters</span></span>
<span data-ttu-id="94a72-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a72-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a72-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a72-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a72-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94a72-146">INPUTS</span></span>

## <span data-ttu-id="94a72-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94a72-147">OUTPUTS</span></span>

### <span data-ttu-id="94a72-148">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="94a72-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="94a72-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94a72-149">NOTES</span></span>

## <span data-ttu-id="94a72-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94a72-150">RELATED LINKS</span></span>
