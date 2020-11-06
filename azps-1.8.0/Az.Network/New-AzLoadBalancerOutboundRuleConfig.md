---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50a8cd14c6ea61f7c772df96f4addb9ae7955444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600320"
---
# <span data-ttu-id="84030-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84030-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="84030-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84030-102">SYNOPSIS</span></span>
<span data-ttu-id="84030-103">Cria uma configuração de regra de saída para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="84030-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="84030-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84030-104">SYNTAX</span></span>

### <span data-ttu-id="84030-105">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="84030-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84030-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="84030-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84030-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84030-107">DESCRIPTION</span></span>
<span data-ttu-id="84030-108">O cmdlet **New-AzLoadBalancerOutboundRuleConfig** cria uma configuração de regra de saída para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="84030-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="84030-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84030-109">EXAMPLES</span></span>

### <span data-ttu-id="84030-110">Exemplo 1: criar uma configuração de regra de saída para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="84030-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="84030-111">O primeiro comando cria um endereço IP público chamado MyPublicIP no grupo de recursos chamado MyResource Group e, em seguida, armazena-o na variável $publicip.</span><span class="sxs-lookup"><span data-stu-id="84030-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="84030-112">O segundo comando cria uma configuração de IP de front-end chamada FrontendIpConfig01 usando o endereço IP público no $publicip e, em seguida, armazena-o na variável $frontend.</span><span class="sxs-lookup"><span data-stu-id="84030-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="84030-113">O terceiro comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool01 e, em seguida, armazena-a na variável $backend.</span><span class="sxs-lookup"><span data-stu-id="84030-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="84030-114">O quarto comando cria uma configuração de regra de saída chamada MyOutboundRule usando os objetos front-end e back-end no $frontend e $backend.</span><span class="sxs-lookup"><span data-stu-id="84030-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="84030-115">Os parâmetros *Protocol* , *FrontendIPConfiguration* e *BackendAddressPool* são necessários para criar uma configuração de regra de saída.</span><span class="sxs-lookup"><span data-stu-id="84030-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="84030-116">OS</span><span class="sxs-lookup"><span data-stu-id="84030-116">PARAMETERS</span></span>

### <span data-ttu-id="84030-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="84030-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="84030-118">O número de portas de saída a serem usadas para NAT.</span><span class="sxs-lookup"><span data-stu-id="84030-118">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="84030-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="84030-119">-BackendAddressPool</span></span>
<span data-ttu-id="84030-120">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="84030-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="84030-121">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="84030-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="84030-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="84030-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="84030-123">Uma referência a um conjunto de DIPs.</span><span class="sxs-lookup"><span data-stu-id="84030-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="84030-124">O tráfego de saída é de carga aleatória balanceada em IPs no IPs de back-end.</span><span class="sxs-lookup"><span data-stu-id="84030-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="84030-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84030-125">-DefaultProfile</span></span>
<span data-ttu-id="84030-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84030-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84030-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="84030-127">-EnableTcpReset</span></span>
<span data-ttu-id="84030-128">Receber a redefinição de TCP bidirecional no tempo limite de ociosidade do fluxo TCP ou terminação inesperada de conexão.</span><span class="sxs-lookup"><span data-stu-id="84030-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="84030-129">Esse elemento é usado apenas quando o protocolo é definido como TCP.</span><span class="sxs-lookup"><span data-stu-id="84030-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="84030-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="84030-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="84030-131">Os endereços IP de front-end do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="84030-131">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="84030-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="84030-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="84030-133">O tempo limite para a conexão ociosa TCP</span><span class="sxs-lookup"><span data-stu-id="84030-133">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="84030-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="84030-134">-Name</span></span>
<span data-ttu-id="84030-135">Nome da regra de saída.</span><span class="sxs-lookup"><span data-stu-id="84030-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="84030-136">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="84030-136">-Protocol</span></span>
<span data-ttu-id="84030-137">Protocolo-TCP, UDP ou todos</span><span class="sxs-lookup"><span data-stu-id="84030-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="84030-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="84030-138">-Confirm</span></span>
<span data-ttu-id="84030-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84030-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84030-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84030-140">-WhatIf</span></span>
<span data-ttu-id="84030-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="84030-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84030-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84030-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84030-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84030-143">CommonParameters</span></span>
<span data-ttu-id="84030-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84030-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84030-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84030-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84030-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84030-146">INPUTS</span></span>

### <span data-ttu-id="84030-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="84030-147">System.Int32</span></span>

### <span data-ttu-id="84030-148">System. String</span><span class="sxs-lookup"><span data-stu-id="84030-148">System.String</span></span>

### <span data-ttu-id="84030-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="84030-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="84030-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="84030-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="84030-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84030-151">OUTPUTS</span></span>

### <span data-ttu-id="84030-152">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="84030-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="84030-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84030-153">NOTES</span></span>

## <span data-ttu-id="84030-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84030-154">RELATED LINKS</span></span>

[<span data-ttu-id="84030-155">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84030-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="84030-156">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84030-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="84030-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84030-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="84030-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="84030-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
