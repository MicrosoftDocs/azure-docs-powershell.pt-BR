---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114861"
---
# <span data-ttu-id="bdb60-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-101">New-AzFirewall</span></span>

## <span data-ttu-id="bdb60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdb60-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb60-103">Cria um novo firewall em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdb60-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="bdb60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdb60-104">SYNTAX</span></span>

### <span data-ttu-id="bdb60-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdb60-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdb60-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="bdb60-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdb60-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="bdb60-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdb60-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdb60-108">DESCRIPTION</span></span>
<span data-ttu-id="bdb60-109">O cmdlet **New-AzFirewall** cria um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb60-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="bdb60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdb60-110">EXAMPLES</span></span>

### <span data-ttu-id="bdb60-111">Exemplo 1: criar um firewall anexado a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="bdb60-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="bdb60-112">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bdb60-113">Como nenhuma regra foi especificada, o Firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="bdb60-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="bdb60-114">Ameaça a Intel também será executada no modo padrão-Alert-o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="bdb60-115">Exemplo 2: criar um firewall que permita todo o tráfego HTTPS</span><span class="sxs-lookup"><span data-stu-id="bdb60-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="bdb60-116">Este exemplo cria um firewall que permite todo o tráfego HTTPS na porta 443.</span><span class="sxs-lookup"><span data-stu-id="bdb60-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="bdb60-117">Ameaça a Intel será executada no modo padrão-Alert-lo, o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="bdb60-118">Exemplo 3: DNAT-redirecionar o tráfego destinado para 10.1.2.3:80 para 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="bdb60-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="bdb60-119">Este exemplo criou um firewall que converteu o IP de destino e a porta de todos os pacotes destinados a 10.1.2.3:80 para 10.2.3.4: ameaça de 8080 a Intel está desativada neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="bdb60-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="bdb60-120">Exemplo 4: criar um firewall sem regras e com ameaças à Intel em modo de alerta</span><span class="sxs-lookup"><span data-stu-id="bdb60-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="bdb60-121">Este exemplo cria um firewall que bloqueia todo o tráfego (comportamento padrão) e tem ameaça Intel em execução no modo de alerta.</span><span class="sxs-lookup"><span data-stu-id="bdb60-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="bdb60-122">Isso significa que os logs de alerta são emitidos para tráfego mal-intencionado antes de aplicar as outras regras (neste caso, apenas a regra padrão-negar tudo)</span><span class="sxs-lookup"><span data-stu-id="bdb60-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="bdb60-123">Exemplo 5: criar um firewall que permita todo o tráfego HTTP na porta 8080, mas bloqueia domínios mal-intencionados identificados pela Intel</span><span class="sxs-lookup"><span data-stu-id="bdb60-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="bdb60-124">Este exemplo cria um firewall que permite todo o tráfego HTTP na porta 8080, a menos que seja considerado mal-intencionado pela Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="bdb60-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="bdb60-125">Ao executar no modo negar, ao contrário do alerta, o tráfego é considerado mal-intencionado pela ameaça, a Intel não está apenas registrada, mas também bloqueada.</span><span class="sxs-lookup"><span data-stu-id="bdb60-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="bdb60-126">Exemplo 6: criar um firewall sem regras e com zonas de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="bdb60-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="bdb60-127">Este exemplo cria um firewall com todas as zonas de disponibilidade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bdb60-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="bdb60-128">Exemplo 7: criar um firewall com dois ou mais endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="bdb60-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="bdb60-129">Este exemplo cria um firewall anexado à rede virtual "vnet" com dois endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="bdb60-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="bdb60-130">Exemplo 8: criar um firewall que permita o tráfego do MSSQL para um banco de dados SQL específico</span><span class="sxs-lookup"><span data-stu-id="bdb60-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="bdb60-131">Este exemplo cria um firewall que permite o tráfego do MSSQL na porta padrão 1433 para o banco de dados SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="bdb60-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="bdb60-132">Exemplo 9: criar um firewall anexado a um hub virtual</span><span class="sxs-lookup"><span data-stu-id="bdb60-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="bdb60-133">Este exemplo cria um firewall anexado ao virtual Hub "vHub".</span><span class="sxs-lookup"><span data-stu-id="bdb60-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="bdb60-134">Uma política de firewall $fp será anexada ao firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="bdb60-135">Esse firewall permite/nega o tráfego com base nas regras mencionadas na política de firewall $fp.</span><span class="sxs-lookup"><span data-stu-id="bdb60-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="bdb60-136">O Hub virtual e o firewall devem estar nas mesmas regiões.</span><span class="sxs-lookup"><span data-stu-id="bdb60-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="bdb60-137">Exemplo 10: criar um firewall com a configuração da lista branca do Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="bdb60-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="bdb60-138">Este exemplo cria um firewall que a lista branca "www.microsoft.com" e "8.8.8.8" da inteligência de ameaças</span><span class="sxs-lookup"><span data-stu-id="bdb60-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="bdb60-139">Exemplo 11: criar um firewall com configuração personalizada de intervalo particular</span><span class="sxs-lookup"><span data-stu-id="bdb60-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="bdb60-140">Este exemplo cria um firewall que trata "99.99.99.0/24" e "66.66.0.0/16" como intervalos de IP privados e não o tráfego de SNAT para esses endereços</span><span class="sxs-lookup"><span data-stu-id="bdb60-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="bdb60-141">Exemplo 12: criar um firewall com uma sub-rede de gerenciamento e um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="bdb60-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="bdb60-142">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bdb60-143">Como nenhuma regra foi especificada, o Firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="bdb60-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="bdb60-144">Ameaça a Intel também será executada no modo padrão-Alert-o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="bdb60-145">Para dar suporte a cenários de "encapsulamento forçado", esse firewall usará a sub-rede "AzureFirewallManagementSubnet" e o endereço IP público de gerenciamento para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="bdb60-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="bdb60-146">Exemplo 13: criar um firewall com a política de firewall anexada a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="bdb60-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="bdb60-147">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bdb60-148">As regras e a inteligência de ameaças que serão aplicadas ao firewall serão tiradas da política de firewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="bdb60-149">Exemplo 14: criar um firewall com servidores proxy e DNS DNS</span><span class="sxs-lookup"><span data-stu-id="bdb60-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="bdb60-150">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bdb60-151">O proxy de DNS está habilitado para esse firewall e dois servidores DNS são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="bdb60-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="bdb60-152">Além disso, exija que o proxy DNS para regras de rede esteja definido, portanto, se houver regras de rede com FQDNs, o proxy DNS será usado para eles também.</span><span class="sxs-lookup"><span data-stu-id="bdb60-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="bdb60-153">Exemplo 15: criar um firewall com vários IPs.</span><span class="sxs-lookup"><span data-stu-id="bdb60-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="bdb60-154">O firewall pode ser associado ao Hub virtual</span><span class="sxs-lookup"><span data-stu-id="bdb60-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="bdb60-155">Este exemplo cria um firewall anexado ao "Hub" do Hub virtual no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bdb60-156">O firewall será atribuído a 2 IPs públicos criados implicitamente.</span><span class="sxs-lookup"><span data-stu-id="bdb60-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="bdb60-157">16: criar um firewall com permitir FTP ativo.</span><span class="sxs-lookup"><span data-stu-id="bdb60-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="bdb60-158">Este exemplo cria um firewall com o sinalizador permitir FTP ativo.</span><span class="sxs-lookup"><span data-stu-id="bdb60-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="bdb60-159">OS</span><span class="sxs-lookup"><span data-stu-id="bdb60-159">PARAMETERS</span></span>

