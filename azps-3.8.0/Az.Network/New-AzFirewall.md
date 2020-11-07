---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777227"
---
# <span data-ttu-id="c852e-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c852e-101">New-AzFirewall</span></span>

## <span data-ttu-id="c852e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c852e-102">SYNOPSIS</span></span>
<span data-ttu-id="c852e-103">Cria um novo firewall em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c852e-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="c852e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c852e-104">SYNTAX</span></span>

### <span data-ttu-id="c852e-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="c852e-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c852e-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="c852e-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c852e-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="c852e-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c852e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c852e-108">DESCRIPTION</span></span>
<span data-ttu-id="c852e-109">O cmdlet **New-AzFirewall** cria um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="c852e-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="c852e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c852e-110">EXAMPLES</span></span>

### <span data-ttu-id="c852e-111">1: criar um firewall anexado a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="c852e-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="c852e-112">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c852e-113">Como nenhuma regra foi especificada, o Firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="c852e-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="c852e-114">Ameaça a Intel também será executada no modo padrão-Alert-o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="c852e-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="c852e-115">2: criar um firewall que permita todo o tráfego HTTPS</span><span class="sxs-lookup"><span data-stu-id="c852e-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="c852e-116">Este exemplo cria um firewall que permite todo o tráfego HTTPS na porta 443.</span><span class="sxs-lookup"><span data-stu-id="c852e-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="c852e-117">Ameaça a Intel será executada no modo padrão-Alert-lo, o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="c852e-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="c852e-118">3: DNAT-redirecionar o tráfego destinado ao 10.1.2.3:80 para 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="c852e-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="c852e-119">Este exemplo criou um firewall que converteu o IP de destino e a porta de todos os pacotes destinados a 10.1.2.3:80 para 10.2.3.4: ameaça de 8080 a Intel está desativada neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="c852e-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="c852e-120">4: criar um firewall sem regras e com ameaças à Intel em modo de alerta</span><span class="sxs-lookup"><span data-stu-id="c852e-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="c852e-121">Este exemplo cria um firewall que bloqueia todo o tráfego (comportamento padrão) e tem ameaça Intel em execução no modo de alerta.</span><span class="sxs-lookup"><span data-stu-id="c852e-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="c852e-122">Isso significa que os logs de alerta são emitidos para tráfego mal-intencionado antes de aplicar as outras regras (neste caso, apenas a regra padrão-negar tudo)</span><span class="sxs-lookup"><span data-stu-id="c852e-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="c852e-123">5: criar um firewall que permita todo o tráfego HTTP na porta 8080, mas bloquear domínios maliciosos identificados pela Intel® Threat</span><span class="sxs-lookup"><span data-stu-id="c852e-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="c852e-124">Este exemplo cria um firewall que permite todo o tráfego HTTP na porta 8080, a menos que seja considerado mal-intencionado pela Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="c852e-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="c852e-125">Ao executar no modo negar, ao contrário do alerta, o tráfego é considerado mal-intencionado pela ameaça, a Intel não está apenas registrada, mas também bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c852e-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="c852e-126">6: criar um firewall sem regras e zonas de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="c852e-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="c852e-127">Este exemplo cria um firewall com todas as zonas de disponibilidade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c852e-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="c852e-128">7: criar um firewall com dois ou mais endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="c852e-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="c852e-129">Este exemplo cria um firewall anexado à rede virtual "vnet" com dois endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="c852e-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="c852e-130">8: criar um firewall que permita o tráfego do MSSQL para um banco de dados SQL específico</span><span class="sxs-lookup"><span data-stu-id="c852e-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="c852e-131">Este exemplo cria um firewall que permite o tráfego do MSSQL na porta padrão 1433 para o banco de dados SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="c852e-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="c852e-132">9: criar um firewall anexado a um hub virtual</span><span class="sxs-lookup"><span data-stu-id="c852e-132">9:  Create a Firewall attached to a virtual hub</span></span>
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="c852e-133">Este exemplo cria um firewall anexado ao virtual Hub "vHub".</span><span class="sxs-lookup"><span data-stu-id="c852e-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="c852e-134">Uma política de firewall $fp será anexada ao firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="c852e-135">Esse firewall permite/nega o tráfego com base nas regras mencionadas na política de firewall $fp.</span><span class="sxs-lookup"><span data-stu-id="c852e-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="c852e-136">O Hub virtual e o firewall devem estar nas mesmas regiões.</span><span class="sxs-lookup"><span data-stu-id="c852e-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="c852e-137">10: criar um firewall com a configuração da lista branca do Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c852e-137">10: Create a Firewall with threat intelligence whitelist setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="c852e-138">Este exemplo cria um firewall que a lista branca "www.microsoft.com" e "8.8.8.8" da inteligência de ameaças</span><span class="sxs-lookup"><span data-stu-id="c852e-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="c852e-139">11: criar um firewall com configuração personalizada de intervalo particular</span><span class="sxs-lookup"><span data-stu-id="c852e-139">11: Create a Firewall with customized private range setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="c852e-140">Este exemplo cria um firewall que trata "99.99.99.0/24" e "66.66.0.0/16" como intervalos de IP privados e não o tráfego de SNAT para esses endereços</span><span class="sxs-lookup"><span data-stu-id="c852e-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="c852e-141">12: criar um firewall com uma sub-rede de gerenciamento e um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="c852e-141">12:  Create a Firewall with a management subnet and Public IP address</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="c852e-142">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c852e-143">Como nenhuma regra foi especificada, o Firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="c852e-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="c852e-144">Ameaça a Intel também será executada no modo padrão-Alert-o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="c852e-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="c852e-145">Para dar suporte a cenários de "encapsulamento forçado", esse firewall usará a sub-rede "AzureFirewallManagementSubnet" e o endereço IP público de gerenciamento para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="c852e-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="c852e-146">13: criar um firewall com a política de firewall anexada a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="c852e-146">13:  Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="c852e-147">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c852e-148">As regras e a inteligência de ameaças que serão aplicadas ao firewall serão tiradas da política de firewall</span><span class="sxs-lookup"><span data-stu-id="c852e-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

