---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: acc741bc038e7fe3a9612e2bc6b4e9abe6bab800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432058"
---
# <span data-ttu-id="de209-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de209-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="de209-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de209-102">SYNOPSIS</span></span>
<span data-ttu-id="de209-103">Define o estado da meta para uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de209-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de209-104">SYNTAX</span></span>

### <span data-ttu-id="de209-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de209-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de209-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="de209-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de209-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de209-107">DESCRIPTION</span></span>
<span data-ttu-id="de209-108">O cmdlet **set-AzureRmLoadBalancerRuleConfig** define o estado da meta para uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="de209-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de209-109">EXAMPLES</span></span>

### <span data-ttu-id="de209-110">Exemplo 1: modificar uma configuração de regra de balanceamento de carga</span><span class="sxs-lookup"><span data-stu-id="de209-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="de209-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="de209-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="de209-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzureRmLoadBalancerRuleConfig, o que adiciona uma regra chamada NewRule a ela.</span><span class="sxs-lookup"><span data-stu-id="de209-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="de209-113">O terceiro comando passa o balanceador de carga para **set-AzureRmLoadBalancerRuleConfig** , que define a nova configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="de209-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="de209-114">Observe que a configuração não habilita um endereço IP flutuante, que foi habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="de209-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="de209-115">OS</span><span class="sxs-lookup"><span data-stu-id="de209-115">PARAMETERS</span></span>

### <span data-ttu-id="de209-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de209-116">-BackendAddressPool</span></span>
<span data-ttu-id="de209-117">Especifica um objeto **BackendAddressPool** para associar a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="de209-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="de209-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="de209-119">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="de209-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="de209-120">-BackendPort</span></span>
<span data-ttu-id="de209-121">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="de209-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="de209-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de209-122">-DefaultProfile</span></span>
<span data-ttu-id="de209-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de209-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de209-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="de209-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="de209-125">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="de209-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="de209-126">-EnableFloatingIP</span></span>
<span data-ttu-id="de209-127">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="de209-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="de209-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="de209-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="de209-129">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="de209-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="de209-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="de209-131">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="de209-131">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="de209-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="de209-132">-FrontendPort</span></span>
<span data-ttu-id="de209-133">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="de209-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="de209-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="de209-135">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="de209-136">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="de209-136">-LoadBalancer</span></span>
<span data-ttu-id="de209-137">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-137">Specifies a load balancer.</span></span>
<span data-ttu-id="de209-138">Esse cmdlet define a configuração de regra de estado de meta para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="de209-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="de209-139">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="de209-139">-LoadDistribution</span></span>
<span data-ttu-id="de209-140">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-140">Specifies a load distribution.</span></span>
<span data-ttu-id="de209-141">Os valores aceitáveis para esse parâmetro são: SourceIP e SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="de209-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="de209-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="de209-142">-Name</span></span>
<span data-ttu-id="de209-143">Especifica o nome de um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="de209-144">-Teste</span><span class="sxs-lookup"><span data-stu-id="de209-144">-Probe</span></span>
<span data-ttu-id="de209-145">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="de209-146">-Probeid</span><span class="sxs-lookup"><span data-stu-id="de209-146">-ProbeId</span></span>
<span data-ttu-id="de209-147">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="de209-148">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="de209-148">-Protocol</span></span>
<span data-ttu-id="de209-149">Especifica o protocolo que corresponde a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="de209-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="de209-150">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="de209-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="de209-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de209-151">CommonParameters</span></span>
<span data-ttu-id="de209-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de209-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de209-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de209-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de209-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de209-154">INPUTS</span></span>

### <span data-ttu-id="de209-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="de209-155">PSLoadBalancer</span></span>
<span data-ttu-id="de209-156">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="de209-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="de209-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de209-157">OUTPUTS</span></span>

### <span data-ttu-id="de209-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="de209-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="de209-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de209-159">NOTES</span></span>

## <span data-ttu-id="de209-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de209-160">RELATED LINKS</span></span>

[<span data-ttu-id="de209-161">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de209-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="de209-162">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de209-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="de209-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de209-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="de209-164">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de209-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="de209-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="de209-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

