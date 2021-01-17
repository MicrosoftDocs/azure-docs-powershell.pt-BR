---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434628"
---
# <span data-ttu-id="f6795-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6795-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f6795-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6795-102">SYNOPSIS</span></span>
<span data-ttu-id="f6795-103">Define uma configuração de regra NAT de entrada para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f6795-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f6795-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6795-104">SYNTAX</span></span>

### <span data-ttu-id="f6795-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="f6795-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6795-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6795-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6795-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6795-107">DESCRIPTION</span></span>
<span data-ttu-id="f6795-108">O cmdlet **set-AzLoadBalancerInboundNatRuleConfig** define uma configuração de regra NAT (conversão de endereços de rede) de entrada para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6795-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f6795-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6795-109">EXAMPLES</span></span>

### <span data-ttu-id="f6795-110">Exemplo 1: modificar a configuração da regra NAT de entrada em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="f6795-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="f6795-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="f6795-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="f6795-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga em $slb para adicionar-AzLoadBalancerInboundNatRuleConfig, o que adiciona uma configuração de regra NAT de entrada a ele.</span><span class="sxs-lookup"><span data-stu-id="f6795-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="f6795-113">O terceiro comando passa o balanceador de carga para **set-AzLoadBalancerInboundNatRuleConfig**, que salva e atualiza a configuração da regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6795-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="f6795-114">Observe que a configuração da regra foi definida sem habilitar o IP flutuante, que foi habilitado pelo comando anterior.</span><span class="sxs-lookup"><span data-stu-id="f6795-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="f6795-115">OS</span><span class="sxs-lookup"><span data-stu-id="f6795-115">PARAMETERS</span></span>

### <span data-ttu-id="f6795-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f6795-116">-BackendPort</span></span>
<span data-ttu-id="f6795-117">Especifica a porta de back-end para o tráfego correspondente a essa configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="f6795-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="f6795-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6795-118">-DefaultProfile</span></span>
<span data-ttu-id="f6795-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6795-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6795-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f6795-120">-EnableFloatingIP</span></span>
<span data-ttu-id="f6795-121">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="f6795-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f6795-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f6795-122">-EnableTcpReset</span></span>
<span data-ttu-id="f6795-123">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="f6795-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="f6795-124">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="f6795-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f6795-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6795-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f6795-126">Especifica uma lista de endereços IP front-end a serem associados a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6795-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f6795-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f6795-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f6795-128">Especifica a ID de uma configuração de endereço IP de front-end.</span><span class="sxs-lookup"><span data-stu-id="f6795-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f6795-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f6795-129">-FrontendPort</span></span>
<span data-ttu-id="f6795-130">Especifica a porta de front-end que corresponde a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f6795-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f6795-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f6795-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f6795-132">Especifica o período de tempo, em minutos, em que o estado das conversas é mantido em um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f6795-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f6795-133">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="f6795-133">-LoadBalancer</span></span>
<span data-ttu-id="f6795-134">Especifica um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="f6795-134">Specifies a load balancer.</span></span>
<span data-ttu-id="f6795-135">Este cmdlet define uma configuração de regra NAT de entrada para o balanceador de carga que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f6795-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f6795-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6795-136">-Name</span></span>
<span data-ttu-id="f6795-137">Especifica o nome de uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6795-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f6795-138">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f6795-138">-Protocol</span></span>
<span data-ttu-id="f6795-139">Especifica o protocolo que corresponde a uma configuração de regra NAT de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6795-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="f6795-140">Os valores aceitáveis para esse parâmetro são: TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="f6795-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f6795-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6795-141">-Confirm</span></span>
<span data-ttu-id="f6795-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6795-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6795-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6795-143">-WhatIf</span></span>
<span data-ttu-id="f6795-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6795-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6795-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6795-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6795-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6795-146">CommonParameters</span></span>
<span data-ttu-id="f6795-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6795-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6795-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6795-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6795-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6795-149">INPUTS</span></span>

### <span data-ttu-id="f6795-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6795-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f6795-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f6795-151">System.String</span></span>

### <span data-ttu-id="f6795-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f6795-152">System.Int32</span></span>

### <span data-ttu-id="f6795-153">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6795-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="f6795-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6795-154">OUTPUTS</span></span>

### <span data-ttu-id="f6795-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6795-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f6795-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6795-156">NOTES</span></span>

## <span data-ttu-id="f6795-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6795-157">RELATED LINKS</span></span>

[<span data-ttu-id="f6795-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6795-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f6795-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f6795-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f6795-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6795-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f6795-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6795-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f6795-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f6795-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