## <span data-ttu-id="c852e-149">OS</span><span class="sxs-lookup"><span data-stu-id="c852e-149">PARAMETERS</span></span>

### <span data-ttu-id="c852e-150">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c852e-150">-ApplicationRuleCollection</span></span>
<span data-ttu-id="c852e-151">Especifica as coleções de regras do aplicativo para o novo firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-151">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="c852e-152">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c852e-152">-AsJob</span></span>
<span data-ttu-id="c852e-153">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c852e-153">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c852e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c852e-154">-DefaultProfile</span></span>
<span data-ttu-id="c852e-155">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c852e-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c852e-156">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c852e-156">-FirewallPolicyId</span></span>
<span data-ttu-id="c852e-157">A política de firewall anexada ao firewall</span><span class="sxs-lookup"><span data-stu-id="c852e-157">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="c852e-158">-Force</span><span class="sxs-lookup"><span data-stu-id="c852e-158">-Force</span></span>
<span data-ttu-id="c852e-159">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c852e-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c852e-160">-Local</span><span class="sxs-lookup"><span data-stu-id="c852e-160">-Location</span></span>
<span data-ttu-id="c852e-161">Especifica a região do firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-161">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="c852e-162">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c852e-162">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="c852e-163">Um ou mais endereços IP públicos a serem usados para tráfego de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="c852e-163">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="c852e-164">Os endereços IP públicos devem usar SKU padrão e devem pertencer ao mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-164">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="c852e-165">-Name</span></span>
<span data-ttu-id="c852e-166">Especifica o nome do firewall do Azure que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="c852e-166">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c852e-167">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c852e-167">-NatRuleCollection</span></span>
<span data-ttu-id="c852e-168">A lista de AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c852e-168">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="c852e-169">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c852e-169">-NetworkRuleCollection</span></span>
<span data-ttu-id="c852e-170">A lista de AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c852e-170">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="c852e-171">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="c852e-171">-PrivateRange</span></span>
<span data-ttu-id="c852e-172">O IP privado se faixas ao qual o tráfego não será SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="c852e-172">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-173">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c852e-173">-PublicIpAddress</span></span>
<span data-ttu-id="c852e-174">Um ou mais endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="c852e-174">One or more Public IP Addresses.</span></span> <span data-ttu-id="c852e-175">Os endereços IP públicos devem usar SKU padrão e devem pertencer ao mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-175">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-176">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="c852e-176">-PublicIpName</span></span>
<span data-ttu-id="c852e-177">Nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="c852e-177">Public Ip Name.</span></span> <span data-ttu-id="c852e-178">O IP público deve usar a SKU padrão e deve pertencer ao mesmo grupo de recursos do firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-178">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c852e-179">-ResourceGroupName</span></span>
<span data-ttu-id="c852e-180">Especifica o nome de um grupo de recursos para conter o firewall.</span><span class="sxs-lookup"><span data-stu-id="c852e-180">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="c852e-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="c852e-181">-Sku</span></span>
<span data-ttu-id="c852e-182">O tipo de SKU para firewall</span><span class="sxs-lookup"><span data-stu-id="c852e-182">The sku type for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-183">-Marca</span><span class="sxs-lookup"><span data-stu-id="c852e-183">-Tag</span></span>
<span data-ttu-id="c852e-184">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c852e-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c852e-185">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c852e-185">For example:</span></span>

