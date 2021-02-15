---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111549"
---
# <span data-ttu-id="f644f-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f644f-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="f644f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f644f-102">SYNOPSIS</span></span>
<span data-ttu-id="f644f-103">Define uma configuração de regra de saída para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f644f-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f644f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f644f-104">SYNTAX</span></span>

### <span data-ttu-id="f644f-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f644f-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f644f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f644f-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f644f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f644f-107">DESCRIPTION</span></span>
<span data-ttu-id="f644f-108">O cmdlet **Set-AzLoadBalancerOutboundRuleConfig** define uma configuração de regra de saída para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="f644f-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f644f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f644f-109">EXAMPLES</span></span>

### <span data-ttu-id="f644f-110">Exemplo 1: Modificar a configuração da regra de saída em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f644f-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="f644f-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb dados.</span><span class="sxs-lookup"><span data-stu-id="f644f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="f644f-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para Add-AzLoadBalancerOutboundRuleConfig, que adiciona uma configuração de regra de saída a ele.</span><span class="sxs-lookup"><span data-stu-id="f644f-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="f644f-113">O terceiro comando passa o balanceador de carga para **Set-AzLoadBalancerOutboundRuleConfig,** que salva e atualiza a configuração da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="f644f-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="f644f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f644f-114">PARAMETERS</span></span>

### <span data-ttu-id="f644f-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="f644f-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="f644f-116">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="f644f-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="f644f-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f644f-117">-BackendAddressPool</span></span>
<span data-ttu-id="f644f-118">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="f644f-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="f644f-119">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="f644f-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="f644f-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f644f-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="f644f-121">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="f644f-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="f644f-122">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="f644f-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="f644f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f644f-123">-DefaultProfile</span></span>
<span data-ttu-id="f644f-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f644f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f644f-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f644f-125">-EnableTcpReset</span></span>
<span data-ttu-id="f644f-126">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="f644f-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="f644f-127">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="f644f-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f644f-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f644f-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f644f-129">Os endereços IP Frontend do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f644f-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="f644f-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f644f-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f644f-131">O tempo de tempo para a conexão Ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="f644f-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="f644f-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f644f-132">-LoadBalancer</span></span>
<span data-ttu-id="f644f-133">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f644f-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="f644f-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="f644f-134">-Name</span></span>
<span data-ttu-id="f644f-135">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="f644f-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="f644f-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f644f-136">-Protocol</span></span>
<span data-ttu-id="f644f-137">Protocolo - TCP, UDP ou Todos</span><span class="sxs-lookup"><span data-stu-id="f644f-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="f644f-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f644f-138">-Confirm</span></span>
<span data-ttu-id="f644f-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f644f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f644f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f644f-140">-WhatIf</span></span>
<span data-ttu-id="f644f-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f644f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f644f-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f644f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f644f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f644f-143">CommonParameters</span></span>
<span data-ttu-id="f644f-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f644f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f644f-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f644f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f644f-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="f644f-146">INPUTS</span></span>

### <span data-ttu-id="f644f-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f644f-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f644f-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f644f-148">System.Int32</span></span>

### <span data-ttu-id="f644f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f644f-149">System.String</span></span>

### <span data-ttu-id="f644f-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="f644f-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="f644f-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f644f-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f644f-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="f644f-152">OUTPUTS</span></span>

### <span data-ttu-id="f644f-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f644f-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f644f-154">Notas</span><span class="sxs-lookup"><span data-stu-id="f644f-154">NOTES</span></span>

## <span data-ttu-id="f644f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f644f-155">RELATED LINKS</span></span>

[<span data-ttu-id="f644f-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f644f-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f644f-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f644f-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f644f-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f644f-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="f644f-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f644f-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
