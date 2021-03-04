---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50f3c3a02410adda37b26c88cd5196c4ae232f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887874"
---
# <span data-ttu-id="32b39-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32b39-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="32b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b39-102">SYNOPSIS</span></span>
<span data-ttu-id="32b39-103">Cria uma configuração de regra de saída para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="32b39-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="32b39-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32b39-104">SYNTAX</span></span>

### <span data-ttu-id="32b39-105">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="32b39-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32b39-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="32b39-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32b39-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32b39-107">DESCRIPTION</span></span>
<span data-ttu-id="32b39-108">O cmdlet **New-AzLoadBalancerOutboundRuleConfig** cria uma configuração de regra de saída para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="32b39-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="32b39-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32b39-109">EXAMPLES</span></span>

### <span data-ttu-id="32b39-110">Exemplo 1: Criar uma configuração de regra de saída para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="32b39-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="32b39-111">O primeiro comando cria um endereço IP público chamado MyPublicIP no grupo de recursos chamado MyResourceGroup e o armazena na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="32b39-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="32b39-112">O segundo comando cria uma configuração ip front-end chamada FrontendIpConfig01 usando o endereço IP público no $publicip e, em seguida, o armazena na variável $frontend.</span><span class="sxs-lookup"><span data-stu-id="32b39-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="32b39-113">O terceiro comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool01 e o armazena na variável $backend backend.</span><span class="sxs-lookup"><span data-stu-id="32b39-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="32b39-114">O quarto comando cria uma configuração de regra de saída chamada MyOutboundRule usando os objetos front-end e back-end em $frontend e $backend.</span><span class="sxs-lookup"><span data-stu-id="32b39-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="32b39-115">Os *parâmetros Protocol*, *FrontendIPConfiguration* e *BackendAddressPool* são todos necessários para criar uma configuração de regra de saída.</span><span class="sxs-lookup"><span data-stu-id="32b39-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="32b39-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="32b39-116">Example 2</span></span>

<span data-ttu-id="32b39-117">Cria uma configuração de regra de saída para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="32b39-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="32b39-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="32b39-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="32b39-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32b39-119">PARAMETERS</span></span>

### <span data-ttu-id="32b39-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="32b39-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="32b39-121">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="32b39-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="32b39-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="32b39-122">-BackendAddressPool</span></span>
<span data-ttu-id="32b39-123">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="32b39-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="32b39-124">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="32b39-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="32b39-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="32b39-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="32b39-126">Uma referência a um pool de DIPs.</span><span class="sxs-lookup"><span data-stu-id="32b39-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="32b39-127">O tráfego de saída é carregado aleatoriamente balanceado entre IPs nos IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="32b39-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="32b39-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b39-128">-DefaultProfile</span></span>
<span data-ttu-id="32b39-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32b39-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b39-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="32b39-130">-EnableTcpReset</span></span>
<span data-ttu-id="32b39-131">Receber redefinição TCP bidirecional no tempo de ociosidade do fluxo TCP ou término inesperado da conexão.</span><span class="sxs-lookup"><span data-stu-id="32b39-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="32b39-132">Esse elemento só é usado quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="32b39-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="32b39-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="32b39-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="32b39-134">Os endereços IP Frontend do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="32b39-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32b39-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="32b39-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="32b39-136">O tempo de tempo para a conexão ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="32b39-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="32b39-137">-Name</span><span class="sxs-lookup"><span data-stu-id="32b39-137">-Name</span></span>
<span data-ttu-id="32b39-138">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="32b39-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="32b39-139">-Protocol</span><span class="sxs-lookup"><span data-stu-id="32b39-139">-Protocol</span></span>
<span data-ttu-id="32b39-140">Protocolo - TCP, UDP ou Todos</span><span class="sxs-lookup"><span data-stu-id="32b39-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="32b39-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32b39-141">-Confirm</span></span>
<span data-ttu-id="32b39-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b39-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b39-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b39-143">-WhatIf</span></span>
<span data-ttu-id="32b39-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32b39-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b39-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32b39-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b39-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b39-146">CommonParameters</span></span>
<span data-ttu-id="32b39-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b39-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b39-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b39-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b39-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32b39-149">INPUTS</span></span>

### <span data-ttu-id="32b39-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="32b39-150">System.Int32</span></span>

### <span data-ttu-id="32b39-151">System.String</span><span class="sxs-lookup"><span data-stu-id="32b39-151">System.String</span></span>

### <span data-ttu-id="32b39-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="32b39-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="32b39-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="32b39-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="32b39-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32b39-154">OUTPUTS</span></span>

### <span data-ttu-id="32b39-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="32b39-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="32b39-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="32b39-156">NOTES</span></span>

## <span data-ttu-id="32b39-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32b39-157">RELATED LINKS</span></span>

[<span data-ttu-id="32b39-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32b39-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="32b39-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32b39-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="32b39-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32b39-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="32b39-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="32b39-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