<span data-ttu-id="c852e-186">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c852e-186">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c852e-187">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="c852e-187">-ThreatIntelMode</span></span>
<span data-ttu-id="c852e-188">Especifica o modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="c852e-188">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="c852e-189">O modo padrão é alerta, não está desligado.</span><span class="sxs-lookup"><span data-stu-id="c852e-189">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-190">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c852e-190">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="c852e-191">A lista branca para inteligência de ameaças</span><span class="sxs-lookup"><span data-stu-id="c852e-191">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-192">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="c852e-192">-VirtualHubId</span></span>
<span data-ttu-id="c852e-193">O Hub virtual ao qual um firewall está anexado</span><span class="sxs-lookup"><span data-stu-id="c852e-193">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="c852e-194">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c852e-194">-VirtualNetwork</span></span>
<span data-ttu-id="c852e-195">Rede virtual</span><span class="sxs-lookup"><span data-stu-id="c852e-195">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-196">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c852e-196">-VirtualNetworkName</span></span>
<span data-ttu-id="c852e-197">Especifica o nome da rede virtual para a qual o firewall será implantado.</span><span class="sxs-lookup"><span data-stu-id="c852e-197">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="c852e-198">A rede virtual e o firewall devem pertencer ao mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c852e-198">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="c852e-199">-Zone</span></span>
<span data-ttu-id="c852e-200">Uma lista de zonas de disponibilidade que indicam para onde o firewall precisa vir.</span><span class="sxs-lookup"><span data-stu-id="c852e-200">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c852e-201">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c852e-201">-Confirm</span></span>
<span data-ttu-id="c852e-202">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c852e-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c852e-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c852e-203">-WhatIf</span></span>
<span data-ttu-id="c852e-204">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c852e-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c852e-205">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c852e-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c852e-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c852e-206">CommonParameters</span></span>
<span data-ttu-id="c852e-207">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c852e-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c852e-208">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c852e-208">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c852e-209">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c852e-209">INPUTS</span></span>

### <span data-ttu-id="c852e-210">System. String</span><span class="sxs-lookup"><span data-stu-id="c852e-210">System.String</span></span>

### <span data-ttu-id="c852e-211">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c852e-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="c852e-212">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="c852e-212">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="c852e-213">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c852e-213">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="c852e-214">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="c852e-214">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="c852e-215">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="c852e-215">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="c852e-216">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="c852e-216">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="c852e-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c852e-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c852e-218">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c852e-218">OUTPUTS</span></span>

### <span data-ttu-id="c852e-219">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c852e-219">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c852e-220">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c852e-220">NOTES</span></span>

## <span data-ttu-id="c852e-221">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c852e-221">RELATED LINKS</span></span>

[<span data-ttu-id="c852e-222">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c852e-222">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="c852e-223">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c852e-223">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="c852e-224">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c852e-224">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="c852e-225">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c852e-225">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="c852e-226">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c852e-226">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="c852e-227">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c852e-227">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
