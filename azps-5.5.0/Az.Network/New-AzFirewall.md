---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111645"
---
# <span data-ttu-id="1be0a-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-101">New-AzFirewall</span></span>

## <span data-ttu-id="1be0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1be0a-102">SYNOPSIS</span></span>
<span data-ttu-id="1be0a-103">Cria um novo Firewall em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1be0a-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="1be0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1be0a-104">SYNTAX</span></span>

### <span data-ttu-id="1be0a-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1be0a-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1be0a-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="1be0a-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1be0a-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="1be0a-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1be0a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1be0a-108">DESCRIPTION</span></span>
<span data-ttu-id="1be0a-109">O **cmdlet New-AzFirewall** cria um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="1be0a-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="1be0a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1be0a-110">EXAMPLES</span></span>

### <span data-ttu-id="1be0a-111">Exemplo 1: Criar um Firewall anexado a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="1be0a-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="1be0a-112">Este exemplo cria um Firewall anexado à "vnet" de rede virtual no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1be0a-113">Como nenhuma regra foi especificada, o firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="1be0a-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="1be0a-114">A Inteligência contra Ameaças também será executado no modo padrão - Alerta - o que significa que o tráfego mal-intencionado será registrado, mas não será negado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="1be0a-115">Exemplo 2: Criar um Firewall que permite todo o tráfego HTTPS</span><span class="sxs-lookup"><span data-stu-id="1be0a-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="1be0a-116">Este exemplo cria um Firewall que permite todo o tráfego HTTPS na porta 443.</span><span class="sxs-lookup"><span data-stu-id="1be0a-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="1be0a-117">A Inteligência contra Ameaças será executado no modo padrão - Alerta - o que significa que o tráfego mal-intencionado será registrado, mas não será negado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="1be0a-118">Exemplo 3: LTDT - redirecionar o tráfego destinado a 10.1.2.3:80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="1be0a-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="1be0a-119">Este exemplo criou um Firewall que traduziu o IP de destino e a porta de todos os pacotes destinados a 10.1.2.3:80 a 10.2.3.4:8080 Threat Intel está desligado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="1be0a-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="1be0a-120">Exemplo 4: Criar um Firewall sem regras e com a Inteligência contra Ameaças no modo de Alerta</span><span class="sxs-lookup"><span data-stu-id="1be0a-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="1be0a-121">Este exemplo cria um Firewall que bloqueia todo o tráfego (comportamento padrão) e tem a Intel Threat em execução no modo alerta.</span><span class="sxs-lookup"><span data-stu-id="1be0a-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="1be0a-122">Isso significa que os logs de alerta são emitidos para tráfego mal-intencionado antes de aplicar as outras regras (nesse caso, apenas a regra padrão – Negar Tudo)</span><span class="sxs-lookup"><span data-stu-id="1be0a-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="1be0a-123">Exemplo 5: Criar um Firewall que permite todo o tráfego HTTP na porta 8080, mas bloqueia domínios mal-intencionados identificados pela Threat Intel</span><span class="sxs-lookup"><span data-stu-id="1be0a-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="1be0a-124">Este exemplo cria um Firewall que permite todo o tráfego HTTP na porta 8080, a menos que ele seja considerado mal-intencionado pela Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="1be0a-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="1be0a-125">Ao executar no modo Negar, ao contrário de Alerta, o tráfego considerado mal-intencionado pela Intel não é apenas registrado, mas também bloqueado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="1be0a-126">Exemplo 6: Criar um Firewall sem regras e com zonas de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="1be0a-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="1be0a-127">Este exemplo cria um Firewall com todas as zonas de disponibilidade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1be0a-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="1be0a-128">Exemplo 7: Criar um Firewall com dois ou mais Endereços IP Públicos</span><span class="sxs-lookup"><span data-stu-id="1be0a-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="1be0a-129">Este exemplo cria um Firewall anexado à "vnet" de rede virtual com dois endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="1be0a-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="1be0a-130">Exemplo 8: Criar um Firewall que permite o tráfego MSSQL para um banco de dados SQL específico</span><span class="sxs-lookup"><span data-stu-id="1be0a-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="1be0a-131">Este exemplo cria um Firewall que permite o tráfego MSSQL na porta padrão 1433 para o banco de dados SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="1be0a-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="1be0a-132">Exemplo 9: Criar um Firewall anexado a um hub virtual</span><span class="sxs-lookup"><span data-stu-id="1be0a-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="1be0a-133">Este exemplo cria um Firewall anexado ao hub virtual "vHub".</span><span class="sxs-lookup"><span data-stu-id="1be0a-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="1be0a-134">Uma política de firewall $fp será anexada ao firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="1be0a-135">Esse firewall permite/nega o tráfego com base nas regras mencionadas na política de firewall $fp.</span><span class="sxs-lookup"><span data-stu-id="1be0a-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="1be0a-136">O hub virtual e o firewall devem estar nas mesmas regiões.</span><span class="sxs-lookup"><span data-stu-id="1be0a-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="1be0a-137">Exemplo 10: Criar um Firewall com a configuração de lista de contatos de inteligência contra ameaças</span><span class="sxs-lookup"><span data-stu-id="1be0a-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="1be0a-138">Este exemplo cria um Firewall que lista "www.microsoft.com" e "8.8.8.8" a partir da inteligência contra ameaças</span><span class="sxs-lookup"><span data-stu-id="1be0a-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="1be0a-139">Exemplo 11: Criar um Firewall com configuração de intervalo particular personalizada</span><span class="sxs-lookup"><span data-stu-id="1be0a-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="1be0a-140">Este exemplo cria um Firewall que trata "99.99.99.0/24" e "66.66.0.0/16" como intervalos IP particulares e não gera tráfego para esses endereços</span><span class="sxs-lookup"><span data-stu-id="1be0a-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="1be0a-141">Exemplo 12: Criar um Firewall com uma sub-rede de gerenciamento e um endereço IP público</span><span class="sxs-lookup"><span data-stu-id="1be0a-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="1be0a-142">Este exemplo cria um Firewall anexado à "vnet" de rede virtual no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1be0a-143">Como nenhuma regra foi especificada, o firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="1be0a-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="1be0a-144">A Inteligência contra Ameaças também será executado no modo padrão - Alerta - o que significa que o tráfego mal-intencionado será registrado, mas não será negado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="1be0a-145">Para dar suporte a cenários de "túnel forçado", esse firewall usará a sub-rede "AzureFirewallManagementSubnet" e o endereço IP público de gerenciamento para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="1be0a-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="1be0a-146">Exemplo 13: Criar um Firewall com Política de Firewall anexada a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="1be0a-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="1be0a-147">Este exemplo cria um Firewall anexado à "vnet" de rede virtual no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1be0a-148">As regras e inteligência contra ameaças que serão aplicadas ao firewall serão tiradas da política de firewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="1be0a-149">Exemplo 14: Criar um Firewall com Servidores DNS e Proxy DNS</span><span class="sxs-lookup"><span data-stu-id="1be0a-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="1be0a-150">Este exemplo cria um Firewall anexado à "vnet" de rede virtual no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1be0a-151">O Proxy DNS está habilitado para esse firewall e dois Servidores DNS são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="1be0a-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="1be0a-152">Além disso, exigir que as regras de Rede de Proxy DNS sejam definidas, portanto, se houver alguma regra de rede com FQDNs, o proxy DNS também será usado para elas.</span><span class="sxs-lookup"><span data-stu-id="1be0a-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="1be0a-153">Exemplo 15: Criar um Firewall com vários IPs.</span><span class="sxs-lookup"><span data-stu-id="1be0a-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="1be0a-154">O Firewall pode ser associado ao Hub Virtual</span><span class="sxs-lookup"><span data-stu-id="1be0a-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="1be0a-155">Este exemplo cria um Firewall anexado ao "hub" do hub virtual no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1be0a-156">O Firewall receberá dois IPs públicos criados implicitamente.</span><span class="sxs-lookup"><span data-stu-id="1be0a-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="1be0a-157">16: Criar um Firewall com Permitir FTP Ativo.</span><span class="sxs-lookup"><span data-stu-id="1be0a-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="1be0a-158">Este exemplo cria um Firewall com o sinalizador FTP ativo de permitir.</span><span class="sxs-lookup"><span data-stu-id="1be0a-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="1be0a-159">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1be0a-159">PARAMETERS</span></span>

