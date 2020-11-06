---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: 10e39f72de835b77a0a8e91f0752b18ee739e0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441304"
---
# <span data-ttu-id="53ac3-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53ac3-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="53ac3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="53ac3-103">Cria um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53ac3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53ac3-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53ac3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53ac3-105">DESCRIPTION</span></span>
<span data-ttu-id="53ac3-106">O cmdlet **New-AzureRmLoadBalancer** cria um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="53ac3-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="53ac3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53ac3-107">EXAMPLES</span></span>

### <span data-ttu-id="53ac3-108">Exemplo 1: criar um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="53ac3-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="53ac3-109">A implantação de um balanceador de carga exige que você primeiro crie vários objetos e os primeiros sete comandos mostram como criar esses objetos.</span><span class="sxs-lookup"><span data-stu-id="53ac3-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="53ac3-110">O oitavo comando cria um balanceador de carga chamado MyLoadBalancer no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="53ac3-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="53ac3-111">O nono e o último comando recebem o novo balanceador de carga para garantir que ele foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="53ac3-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="53ac3-112">Observe que este exemplo mostra apenas como criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="53ac3-113">Você também deve configurá-lo usando o cmdlet Add-AzureRmNetworkInterfaceIpConfig para atribuir NICs a máquinas virtuais diferentes.</span><span class="sxs-lookup"><span data-stu-id="53ac3-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="53ac3-114">OS</span><span class="sxs-lookup"><span data-stu-id="53ac3-114">PARAMETERS</span></span>

### <span data-ttu-id="53ac3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53ac3-115">-AsJob</span></span>
<span data-ttu-id="53ac3-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="53ac3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53ac3-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53ac3-117">-BackendAddressPool</span></span>
<span data-ttu-id="53ac3-118">Especifica um pool de endereços de back-end a ser associado a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ac3-119">-DefaultProfile</span></span>
<span data-ttu-id="53ac3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53ac3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53ac3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="53ac3-121">-Force</span></span>
<span data-ttu-id="53ac3-122">Indica que esse cmdlet cria um balanceador de carga, mesmo que já exista um balanceador de carga com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="53ac3-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="53ac3-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="53ac3-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="53ac3-124">Especifica uma lista de endereços IP front-end a serem associados a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="53ac3-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="53ac3-126">-InboundNatRule</span></span>
<span data-ttu-id="53ac3-127">Especifica uma lista de regras de entrada de NAT (conversão de endereço de rede) a serem associadas a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="53ac3-128">-LoadBalancingRule</span></span>
<span data-ttu-id="53ac3-129">Especifica uma lista de regras de balanceamento de carga a serem associadas a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-130">-Local</span><span class="sxs-lookup"><span data-stu-id="53ac3-130">-Location</span></span>
<span data-ttu-id="53ac3-131">Especifica a região na qual criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="53ac3-132">-Name</span></span>
<span data-ttu-id="53ac3-133">Especifica o nome do balanceador de carga criado.</span><span class="sxs-lookup"><span data-stu-id="53ac3-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-134">-Teste</span><span class="sxs-lookup"><span data-stu-id="53ac3-134">-Probe</span></span>
<span data-ttu-id="53ac3-135">Especifica uma lista de testes a serem associados a um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-135">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ac3-136">-ResourceGroupName</span></span>
<span data-ttu-id="53ac3-137">Especifica o nome do grupo de recursos no qual criar um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="53ac3-138">-Sku</span></span>
<span data-ttu-id="53ac3-139">O nome SKU do balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="53ac3-139">The load balancer Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="53ac3-140">-Tag</span></span>
<span data-ttu-id="53ac3-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="53ac3-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="53ac3-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="53ac3-142">For example:</span></span>

<span data-ttu-id="53ac3-143">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="53ac3-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53ac3-144">-Confirm</span></span>
<span data-ttu-id="53ac3-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53ac3-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53ac3-146">-WhatIf</span></span>
<span data-ttu-id="53ac3-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53ac3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53ac3-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53ac3-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ac3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ac3-149">CommonParameters</span></span>
<span data-ttu-id="53ac3-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ac3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ac3-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ac3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ac3-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53ac3-152">INPUTS</span></span>

### <span data-ttu-id="53ac3-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="53ac3-153">None</span></span>
<span data-ttu-id="53ac3-154">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="53ac3-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53ac3-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53ac3-155">OUTPUTS</span></span>

### <span data-ttu-id="53ac3-156">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53ac3-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="53ac3-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53ac3-157">NOTES</span></span>

## <span data-ttu-id="53ac3-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53ac3-158">RELATED LINKS</span></span>

[<span data-ttu-id="53ac3-159">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53ac3-159">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="53ac3-160">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53ac3-160">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="53ac3-161">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53ac3-161">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="53ac3-162">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53ac3-162">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)