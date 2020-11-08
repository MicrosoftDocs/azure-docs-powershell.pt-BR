---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114775"
---
# <span data-ttu-id="b1735-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1735-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="b1735-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1735-102">SYNOPSIS</span></span>
<span data-ttu-id="b1735-103">Atualiza uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b1735-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1735-104">SYNTAX</span></span>

### <span data-ttu-id="b1735-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="b1735-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1735-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1735-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1735-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1735-107">DESCRIPTION</span></span>
<span data-ttu-id="b1735-108">O cmdlet **set-AzLoadBalancerRuleConfig** atualiza uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b1735-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1735-109">EXAMPLES</span></span>

### <span data-ttu-id="b1735-110">Exemplo 1: modificar uma configuração de regra de balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="b1735-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="b1735-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="b1735-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="b1735-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzLoadBalancerRuleConfig, o que adiciona uma regra chamada NewRule a ela.</span><span class="sxs-lookup"><span data-stu-id="b1735-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="b1735-113">O terceiro comando passa o balanceador de carga para **set-AzLoadBalancerRuleConfig** , que define a nova configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="b1735-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="b1735-114">Observe que a configuração não habilita um endereço IP flutuante, que foi habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="b1735-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="b1735-115">OS</span><span class="sxs-lookup"><span data-stu-id="b1735-115">PARAMETERS</span></span>

### <span data-ttu-id="b1735-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b1735-116">-BackendAddressPool</span></span>
<span data-ttu-id="b1735-117">Especifica um objeto **BackendAddressPool** para associar a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1735-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b1735-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="b1735-119">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b1735-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b1735-120">-BackendPort</span></span>
<span data-ttu-id="b1735-121">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="b1735-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="b1735-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1735-122">-DefaultProfile</span></span>
<span data-ttu-id="b1735-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1735-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1735-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="b1735-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="b1735-125">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="b1735-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b1735-126">-EnableFloatingIP</span></span>
<span data-ttu-id="b1735-127">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="b1735-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b1735-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b1735-128">-EnableTcpReset</span></span>
<span data-ttu-id="b1735-129">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="b1735-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b1735-130">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="b1735-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b1735-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1735-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b1735-132">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b1735-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b1735-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b1735-134">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="b1735-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b1735-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b1735-135">-FrontendPort</span></span>
<span data-ttu-id="b1735-136">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b1735-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b1735-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b1735-138">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b1735-139">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="b1735-139">-LoadBalancer</span></span>
<span data-ttu-id="b1735-140">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-140">Specifies a load balancer.</span></span>
<span data-ttu-id="b1735-141">Esse cmdlet atualiza uma configuração de regra para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b1735-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1735-142">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="b1735-142">-LoadDistribution</span></span>
<span data-ttu-id="b1735-143">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-143">Specifies a load distribution.</span></span>
<span data-ttu-id="b1735-144">Os valores aceitáveis para esse parâmetro são: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="b1735-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="b1735-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1735-145">-Name</span></span>
<span data-ttu-id="b1735-146">Especifica o nome de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="b1735-147">-Teste</span><span class="sxs-lookup"><span data-stu-id="b1735-147">-Probe</span></span>
<span data-ttu-id="b1735-148">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1735-149">-Probeid</span><span class="sxs-lookup"><span data-stu-id="b1735-149">-ProbeId</span></span>
<span data-ttu-id="b1735-150">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b1735-151">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="b1735-151">-Protocol</span></span>
<span data-ttu-id="b1735-152">Especifica o protocolo que corresponde a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="b1735-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="b1735-153">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="b1735-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b1735-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1735-154">-Confirm</span></span>
<span data-ttu-id="b1735-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1735-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1735-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1735-156">-WhatIf</span></span>
<span data-ttu-id="b1735-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1735-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1735-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1735-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1735-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1735-159">CommonParameters</span></span>
<span data-ttu-id="b1735-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1735-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1735-161">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1735-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1735-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1735-162">INPUTS</span></span>

### <span data-ttu-id="b1735-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b1735-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b1735-164">System. String</span><span class="sxs-lookup"><span data-stu-id="b1735-164">System.String</span></span>

### <span data-ttu-id="b1735-165">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b1735-165">System.Int32</span></span>

### <span data-ttu-id="b1735-166">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1735-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="b1735-167">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b1735-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="b1735-168">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="b1735-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="b1735-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1735-169">OUTPUTS</span></span>

### <span data-ttu-id="b1735-170">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b1735-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b1735-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1735-171">NOTES</span></span>

## <span data-ttu-id="b1735-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1735-172">RELATED LINKS</span></span>

[<span data-ttu-id="b1735-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1735-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1735-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1735-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1735-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1735-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1735-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1735-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1735-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1735-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


