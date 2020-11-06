---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: a584d473354fd900b117f5661dc738b239f3a92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431345"
---
# <span data-ttu-id="2a0e1-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a0e1-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="2a0e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0e1-103">Define o estado da meta para uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a0e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a0e1-104">SYNTAX</span></span>

### <span data-ttu-id="2a0e1-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a0e1-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a0e1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a0e1-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0e1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a0e1-107">DESCRIPTION</span></span>
<span data-ttu-id="2a0e1-108">O cmdlet **set-AzureRmLoadBalancerRuleConfig** define o estado da meta para uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="2a0e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a0e1-109">EXAMPLES</span></span>

### <span data-ttu-id="2a0e1-110">Exemplo 1: modificar uma configuração de regra de balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="2a0e1-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="2a0e1-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2a0e1-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzureRmLoadBalancerRuleConfig, o que adiciona uma regra chamada NewRule a ela.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="2a0e1-113">O terceiro comando passa o balanceador de carga para **set-AzureRmLoadBalancerRuleConfig** , que define a nova configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="2a0e1-114">Observe que a configuração não habilita um endereço IP flutuante, que foi habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="2a0e1-115">OS</span><span class="sxs-lookup"><span data-stu-id="2a0e1-115">PARAMETERS</span></span>

### <span data-ttu-id="2a0e1-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a0e1-116">-BackendAddressPool</span></span>
<span data-ttu-id="2a0e1-117">Especifica um objeto **BackendAddressPool** para associar a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="2a0e1-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2a0e1-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="2a0e1-119">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2a0e1-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="2a0e1-120">-BackendPort</span></span>
<span data-ttu-id="2a0e1-121">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="2a0e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0e1-122">-DefaultProfile</span></span>
<span data-ttu-id="2a0e1-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0e1-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="2a0e1-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="2a0e1-125">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="2a0e1-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="2a0e1-126">-EnableFloatingIP</span></span>
<span data-ttu-id="2a0e1-127">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="2a0e1-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2a0e1-128">-EnableTcpReset</span></span>
<span data-ttu-id="2a0e1-129">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="2a0e1-130">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2a0e1-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a0e1-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2a0e1-132">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2a0e1-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2a0e1-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="2a0e1-134">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="2a0e1-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="2a0e1-135">-FrontendPort</span></span>
<span data-ttu-id="2a0e1-136">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2a0e1-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2a0e1-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2a0e1-138">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="2a0e1-139">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="2a0e1-139">-LoadBalancer</span></span>
<span data-ttu-id="2a0e1-140">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-140">Specifies a load balancer.</span></span>
<span data-ttu-id="2a0e1-141">Esse cmdlet define a configuração de regra de estado de meta para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-141">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a0e1-142">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="2a0e1-142">-LoadDistribution</span></span>
<span data-ttu-id="2a0e1-143">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-143">Specifies a load distribution.</span></span>
<span data-ttu-id="2a0e1-144">Os valores aceitáveis para esse parâmetro são: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="2a0e1-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a0e1-145">-Name</span></span>
<span data-ttu-id="2a0e1-146">Especifica o nome de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="2a0e1-147">-Teste</span><span class="sxs-lookup"><span data-stu-id="2a0e1-147">-Probe</span></span>
<span data-ttu-id="2a0e1-148">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2a0e1-149">-Probeid</span><span class="sxs-lookup"><span data-stu-id="2a0e1-149">-ProbeId</span></span>
<span data-ttu-id="2a0e1-150">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2a0e1-151">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="2a0e1-151">-Protocol</span></span>
<span data-ttu-id="2a0e1-152">Especifica o protocolo que corresponde a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="2a0e1-153">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="2a0e1-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2a0e1-154">-Confirm</span></span>
<span data-ttu-id="2a0e1-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a0e1-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0e1-156">-WhatIf</span></span>
<span data-ttu-id="2a0e1-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a0e1-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a0e1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0e1-159">CommonParameters</span></span>
<span data-ttu-id="2a0e1-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0e1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0e1-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a0e1-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0e1-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a0e1-162">INPUTS</span></span>

### <span data-ttu-id="2a0e1-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a0e1-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="2a0e1-164">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a0e1-164">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="2a0e1-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a0e1-165">OUTPUTS</span></span>

### <span data-ttu-id="2a0e1-166">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a0e1-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2a0e1-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a0e1-167">NOTES</span></span>

## <span data-ttu-id="2a0e1-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a0e1-168">RELATED LINKS</span></span>

[<span data-ttu-id="2a0e1-169">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a0e1-169">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2a0e1-170">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a0e1-170">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2a0e1-171">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a0e1-171">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2a0e1-172">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a0e1-172">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="2a0e1-173">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a0e1-173">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


