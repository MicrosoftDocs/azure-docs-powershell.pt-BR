---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 98f7052ab0fa326789242cdebaf34f188684993e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428874"
---
# <span data-ttu-id="bb97c-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb97c-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="bb97c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb97c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb97c-103">Define uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="bb97c-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb97c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb97c-104">SYNTAX</span></span>

### <span data-ttu-id="bb97c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb97c-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb97c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bb97c-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb97c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb97c-107">DESCRIPTION</span></span>
<span data-ttu-id="bb97c-108">O cmdlet **set-AzureRmLoadBalancerInboundNatRuleConfig** define uma configuração de regra NAT (conversão de endereços de rede) de entrada para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb97c-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="bb97c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb97c-109">EXAMPLES</span></span>

### <span data-ttu-id="bb97c-110">Exemplo 1: modificar a configuração da regra NAT de entrada em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="bb97c-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="bb97c-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="bb97c-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="bb97c-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga em $slb para adicionar-AzureRmLoadBalancerInboundNatRuleConfig, o que adiciona uma configuração de regra NAT de entrada a ele.</span><span class="sxs-lookup"><span data-stu-id="bb97c-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="bb97c-113">O terceiro comando passa o balanceador de carga para **set-AzureRmLoadBalancerInboundNatRuleConfig** , que salva e atualiza a configuração da regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb97c-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="bb97c-114">Observe que a configuração da regra foi definida sem habilitar o IP flutuante, que foi habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="bb97c-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="bb97c-115">OS</span><span class="sxs-lookup"><span data-stu-id="bb97c-115">PARAMETERS</span></span>

### <span data-ttu-id="bb97c-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="bb97c-116">-BackendPort</span></span>
<span data-ttu-id="bb97c-117">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="bb97c-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="bb97c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb97c-118">-DefaultProfile</span></span>
<span data-ttu-id="bb97c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb97c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb97c-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="bb97c-120">-EnableFloatingIP</span></span>
<span data-ttu-id="bb97c-121">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="bb97c-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="bb97c-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb97c-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bb97c-123">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb97c-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="bb97c-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bb97c-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="bb97c-125">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="bb97c-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="bb97c-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bb97c-126">-FrontendPort</span></span>
<span data-ttu-id="bb97c-127">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="bb97c-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="bb97c-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="bb97c-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bb97c-129">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="bb97c-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="bb97c-130">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="bb97c-130">-LoadBalancer</span></span>
<span data-ttu-id="bb97c-131">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="bb97c-131">Specifies a load balancer.</span></span>
<span data-ttu-id="bb97c-132">Este cmdlet define uma configuração de regra NAT de entrada para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="bb97c-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb97c-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb97c-133">-Name</span></span>
<span data-ttu-id="bb97c-134">Especifica o nome de uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb97c-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="bb97c-135">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="bb97c-135">-Protocol</span></span>
<span data-ttu-id="bb97c-136">Especifica o protocolo que corresponde a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb97c-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="bb97c-137">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="bb97c-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="bb97c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb97c-138">CommonParameters</span></span>
<span data-ttu-id="bb97c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb97c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb97c-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb97c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb97c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb97c-141">INPUTS</span></span>

### <span data-ttu-id="bb97c-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bb97c-142">PSLoadBalancer</span></span>
<span data-ttu-id="bb97c-143">O parâmetro ' loadbalancer ' aceita o valor do tipo ' PSLoadBalancer ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bb97c-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bb97c-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb97c-144">OUTPUTS</span></span>

### <span data-ttu-id="bb97c-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bb97c-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bb97c-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb97c-146">NOTES</span></span>

## <span data-ttu-id="bb97c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb97c-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb97c-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb97c-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bb97c-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bb97c-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="bb97c-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb97c-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bb97c-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb97c-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="bb97c-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bb97c-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

