---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775386"
---
# <span data-ttu-id="d08ad-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d08ad-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d08ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d08ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d08ad-103">Cria uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d08ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d08ad-104">SYNTAX</span></span>

### <span data-ttu-id="d08ad-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d08ad-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d08ad-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d08ad-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d08ad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d08ad-107">DESCRIPTION</span></span>
<span data-ttu-id="d08ad-108">O cmdlet **New-AzLoadBalancerRuleConfig** cria uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="d08ad-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d08ad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d08ad-109">EXAMPLES</span></span>

### <span data-ttu-id="d08ad-110">1: criando uma configuração de regra para um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="d08ad-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="d08ad-111">Os primeiros três comandos configuram um IP público, um front-end e um teste para a configuração de regra no comando por diante.</span><span class="sxs-lookup"><span data-stu-id="d08ad-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="d08ad-112">O comando avançar cria uma nova regra chamada MyLBrule com determinadas especificações.</span><span class="sxs-lookup"><span data-stu-id="d08ad-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="d08ad-113">OS</span><span class="sxs-lookup"><span data-stu-id="d08ad-113">PARAMETERS</span></span>

### <span data-ttu-id="d08ad-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d08ad-114">-BackendAddressPool</span></span>
<span data-ttu-id="d08ad-115">Especifica um objeto **BackendAddressPool** para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d08ad-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="d08ad-117">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d08ad-118">-BackendPort</span></span>
<span data-ttu-id="d08ad-119">Especifica a porta back-end para o tráfego correspondente a essa configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08ad-120">-DefaultProfile</span></span>
<span data-ttu-id="d08ad-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d08ad-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="d08ad-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="d08ad-123">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d08ad-124">-EnableFloatingIP</span></span>
<span data-ttu-id="d08ad-125">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="d08ad-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d08ad-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d08ad-127">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d08ad-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d08ad-129">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="d08ad-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d08ad-130">-FrontendPort</span></span>
<span data-ttu-id="d08ad-131">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d08ad-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d08ad-133">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-134">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="d08ad-134">-LoadDistribution</span></span>
<span data-ttu-id="d08ad-135">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-135">Specifies a load distribution.</span></span>
<span data-ttu-id="d08ad-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d08ad-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d08ad-137">Assume</span><span class="sxs-lookup"><span data-stu-id="d08ad-137">Default</span></span>
- <span data-ttu-id="d08ad-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="d08ad-138">SourceIP</span></span>
- <span data-ttu-id="d08ad-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="d08ad-139">SourceIPProtocol</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="d08ad-140">-Name</span></span>
<span data-ttu-id="d08ad-141">Especifica o nome da regra de balanceamento de carga que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d08ad-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-142">-Teste</span><span class="sxs-lookup"><span data-stu-id="d08ad-142">-Probe</span></span>
<span data-ttu-id="d08ad-143">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-144">-Probeid</span><span class="sxs-lookup"><span data-stu-id="d08ad-144">-ProbeId</span></span>
<span data-ttu-id="d08ad-145">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-146">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="d08ad-146">-Protocol</span></span>
<span data-ttu-id="d08ad-147">Especifica o protocolo que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d08ad-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="d08ad-148">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d08ad-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d08ad-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08ad-149">CommonParameters</span></span>
<span data-ttu-id="d08ad-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08ad-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08ad-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d08ad-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08ad-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d08ad-152">INPUTS</span></span>

## <span data-ttu-id="d08ad-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d08ad-153">OUTPUTS</span></span>

### <span data-ttu-id="d08ad-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="d08ad-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="d08ad-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d08ad-155">NOTES</span></span>

## <span data-ttu-id="d08ad-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d08ad-156">RELATED LINKS</span></span>

[<span data-ttu-id="d08ad-157">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d08ad-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d08ad-158">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d08ad-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d08ad-159">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d08ad-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="d08ad-160">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d08ad-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


