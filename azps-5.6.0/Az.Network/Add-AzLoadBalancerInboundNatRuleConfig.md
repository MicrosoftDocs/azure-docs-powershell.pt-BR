---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 44f8304ce1ee79c114dc4054c8dd7fff3dcd22fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892465"
---
# <span data-ttu-id="674b5-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="674b5-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="674b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="674b5-102">SYNOPSIS</span></span>
<span data-ttu-id="674b5-103">Adiciona uma configuração de regra NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="674b5-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="674b5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="674b5-104">SYNTAX</span></span>

### <span data-ttu-id="674b5-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="674b5-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="674b5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="674b5-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="674b5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="674b5-107">DESCRIPTION</span></span>
<span data-ttu-id="674b5-108">O cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** adiciona uma configuração de regra nat (conversão de endereço de rede de entrada) a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="674b5-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="674b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="674b5-109">EXAMPLES</span></span>

### <span data-ttu-id="674b5-110">Exemplo 1: Adicionar uma configuração de regra NAT de entrada a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="674b5-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="674b5-111">O primeiro comando obtém o balanceador de carga chamado MyloadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="674b5-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="674b5-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para **Add-AzLoadBalancerInboundNatRuleConfig**, que adiciona uma configuração de regra NAT de entrada ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="674b5-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>
<span data-ttu-id="674b5-113">O último comando define a configuração como loadbalancer, se você não executar Set-AzLoadBalancer, suas alterações não serão aplicadas ao loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="674b5-113">The last command sets the configuration to the loadbalancer, if you don't perform Set-AzLoadBalancer, your changes will not be applied to the loadbalancer.</span></span>

## <span data-ttu-id="674b5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="674b5-114">PARAMETERS</span></span>

### <span data-ttu-id="674b5-115">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="674b5-115">-BackendPort</span></span>
<span data-ttu-id="674b5-116">Especifica a porta de back-end para tráfego de uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="674b5-116">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="674b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="674b5-117">-DefaultProfile</span></span>
<span data-ttu-id="674b5-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="674b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="674b5-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="674b5-119">-EnableFloatingIP</span></span>
<span data-ttu-id="674b5-120">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="674b5-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="674b5-121">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="674b5-121">-EnableTcpReset</span></span>
<span data-ttu-id="674b5-122">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="674b5-122">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="674b5-123">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="674b5-123">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="674b5-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="674b5-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="674b5-125">Especifica uma lista de endereços IP front-end para associar a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="674b5-125">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674b5-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="674b5-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="674b5-127">Especifica uma ID para uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="674b5-127">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674b5-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="674b5-128">-FrontendPort</span></span>
<span data-ttu-id="674b5-129">Especifica a porta front-end que é corresponder a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="674b5-129">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="674b5-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="674b5-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="674b5-131">Especifica o período de tempo, em minutos, que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="674b5-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="674b5-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="674b5-132">-LoadBalancer</span></span>
<span data-ttu-id="674b5-133">Especifica um **objeto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="674b5-133">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="674b5-134">Este cmdlet adiciona uma configuração de regra NAT de entrada ao balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="674b5-134">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="674b5-135">-Name</span><span class="sxs-lookup"><span data-stu-id="674b5-135">-Name</span></span>
<span data-ttu-id="674b5-136">Especifica o nome da configuração de regra NAT de entrada a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="674b5-136">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="674b5-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="674b5-137">-Protocol</span></span>
<span data-ttu-id="674b5-138">Especifica o protocolo que é correspondente por uma regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="674b5-138">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="674b5-139">Os valores aceitáveis para este parâmetro são: Tcp ou Udp.</span><span class="sxs-lookup"><span data-stu-id="674b5-139">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674b5-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="674b5-140">-Confirm</span></span>
<span data-ttu-id="674b5-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="674b5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="674b5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="674b5-142">-WhatIf</span></span>
<span data-ttu-id="674b5-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="674b5-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="674b5-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="674b5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="674b5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674b5-145">CommonParameters</span></span>
<span data-ttu-id="674b5-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="674b5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674b5-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="674b5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674b5-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="674b5-148">INPUTS</span></span>

### <span data-ttu-id="674b5-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="674b5-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="674b5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="674b5-150">System.String</span></span>

### <span data-ttu-id="674b5-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="674b5-151">System.Int32</span></span>

### <span data-ttu-id="674b5-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="674b5-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="674b5-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="674b5-153">OUTPUTS</span></span>

### <span data-ttu-id="674b5-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="674b5-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="674b5-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="674b5-155">NOTES</span></span>

## <span data-ttu-id="674b5-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="674b5-156">RELATED LINKS</span></span>

[<span data-ttu-id="674b5-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="674b5-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="674b5-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="674b5-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="674b5-159">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="674b5-159">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="674b5-160">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="674b5-160">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="674b5-161">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="674b5-161">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="674b5-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="674b5-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


