---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 402235f4d98b39ec78ffdc67bd0a01ab16e0400a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428081"
---
# <span data-ttu-id="12678-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12678-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="12678-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12678-102">SYNOPSIS</span></span>
<span data-ttu-id="12678-103">Adiciona uma configuração de regra NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="12678-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12678-104">SYNTAX</span></span>

### <span data-ttu-id="12678-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="12678-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12678-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="12678-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12678-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12678-107">DESCRIPTION</span></span>
<span data-ttu-id="12678-108">O cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** adiciona uma configuração de regra NAT (conversão de endereços de rede) de entrada a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="12678-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="12678-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12678-109">EXAMPLES</span></span>

### <span data-ttu-id="12678-110">Exemplo 1: adicionar uma configuração de regra NAT de entrada a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="12678-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="12678-111">O primeiro comando obtém o balanceador de carga chamado MyloadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="12678-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="12678-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para **Add-AzureRmLoadBalancerInboundNatRuleConfig** , que adiciona uma configuração de regra NAT de entrada ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="12678-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="12678-113">OS</span><span class="sxs-lookup"><span data-stu-id="12678-113">PARAMETERS</span></span>

### <span data-ttu-id="12678-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="12678-114">-BackendPort</span></span>
<span data-ttu-id="12678-115">Especifica a porta de back-end para o tráfego correspondente a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="12678-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="12678-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12678-116">-DefaultProfile</span></span>
<span data-ttu-id="12678-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12678-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12678-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="12678-118">-EnableFloatingIP</span></span>
<span data-ttu-id="12678-119">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="12678-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="12678-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="12678-120">-EnableTcpReset</span></span>
<span data-ttu-id="12678-121">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="12678-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="12678-122">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="12678-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="12678-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="12678-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="12678-124">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="12678-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="12678-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="12678-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="12678-126">Especifica uma ID para uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="12678-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="12678-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="12678-127">-FrontendPort</span></span>
<span data-ttu-id="12678-128">Especifica a porta de front-end que corresponde a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="12678-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="12678-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="12678-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="12678-130">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="12678-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="12678-131">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="12678-131">-LoadBalancer</span></span>
<span data-ttu-id="12678-132">Especifica um objeto **Loadbalancer** .</span><span class="sxs-lookup"><span data-stu-id="12678-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="12678-133">Esse cmdlet adiciona uma configuração de regra NAT de entrada ao balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="12678-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12678-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="12678-134">-Name</span></span>
<span data-ttu-id="12678-135">Especifica o nome da configuração de regra NAT de entrada a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="12678-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="12678-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="12678-136">-Protocol</span></span>
<span data-ttu-id="12678-137">Especifica o protocolo que corresponde a uma regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="12678-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="12678-138">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="12678-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="12678-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12678-139">-Confirm</span></span>
<span data-ttu-id="12678-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12678-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12678-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12678-141">-WhatIf</span></span>
<span data-ttu-id="12678-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12678-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12678-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12678-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12678-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12678-144">CommonParameters</span></span>
<span data-ttu-id="12678-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12678-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12678-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12678-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12678-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12678-147">INPUTS</span></span>

### <span data-ttu-id="12678-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12678-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="12678-149">Parâmetros: loadbalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12678-149">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="12678-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12678-150">OUTPUTS</span></span>

### <span data-ttu-id="12678-151">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12678-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="12678-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12678-152">NOTES</span></span>

## <span data-ttu-id="12678-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12678-153">RELATED LINKS</span></span>

[<span data-ttu-id="12678-154">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12678-154">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="12678-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12678-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="12678-156">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12678-156">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="12678-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12678-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="12678-158">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="12678-158">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="12678-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12678-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)