### <span data-ttu-id="1be0a-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="1be0a-160">-AllowActiveFTP</span></span>
<span data-ttu-id="1be0a-161">Permite FTP Ativo no Firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="1be0a-162">Por padrão, ela está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1be0a-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="1be0a-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1be0a-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="1be0a-164">Especifica as coleções de regras de aplicativo para o novo Firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-164">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="1be0a-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1be0a-165">-AsJob</span></span>
<span data-ttu-id="1be0a-166">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1be0a-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1be0a-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be0a-167">-DefaultProfile</span></span>
<span data-ttu-id="1be0a-168">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1be0a-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1be0a-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="1be0a-169">-DnsServer</span></span>
<span data-ttu-id="1be0a-170">A lista de Servidores DNS a serem usados para a resolução de DNS,</span><span class="sxs-lookup"><span data-stu-id="1be0a-170">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="1be0a-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="1be0a-171">-EnableDnsProxy</span></span>
<span data-ttu-id="1be0a-172">Habilitar Proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="1be0a-172">Enable DNS Proxy.</span></span> <span data-ttu-id="1be0a-173">Por padrão, ela está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1be0a-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="1be0a-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1be0a-174">-FirewallPolicyId</span></span>
<span data-ttu-id="1be0a-175">A política de firewall anexada ao firewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-175">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="1be0a-176">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1be0a-176">-Force</span></span>
<span data-ttu-id="1be0a-177">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1be0a-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1be0a-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="1be0a-178">-HubIPAddress</span></span>
<span data-ttu-id="1be0a-179">Os endereços IP do firewall anexados a um hub virtual</span><span class="sxs-lookup"><span data-stu-id="1be0a-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be0a-180">-Local</span><span class="sxs-lookup"><span data-stu-id="1be0a-180">-Location</span></span>
<span data-ttu-id="1be0a-181">Especifica a região do Firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="1be0a-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1be0a-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="1be0a-183">Um ou mais Endereços IP Públicos a ser usado para o tráfego de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="1be0a-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="1be0a-184">Os endereços IP públicos devem usar a SKU Padrão e devem pertencer ao mesmo grupo de recursos que o Firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="1be0a-185">-Nome</span><span class="sxs-lookup"><span data-stu-id="1be0a-185">-Name</span></span>
<span data-ttu-id="1be0a-186">Especifica o nome do Firewall do Azure que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="1be0a-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1be0a-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1be0a-187">-NatRuleCollection</span></span>
<span data-ttu-id="1be0a-188">A lista de AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="1be0a-188">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="1be0a-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1be0a-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="1be0a-190">A lista de AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="1be0a-190">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="1be0a-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="1be0a-191">-PrivateRange</span></span>
<span data-ttu-id="1be0a-192">Os intervalos ip particulares para os quais o tráfego não será SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="1be0a-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="1be0a-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1be0a-193">-PublicIpAddress</span></span>
<span data-ttu-id="1be0a-194">Um ou mais endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="1be0a-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="1be0a-195">Os endereços IP públicos devem usar a SKU Padrão e devem pertencer ao mesmo grupo de recursos que o Firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="1be0a-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="1be0a-196">-PublicIpName</span></span>
<span data-ttu-id="1be0a-197">Nome Ip Público.</span><span class="sxs-lookup"><span data-stu-id="1be0a-197">Public Ip Name.</span></span> <span data-ttu-id="1be0a-198">O IP público deve usar a SKU Padrão e deve pertencer ao mesmo grupo de recursos que o Firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="1be0a-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be0a-199">-ResourceGroupName</span></span>
<span data-ttu-id="1be0a-200">Especifica o nome de um grupo de recursos para conter o Firewall.</span><span class="sxs-lookup"><span data-stu-id="1be0a-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="1be0a-201">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1be0a-201">-SkuName</span></span>
<span data-ttu-id="1be0a-202">O nome da SKU para firewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be0a-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1be0a-203">-SkuTier</span></span>
<span data-ttu-id="1be0a-204">O nível de sku para firewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be0a-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="1be0a-205">-Tag</span></span>
<span data-ttu-id="1be0a-206">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1be0a-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1be0a-207">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1be0a-207">For example:</span></span>

