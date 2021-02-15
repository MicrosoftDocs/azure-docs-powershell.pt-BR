---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115204"
---
# <span data-ttu-id="0cf43-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0cf43-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="0cf43-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cf43-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf43-103">Adiciona uma configuração de regra de saída a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0cf43-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="0cf43-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cf43-104">SYNTAX</span></span>

### <span data-ttu-id="0cf43-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0cf43-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cf43-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf43-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf43-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cf43-107">DESCRIPTION</span></span>
<span data-ttu-id="0cf43-108">O cmdlet **Add-AzLoadBalancerOutboundRuleConfig** adiciona uma configuração de regra de saída a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf43-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="0cf43-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0cf43-109">EXAMPLES</span></span>

### <span data-ttu-id="0cf43-110">Exemplo 1: Adicionar uma configuração de regra de saída a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="0cf43-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="0cf43-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="0cf43-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0cf43-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para **Add-AzLoadBalancerOutboundRuleConfig,** que adiciona uma configuração de regra de saída ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0cf43-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="0cf43-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cf43-113">PARAMETERS</span></span>

### <span data-ttu-id="0cf43-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="0cf43-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="0cf43-115">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="0cf43-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="0cf43-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0cf43-116">-BackendAddressPool</span></span>
<span data-ttu-id="0cf43-117">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="0cf43-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="0cf43-118">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="0cf43-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="0cf43-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0cf43-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="0cf43-120">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="0cf43-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="0cf43-121">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="0cf43-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="0cf43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf43-122">-DefaultProfile</span></span>
<span data-ttu-id="0cf43-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf43-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cf43-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0cf43-124">-EnableTcpReset</span></span>
<span data-ttu-id="0cf43-125">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="0cf43-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="0cf43-126">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="0cf43-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0cf43-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0cf43-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0cf43-128">Os endereços IP Frontend do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0cf43-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="0cf43-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0cf43-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0cf43-130">O tempo de tempo para a conexão Ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="0cf43-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="0cf43-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0cf43-131">-LoadBalancer</span></span>
<span data-ttu-id="0cf43-132">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0cf43-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="0cf43-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="0cf43-133">-Name</span></span>
<span data-ttu-id="0cf43-134">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="0cf43-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="0cf43-135">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="0cf43-135">-Protocol</span></span>
<span data-ttu-id="0cf43-136">Protocolo - TCP, UDP ou Todos</span><span class="sxs-lookup"><span data-stu-id="0cf43-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="0cf43-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0cf43-137">-Confirm</span></span>
<span data-ttu-id="0cf43-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cf43-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf43-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf43-139">-WhatIf</span></span>
<span data-ttu-id="0cf43-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0cf43-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf43-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0cf43-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf43-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf43-142">CommonParameters</span></span>
<span data-ttu-id="0cf43-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf43-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf43-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf43-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf43-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="0cf43-145">INPUTS</span></span>

### <span data-ttu-id="0cf43-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0cf43-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0cf43-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0cf43-147">System.Int32</span></span>

### <span data-ttu-id="0cf43-148">System.String</span><span class="sxs-lookup"><span data-stu-id="0cf43-148">System.String</span></span>

### <span data-ttu-id="0cf43-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="0cf43-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="0cf43-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0cf43-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="0cf43-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="0cf43-151">OUTPUTS</span></span>

### <span data-ttu-id="0cf43-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0cf43-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0cf43-153">Notas</span><span class="sxs-lookup"><span data-stu-id="0cf43-153">NOTES</span></span>

## <span data-ttu-id="0cf43-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cf43-154">RELATED LINKS</span></span>

[<span data-ttu-id="0cf43-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0cf43-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0cf43-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0cf43-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0cf43-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0cf43-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="0cf43-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0cf43-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
