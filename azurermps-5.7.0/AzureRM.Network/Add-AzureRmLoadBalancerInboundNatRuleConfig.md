---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 8e055df66c0623fbddbed8379cb25f165efb7081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603035"
---
# <span data-ttu-id="72648-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72648-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="72648-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72648-102">SYNOPSIS</span></span>
<span data-ttu-id="72648-103">Adiciona uma configuração de regra NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="72648-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72648-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72648-104">SYNTAX</span></span>

### <span data-ttu-id="72648-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72648-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72648-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72648-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72648-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72648-107">DESCRIPTION</span></span>
<span data-ttu-id="72648-108">O cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** adiciona uma configuração de regra NAT (conversão de endereços de rede) de entrada a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="72648-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="72648-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72648-109">EXAMPLES</span></span>

### <span data-ttu-id="72648-110">Exemplo 1: adicionar uma configuração de regra NAT de entrada a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="72648-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="72648-111">O primeiro comando obtém o balanceador de carga chamado MyloadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="72648-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="72648-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para **Add-AzureRmLoadBalancerInboundNatRuleConfig** , que adiciona uma configuração de regra NAT de entrada ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="72648-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="72648-113">OS</span><span class="sxs-lookup"><span data-stu-id="72648-113">PARAMETERS</span></span>

### <span data-ttu-id="72648-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="72648-114">-BackendPort</span></span>
<span data-ttu-id="72648-115">Especifica a porta de back-end para o tráfego correspondente a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="72648-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="72648-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72648-116">-DefaultProfile</span></span>
<span data-ttu-id="72648-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="72648-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72648-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="72648-118">-EnableFloatingIP</span></span>
<span data-ttu-id="72648-119">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="72648-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="72648-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="72648-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="72648-121">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="72648-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="72648-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="72648-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="72648-123">Especifica uma ID para uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="72648-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="72648-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="72648-124">-FrontendPort</span></span>
<span data-ttu-id="72648-125">Especifica a porta de front-end que corresponde a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="72648-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="72648-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="72648-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="72648-127">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="72648-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="72648-128">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="72648-128">-LoadBalancer</span></span>
<span data-ttu-id="72648-129">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="72648-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="72648-130">Esse cmdlet adiciona uma configuração de regra NAT de entrada ao balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="72648-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="72648-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="72648-131">-Name</span></span>
<span data-ttu-id="72648-132">Especifica o nome da configuração de regra NAT de entrada a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="72648-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="72648-133">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="72648-133">-Protocol</span></span>
<span data-ttu-id="72648-134">Especifica o protocolo que corresponde a uma regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="72648-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="72648-135">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="72648-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72648-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72648-136">CommonParameters</span></span>
<span data-ttu-id="72648-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72648-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72648-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72648-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72648-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72648-139">INPUTS</span></span>

### <span data-ttu-id="72648-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72648-140">PSLoadBalancer</span></span>
<span data-ttu-id="72648-141">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="72648-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="72648-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72648-142">OUTPUTS</span></span>

### <span data-ttu-id="72648-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72648-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="72648-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72648-144">NOTES</span></span>

## <span data-ttu-id="72648-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72648-145">RELATED LINKS</span></span>

[<span data-ttu-id="72648-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72648-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="72648-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72648-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="72648-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72648-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="72648-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72648-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="72648-150">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="72648-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="72648-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72648-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


