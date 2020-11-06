---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 0366e9fce7d2955e03b72c502e4da77e2ddee54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603033"
---
# <span data-ttu-id="fb7f0-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb7f0-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="fb7f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7f0-103">Adiciona uma configuração de regra a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb7f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb7f0-104">SYNTAX</span></span>

### <span data-ttu-id="fb7f0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7f0-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb7f0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fb7f0-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7f0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb7f0-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7f0-108">O cmdlet **Add-AzureRmLoadBalancerRuleConfig** adiciona uma configuração de regra a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="fb7f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb7f0-109">EXAMPLES</span></span>

### <span data-ttu-id="fb7f0-110">Exemplo 1: adicionar uma configuração de regra a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="fb7f0-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="fb7f0-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="fb7f0-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para **Adicionar-AzureRmLoadBalancerRuleConfig** , o que adiciona a configuração de regra chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="fb7f0-113">OS</span><span class="sxs-lookup"><span data-stu-id="fb7f0-113">PARAMETERS</span></span>

### <span data-ttu-id="fb7f0-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fb7f0-114">-BackendAddressPool</span></span>
<span data-ttu-id="fb7f0-115">Especifica o pool de endereços back-end a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="fb7f0-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="fb7f0-117">Especifica a ID de um objeto **BackendAddressPool** a ser associado a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fb7f0-118">-BackendPort</span></span>
<span data-ttu-id="fb7f0-119">Especifica a porta back-end para tráfego que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7f0-120">-DefaultProfile</span></span>
<span data-ttu-id="fb7f0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7f0-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="fb7f0-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="fb7f0-123">Configura o SNAT para as VMs no pool de back-end para usar o endereço publicIP especificado no front-end da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="fb7f0-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="fb7f0-124">-EnableFloatingIP</span></span>
<span data-ttu-id="fb7f0-125">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb7f0-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="fb7f0-127">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fb7f0-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="fb7f0-129">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="fb7f0-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="fb7f0-130">-FrontendPort</span></span>
<span data-ttu-id="fb7f0-131">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fb7f0-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fb7f0-133">Especifica o período de tempo, em minutos, para o qual o estado das conversas é mantido no balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="fb7f0-134">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="fb7f0-134">-LoadBalancer</span></span>
<span data-ttu-id="fb7f0-135">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="fb7f0-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="fb7f0-136">Esse cmdlet adiciona uma configuração de regra ao balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb7f0-137">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="fb7f0-137">-LoadDistribution</span></span>
<span data-ttu-id="fb7f0-138">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="fb7f0-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb7f0-139">-Name</span></span>
<span data-ttu-id="fb7f0-140">Especifica o nome da configuração de regra do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-141">-Teste</span><span class="sxs-lookup"><span data-stu-id="fb7f0-141">-Probe</span></span>
<span data-ttu-id="fb7f0-142">Especifica um teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-143">-Probeid</span><span class="sxs-lookup"><span data-stu-id="fb7f0-143">-ProbeId</span></span>
<span data-ttu-id="fb7f0-144">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fb7f0-145">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="fb7f0-145">-Protocol</span></span>
<span data-ttu-id="fb7f0-146">Specfies o protocolo que corresponde a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="fb7f0-147">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="fb7f0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7f0-148">CommonParameters</span></span>
<span data-ttu-id="fb7f0-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7f0-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7f0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7f0-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb7f0-151">INPUTS</span></span>

### <span data-ttu-id="fb7f0-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb7f0-152">PSLoadBalancer</span></span>
<span data-ttu-id="fb7f0-153">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fb7f0-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fb7f0-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb7f0-154">OUTPUTS</span></span>

### <span data-ttu-id="fb7f0-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb7f0-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fb7f0-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb7f0-156">NOTES</span></span>

## <span data-ttu-id="fb7f0-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb7f0-157">RELATED LINKS</span></span>

[<span data-ttu-id="fb7f0-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fb7f0-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fb7f0-159">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb7f0-159">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fb7f0-160">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb7f0-160">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fb7f0-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb7f0-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="fb7f0-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fb7f0-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


