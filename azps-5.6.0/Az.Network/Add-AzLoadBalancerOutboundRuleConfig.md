---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: d59bb27608e1ccf614048dcd27eb6643695ba523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892463"
---
# <span data-ttu-id="d75b9-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d75b9-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="d75b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d75b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d75b9-103">Adiciona uma configuração de regra de saída a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d75b9-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="d75b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d75b9-104">SYNTAX</span></span>

### <span data-ttu-id="d75b9-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d75b9-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75b9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d75b9-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d75b9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d75b9-107">DESCRIPTION</span></span>
<span data-ttu-id="d75b9-108">O cmdlet **Add-AzLoadBalancerOutboundRuleConfig** adiciona uma configuração de regra de saída a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="d75b9-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d75b9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d75b9-109">EXAMPLES</span></span>

### <span data-ttu-id="d75b9-110">Exemplo 1: Adicionar uma configuração de regra de saída a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="d75b9-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="d75b9-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="d75b9-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d75b9-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para **Add-AzLoadBalancerOutboundRuleConfig**, que adiciona uma configuração de regra de saída ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d75b9-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="d75b9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d75b9-113">PARAMETERS</span></span>

### <span data-ttu-id="d75b9-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="d75b9-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="d75b9-115">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="d75b9-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="d75b9-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d75b9-116">-BackendAddressPool</span></span>
<span data-ttu-id="d75b9-117">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="d75b9-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="d75b9-118">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="d75b9-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="d75b9-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d75b9-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="d75b9-120">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="d75b9-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="d75b9-121">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="d75b9-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="d75b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75b9-122">-DefaultProfile</span></span>
<span data-ttu-id="d75b9-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d75b9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d75b9-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d75b9-124">-EnableTcpReset</span></span>
<span data-ttu-id="d75b9-125">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="d75b9-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="d75b9-126">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="d75b9-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d75b9-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d75b9-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d75b9-128">Os endereços IP Frontend do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d75b9-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="d75b9-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d75b9-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d75b9-130">O tempo de tempo para a conexão ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="d75b9-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="d75b9-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d75b9-131">-LoadBalancer</span></span>
<span data-ttu-id="d75b9-132">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d75b9-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="d75b9-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d75b9-133">-Name</span></span>
<span data-ttu-id="d75b9-134">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="d75b9-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="d75b9-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d75b9-135">-Protocol</span></span>
<span data-ttu-id="d75b9-136">Protocolo - TCP, UDP ou Todos</span><span class="sxs-lookup"><span data-stu-id="d75b9-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="d75b9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d75b9-137">-Confirm</span></span>
<span data-ttu-id="d75b9-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75b9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d75b9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d75b9-139">-WhatIf</span></span>
<span data-ttu-id="d75b9-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d75b9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d75b9-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d75b9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d75b9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75b9-142">CommonParameters</span></span>
<span data-ttu-id="d75b9-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75b9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75b9-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d75b9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75b9-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d75b9-145">INPUTS</span></span>

### <span data-ttu-id="d75b9-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d75b9-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d75b9-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d75b9-147">System.Int32</span></span>

### <span data-ttu-id="d75b9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d75b9-148">System.String</span></span>

### <span data-ttu-id="d75b9-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="d75b9-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="d75b9-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d75b9-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="d75b9-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d75b9-151">OUTPUTS</span></span>

### <span data-ttu-id="d75b9-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d75b9-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d75b9-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="d75b9-153">NOTES</span></span>

## <span data-ttu-id="d75b9-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d75b9-154">RELATED LINKS</span></span>

[<span data-ttu-id="d75b9-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d75b9-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d75b9-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d75b9-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d75b9-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d75b9-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d75b9-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d75b9-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
