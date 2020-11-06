---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 79a8442d28d6e04d4e6e013e536663a19faaf3f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600705"
---
# <span data-ttu-id="25e49-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="25e49-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="25e49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25e49-102">SYNOPSIS</span></span>
<span data-ttu-id="25e49-103">Adiciona uma configuração de regra de saída a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="25e49-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="25e49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25e49-104">SYNTAX</span></span>

### <span data-ttu-id="25e49-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="25e49-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e49-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="25e49-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e49-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25e49-107">DESCRIPTION</span></span>
<span data-ttu-id="25e49-108">O cmdlet **Add-AzLoadBalancerOutboundRuleConfig** adiciona uma configuração de regra de saída a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="25e49-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="25e49-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25e49-109">EXAMPLES</span></span>

### <span data-ttu-id="25e49-110">Exemplo 1: adicionar uma configuração de regra de saída a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="25e49-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="25e49-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="25e49-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="25e49-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para **Add-AzLoadBalancerOutboundRuleConfig** , que adiciona uma configuração de regra de saída ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="25e49-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="25e49-113">OS</span><span class="sxs-lookup"><span data-stu-id="25e49-113">PARAMETERS</span></span>

### <span data-ttu-id="25e49-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="25e49-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="25e49-115">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="25e49-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="25e49-116">-BackendAddressPool</span></span>
<span data-ttu-id="25e49-117">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="25e49-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="25e49-118">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="25e49-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="25e49-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="25e49-120">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="25e49-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="25e49-121">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="25e49-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e49-122">-DefaultProfile</span></span>
<span data-ttu-id="25e49-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25e49-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="25e49-124">-EnableTcpReset</span></span>
<span data-ttu-id="25e49-125">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="25e49-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="25e49-126">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="25e49-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="25e49-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="25e49-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="25e49-128">Os endereços IP de front-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="25e49-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="25e49-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="25e49-130">O tempo limite para a conexão ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="25e49-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-131">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="25e49-131">-LoadBalancer</span></span>
<span data-ttu-id="25e49-132">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="25e49-132">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="25e49-133">-Name</span></span>
<span data-ttu-id="25e49-134">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="25e49-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="25e49-135">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="25e49-135">-Protocol</span></span>
<span data-ttu-id="25e49-136">Protocolo-TCP, UDP ou todos</span><span class="sxs-lookup"><span data-stu-id="25e49-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e49-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25e49-137">-Confirm</span></span>
<span data-ttu-id="25e49-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25e49-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e49-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e49-139">-WhatIf</span></span>
<span data-ttu-id="25e49-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25e49-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e49-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25e49-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e49-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e49-142">CommonParameters</span></span>
<span data-ttu-id="25e49-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e49-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e49-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e49-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e49-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25e49-145">INPUTS</span></span>

### <span data-ttu-id="25e49-146">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25e49-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="25e49-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="25e49-147">System.Int32</span></span>

### <span data-ttu-id="25e49-148">System. String</span><span class="sxs-lookup"><span data-stu-id="25e49-148">System.String</span></span>

### <span data-ttu-id="25e49-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="25e49-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="25e49-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="25e49-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="25e49-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25e49-151">OUTPUTS</span></span>

### <span data-ttu-id="25e49-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="25e49-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="25e49-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25e49-153">NOTES</span></span>

## <span data-ttu-id="25e49-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25e49-154">RELATED LINKS</span></span>

[<span data-ttu-id="25e49-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="25e49-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="25e49-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="25e49-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="25e49-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="25e49-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="25e49-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="25e49-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
