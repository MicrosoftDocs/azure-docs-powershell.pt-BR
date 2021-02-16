---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113532"
---
# <span data-ttu-id="910c2-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="910c2-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="910c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="910c2-102">SYNOPSIS</span></span>
<span data-ttu-id="910c2-103">Adiciona uma configuração de regra a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="910c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="910c2-104">SYNTAX</span></span>

### <span data-ttu-id="910c2-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="910c2-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="910c2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="910c2-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="910c2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="910c2-107">DESCRIPTION</span></span>
<span data-ttu-id="910c2-108">O cmdlet **Add-AzLoadBalancerRuleConfig** adiciona uma configuração de regra a um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="910c2-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="910c2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="910c2-109">EXAMPLES</span></span>

### <span data-ttu-id="910c2-110">Exemplo 1: Adicionar uma configuração de regra a um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="910c2-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="910c2-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e o armazena na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="910c2-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="910c2-112">O segundo comando usa o operador de pipeline para passar o balanceador de carga no $slb para **Add-AzLoadBalancerRuleConfig,** que adiciona a configuração de regra chamada NewRule.</span><span class="sxs-lookup"><span data-stu-id="910c2-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="910c2-113">O terceiro comando atualizará o balanceador de carga no azure com a nova Configuração de Regra do Balanceador de Carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="910c2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="910c2-114">PARAMETERS</span></span>

### <span data-ttu-id="910c2-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="910c2-115">-BackendAddressPool</span></span>
<span data-ttu-id="910c2-116">Especifica o pool de endereços back-end para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910c2-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="910c2-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="910c2-118">Especifica a ID de um objeto **BackendAddressPool** para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="910c2-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="910c2-119">-BackendPort</span></span>
<span data-ttu-id="910c2-120">Especifica a porta de back-end do tráfego que é corresponder a uma configuração de regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="910c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910c2-121">-DefaultProfile</span></span>
<span data-ttu-id="910c2-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="910c2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="910c2-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="910c2-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="910c2-124">Configura o SNAT para as VMs no pool de back-end para usar o endereço de IP público especificado na frente da regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="910c2-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="910c2-125">-EnableFloatingIP</span></span>
<span data-ttu-id="910c2-126">Indica que esse cmdlet habilita um endereço IP flutuante para uma configuração de regra.</span><span class="sxs-lookup"><span data-stu-id="910c2-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="910c2-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="910c2-127">-EnableTcpReset</span></span>
<span data-ttu-id="910c2-128">Receba a Redefinição de TCP bidirecional no tempo ocioso de fluxo TCP ou término de conexão inesperado.</span><span class="sxs-lookup"><span data-stu-id="910c2-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="910c2-129">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="910c2-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="910c2-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="910c2-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="910c2-131">Especifica uma lista de endereços IP front-end para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="910c2-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="910c2-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="910c2-133">Especifica a ID de uma configuração de endereço IP front-end.</span><span class="sxs-lookup"><span data-stu-id="910c2-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="910c2-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="910c2-134">-FrontendPort</span></span>
<span data-ttu-id="910c2-135">Especifica a porta front-end que é corresponder a uma configuração de regra de balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="910c2-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="910c2-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="910c2-137">Especifica o tempo, em minutos, de que o estado das conversas é mantido no balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="910c2-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="910c2-138">-LoadBalancer</span></span>
<span data-ttu-id="910c2-139">Especifica um **objeto LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="910c2-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="910c2-140">Este cmdlet adiciona uma configuração de regra ao balanceador de carga especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="910c2-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="910c2-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="910c2-141">-LoadDistribution</span></span>
<span data-ttu-id="910c2-142">Especifica uma distribuição de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="910c2-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="910c2-143">-Name</span></span>
<span data-ttu-id="910c2-144">Especifica o nome da configuração da regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="910c2-145">-Desmão</span><span class="sxs-lookup"><span data-stu-id="910c2-145">-Probe</span></span>
<span data-ttu-id="910c2-146">Especifica uma transição para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="910c2-147">-ElaId</span><span class="sxs-lookup"><span data-stu-id="910c2-147">-ProbeId</span></span>
<span data-ttu-id="910c2-148">Especifica a ID do teste para associar a uma configuração de regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="910c2-149">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="910c2-149">-Protocol</span></span>
<span data-ttu-id="910c2-150">Especifica o protocolo que é correspondente a uma regra de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="910c2-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="910c2-151">Os valores aceitáveis para este parâmetro são: Tcp ou Udp.</span><span class="sxs-lookup"><span data-stu-id="910c2-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="910c2-152">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="910c2-152">-Confirm</span></span>
<span data-ttu-id="910c2-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="910c2-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="910c2-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="910c2-154">-WhatIf</span></span>
<span data-ttu-id="910c2-155">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="910c2-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="910c2-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="910c2-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="910c2-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910c2-157">CommonParameters</span></span>
<span data-ttu-id="910c2-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="910c2-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910c2-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="910c2-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910c2-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="910c2-160">INPUTS</span></span>

### <span data-ttu-id="910c2-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="910c2-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="910c2-162">System.String</span><span class="sxs-lookup"><span data-stu-id="910c2-162">System.String</span></span>

### <span data-ttu-id="910c2-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="910c2-163">System.Int32</span></span>

### <span data-ttu-id="910c2-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="910c2-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="910c2-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="910c2-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="910c2-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="910c2-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="910c2-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="910c2-167">OUTPUTS</span></span>

### <span data-ttu-id="910c2-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="910c2-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="910c2-169">Notas</span><span class="sxs-lookup"><span data-stu-id="910c2-169">NOTES</span></span>

## <span data-ttu-id="910c2-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="910c2-170">RELATED LINKS</span></span>

[<span data-ttu-id="910c2-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="910c2-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="910c2-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="910c2-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="910c2-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="910c2-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="910c2-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="910c2-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="910c2-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="910c2-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


