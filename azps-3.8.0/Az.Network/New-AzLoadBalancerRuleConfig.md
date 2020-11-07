---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d93bf82421851a79399061861ed9f2ca29d9a5c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777339"
---
# <span data-ttu-id="255b9-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="255b9-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="255b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="255b9-102">SYNOPSIS</span></span>
<span data-ttu-id="255b9-103">Cria uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="255b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="255b9-104">SYNTAX</span></span>

### <span data-ttu-id="255b9-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="255b9-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="255b9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="255b9-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="255b9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="255b9-107">DESCRIPTION</span></span>
<span data-ttu-id="255b9-108">O cmdlet **New-AzLoadBalancerRuleConfig** cria uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="255b9-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="255b9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="255b9-109">EXAMPLES</span></span>

### <span data-ttu-id="255b9-110">1: criando uma configuração de regra para um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="255b9-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="255b9-111">Os primeiros três comandos configuram um IP público, um front-end e um teste para a configuração de regra no comando por diante.</span><span class="sxs-lookup"><span data-stu-id="255b9-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="255b9-112">O comando avançar cria uma nova regra chamada MyLBrule com determinadas especificações.</span><span class="sxs-lookup"><span data-stu-id="255b9-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="255b9-113">OS</span><span class="sxs-lookup"><span data-stu-id="255b9-113">PARAMETERS</span></span>

### <span data-ttu-id="255b9-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="255b9-114">-BackendAddressPool</span></span>
<span data-ttu-id="255b9-115">Especifica um objeto **BackendAddressPool** para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="255b9-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="255b9-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="255b9-117">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="255b9-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="255b9-118">-BackendPort</span></span>
<span data-ttu-id="255b9-119">Especifica a porta back-end para o tráfego correspondente a essa configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="255b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255b9-120">-DefaultProfile</span></span>
<span data-ttu-id="255b9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="255b9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="255b9-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="255b9-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="255b9-123">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="255b9-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="255b9-124">-EnableFloatingIP</span></span>
<span data-ttu-id="255b9-125">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="255b9-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="255b9-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="255b9-126">-EnableTcpReset</span></span>
<span data-ttu-id="255b9-127">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="255b9-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="255b9-128">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="255b9-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="255b9-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="255b9-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="255b9-130">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="255b9-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="255b9-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="255b9-132">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="255b9-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="255b9-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="255b9-133">-FrontendPort</span></span>
<span data-ttu-id="255b9-134">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="255b9-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="255b9-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="255b9-136">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="255b9-137">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="255b9-137">-LoadDistribution</span></span>
<span data-ttu-id="255b9-138">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-138">Specifies a load distribution.</span></span>
<span data-ttu-id="255b9-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="255b9-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="255b9-140">Assume</span><span class="sxs-lookup"><span data-stu-id="255b9-140">Default</span></span>
- <span data-ttu-id="255b9-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="255b9-141">SourceIP</span></span>
- <span data-ttu-id="255b9-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="255b9-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="255b9-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="255b9-143">-Name</span></span>
<span data-ttu-id="255b9-144">Especifica o nome da regra de balanceamento de carga que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="255b9-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="255b9-145">-Teste</span><span class="sxs-lookup"><span data-stu-id="255b9-145">-Probe</span></span>
<span data-ttu-id="255b9-146">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="255b9-147">-Probeid</span><span class="sxs-lookup"><span data-stu-id="255b9-147">-ProbeId</span></span>
<span data-ttu-id="255b9-148">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="255b9-149">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="255b9-149">-Protocol</span></span>
<span data-ttu-id="255b9-150">Especifica o protocolo que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="255b9-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="255b9-151">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="255b9-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="255b9-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="255b9-152">-Confirm</span></span>
<span data-ttu-id="255b9-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="255b9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="255b9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="255b9-154">-WhatIf</span></span>
<span data-ttu-id="255b9-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="255b9-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="255b9-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="255b9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="255b9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255b9-157">CommonParameters</span></span>
<span data-ttu-id="255b9-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255b9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255b9-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="255b9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255b9-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="255b9-160">INPUTS</span></span>

### <span data-ttu-id="255b9-161">System. String</span><span class="sxs-lookup"><span data-stu-id="255b9-161">System.String</span></span>

### <span data-ttu-id="255b9-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="255b9-162">System.Int32</span></span>

### <span data-ttu-id="255b9-163">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="255b9-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="255b9-164">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="255b9-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="255b9-165">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="255b9-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="255b9-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="255b9-166">OUTPUTS</span></span>

### <span data-ttu-id="255b9-167">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="255b9-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="255b9-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="255b9-168">NOTES</span></span>

## <span data-ttu-id="255b9-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="255b9-169">RELATED LINKS</span></span>

[<span data-ttu-id="255b9-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="255b9-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="255b9-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="255b9-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="255b9-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="255b9-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="255b9-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="255b9-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


