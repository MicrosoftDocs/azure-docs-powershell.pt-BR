---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118259"
---
# <span data-ttu-id="3f128-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f128-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="3f128-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f128-102">SYNOPSIS</span></span>
<span data-ttu-id="3f128-103">Atualiza uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="3f128-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f128-104">SYNTAX</span></span>

### <span data-ttu-id="3f128-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3f128-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f128-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f128-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f128-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f128-107">DESCRIPTION</span></span>
<span data-ttu-id="3f128-108">O cmdlet **Set-AzLoadBalancerRuleConfig** atualiza uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="3f128-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f128-109">EXAMPLES</span></span>

### <span data-ttu-id="3f128-110">Exemplo 1: Modificar uma configuração de regra de balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="3f128-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="3f128-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb dados.</span><span class="sxs-lookup"><span data-stu-id="3f128-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="3f128-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para Add-AzLoadBalancerRuleConfig, que adiciona uma regra chamada NewRule a ele.</span><span class="sxs-lookup"><span data-stu-id="3f128-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="3f128-113">O terceiro comando passa o balanceador de carga **para Set-AzLoadBalancerRuleConfig,** que define a nova configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="3f128-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="3f128-114">Observe que a configuração não habilita um endereço IP flutuante, que tinha sido habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="3f128-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="3f128-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f128-115">PARAMETERS</span></span>

### <span data-ttu-id="3f128-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f128-116">-BackendAddressPool</span></span>
<span data-ttu-id="3f128-117">Especifica um objeto **BackendAddressPool** para associar a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="3f128-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3f128-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="3f128-119">Especifica a ID de um objeto **BackendAddressPool** para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3f128-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="3f128-120">-BackendPort</span></span>
<span data-ttu-id="3f128-121">Especifica a porta de back-end do tráfego que é corresponder a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="3f128-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="3f128-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f128-122">-DefaultProfile</span></span>
<span data-ttu-id="3f128-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3f128-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f128-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="3f128-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="3f128-125">Configura o SNAT para as VMs no pool de back-end para usar o endereço de IP público especificado na frente da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="3f128-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="3f128-126">-EnableFloatingIP</span></span>
<span data-ttu-id="3f128-127">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="3f128-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="3f128-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="3f128-128">-EnableTcpReset</span></span>
<span data-ttu-id="3f128-129">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="3f128-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="3f128-130">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="3f128-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="3f128-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f128-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="3f128-132">Especifica uma lista de endereços IP front-end para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3f128-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3f128-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="3f128-134">Especifica a ID de uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="3f128-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="3f128-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3f128-135">-FrontendPort</span></span>
<span data-ttu-id="3f128-136">Especifica a porta front-end que é corresponder a uma configuração de regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3f128-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3f128-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="3f128-138">Especifica o tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="3f128-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f128-139">-LoadBalancer</span></span>
<span data-ttu-id="3f128-140">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-140">Specifies a load balancer.</span></span>
<span data-ttu-id="3f128-141">Este cmdlet atualiza uma configuração de regra para o balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3f128-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f128-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="3f128-142">-LoadDistribution</span></span>
<span data-ttu-id="3f128-143">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-143">Specifies a load distribution.</span></span>
<span data-ttu-id="3f128-144">Os valores aceitáveis para este parâmetro são: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="3f128-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="3f128-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f128-145">-Name</span></span>
<span data-ttu-id="3f128-146">Especifica o nome de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="3f128-147">-Desmão</span><span class="sxs-lookup"><span data-stu-id="3f128-147">-Probe</span></span>
<span data-ttu-id="3f128-148">Especifica uma transição para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3f128-149">-ElaId</span><span class="sxs-lookup"><span data-stu-id="3f128-149">-ProbeId</span></span>
<span data-ttu-id="3f128-150">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="3f128-151">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="3f128-151">-Protocol</span></span>
<span data-ttu-id="3f128-152">Especifica o protocolo que é correspondente a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="3f128-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="3f128-153">Os valores aceitáveis para este parâmetro são: Tcp ou Udp.</span><span class="sxs-lookup"><span data-stu-id="3f128-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="3f128-154">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3f128-154">-Confirm</span></span>
<span data-ttu-id="3f128-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f128-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f128-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f128-156">-WhatIf</span></span>
<span data-ttu-id="3f128-157">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3f128-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f128-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f128-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f128-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f128-159">CommonParameters</span></span>
<span data-ttu-id="3f128-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f128-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f128-161">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f128-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f128-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f128-162">INPUTS</span></span>

### <span data-ttu-id="3f128-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f128-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="3f128-164">System.String</span><span class="sxs-lookup"><span data-stu-id="3f128-164">System.String</span></span>

### <span data-ttu-id="3f128-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3f128-165">System.Int32</span></span>

### <span data-ttu-id="3f128-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f128-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="3f128-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f128-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="3f128-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="3f128-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="3f128-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f128-169">OUTPUTS</span></span>

### <span data-ttu-id="3f128-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3f128-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3f128-171">Notas</span><span class="sxs-lookup"><span data-stu-id="3f128-171">NOTES</span></span>

## <span data-ttu-id="3f128-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f128-172">RELATED LINKS</span></span>

[<span data-ttu-id="3f128-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f128-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3f128-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f128-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3f128-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f128-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3f128-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f128-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3f128-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f128-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