<span data-ttu-id="1be0a-208">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1be0a-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1be0a-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="1be0a-209">-ThreatIntelMode</span></span>
<span data-ttu-id="1be0a-210">Especifica o modo de operação para Inteligência contra Ameaças.</span><span class="sxs-lookup"><span data-stu-id="1be0a-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="1be0a-211">O modo padrão é Alerta, não Desligado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-211">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="1be0a-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="1be0a-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="1be0a-213">A lista de whitelist para Inteligência contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="1be0a-213">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="1be0a-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="1be0a-214">-VirtualHubId</span></span>
<span data-ttu-id="1be0a-215">O hub virtual ao que um firewall está anexado</span><span class="sxs-lookup"><span data-stu-id="1be0a-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="1be0a-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1be0a-216">-VirtualNetwork</span></span>
<span data-ttu-id="1be0a-217">Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="1be0a-217">Virtual Network</span></span>

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

### <span data-ttu-id="1be0a-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1be0a-218">-VirtualNetworkName</span></span>
<span data-ttu-id="1be0a-219">Especifica o nome da rede virtual para a qual o Firewall será implantado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="1be0a-220">A rede virtual e o Firewall devem pertencer ao mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1be0a-220">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="1be0a-221">-Zona</span><span class="sxs-lookup"><span data-stu-id="1be0a-221">-Zone</span></span>
<span data-ttu-id="1be0a-222">Uma lista de zonas de disponibilidade que denotam de onde o firewall precisa ser vindo.</span><span class="sxs-lookup"><span data-stu-id="1be0a-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="1be0a-223">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1be0a-223">-Confirm</span></span>
<span data-ttu-id="1be0a-224">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1be0a-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be0a-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be0a-225">-WhatIf</span></span>
<span data-ttu-id="1be0a-226">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be0a-227">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1be0a-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be0a-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be0a-228">CommonParameters</span></span>
<span data-ttu-id="1be0a-229">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be0a-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be0a-230">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1be0a-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be0a-231">Entradas</span><span class="sxs-lookup"><span data-stu-id="1be0a-231">INPUTS</span></span>

### <span data-ttu-id="1be0a-232">System.String</span><span class="sxs-lookup"><span data-stu-id="1be0a-232">System.String</span></span>

### <span data-ttu-id="1be0a-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1be0a-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="1be0a-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="1be0a-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="1be0a-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1be0a-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="1be0a-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="1be0a-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="1be0a-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="1be0a-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="1be0a-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="1be0a-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="1be0a-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1be0a-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1be0a-240">Saídas</span><span class="sxs-lookup"><span data-stu-id="1be0a-240">OUTPUTS</span></span>

### <span data-ttu-id="1be0a-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1be0a-242">Notas</span><span class="sxs-lookup"><span data-stu-id="1be0a-242">NOTES</span></span>

## <span data-ttu-id="1be0a-243">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1be0a-243">RELATED LINKS</span></span>

[<span data-ttu-id="1be0a-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="1be0a-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="1be0a-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1be0a-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="1be0a-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1be0a-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="1be0a-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1be0a-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="1be0a-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1be0a-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
