---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1c813a7ac23ae8bc161f10df02ac618d5f6a7a81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431347"
---
# <span data-ttu-id="15a51-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15a51-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="15a51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15a51-102">SYNOPSIS</span></span>
<span data-ttu-id="15a51-103">Define uma configuração de regra de saída para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="15a51-103">Sets an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15a51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15a51-104">SYNTAX</span></span>

### <span data-ttu-id="15a51-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="15a51-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15a51-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15a51-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15a51-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15a51-107">DESCRIPTION</span></span>
<span data-ttu-id="15a51-108">O cmdlet **set-AzureRmLoadBalancerOutboundRuleConfig** define uma configuração de regra de saída para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="15a51-108">The **Set-AzureRmLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="15a51-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15a51-109">EXAMPLES</span></span>

### <span data-ttu-id="15a51-110">Exemplo 1: modificar a configuração da regra de saída em um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="15a51-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="15a51-111">O primeiro comando obtém o balanceador de carga chamado MyLoadBalancer e, em seguida, armazena-o na variável $slb.</span><span class="sxs-lookup"><span data-stu-id="15a51-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="15a51-112">O segundo comando usa o operador pipeline para passar o balanceador de carga em $slb para adicionar-AzureRmLoadBalancerOutboundRuleConfig, o que adiciona uma configuração de regra de saída a ele.</span><span class="sxs-lookup"><span data-stu-id="15a51-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="15a51-113">O terceiro comando passa o balanceador de carga para **set-AzureRmLoadBalancerOutboundRuleConfig** , que salva e atualiza a configuração da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="15a51-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="15a51-114">OS</span><span class="sxs-lookup"><span data-stu-id="15a51-114">PARAMETERS</span></span>

### <span data-ttu-id="15a51-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="15a51-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="15a51-116">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="15a51-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="15a51-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15a51-117">-BackendAddressPool</span></span>
<span data-ttu-id="15a51-118">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="15a51-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="15a51-119">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="15a51-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a51-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="15a51-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="15a51-121">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="15a51-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="15a51-122">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="15a51-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a51-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a51-123">-DefaultProfile</span></span>
<span data-ttu-id="15a51-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15a51-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a51-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="15a51-125">-EnableTcpReset</span></span>
<span data-ttu-id="15a51-126">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="15a51-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="15a51-127">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="15a51-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="15a51-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="15a51-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="15a51-129">Os endereços IP de front-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="15a51-129">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a51-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="15a51-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="15a51-131">O tempo limite para a conexão ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="15a51-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="15a51-132">-Loadbalancer</span><span class="sxs-lookup"><span data-stu-id="15a51-132">-LoadBalancer</span></span>
<span data-ttu-id="15a51-133">A referência do recurso de balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="15a51-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="15a51-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="15a51-134">-Name</span></span>
<span data-ttu-id="15a51-135">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="15a51-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="15a51-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="15a51-136">-Protocol</span></span>
<span data-ttu-id="15a51-137">Protocolo-TCP, UDP ou todos</span><span class="sxs-lookup"><span data-stu-id="15a51-137">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a51-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="15a51-138">-Confirm</span></span>
<span data-ttu-id="15a51-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15a51-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a51-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a51-140">-WhatIf</span></span>
<span data-ttu-id="15a51-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="15a51-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a51-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="15a51-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a51-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a51-143">CommonParameters</span></span>
<span data-ttu-id="15a51-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a51-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a51-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a51-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a51-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15a51-146">INPUTS</span></span>

### <span data-ttu-id="15a51-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15a51-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="15a51-148">System. Int32 System. String System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Network. Models. PSResourceId, Microsoft. Azure. Commands. Network, Version = 6.5.0.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15a51-148">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="15a51-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15a51-149">OUTPUTS</span></span>

### <span data-ttu-id="15a51-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="15a51-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="15a51-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15a51-151">NOTES</span></span>

## <span data-ttu-id="15a51-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15a51-152">RELATED LINKS</span></span>
