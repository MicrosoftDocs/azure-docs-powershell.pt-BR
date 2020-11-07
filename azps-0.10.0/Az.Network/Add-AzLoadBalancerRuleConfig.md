---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 52e1759f82ba6663215907a93f89f562df1b6afa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775628"
---
# <span data-ttu-id="49b54-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49b54-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="49b54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49b54-102">SYNOPSIS</span></span>
<span data-ttu-id="49b54-103">Adiciona uma configuração de regra a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="49b54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49b54-104">SYNTAX</span></span>

### <span data-ttu-id="49b54-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="49b54-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49b54-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="49b54-106">SetByResource</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b54-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49b54-107">DESCRIPTION</span></span>
<span data-ttu-id="49b54-108">O cmdlet **Add-AzLoadBalancerRuleConfig** adiciona uma configuração de regra a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="49b54-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="49b54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49b54-109">EXAMPLES</span></span>

### <span data-ttu-id="49b54-110">Exemplo 1: adicionar uma configuração de regra a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="49b54-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="49b54-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="49b54-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="49b54-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para **Adicionar-AzLoadBalancerRuleConfig** , o que adiciona a configuração de regra chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="49b54-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="49b54-113">OS</span><span class="sxs-lookup"><span data-stu-id="49b54-113">PARAMETERS</span></span>

### <span data-ttu-id="49b54-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="49b54-114">-BackendAddressPool</span></span>
<span data-ttu-id="49b54-115">Especifica o pool de endereços back-end a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="49b54-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="49b54-117">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="49b54-118">-BackendPort</span></span>
<span data-ttu-id="49b54-119">Especifica a porta back-end para tráfego que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b54-120">-DefaultProfile</span></span>
<span data-ttu-id="49b54-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49b54-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b54-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="49b54-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="49b54-123">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="49b54-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="49b54-124">-EnableFloatingIP</span></span>
<span data-ttu-id="49b54-125">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="49b54-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="49b54-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="49b54-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="49b54-127">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="49b54-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="49b54-129">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="49b54-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="49b54-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="49b54-130">-FrontendPort</span></span>
<span data-ttu-id="49b54-131">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="49b54-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="49b54-133">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido no balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="49b54-134">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="49b54-134">-LoadBalancer</span></span>
<span data-ttu-id="49b54-135">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="49b54-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="49b54-136">Esse cmdlet adiciona uma configuração de regra ao balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="49b54-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="49b54-137">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="49b54-137">-LoadDistribution</span></span>
<span data-ttu-id="49b54-138">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="49b54-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="49b54-139">-Name</span></span>
<span data-ttu-id="49b54-140">Especifica o nome da configuração de regra do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-141">-Teste</span><span class="sxs-lookup"><span data-stu-id="49b54-141">-Probe</span></span>
<span data-ttu-id="49b54-142">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-143">-Probeid</span><span class="sxs-lookup"><span data-stu-id="49b54-143">-ProbeId</span></span>
<span data-ttu-id="49b54-144">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="49b54-145">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="49b54-145">-Protocol</span></span>
<span data-ttu-id="49b54-146">Specfies o protocolo que corresponde a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="49b54-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="49b54-147">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="49b54-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="49b54-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b54-148">CommonParameters</span></span>
<span data-ttu-id="49b54-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b54-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b54-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b54-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b54-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49b54-151">INPUTS</span></span>

### <span data-ttu-id="49b54-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b54-152">PSLoadBalancer</span></span>
<span data-ttu-id="49b54-153">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="49b54-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="49b54-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49b54-154">OUTPUTS</span></span>

### <span data-ttu-id="49b54-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b54-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="49b54-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49b54-156">NOTES</span></span>

## <span data-ttu-id="49b54-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49b54-157">RELATED LINKS</span></span>

[<span data-ttu-id="49b54-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="49b54-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="49b54-159">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49b54-159">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="49b54-160">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49b54-160">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="49b54-161">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49b54-161">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="49b54-162">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="49b54-162">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