### <span data-ttu-id="bdb60-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bdb60-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="bdb60-161">Especifica as coleções de regras do aplicativo para o novo firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-161">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-162">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdb60-162">-AsJob</span></span>
<span data-ttu-id="bdb60-163">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bdb60-163">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdb60-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb60-164">-DefaultProfile</span></span>
<span data-ttu-id="bdb60-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb60-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bdb60-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="bdb60-167">Requer a funcionalidade proxy DNS para FQDNs nas regras de rede.</span><span class="sxs-lookup"><span data-stu-id="bdb60-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

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

### <span data-ttu-id="bdb60-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="bdb60-168">-DnsServer</span></span>
<span data-ttu-id="bdb60-169">A lista de servidores DNS a serem usados para resolução de DNS</span><span class="sxs-lookup"><span data-stu-id="bdb60-169">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="bdb60-170">-EnableDnsProxy</span></span>
<span data-ttu-id="bdb60-171">Habilite o proxy de DNS.</span><span class="sxs-lookup"><span data-stu-id="bdb60-171">Enable DNS Proxy.</span></span> <span data-ttu-id="bdb60-172">Por padrão, ele é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-172">By default it is disabled.</span></span>


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

### <span data-ttu-id="bdb60-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="bdb60-173">-AllowActiveFTP</span></span>
<span data-ttu-id="bdb60-174">Permite FTP ativo no firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="bdb60-175">Por padrão, ele é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-175">By default it is disabled.</span></span>


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

