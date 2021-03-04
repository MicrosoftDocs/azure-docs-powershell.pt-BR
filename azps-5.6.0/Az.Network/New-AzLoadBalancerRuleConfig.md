---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 544d43ab3a82ff7eb00712ea121d3f799d632f79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890603"
---
# <span data-ttu-id="10dc6-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10dc6-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="10dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="10dc6-103">Cria uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="10dc6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10dc6-104">SYNTAX</span></span>

### <span data-ttu-id="10dc6-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10dc6-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10dc6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10dc6-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10dc6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="10dc6-108">O cmdlet **New-AzLoadBalancerRuleConfig** cria uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="10dc6-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="10dc6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10dc6-109">EXAMPLES</span></span>

### <span data-ttu-id="10dc6-110">Exemplo 1: Criando uma configuração de regra para um Balanceador de Carga do Azure</span><span class="sxs-lookup"><span data-stu-id="10dc6-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="10dc6-111">Os três primeiros comandos configuram um IP público, um front-end e uma sonda para a configuração de regra no comando forth.</span><span class="sxs-lookup"><span data-stu-id="10dc6-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="10dc6-112">O comando forth cria uma nova regra chamada MyLBrule com determinadas especificações.</span><span class="sxs-lookup"><span data-stu-id="10dc6-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="10dc6-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10dc6-113">PARAMETERS</span></span>

### <span data-ttu-id="10dc6-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="10dc6-114">-BackendAddressPool</span></span>
<span data-ttu-id="10dc6-115">Especifica um **objeto BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="10dc6-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="10dc6-117">Especifica a ID de um **objeto BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="10dc6-118">-BackendPort</span></span>
<span data-ttu-id="10dc6-119">Especifica a porta de back-end para tráfego que é corresponder a essa configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10dc6-120">-DefaultProfile</span></span>
<span data-ttu-id="10dc6-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="10dc6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10dc6-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="10dc6-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="10dc6-123">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="10dc6-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="10dc6-124">-EnableFloatingIP</span></span>
<span data-ttu-id="10dc6-125">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="10dc6-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="10dc6-126">-EnableTcpReset</span></span>
<span data-ttu-id="10dc6-127">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="10dc6-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="10dc6-128">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="10dc6-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="10dc6-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10dc6-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="10dc6-130">Especifica uma lista de endereços IP front-end para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="10dc6-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="10dc6-132">Especifica a ID de uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="10dc6-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="10dc6-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="10dc6-133">-FrontendPort</span></span>
<span data-ttu-id="10dc6-134">Especifica a porta front-end que é corresponder a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="10dc6-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="10dc6-136">Especifica o período de tempo, em minutos, que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="10dc6-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="10dc6-137">-LoadDistribution</span></span>
<span data-ttu-id="10dc6-138">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-138">Specifies a load distribution.</span></span>
<span data-ttu-id="10dc6-139">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="10dc6-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10dc6-140">Padrão</span><span class="sxs-lookup"><span data-stu-id="10dc6-140">Default</span></span>
- <span data-ttu-id="10dc6-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="10dc6-141">SourceIP</span></span>
- <span data-ttu-id="10dc6-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="10dc6-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="10dc6-143">-Name</span><span class="sxs-lookup"><span data-stu-id="10dc6-143">-Name</span></span>
<span data-ttu-id="10dc6-144">Especifica o nome da regra de balanceamento de carga que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="10dc6-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="10dc6-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="10dc6-145">-Probe</span></span>
<span data-ttu-id="10dc6-146">Especifica uma sonda a ser associada a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="10dc6-147">-ProbeId</span></span>
<span data-ttu-id="10dc6-148">Especifica a ID da sonda a ser associada a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="10dc6-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="10dc6-149">-Protocol</span></span>
<span data-ttu-id="10dc6-150">Especifica o protocolo que é correspondente por uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="10dc6-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="10dc6-151">Os valores aceitáveis para este parâmetro são: Tcp ou Udp.</span><span class="sxs-lookup"><span data-stu-id="10dc6-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="10dc6-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10dc6-152">-Confirm</span></span>
<span data-ttu-id="10dc6-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10dc6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10dc6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10dc6-154">-WhatIf</span></span>
<span data-ttu-id="10dc6-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10dc6-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10dc6-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10dc6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10dc6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10dc6-157">CommonParameters</span></span>
<span data-ttu-id="10dc6-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10dc6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10dc6-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10dc6-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10dc6-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10dc6-160">INPUTS</span></span>

### <span data-ttu-id="10dc6-161">System.String</span><span class="sxs-lookup"><span data-stu-id="10dc6-161">System.String</span></span>

### <span data-ttu-id="10dc6-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="10dc6-162">System.Int32</span></span>

### <span data-ttu-id="10dc6-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10dc6-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="10dc6-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="10dc6-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="10dc6-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="10dc6-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="10dc6-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10dc6-166">OUTPUTS</span></span>

### <span data-ttu-id="10dc6-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="10dc6-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="10dc6-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="10dc6-168">NOTES</span></span>

## <span data-ttu-id="10dc6-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10dc6-169">RELATED LINKS</span></span>

[<span data-ttu-id="10dc6-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10dc6-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="10dc6-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10dc6-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="10dc6-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10dc6-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="10dc6-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10dc6-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


