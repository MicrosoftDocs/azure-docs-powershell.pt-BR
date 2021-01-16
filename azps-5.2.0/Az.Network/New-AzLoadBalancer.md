---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261765"
---
# <span data-ttu-id="69364-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69364-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="69364-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69364-102">SYNOPSIS</span></span>
<span data-ttu-id="69364-103">Cria um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-103">Creates a load balancer.</span></span>

## <span data-ttu-id="69364-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69364-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69364-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69364-105">DESCRIPTION</span></span>
<span data-ttu-id="69364-106">O cmdlet **New-AzLoadBalancer** cria um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="69364-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="69364-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69364-107">EXAMPLES</span></span>

### <span data-ttu-id="69364-108">Exemplo 1: criar um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="69364-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="69364-109">A implantação de um balanceador de carga exige que você primeiro crie vários objetos e os primeiros sete comandos mostram como criar esses objetos.</span><span class="sxs-lookup"><span data-stu-id="69364-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="69364-110">O oitavo comando cria um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="69364-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="69364-111">O nono e o último comando recebem o novo balanceador de carga para garantir que ele foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="69364-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="69364-112">Observe que este exemplo mostra apenas como criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="69364-113">Você também deve configurá-lo usando o cmdlet Add-AzNetworkInterfaceIpConfig para atribuir NICs a máquinas virtuais diferentes.</span><span class="sxs-lookup"><span data-stu-id="69364-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="69364-114">Exemplo 2: criar um balanceador de carga global</span><span class="sxs-lookup"><span data-stu-id="69364-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="69364-115">A implantação de um balanceador de carga global exige que você primeiro crie vários objetos, e os cinco primeiros comandos mostram como criar esses objetos.</span><span class="sxs-lookup"><span data-stu-id="69364-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="69364-116">O sexto comando cria um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="69364-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="69364-117">O sétimo e o último comando recebem o novo balanceador de carga para garantir que ele foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="69364-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="69364-118">Observe que este exemplo mostra apenas como criar um balanceador de carga global.</span><span class="sxs-lookup"><span data-stu-id="69364-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="69364-119">Você também deve configurá-lo usando o cmdlet New-AzLoadBalancerBackendAddressConfig para atribuir IDs de ipconfig de front-end de carga regional ao pool de endereços back-end</span><span class="sxs-lookup"><span data-stu-id="69364-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="69364-120">OS</span><span class="sxs-lookup"><span data-stu-id="69364-120">PARAMETERS</span></span>

### <span data-ttu-id="69364-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69364-121">-AsJob</span></span>
<span data-ttu-id="69364-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69364-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69364-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="69364-123">-BackendAddressPool</span></span>
<span data-ttu-id="69364-124">Especifica um pool de endereços de back-end a ser associado a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-124">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69364-125">-DefaultProfile</span></span>
<span data-ttu-id="69364-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69364-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69364-127">-Force</span><span class="sxs-lookup"><span data-stu-id="69364-127">-Force</span></span>
<span data-ttu-id="69364-128">Indica que esse cmdlet cria um balanceador de carga, mesmo que já exista um balanceador de carga com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="69364-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="69364-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="69364-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="69364-130">Especifica uma lista de endereços IP front-end a serem associados a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="69364-131">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="69364-132">-InboundNatRule</span></span>
<span data-ttu-id="69364-133">Especifica uma lista de regras de entrada de NAT (conversão de endereço de rede) a serem associadas a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="69364-134">-LoadBalancingRule</span></span>
<span data-ttu-id="69364-135">Especifica uma lista de regras de balanceamento de carga a serem associadas a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-136">-Local</span><span class="sxs-lookup"><span data-stu-id="69364-136">-Location</span></span>
<span data-ttu-id="69364-137">Especifica a região na qual criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="69364-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="69364-138">-Name</span></span>
<span data-ttu-id="69364-139">Especifica o nome do balanceador de carga criado.</span><span class="sxs-lookup"><span data-stu-id="69364-139">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="69364-140">-OutboundRule</span></span>
<span data-ttu-id="69364-141">As regras de saída.</span><span class="sxs-lookup"><span data-stu-id="69364-141">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-142">-Teste</span><span class="sxs-lookup"><span data-stu-id="69364-142">-Probe</span></span>
<span data-ttu-id="69364-143">Especifica uma lista de testes a serem associados a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-143">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69364-144">-ResourceGroupName</span></span>
<span data-ttu-id="69364-145">Especifica o nome do grupo de recursos no qual criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="69364-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="69364-146">-Sku</span></span>
<span data-ttu-id="69364-147">O nome SKU do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="69364-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="69364-148">-Tag</span></span>
<span data-ttu-id="69364-149">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="69364-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="69364-150">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="69364-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69364-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="69364-151">-Tier</span></span>
<span data-ttu-id="69364-152">A camada SKU do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="69364-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="69364-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="69364-153">-Confirm</span></span>
<span data-ttu-id="69364-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69364-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69364-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69364-155">-WhatIf</span></span>
<span data-ttu-id="69364-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69364-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69364-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69364-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69364-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69364-158">CommonParameters</span></span>
<span data-ttu-id="69364-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69364-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69364-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69364-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69364-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69364-161">INPUTS</span></span>

### <span data-ttu-id="69364-162">System. String</span><span class="sxs-lookup"><span data-stu-id="69364-162">System.String</span></span>

### <span data-ttu-id="69364-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="69364-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="69364-164">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="69364-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="69364-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="69364-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="69364-166">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule []</span><span class="sxs-lookup"><span data-stu-id="69364-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="69364-167">Microsoft. Azure. Commands. Network. Models. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="69364-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="69364-168">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="69364-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="69364-169">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool []</span><span class="sxs-lookup"><span data-stu-id="69364-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="69364-170">Microsoft. Azure. Commands. Network. Models. PSOutboundRule []</span><span class="sxs-lookup"><span data-stu-id="69364-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="69364-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69364-171">OUTPUTS</span></span>

### <span data-ttu-id="69364-172">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69364-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="69364-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69364-173">NOTES</span></span>

## <span data-ttu-id="69364-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69364-174">RELATED LINKS</span></span>

[<span data-ttu-id="69364-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="69364-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="69364-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69364-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="69364-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69364-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="69364-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="69364-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
