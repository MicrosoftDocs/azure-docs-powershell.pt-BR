---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115207"
---
# <span data-ttu-id="4cae2-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cae2-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4cae2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cae2-102">SYNOPSIS</span></span>
<span data-ttu-id="4cae2-103">Adiciona uma configuração de regra NAT de entrada a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4cae2-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="4cae2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cae2-104">SYNTAX</span></span>

### <span data-ttu-id="4cae2-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4cae2-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cae2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cae2-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cae2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cae2-107">DESCRIPTION</span></span>
<span data-ttu-id="4cae2-108">O cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** adiciona uma configuração de regra nat (conversão de endereço de rede de entrada) a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cae2-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="4cae2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4cae2-109">EXAMPLES</span></span>

### <span data-ttu-id="4cae2-110">Exemplo 1: Adicionar uma configuração de regra NAT de entrada a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="4cae2-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="4cae2-111">O primeiro comando obtém o balanceador de carga chamado MyloadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="4cae2-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="4cae2-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para **Add-AzLoadBalancerInboundNatRuleConfig,** que adiciona uma configuração de regra NAT de entrada ao balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4cae2-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="4cae2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cae2-113">PARAMETERS</span></span>

### <span data-ttu-id="4cae2-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4cae2-114">-BackendPort</span></span>
<span data-ttu-id="4cae2-115">Especifica a porta de back-end do tráfego que é corresponder a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="4cae2-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="4cae2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cae2-116">-DefaultProfile</span></span>
<span data-ttu-id="4cae2-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4cae2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cae2-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4cae2-118">-EnableFloatingIP</span></span>
<span data-ttu-id="4cae2-119">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="4cae2-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4cae2-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4cae2-120">-EnableTcpReset</span></span>
<span data-ttu-id="4cae2-121">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="4cae2-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4cae2-122">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="4cae2-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4cae2-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cae2-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4cae2-124">Especifica uma lista de endereços IP front-end para associar a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="4cae2-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="4cae2-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4cae2-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4cae2-126">Especifica uma ID para uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="4cae2-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="4cae2-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4cae2-127">-FrontendPort</span></span>
<span data-ttu-id="4cae2-128">Especifica a porta front-end que é corresponder a uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="4cae2-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="4cae2-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4cae2-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4cae2-130">Especifica o tempo, em minutos, de que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4cae2-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="4cae2-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cae2-131">-LoadBalancer</span></span>
<span data-ttu-id="4cae2-132">Especifica um **objeto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="4cae2-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="4cae2-133">Esse cmdlet adiciona uma configuração de regra NAT de entrada ao balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4cae2-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cae2-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cae2-134">-Name</span></span>
<span data-ttu-id="4cae2-135">Especifica o nome da configuração da regra NAT de entrada a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="4cae2-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="4cae2-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="4cae2-136">-Protocol</span></span>
<span data-ttu-id="4cae2-137">Especifica o protocolo que é correspondente a uma regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="4cae2-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="4cae2-138">Os valores aceitáveis para este parâmetro são: Tcp ou Udp.</span><span class="sxs-lookup"><span data-stu-id="4cae2-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="4cae2-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4cae2-139">-Confirm</span></span>
<span data-ttu-id="4cae2-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cae2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cae2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cae2-141">-WhatIf</span></span>
<span data-ttu-id="4cae2-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4cae2-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cae2-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cae2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cae2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cae2-144">CommonParameters</span></span>
<span data-ttu-id="4cae2-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cae2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cae2-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cae2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cae2-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="4cae2-147">INPUTS</span></span>

### <span data-ttu-id="4cae2-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cae2-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="4cae2-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4cae2-149">System.String</span></span>

### <span data-ttu-id="4cae2-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4cae2-150">System.Int32</span></span>

### <span data-ttu-id="4cae2-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cae2-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="4cae2-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="4cae2-152">OUTPUTS</span></span>

### <span data-ttu-id="4cae2-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cae2-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4cae2-154">Notas</span><span class="sxs-lookup"><span data-stu-id="4cae2-154">NOTES</span></span>

## <span data-ttu-id="4cae2-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cae2-155">RELATED LINKS</span></span>

[<span data-ttu-id="4cae2-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cae2-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4cae2-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cae2-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4cae2-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cae2-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4cae2-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cae2-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4cae2-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cae2-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="4cae2-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4cae2-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


