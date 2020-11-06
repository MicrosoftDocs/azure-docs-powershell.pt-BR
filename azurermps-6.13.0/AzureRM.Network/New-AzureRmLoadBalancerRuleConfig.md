---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430149"
---
# <span data-ttu-id="ff1e7-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1e7-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="ff1e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff1e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1e7-103">Cria uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff1e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff1e7-104">SYNTAX</span></span>

### <span data-ttu-id="ff1e7-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff1e7-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff1e7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff1e7-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff1e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff1e7-107">DESCRIPTION</span></span>
<span data-ttu-id="ff1e7-108">O cmdlet **New-AzureRmLoadBalancerRuleConfig** cria uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ff1e7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff1e7-109">EXAMPLES</span></span>

### <span data-ttu-id="ff1e7-110">1: criando uma configuração de regra para um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="ff1e7-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="ff1e7-111">Os primeiros três comandos configuram um IP público, um front-end e um teste para a configuração de regra no comando por diante.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="ff1e7-112">O comando avançar cria uma nova regra chamada MyLBrule com determinadas especificações.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="ff1e7-113">OS</span><span class="sxs-lookup"><span data-stu-id="ff1e7-113">PARAMETERS</span></span>

### <span data-ttu-id="ff1e7-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ff1e7-114">-BackendAddressPool</span></span>
<span data-ttu-id="ff1e7-115">Especifica um objeto **BackendAddressPool** para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ff1e7-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="ff1e7-117">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ff1e7-118">-BackendPort</span></span>
<span data-ttu-id="ff1e7-119">Especifica a porta back-end para o tráfego correspondente a essa configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1e7-120">-DefaultProfile</span></span>
<span data-ttu-id="ff1e7-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff1e7-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="ff1e7-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="ff1e7-123">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="ff1e7-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ff1e7-124">-EnableFloatingIP</span></span>
<span data-ttu-id="ff1e7-125">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ff1e7-126">-EnableTcpReset</span></span>
<span data-ttu-id="ff1e7-127">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ff1e7-128">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ff1e7-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff1e7-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ff1e7-130">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ff1e7-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ff1e7-132">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ff1e7-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ff1e7-133">-FrontendPort</span></span>
<span data-ttu-id="ff1e7-134">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ff1e7-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ff1e7-136">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ff1e7-137">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="ff1e7-137">-LoadDistribution</span></span>
<span data-ttu-id="ff1e7-138">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-138">Specifies a load distribution.</span></span>
<span data-ttu-id="ff1e7-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ff1e7-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff1e7-140">Assume</span><span class="sxs-lookup"><span data-stu-id="ff1e7-140">Default</span></span>
- <span data-ttu-id="ff1e7-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="ff1e7-141">SourceIP</span></span>
- <span data-ttu-id="ff1e7-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="ff1e7-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="ff1e7-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff1e7-143">-Name</span></span>
<span data-ttu-id="ff1e7-144">Especifica o nome da regra de balanceamento de carga que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ff1e7-145">-Teste</span><span class="sxs-lookup"><span data-stu-id="ff1e7-145">-Probe</span></span>
<span data-ttu-id="ff1e7-146">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-147">-Probeid</span><span class="sxs-lookup"><span data-stu-id="ff1e7-147">-ProbeId</span></span>
<span data-ttu-id="ff1e7-148">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ff1e7-149">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="ff1e7-149">-Protocol</span></span>
<span data-ttu-id="ff1e7-150">Especifica o protocolo que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="ff1e7-151">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="ff1e7-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff1e7-152">-Confirm</span></span>
<span data-ttu-id="ff1e7-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff1e7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff1e7-154">-WhatIf</span></span>
<span data-ttu-id="ff1e7-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff1e7-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff1e7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1e7-157">CommonParameters</span></span>
<span data-ttu-id="ff1e7-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff1e7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1e7-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1e7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1e7-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff1e7-160">INPUTS</span></span>

### <span data-ttu-id="ff1e7-161">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ff1e7-161">None</span></span>

## <span data-ttu-id="ff1e7-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff1e7-162">OUTPUTS</span></span>

### <span data-ttu-id="ff1e7-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="ff1e7-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="ff1e7-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff1e7-164">NOTES</span></span>

## <span data-ttu-id="ff1e7-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff1e7-165">RELATED LINKS</span></span>

[<span data-ttu-id="ff1e7-166">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1e7-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ff1e7-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1e7-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ff1e7-168">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1e7-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="ff1e7-169">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff1e7-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)