### <span data-ttu-id="bdb60-176">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="bdb60-176">-FirewallPolicyId</span></span>
<span data-ttu-id="bdb60-177">A política de firewall anexada ao firewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-177">The firewall policy attached to the firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-178">-Force</span><span class="sxs-lookup"><span data-stu-id="bdb60-178">-Force</span></span>
<span data-ttu-id="bdb60-179">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bdb60-179">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bdb60-180">-HubIPAddresses</span><span class="sxs-lookup"><span data-stu-id="bdb60-180">-HubIPAddresses</span></span>
<span data-ttu-id="bdb60-181">Os endereços IP do firewall anexado a um hub virtual</span><span class="sxs-lookup"><span data-stu-id="bdb60-181">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-182">-Local</span><span class="sxs-lookup"><span data-stu-id="bdb60-182">-Location</span></span>
<span data-ttu-id="bdb60-183">Especifica a região do firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-183">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="bdb60-184">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdb60-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="bdb60-185">Um ou mais endereços IP públicos a serem usados para tráfego de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="bdb60-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="bdb60-186">Os endereços IP públicos devem usar SKU padrão e devem pertencer ao mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdb60-187">-Name</span></span>
<span data-ttu-id="bdb60-188">Especifica o nome do firewall do Azure que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="bdb60-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bdb60-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bdb60-189">-NatRuleCollection</span></span>
<span data-ttu-id="bdb60-190">A lista de AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="bdb60-190">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bdb60-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="bdb60-192">A lista de AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="bdb60-192">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="bdb60-193">-PrivateRange</span></span>
<span data-ttu-id="bdb60-194">O IP privado se faixas ao qual o tráfego não será SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="bdb60-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-195">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdb60-195">-PublicIpAddress</span></span>
<span data-ttu-id="bdb60-196">Um ou mais endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="bdb60-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="bdb60-197">Os endereços IP públicos devem usar SKU padrão e devem pertencer ao mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="bdb60-198">-PublicIpName</span></span>
<span data-ttu-id="bdb60-199">Nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="bdb60-199">Public Ip Name.</span></span> <span data-ttu-id="bdb60-200">O IP público deve usar a SKU padrão e deve pertencer ao mesmo grupo de recursos do firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb60-201">-ResourceGroupName</span></span>
<span data-ttu-id="bdb60-202">Especifica o nome de um grupo de recursos para conter o firewall.</span><span class="sxs-lookup"><span data-stu-id="bdb60-202">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="bdb60-203">-SKU</span><span class="sxs-lookup"><span data-stu-id="bdb60-203">-Sku</span></span>
<span data-ttu-id="bdb60-204">O tipo de SKU para firewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-204">The sku type for firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-205">-Marca</span><span class="sxs-lookup"><span data-stu-id="bdb60-205">-Tag</span></span>
<span data-ttu-id="bdb60-206">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bdb60-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bdb60-207">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="bdb60-207">For example:</span></span>

<span data-ttu-id="bdb60-208">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bdb60-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bdb60-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="bdb60-209">-ThreatIntelMode</span></span>
<span data-ttu-id="bdb60-210">Especifica o modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="bdb60-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="bdb60-211">O modo padrão é alerta, não está desligado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="bdb60-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="bdb60-213">A lista branca para inteligência de ameaças</span><span class="sxs-lookup"><span data-stu-id="bdb60-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="bdb60-214">-VirtualHubId</span></span>
<span data-ttu-id="bdb60-215">O Hub virtual ao qual um firewall está anexado</span><span class="sxs-lookup"><span data-stu-id="bdb60-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bdb60-216">-VirtualNetwork</span></span>
<span data-ttu-id="bdb60-217">Rede virtual</span><span class="sxs-lookup"><span data-stu-id="bdb60-217">Virtual Network</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bdb60-218">-VirtualNetworkName</span></span>
<span data-ttu-id="bdb60-219">Especifica o nome da rede virtual para a qual o firewall será implantado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="bdb60-220">A rede virtual e o firewall devem pertencer ao mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdb60-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="bdb60-221">-Zone</span></span>
<span data-ttu-id="bdb60-222">Uma lista de zonas de disponibilidade que indicam para onde o firewall precisa vir.</span><span class="sxs-lookup"><span data-stu-id="bdb60-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb60-223">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdb60-223">-Confirm</span></span>
<span data-ttu-id="bdb60-224">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb60-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb60-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb60-225">-WhatIf</span></span>
<span data-ttu-id="bdb60-226">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb60-227">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdb60-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb60-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb60-228">CommonParameters</span></span>
<span data-ttu-id="bdb60-229">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb60-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb60-230">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdb60-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb60-231">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdb60-231">INPUTS</span></span>

### <span data-ttu-id="bdb60-232">System. String</span><span class="sxs-lookup"><span data-stu-id="bdb60-232">System.String</span></span>

### <span data-ttu-id="bdb60-233">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bdb60-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="bdb60-234">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="bdb60-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="bdb60-235">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bdb60-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="bdb60-236">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="bdb60-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="bdb60-237">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="bdb60-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="bdb60-238">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="bdb60-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="bdb60-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bdb60-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bdb60-240">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdb60-240">OUTPUTS</span></span>

### <span data-ttu-id="bdb60-241">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="bdb60-242">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdb60-242">NOTES</span></span>

## <span data-ttu-id="bdb60-243">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdb60-243">RELATED LINKS</span></span>

[<span data-ttu-id="bdb60-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="bdb60-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="bdb60-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="bdb60-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="bdb60-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bdb60-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="bdb60-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bdb60-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="bdb60-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bdb60-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
