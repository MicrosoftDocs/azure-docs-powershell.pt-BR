---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 482f729f0ee3fa3efc6a78a1bc2b5fbbd3fe1d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772199"
---
# <span data-ttu-id="70bb5-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70bb5-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="70bb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="70bb5-103">Define uma configuração de regra de saída para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="70bb5-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="70bb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70bb5-104">SYNTAX</span></span>

### <span data-ttu-id="70bb5-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="70bb5-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bb5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="70bb5-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70bb5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70bb5-107">DESCRIPTION</span></span>
<span data-ttu-id="70bb5-108">O cmdlet **set-AzLoadBalancerOutboundRuleConfig** define uma configuração de regra de saída para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="70bb5-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="70bb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70bb5-109">EXAMPLES</span></span>

### <span data-ttu-id="70bb5-110">Exemplo 1: modificar a configuração da regra de saída em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="70bb5-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="70bb5-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="70bb5-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="70bb5-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzLoadBalancerOutboundRuleConfig, o que adiciona uma configuração de regra de saída a ele.</span><span class="sxs-lookup"><span data-stu-id="70bb5-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="70bb5-113">O terceiro comando passa o balanceador de carga para **set-AzLoadBalancerOutboundRuleConfig** , que salva e atualiza a configuração da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="70bb5-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="70bb5-114">OS</span><span class="sxs-lookup"><span data-stu-id="70bb5-114">PARAMETERS</span></span>

### <span data-ttu-id="70bb5-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="70bb5-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="70bb5-116">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="70bb5-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="70bb5-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="70bb5-117">-BackendAddressPool</span></span>
<span data-ttu-id="70bb5-118">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="70bb5-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="70bb5-119">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="70bb5-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="70bb5-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="70bb5-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="70bb5-121">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="70bb5-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="70bb5-122">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="70bb5-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="70bb5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bb5-123">-DefaultProfile</span></span>
<span data-ttu-id="70bb5-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70bb5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70bb5-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="70bb5-125">-EnableTcpReset</span></span>
<span data-ttu-id="70bb5-126">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="70bb5-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="70bb5-127">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="70bb5-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="70bb5-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="70bb5-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="70bb5-129">Os endereços IP de front-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="70bb5-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="70bb5-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="70bb5-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="70bb5-131">O tempo limite para a conexão ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="70bb5-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="70bb5-132">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="70bb5-132">-LoadBalancer</span></span>
<span data-ttu-id="70bb5-133">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="70bb5-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="70bb5-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="70bb5-134">-Name</span></span>
<span data-ttu-id="70bb5-135">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="70bb5-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="70bb5-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="70bb5-136">-Protocol</span></span>
<span data-ttu-id="70bb5-137">Protocolo-TCP, UDP ou todos</span><span class="sxs-lookup"><span data-stu-id="70bb5-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="70bb5-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70bb5-138">-Confirm</span></span>
<span data-ttu-id="70bb5-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70bb5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70bb5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70bb5-140">-WhatIf</span></span>
<span data-ttu-id="70bb5-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70bb5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70bb5-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70bb5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70bb5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bb5-143">CommonParameters</span></span>
<span data-ttu-id="70bb5-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70bb5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bb5-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bb5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bb5-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70bb5-146">INPUTS</span></span>

### <span data-ttu-id="70bb5-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70bb5-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="70bb5-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="70bb5-148">System.Int32</span></span>

### <span data-ttu-id="70bb5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="70bb5-149">System.String</span></span>

### <span data-ttu-id="70bb5-150">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="70bb5-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="70bb5-151">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="70bb5-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="70bb5-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70bb5-152">OUTPUTS</span></span>

### <span data-ttu-id="70bb5-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70bb5-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="70bb5-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70bb5-154">NOTES</span></span>

## <span data-ttu-id="70bb5-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70bb5-155">RELATED LINKS</span></span>

[<span data-ttu-id="70bb5-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70bb5-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="70bb5-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70bb5-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="70bb5-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70bb5-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="70bb5-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="70bb5-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
