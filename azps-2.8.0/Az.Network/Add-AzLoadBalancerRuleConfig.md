---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: e6df07d9d3f133390c6c6d14e092e7983324f753
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772088"
---
# <span data-ttu-id="4dae0-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4dae0-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4dae0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4dae0-102">SYNOPSIS</span></span>
<span data-ttu-id="4dae0-103">Adiciona uma configuração de regra a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="4dae0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dae0-104">SYNTAX</span></span>

### <span data-ttu-id="4dae0-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="4dae0-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dae0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4dae0-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dae0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4dae0-107">DESCRIPTION</span></span>
<span data-ttu-id="4dae0-108">O cmdlet **Add-AzLoadBalancerRuleConfig** adiciona uma configuração de regra a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="4dae0-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="4dae0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4dae0-109">EXAMPLES</span></span>

### <span data-ttu-id="4dae0-110">Exemplo 1: adicionar uma configuração de regra a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="4dae0-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="4dae0-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="4dae0-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="4dae0-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para **Adicionar-AzLoadBalancerRuleConfig** , o que adiciona a configuração de regra chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="4dae0-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="4dae0-113">O terceiro comando atualizará o balanceador de carga no Azure com a nova configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="4dae0-114">OS</span><span class="sxs-lookup"><span data-stu-id="4dae0-114">PARAMETERS</span></span>

### <span data-ttu-id="4dae0-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4dae0-115">-BackendAddressPool</span></span>
<span data-ttu-id="4dae0-116">Especifica o pool de endereços back-end a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4dae0-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="4dae0-118">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4dae0-119">-BackendPort</span></span>
<span data-ttu-id="4dae0-120">Especifica a porta back-end para tráfego que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dae0-121">-DefaultProfile</span></span>
<span data-ttu-id="4dae0-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4dae0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dae0-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="4dae0-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="4dae0-124">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="4dae0-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4dae0-125">-EnableFloatingIP</span></span>
<span data-ttu-id="4dae0-126">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="4dae0-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4dae0-127">-EnableTcpReset</span></span>
<span data-ttu-id="4dae0-128">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="4dae0-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4dae0-129">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="4dae0-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4dae0-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4dae0-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4dae0-131">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4dae0-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4dae0-133">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="4dae0-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="4dae0-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4dae0-134">-FrontendPort</span></span>
<span data-ttu-id="4dae0-135">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4dae0-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4dae0-137">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido no balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="4dae0-138">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="4dae0-138">-LoadBalancer</span></span>
<span data-ttu-id="4dae0-139">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="4dae0-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="4dae0-140">Esse cmdlet adiciona uma configuração de regra ao balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4dae0-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4dae0-141">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="4dae0-141">-LoadDistribution</span></span>
<span data-ttu-id="4dae0-142">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="4dae0-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dae0-143">-Name</span></span>
<span data-ttu-id="4dae0-144">Especifica o nome da configuração de regra do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-145">-Teste</span><span class="sxs-lookup"><span data-stu-id="4dae0-145">-Probe</span></span>
<span data-ttu-id="4dae0-146">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-147">-Probeid</span><span class="sxs-lookup"><span data-stu-id="4dae0-147">-ProbeId</span></span>
<span data-ttu-id="4dae0-148">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4dae0-149">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="4dae0-149">-Protocol</span></span>
<span data-ttu-id="4dae0-150">Especifica o protocolo que corresponde a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4dae0-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="4dae0-151">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="4dae0-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="4dae0-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4dae0-152">-Confirm</span></span>
<span data-ttu-id="4dae0-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dae0-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dae0-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dae0-154">-WhatIf</span></span>
<span data-ttu-id="4dae0-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4dae0-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4dae0-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4dae0-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dae0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dae0-157">CommonParameters</span></span>
<span data-ttu-id="4dae0-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dae0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dae0-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dae0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dae0-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4dae0-160">INPUTS</span></span>

### <span data-ttu-id="4dae0-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4dae0-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="4dae0-162">System. String</span><span class="sxs-lookup"><span data-stu-id="4dae0-162">System.String</span></span>

### <span data-ttu-id="4dae0-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4dae0-163">System.Int32</span></span>

### <span data-ttu-id="4dae0-164">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4dae0-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="4dae0-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4dae0-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="4dae0-166">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="4dae0-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="4dae0-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4dae0-167">OUTPUTS</span></span>

### <span data-ttu-id="4dae0-168">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4dae0-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4dae0-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4dae0-169">NOTES</span></span>

## <span data-ttu-id="4dae0-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4dae0-170">RELATED LINKS</span></span>

[<span data-ttu-id="4dae0-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4dae0-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4dae0-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4dae0-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4dae0-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4dae0-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4dae0-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4dae0-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4dae0-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4dae0-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

