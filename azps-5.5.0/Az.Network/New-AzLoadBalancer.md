---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111640"
---
# <span data-ttu-id="da829-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da829-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="da829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da829-102">SYNOPSIS</span></span>
<span data-ttu-id="da829-103">Cria um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-103">Creates a load balancer.</span></span>

## <span data-ttu-id="da829-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da829-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da829-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="da829-105">DESCRIPTION</span></span>
<span data-ttu-id="da829-106">O **cmdlet New-AzLoadBalancer** cria um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="da829-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="da829-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="da829-107">EXAMPLES</span></span>

### <span data-ttu-id="da829-108">Exemplo 1: Criar um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="da829-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="da829-109">A implantação de um balanceador de carga exige que você primeiro crie vários objetos, e os sete primeiros comandos mostram como criar esses objetos.</span><span class="sxs-lookup"><span data-stu-id="da829-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="da829-110">O oitavo comando cria um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da829-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="da829-111">O nono e último comando obtém o novo balanceador de carga para garantir que ele tenha sido criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="da829-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="da829-112">Observe que este exemplo mostra apenas como criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="da829-113">Você também deve configurá-lo usando o cmdlet Add-AzNetworkInterfaceIpConfig para atribuir os NICs a diferentes máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="da829-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="da829-114">Exemplo 2: Criar um balanceador de carga global</span><span class="sxs-lookup"><span data-stu-id="da829-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="da829-115">A implantação de um balanceador de carga global exige que você primeiro crie vários objetos, e os cinco primeiros comandos mostram como criar esses objetos.</span><span class="sxs-lookup"><span data-stu-id="da829-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="da829-116">O sexto comando cria um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da829-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="da829-117">O sétimo e último comando obtém o novo balanceador de carga para garantir que ele tenha sido criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="da829-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="da829-118">Observe que este exemplo mostra apenas como criar um balanceador de carga global.</span><span class="sxs-lookup"><span data-stu-id="da829-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="da829-119">Você também deve configurá-lo usando o cmdlet New-AzLoadBalancerBackendAddressConfig para atribuir ids ipconfig frontend do saldo de carga regional ao seu pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="da829-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="da829-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da829-120">PARAMETERS</span></span>

### <span data-ttu-id="da829-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da829-121">-AsJob</span></span>
<span data-ttu-id="da829-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="da829-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da829-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="da829-123">-BackendAddressPool</span></span>
<span data-ttu-id="da829-124">Especifica um pool de endereços back-end para associar a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-124">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="da829-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da829-125">-DefaultProfile</span></span>
<span data-ttu-id="da829-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="da829-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da829-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="da829-127">-Force</span></span>
<span data-ttu-id="da829-128">Indica que esse cmdlet cria um balanceador de carga mesmo que já exista um balanceador de carga com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="da829-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="da829-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="da829-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="da829-130">Especifica uma lista de endereços IP front-end para associar a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="da829-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="da829-131">-InboundNatPool</span></span>
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

### <span data-ttu-id="da829-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="da829-132">-InboundNatRule</span></span>
<span data-ttu-id="da829-133">Especifica uma lista de regras de conversão de endereço de rede de entrada (NAT) para associar a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="da829-134">-Load ComncingRule</span><span class="sxs-lookup"><span data-stu-id="da829-134">-LoadBalancingRule</span></span>
<span data-ttu-id="da829-135">Especifica uma lista de regras de balanceamento de carga para associar a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="da829-136">-Local</span><span class="sxs-lookup"><span data-stu-id="da829-136">-Location</span></span>
<span data-ttu-id="da829-137">Especifica a região na qual criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="da829-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="da829-138">-Name</span></span>
<span data-ttu-id="da829-139">Especifica o nome do balanceador de carga que isso cria.</span><span class="sxs-lookup"><span data-stu-id="da829-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="da829-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="da829-140">-OutboundRule</span></span>
<span data-ttu-id="da829-141">As regras de saída.</span><span class="sxs-lookup"><span data-stu-id="da829-141">The outbound rules.</span></span>

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

### <span data-ttu-id="da829-142">-Desmão</span><span class="sxs-lookup"><span data-stu-id="da829-142">-Probe</span></span>
<span data-ttu-id="da829-143">Especifica uma lista de pontos negativos para associar a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-143">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="da829-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da829-144">-ResourceGroupName</span></span>
<span data-ttu-id="da829-145">Especifica o nome do grupo de recursos no qual criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="da829-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="da829-146">-Sku</span></span>
<span data-ttu-id="da829-147">O nome SKU do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="da829-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="da829-148">-Tag</span></span>
<span data-ttu-id="da829-149">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="da829-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="da829-150">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="da829-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="da829-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="da829-151">-Tier</span></span>
<span data-ttu-id="da829-152">A camada SKU do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="da829-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="da829-153">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="da829-153">-Confirm</span></span>
<span data-ttu-id="da829-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da829-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da829-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da829-155">-WhatIf</span></span>
<span data-ttu-id="da829-156">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="da829-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da829-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da829-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da829-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da829-158">CommonParameters</span></span>
<span data-ttu-id="da829-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da829-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da829-160">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da829-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da829-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="da829-161">INPUTS</span></span>

### <span data-ttu-id="da829-162">System.String</span><span class="sxs-lookup"><span data-stu-id="da829-162">System.String</span></span>

### <span data-ttu-id="da829-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="da829-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="da829-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="da829-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="da829-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="da829-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="da829-166">Microsoft.Azure.Commands.Network.Models.PSLoad QuencingRule[]</span><span class="sxs-lookup"><span data-stu-id="da829-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="da829-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="da829-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="da829-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="da829-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="da829-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="da829-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="da829-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="da829-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="da829-171">Saídas</span><span class="sxs-lookup"><span data-stu-id="da829-171">OUTPUTS</span></span>

### <span data-ttu-id="da829-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da829-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="da829-173">Notas</span><span class="sxs-lookup"><span data-stu-id="da829-173">NOTES</span></span>

## <span data-ttu-id="da829-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da829-174">RELATED LINKS</span></span>

[<span data-ttu-id="da829-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="da829-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="da829-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da829-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="da829-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da829-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="da829-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da829-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
