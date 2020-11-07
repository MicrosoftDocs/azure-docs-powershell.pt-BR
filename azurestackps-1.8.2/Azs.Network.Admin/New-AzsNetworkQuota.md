---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946815"
---
# <span data-ttu-id="e2b9a-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="e2b9a-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="e2b9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b9a-103">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-103">Create or update a quota.</span></span>

## <span data-ttu-id="e2b9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2b9a-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b9a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b9a-106">Criar ou atualizar uma cota.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-106">Create or update a quota.</span></span>

## <span data-ttu-id="e2b9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b9a-108">EXEMPLO 1</span><span class="sxs-lookup"><span data-stu-id="e2b9a-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="e2b9a-109">Crie uma nova cota de rede com todos os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="e2b9a-110">EXEMPLO 2</span><span class="sxs-lookup"><span data-stu-id="e2b9a-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="e2b9a-111">Crie uma nova cota de rede com valores não padrão para a cota.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="e2b9a-112">OS</span><span class="sxs-lookup"><span data-stu-id="e2b9a-112">PARAMETERS</span></span>

### <span data-ttu-id="e2b9a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2b9a-113">-Name</span></span>
<span data-ttu-id="e2b9a-114">Nome do recurso de cota de rede.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-114">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e2b9a-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="e2b9a-116">O máximo de NICs permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-116">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e2b9a-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="e2b9a-118">O máximo de endereços IP públicos permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-118">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e2b9a-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="e2b9a-120">O número máximo de conexões de gateway virtual de rede permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e2b9a-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="e2b9a-122">O número máximo de redes virtuais permitidas por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-122">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e2b9a-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="e2b9a-124">O número máximo de gateways de rede virtual permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e2b9a-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="e2b9a-126">O número máximo de grupos de segurança permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-126">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="e2b9a-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="e2b9a-128">O número máximo de balanceadores de carga permitidos por assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-128">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-129">-Local</span><span class="sxs-lookup"><span data-stu-id="e2b9a-129">-Location</span></span>
<span data-ttu-id="e2b9a-130">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-130">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="e2b9a-131">-MigrationPhase</span></span>
<span data-ttu-id="e2b9a-132">Estado de migração como None, prepare, Commit e Abort.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b9a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b9a-133">-WhatIf</span></span>
<span data-ttu-id="e2b9a-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b9a-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b9a-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2b9a-136">-Confirm</span></span>
<span data-ttu-id="e2b9a-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b9a-138">CommonParameters</span></span>
<span data-ttu-id="e2b9a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b9a-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b9a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b9a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2b9a-141">INPUTS</span></span>

## <span data-ttu-id="e2b9a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2b9a-142">OUTPUTS</span></span>

### <span data-ttu-id="e2b9a-143">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="e2b9a-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="e2b9a-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2b9a-144">NOTES</span></span>

## <span data-ttu-id="e2b9a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2b9a-145">RELATED LINKS</span></span>
