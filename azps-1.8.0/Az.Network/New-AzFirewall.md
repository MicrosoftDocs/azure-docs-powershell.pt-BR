---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600345"
---
# <span data-ttu-id="b4f26-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b4f26-101">New-AzFirewall</span></span>

## <span data-ttu-id="b4f26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4f26-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f26-103">Cria um novo firewall em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4f26-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="b4f26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4f26-104">SYNTAX</span></span>

### <span data-ttu-id="b4f26-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4f26-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f26-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="b4f26-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f26-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4f26-107">DESCRIPTION</span></span>
<span data-ttu-id="b4f26-108">O cmdlet **New-AzFirewall** cria um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f26-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="b4f26-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4f26-109">EXAMPLES</span></span>

### <span data-ttu-id="b4f26-110">1: criar um firewall anexado a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="b4f26-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="b4f26-111">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="b4f26-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="b4f26-112">Como nenhuma regra foi especificada, o Firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="b4f26-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="b4f26-113">Ameaça a Intel também será executada no modo padrão-Alert-o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="b4f26-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="b4f26-114">2: criar um firewall que permita todo o tráfego HTTPS</span><span class="sxs-lookup"><span data-stu-id="b4f26-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="b4f26-115">Este exemplo cria um firewall que permite todo o tráfego HTTPS na porta 443.</span><span class="sxs-lookup"><span data-stu-id="b4f26-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="b4f26-116">Ameaça a Intel será executada no modo padrão-Alert-lo, o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="b4f26-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="b4f26-117">3: DNAT-redirecionar o tráfego destinado ao 10.1.2.3:80 para 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="b4f26-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="b4f26-118">Este exemplo criou um firewall que converteu o IP de destino e a porta de todos os pacotes destinados a 10.1.2.3:80 para 10.2.3.4: ameaça de 8080 a Intel está desativada neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="b4f26-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="b4f26-119">4: criar um firewall sem regras e com ameaças à Intel em modo de alerta</span><span class="sxs-lookup"><span data-stu-id="b4f26-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="b4f26-120">Este exemplo cria um firewall que bloqueia todo o tráfego (comportamento padrão) e tem ameaça Intel em execução no modo de alerta.</span><span class="sxs-lookup"><span data-stu-id="b4f26-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="b4f26-121">Isso significa que os logs de alerta são emitidos para tráfego mal-intencionado antes de aplicar as outras regras (neste caso, apenas a regra padrão-negar tudo)</span><span class="sxs-lookup"><span data-stu-id="b4f26-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="b4f26-122">5: criar um firewall que permita todo o tráfego HTTP na porta 8080, mas bloquear domínios maliciosos identificados pela Intel® Threat</span><span class="sxs-lookup"><span data-stu-id="b4f26-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="b4f26-123">Este exemplo cria um firewall que permite todo o tráfego HTTP na porta 8080, a menos que seja considerado mal-intencionado pela Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="b4f26-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="b4f26-124">Ao executar no modo negar, ao contrário do alerta, o tráfego é considerado mal-intencionado pela ameaça, a Intel não está apenas registrada, mas também bloqueada.</span><span class="sxs-lookup"><span data-stu-id="b4f26-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="b4f26-125">OS</span><span class="sxs-lookup"><span data-stu-id="b4f26-125">PARAMETERS</span></span>

### <span data-ttu-id="b4f26-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b4f26-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="b4f26-127">Especifica as coleções de regras do aplicativo para o novo firewall.</span><span class="sxs-lookup"><span data-stu-id="b4f26-127">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f26-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4f26-128">-AsJob</span></span>
<span data-ttu-id="b4f26-129">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b4f26-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4f26-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f26-130">-DefaultProfile</span></span>
<span data-ttu-id="b4f26-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f26-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4f26-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b4f26-132">-Force</span></span>
<span data-ttu-id="b4f26-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b4f26-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4f26-134">-Local</span><span class="sxs-lookup"><span data-stu-id="b4f26-134">-Location</span></span>
<span data-ttu-id="b4f26-135">Especifica a região do firewall.</span><span class="sxs-lookup"><span data-stu-id="b4f26-135">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="b4f26-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4f26-136">-Name</span></span>
<span data-ttu-id="b4f26-137">Especifica o nome do firewall do Azure que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="b4f26-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b4f26-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b4f26-138">-NatRuleCollection</span></span>
<span data-ttu-id="b4f26-139">A lista de AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="b4f26-139">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f26-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b4f26-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="b4f26-141">A lista de AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="b4f26-141">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f26-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="b4f26-142">-PublicIpName</span></span>
<span data-ttu-id="b4f26-143">Nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="b4f26-143">Public Ip Name.</span></span> <span data-ttu-id="b4f26-144">O IP público deve usar a SKU padrão e deve pertencer ao mesmo grupo de recursos do firewall.</span><span class="sxs-lookup"><span data-stu-id="b4f26-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f26-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f26-145">-ResourceGroupName</span></span>
<span data-ttu-id="b4f26-146">Especifica o nome de um grupo de recursos para conter o firewall.</span><span class="sxs-lookup"><span data-stu-id="b4f26-146">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="b4f26-147">-Marca</span><span class="sxs-lookup"><span data-stu-id="b4f26-147">-Tag</span></span>
<span data-ttu-id="b4f26-148">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b4f26-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4f26-149">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b4f26-149">For example:</span></span>

<span data-ttu-id="b4f26-150">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b4f26-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b4f26-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="b4f26-151">-ThreatIntelMode</span></span>
<span data-ttu-id="b4f26-152">Especifica o modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="b4f26-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="b4f26-153">O modo padrão é alerta, não está desligado.</span><span class="sxs-lookup"><span data-stu-id="b4f26-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f26-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b4f26-154">-VirtualNetworkName</span></span>
<span data-ttu-id="b4f26-155">Especifica o nome da rede virtual para a qual o firewall será implantado.</span><span class="sxs-lookup"><span data-stu-id="b4f26-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="b4f26-156">A rede virtual e o firewall devem pertencer ao mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4f26-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f26-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4f26-157">-Confirm</span></span>
<span data-ttu-id="b4f26-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4f26-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f26-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f26-159">-WhatIf</span></span>
<span data-ttu-id="b4f26-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4f26-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4f26-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4f26-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f26-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f26-162">CommonParameters</span></span>
<span data-ttu-id="b4f26-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f26-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f26-164">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f26-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f26-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4f26-165">INPUTS</span></span>

### <span data-ttu-id="b4f26-166">System. String</span><span class="sxs-lookup"><span data-stu-id="b4f26-166">System.String</span></span>

### <span data-ttu-id="b4f26-167">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="b4f26-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="b4f26-168">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="b4f26-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="b4f26-169">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="b4f26-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="b4f26-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4f26-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4f26-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4f26-171">OUTPUTS</span></span>

### <span data-ttu-id="b4f26-172">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="b4f26-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="b4f26-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4f26-173">NOTES</span></span>

## <span data-ttu-id="b4f26-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4f26-174">RELATED LINKS</span></span>

[<span data-ttu-id="b4f26-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b4f26-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="b4f26-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b4f26-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="b4f26-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b4f26-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="b4f26-178">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b4f26-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="b4f26-179">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b4f26-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="b4f26-180">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b4f26-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
