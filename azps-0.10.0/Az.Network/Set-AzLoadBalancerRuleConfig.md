---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: f566c2b9ac771071a9eb72673edb7e5218656c9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776532"
---
# <span data-ttu-id="30740-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30740-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="30740-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30740-102">SYNOPSIS</span></span>
<span data-ttu-id="30740-103">Define o estado da meta para uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-103">Sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="30740-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30740-104">SYNTAX</span></span>

### <span data-ttu-id="30740-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="30740-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30740-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="30740-106">SetByResource</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30740-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30740-107">DESCRIPTION</span></span>
<span data-ttu-id="30740-108">O cmdlet **set-AzLoadBalancerRuleConfig** define o estado da meta para uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-108">The **Set-AzLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="30740-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30740-109">EXAMPLES</span></span>

### <span data-ttu-id="30740-110">Exemplo 1: modificar uma configuração de regra de balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="30740-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="30740-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="30740-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="30740-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzLoadBalancerRuleConfig, o que adiciona uma regra chamada NewRule a ela.</span><span class="sxs-lookup"><span data-stu-id="30740-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="30740-113">O terceiro comando passa o balanceador de carga para **set-AzLoadBalancerRuleConfig** , que define a nova configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="30740-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="30740-114">Observe que a configuração não habilita um endereço IP flutuante, que foi habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="30740-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="30740-115">OS</span><span class="sxs-lookup"><span data-stu-id="30740-115">PARAMETERS</span></span>

### <span data-ttu-id="30740-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30740-116">-BackendAddressPool</span></span>
<span data-ttu-id="30740-117">Especifica um objeto **BackendAddressPool** para associar a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="30740-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="30740-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="30740-119">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30740-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="30740-120">-BackendPort</span></span>
<span data-ttu-id="30740-121">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="30740-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="30740-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30740-122">-DefaultProfile</span></span>
<span data-ttu-id="30740-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30740-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30740-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="30740-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="30740-125">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="30740-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="30740-126">-EnableFloatingIP</span></span>
<span data-ttu-id="30740-127">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="30740-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="30740-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="30740-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="30740-129">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30740-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="30740-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="30740-131">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="30740-131">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="30740-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="30740-132">-FrontendPort</span></span>
<span data-ttu-id="30740-133">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30740-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="30740-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="30740-135">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="30740-136">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="30740-136">-LoadBalancer</span></span>
<span data-ttu-id="30740-137">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-137">Specifies a load balancer.</span></span>
<span data-ttu-id="30740-138">Esse cmdlet define a configuração de regra de estado de meta para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="30740-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30740-139">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="30740-139">-LoadDistribution</span></span>
<span data-ttu-id="30740-140">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-140">Specifies a load distribution.</span></span>
<span data-ttu-id="30740-141">Os valores aceitáveis para esse parâmetro são: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="30740-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="30740-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="30740-142">-Name</span></span>
<span data-ttu-id="30740-143">Especifica o nome de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="30740-144">-Teste</span><span class="sxs-lookup"><span data-stu-id="30740-144">-Probe</span></span>
<span data-ttu-id="30740-145">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30740-146">-Probeid</span><span class="sxs-lookup"><span data-stu-id="30740-146">-ProbeId</span></span>
<span data-ttu-id="30740-147">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="30740-148">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="30740-148">-Protocol</span></span>
<span data-ttu-id="30740-149">Especifica o protocolo que corresponde a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="30740-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="30740-150">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="30740-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="30740-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30740-151">CommonParameters</span></span>
<span data-ttu-id="30740-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30740-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30740-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30740-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30740-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30740-154">INPUTS</span></span>

### <span data-ttu-id="30740-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30740-155">PSLoadBalancer</span></span>
<span data-ttu-id="30740-156">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="30740-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="30740-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30740-157">OUTPUTS</span></span>

### <span data-ttu-id="30740-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30740-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30740-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30740-159">NOTES</span></span>

## <span data-ttu-id="30740-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30740-160">RELATED LINKS</span></span>

[<span data-ttu-id="30740-161">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30740-161">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="30740-162">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30740-162">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="30740-163">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30740-163">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="30740-164">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30740-164">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="30740-165">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30740-165">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


