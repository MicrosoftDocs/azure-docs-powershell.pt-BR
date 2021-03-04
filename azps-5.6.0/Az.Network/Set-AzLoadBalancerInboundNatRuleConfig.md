---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a0d5adbc1e3fb2b38ded91431ab0cf349c541ebd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886872"
---
# <span data-ttu-id="53bbb-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53bbb-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="53bbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="53bbb-103">Define uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53bbb-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="53bbb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="53bbb-104">SYNTAX</span></span>

### <span data-ttu-id="53bbb-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="53bbb-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bbb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="53bbb-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53bbb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="53bbb-107">DESCRIPTION</span></span>
<span data-ttu-id="53bbb-108">O cmdlet **Set-AzLoadBalancerInboundNatRuleConfig** define uma configuração de regra nat (conversão de endereço de rede de entrada) para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="53bbb-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="53bbb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53bbb-109">EXAMPLES</span></span>

### <span data-ttu-id="53bbb-110">Exemplo 1: Modificar a configuração da regra NAT de entrada em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="53bbb-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="53bbb-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="53bbb-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="53bbb-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para Add-AzLoadBalancerInboundNatRuleConfig, que adiciona uma configuração de regra NAT de entrada a ela.</span><span class="sxs-lookup"><span data-stu-id="53bbb-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="53bbb-113">O terceiro comando passa o balanceador de carga para **Set-AzLoadBalancerInboundNatRuleConfig**, que salva e atualiza a configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="53bbb-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="53bbb-114">Observe que a configuração da regra foi definida sem habilitar o IP flutuante, que tinha sido habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="53bbb-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="53bbb-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="53bbb-115">PARAMETERS</span></span>

### <span data-ttu-id="53bbb-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="53bbb-116">-BackendPort</span></span>
<span data-ttu-id="53bbb-117">Especifica a porta de back-end para tráfego que é corresponder a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="53bbb-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="53bbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bbb-118">-DefaultProfile</span></span>
<span data-ttu-id="53bbb-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="53bbb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53bbb-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="53bbb-120">-EnableFloatingIP</span></span>
<span data-ttu-id="53bbb-121">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="53bbb-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="53bbb-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="53bbb-122">-EnableTcpReset</span></span>
<span data-ttu-id="53bbb-123">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="53bbb-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="53bbb-124">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="53bbb-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="53bbb-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="53bbb-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="53bbb-126">Especifica uma lista de endereços IP front-end para associar a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="53bbb-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="53bbb-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="53bbb-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="53bbb-128">Especifica a ID de uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="53bbb-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="53bbb-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="53bbb-129">-FrontendPort</span></span>
<span data-ttu-id="53bbb-130">Especifica a porta front-end que é corresponder a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53bbb-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="53bbb-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="53bbb-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="53bbb-132">Especifica o período de tempo, em minutos, que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53bbb-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="53bbb-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53bbb-133">-LoadBalancer</span></span>
<span data-ttu-id="53bbb-134">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53bbb-134">Specifies a load balancer.</span></span>
<span data-ttu-id="53bbb-135">Este cmdlet define uma configuração de regra NAT de entrada para o balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="53bbb-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="53bbb-136">-Name</span><span class="sxs-lookup"><span data-stu-id="53bbb-136">-Name</span></span>
<span data-ttu-id="53bbb-137">Especifica o nome de uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="53bbb-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="53bbb-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="53bbb-138">-Protocol</span></span>
<span data-ttu-id="53bbb-139">Especifica o protocolo que é correspondente por uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="53bbb-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="53bbb-140">Os valores aceitáveis para este parâmetro são: Tcp ou Udp.</span><span class="sxs-lookup"><span data-stu-id="53bbb-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="53bbb-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53bbb-141">-Confirm</span></span>
<span data-ttu-id="53bbb-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53bbb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53bbb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53bbb-143">-WhatIf</span></span>
<span data-ttu-id="53bbb-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53bbb-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53bbb-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53bbb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53bbb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bbb-146">CommonParameters</span></span>
<span data-ttu-id="53bbb-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bbb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bbb-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bbb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bbb-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53bbb-149">INPUTS</span></span>

### <span data-ttu-id="53bbb-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53bbb-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="53bbb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="53bbb-151">System.String</span></span>

### <span data-ttu-id="53bbb-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="53bbb-152">System.Int32</span></span>

### <span data-ttu-id="53bbb-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53bbb-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="53bbb-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="53bbb-154">OUTPUTS</span></span>

### <span data-ttu-id="53bbb-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53bbb-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="53bbb-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="53bbb-156">NOTES</span></span>

## <span data-ttu-id="53bbb-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53bbb-157">RELATED LINKS</span></span>

[<span data-ttu-id="53bbb-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53bbb-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="53bbb-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53bbb-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="53bbb-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53bbb-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="53bbb-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53bbb-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="53bbb-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53bbb-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


