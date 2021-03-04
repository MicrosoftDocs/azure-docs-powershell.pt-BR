---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 76adf0c831b79b219598a254a859b8603f8c3f27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892081"
---
# <span data-ttu-id="1b76d-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b76d-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="1b76d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b76d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b76d-103">Define uma configuração de regra de saída para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1b76d-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="1b76d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1b76d-104">SYNTAX</span></span>

### <span data-ttu-id="1b76d-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1b76d-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b76d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b76d-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b76d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1b76d-107">DESCRIPTION</span></span>
<span data-ttu-id="1b76d-108">O cmdlet **Set-AzLoadBalancerOutboundRuleConfig** define uma configuração de regra de saída para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b76d-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="1b76d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b76d-109">EXAMPLES</span></span>

### <span data-ttu-id="1b76d-110">Exemplo 1: Modificar a configuração da regra de saída em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="1b76d-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="1b76d-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="1b76d-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="1b76d-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para Add-AzLoadBalancerOutboundRuleConfig, que adiciona uma configuração de regra de saída a ele.</span><span class="sxs-lookup"><span data-stu-id="1b76d-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="1b76d-113">O terceiro comando passa o balanceador de carga para **Set-AzLoadBalancerOutboundRuleConfig**, que salva e atualiza a configuração da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="1b76d-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="1b76d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1b76d-114">PARAMETERS</span></span>

### <span data-ttu-id="1b76d-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="1b76d-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="1b76d-116">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="1b76d-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="1b76d-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b76d-117">-BackendAddressPool</span></span>
<span data-ttu-id="1b76d-118">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="1b76d-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="1b76d-119">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="1b76d-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="1b76d-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1b76d-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="1b76d-121">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="1b76d-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="1b76d-122">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="1b76d-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="1b76d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b76d-123">-DefaultProfile</span></span>
<span data-ttu-id="1b76d-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b76d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b76d-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1b76d-125">-EnableTcpReset</span></span>
<span data-ttu-id="1b76d-126">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="1b76d-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="1b76d-127">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="1b76d-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="1b76d-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b76d-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1b76d-129">Os endereços IP Frontend do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1b76d-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="1b76d-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1b76d-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1b76d-131">O tempo de tempo para a conexão ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="1b76d-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="1b76d-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b76d-132">-LoadBalancer</span></span>
<span data-ttu-id="1b76d-133">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1b76d-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="1b76d-134">-Name</span><span class="sxs-lookup"><span data-stu-id="1b76d-134">-Name</span></span>
<span data-ttu-id="1b76d-135">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="1b76d-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="1b76d-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1b76d-136">-Protocol</span></span>
<span data-ttu-id="1b76d-137">Protocolo - TCP, UDP ou Todos</span><span class="sxs-lookup"><span data-stu-id="1b76d-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="1b76d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b76d-138">-Confirm</span></span>
<span data-ttu-id="1b76d-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b76d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b76d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b76d-140">-WhatIf</span></span>
<span data-ttu-id="1b76d-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b76d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b76d-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b76d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b76d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b76d-143">CommonParameters</span></span>
<span data-ttu-id="1b76d-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b76d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b76d-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b76d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b76d-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b76d-146">INPUTS</span></span>

### <span data-ttu-id="1b76d-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b76d-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="1b76d-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1b76d-148">System.Int32</span></span>

### <span data-ttu-id="1b76d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1b76d-149">System.String</span></span>

### <span data-ttu-id="1b76d-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="1b76d-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="1b76d-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1b76d-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="1b76d-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1b76d-152">OUTPUTS</span></span>

### <span data-ttu-id="1b76d-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b76d-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b76d-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="1b76d-154">NOTES</span></span>

## <span data-ttu-id="1b76d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b76d-155">RELATED LINKS</span></span>

[<span data-ttu-id="1b76d-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b76d-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1b76d-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b76d-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1b76d-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b76d-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1b76d-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b76d-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
