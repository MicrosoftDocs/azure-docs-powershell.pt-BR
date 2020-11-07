---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: f3e256def28dff292efc5ba4278dc4f56b3ec721
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786434"
---
# <span data-ttu-id="056c7-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="056c7-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="056c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="056c7-102">SYNOPSIS</span></span>
<span data-ttu-id="056c7-103">Cria uma configuração de regra para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="056c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="056c7-104">SYNTAX</span></span>

### <span data-ttu-id="056c7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="056c7-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="056c7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="056c7-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="056c7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="056c7-107">DESCRIPTION</span></span>
<span data-ttu-id="056c7-108">O cmdlet **New-AzureRmLoadBalancerRuleConfig** cria uma configuração de regra para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="056c7-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="056c7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="056c7-109">EXAMPLES</span></span>

### <span data-ttu-id="056c7-110">1: criando uma configuração de regra para um balanceador de carga do Azure</span><span class="sxs-lookup"><span data-stu-id="056c7-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="056c7-111">Os primeiros três comandos configuram um IP público, um front-end e um teste para a configuração de regra no comando por diante.</span><span class="sxs-lookup"><span data-stu-id="056c7-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="056c7-112">O comando avançar cria uma nova regra chamada MyLBrule com determinadas especificações.</span><span class="sxs-lookup"><span data-stu-id="056c7-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="056c7-113">OS</span><span class="sxs-lookup"><span data-stu-id="056c7-113">PARAMETERS</span></span>

### <span data-ttu-id="056c7-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="056c7-114">-BackendAddressPool</span></span>
<span data-ttu-id="056c7-115">Especifica um objeto **BackendAddressPool** para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="056c7-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="056c7-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="056c7-117">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="056c7-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="056c7-118">-BackendPort</span></span>
<span data-ttu-id="056c7-119">Especifica a porta back-end para o tráfego correspondente a essa configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="056c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056c7-120">-DefaultProfile</span></span>
<span data-ttu-id="056c7-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="056c7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="056c7-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="056c7-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="056c7-123">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="056c7-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="056c7-124">-EnableFloatingIP</span></span>
<span data-ttu-id="056c7-125">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="056c7-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="056c7-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="056c7-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="056c7-127">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="056c7-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="056c7-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="056c7-129">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="056c7-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="056c7-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="056c7-130">-FrontendPort</span></span>
<span data-ttu-id="056c7-131">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="056c7-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="056c7-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="056c7-133">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="056c7-134">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="056c7-134">-LoadDistribution</span></span>
<span data-ttu-id="056c7-135">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-135">Specifies a load distribution.</span></span>
<span data-ttu-id="056c7-136">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="056c7-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="056c7-137">Assume</span><span class="sxs-lookup"><span data-stu-id="056c7-137">Default</span></span>
- <span data-ttu-id="056c7-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="056c7-138">SourceIP</span></span>
- <span data-ttu-id="056c7-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="056c7-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="056c7-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="056c7-140">-Name</span></span>
<span data-ttu-id="056c7-141">Especifica o nome da regra de balanceamento de carga que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="056c7-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="056c7-142">-Teste</span><span class="sxs-lookup"><span data-stu-id="056c7-142">-Probe</span></span>
<span data-ttu-id="056c7-143">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="056c7-144">-Probeid</span><span class="sxs-lookup"><span data-stu-id="056c7-144">-ProbeId</span></span>
<span data-ttu-id="056c7-145">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="056c7-146">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="056c7-146">-Protocol</span></span>
<span data-ttu-id="056c7-147">Especifica o protocolo que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="056c7-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="056c7-148">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="056c7-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="056c7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056c7-149">CommonParameters</span></span>
<span data-ttu-id="056c7-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="056c7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056c7-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="056c7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056c7-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="056c7-152">INPUTS</span></span>

## <span data-ttu-id="056c7-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="056c7-153">OUTPUTS</span></span>

### <span data-ttu-id="056c7-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="056c7-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="056c7-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="056c7-155">NOTES</span></span>

## <span data-ttu-id="056c7-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="056c7-156">RELATED LINKS</span></span>

[<span data-ttu-id="056c7-157">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="056c7-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="056c7-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="056c7-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="056c7-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="056c7-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="056c7-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="056c7-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


