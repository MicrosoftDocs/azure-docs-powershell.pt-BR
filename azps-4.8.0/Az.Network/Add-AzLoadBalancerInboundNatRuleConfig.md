---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111610"
---
# <span data-ttu-id="f41c4-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f41c4-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f41c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f41c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f41c4-103">Adiciona uma configuração de regra NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f41c4-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="f41c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f41c4-104">SYNTAX</span></span>

### <span data-ttu-id="f41c4-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f41c4-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f41c4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f41c4-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f41c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f41c4-107">DESCRIPTION</span></span>
<span data-ttu-id="f41c4-108">O cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** adiciona uma configuração de regra NAT (conversão de endereços de rede) de entrada a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="f41c4-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f41c4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f41c4-109">EXAMPLES</span></span>

### <span data-ttu-id="f41c4-110">Exemplo 1: adicionar uma configuração de regra NAT de entrada a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f41c4-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="f41c4-111">O primeiro comando obtém o balanceador de carga chamado MyloadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="f41c4-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f41c4-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para **Add-AzLoadBalancerInboundNatRuleConfig** , que adiciona uma configuração de regra NAT de entrada ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f41c4-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="f41c4-113">OS</span><span class="sxs-lookup"><span data-stu-id="f41c4-113">PARAMETERS</span></span>

### <span data-ttu-id="f41c4-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f41c4-114">-BackendPort</span></span>
<span data-ttu-id="f41c4-115">Especifica a porta de back-end para o tráfego correspondente a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="f41c4-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="f41c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41c4-116">-DefaultProfile</span></span>
<span data-ttu-id="f41c4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f41c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f41c4-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f41c4-118">-EnableFloatingIP</span></span>
<span data-ttu-id="f41c4-119">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="f41c4-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f41c4-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f41c4-120">-EnableTcpReset</span></span>
<span data-ttu-id="f41c4-121">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="f41c4-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="f41c4-122">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="f41c4-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f41c4-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f41c4-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f41c4-124">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="f41c4-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f41c4-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f41c4-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f41c4-126">Especifica uma ID para uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="f41c4-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f41c4-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f41c4-127">-FrontendPort</span></span>
<span data-ttu-id="f41c4-128">Especifica a porta de front-end que corresponde a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="f41c4-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="f41c4-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f41c4-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f41c4-130">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f41c4-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f41c4-131">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="f41c4-131">-LoadBalancer</span></span>
<span data-ttu-id="f41c4-132">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="f41c4-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f41c4-133">Esse cmdlet adiciona uma configuração de regra NAT de entrada ao balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f41c4-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f41c4-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="f41c4-134">-Name</span></span>
<span data-ttu-id="f41c4-135">Especifica o nome da configuração de regra NAT de entrada a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="f41c4-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="f41c4-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f41c4-136">-Protocol</span></span>
<span data-ttu-id="f41c4-137">Especifica o protocolo que corresponde a uma regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="f41c4-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="f41c4-138">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="f41c4-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f41c4-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f41c4-139">-Confirm</span></span>
<span data-ttu-id="f41c4-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f41c4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f41c4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f41c4-141">-WhatIf</span></span>
<span data-ttu-id="f41c4-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f41c4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f41c4-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f41c4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f41c4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41c4-144">CommonParameters</span></span>
<span data-ttu-id="f41c4-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f41c4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41c4-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f41c4-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41c4-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f41c4-147">INPUTS</span></span>

### <span data-ttu-id="f41c4-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f41c4-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f41c4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f41c4-149">System.String</span></span>

### <span data-ttu-id="f41c4-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f41c4-150">System.Int32</span></span>

### <span data-ttu-id="f41c4-151">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f41c4-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="f41c4-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f41c4-152">OUTPUTS</span></span>

### <span data-ttu-id="f41c4-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f41c4-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f41c4-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f41c4-154">NOTES</span></span>

## <span data-ttu-id="f41c4-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f41c4-155">RELATED LINKS</span></span>

[<span data-ttu-id="f41c4-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f41c4-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f41c4-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f41c4-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f41c4-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f41c4-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f41c4-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f41c4-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f41c4-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f41c4-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="f41c4-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f41c4-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


