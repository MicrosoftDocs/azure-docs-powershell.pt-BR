---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771639"
---
# <span data-ttu-id="7fbf4-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7fbf4-101">New-AzFirewall</span></span>

## <span data-ttu-id="7fbf4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fbf4-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbf4-103">Cria um novo firewall em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="7fbf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fbf4-104">SYNTAX</span></span>

### <span data-ttu-id="7fbf4-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fbf4-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fbf4-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="7fbf4-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fbf4-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="7fbf4-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fbf4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fbf4-108">DESCRIPTION</span></span>
<span data-ttu-id="7fbf4-109">O cmdlet **New-AzFirewall** cria um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="7fbf4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fbf4-110">EXAMPLES</span></span>

### <span data-ttu-id="7fbf4-111">1: criar um firewall anexado a uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="7fbf4-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="7fbf4-112">Este exemplo cria um firewall anexado à rede virtual "vnet" no mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="7fbf4-113">Como nenhuma regra foi especificada, o Firewall bloqueará todo o tráfego (comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="7fbf4-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="7fbf4-114">Ameaça a Intel também será executada no modo padrão-Alert-o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="7fbf4-115">2: criar um firewall que permita todo o tráfego HTTPS</span><span class="sxs-lookup"><span data-stu-id="7fbf4-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="7fbf4-116">Este exemplo cria um firewall que permite todo o tráfego HTTPS na porta 443.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="7fbf4-117">Ameaça a Intel será executada no modo padrão-Alert-lo, o que significa que o tráfego mal-intencionado será registrado, mas não negado.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="7fbf4-118">3: DNAT-redirecionar o tráfego destinado ao 10.1.2.3:80 para 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="7fbf4-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="7fbf4-119">Este exemplo criou um firewall que converteu o IP de destino e a porta de todos os pacotes destinados a 10.1.2.3:80 para 10.2.3.4: ameaça de 8080 a Intel está desativada neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="7fbf4-120">4: criar um firewall sem regras e com ameaças à Intel em modo de alerta</span><span class="sxs-lookup"><span data-stu-id="7fbf4-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="7fbf4-121">Este exemplo cria um firewall que bloqueia todo o tráfego (comportamento padrão) e tem ameaça Intel em execução no modo de alerta.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="7fbf4-122">Isso significa que os logs de alerta são emitidos para tráfego mal-intencionado antes de aplicar as outras regras (neste caso, apenas a regra padrão-negar tudo)</span><span class="sxs-lookup"><span data-stu-id="7fbf4-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="7fbf4-123">5: criar um firewall que permita todo o tráfego HTTP na porta 8080, mas bloquear domínios maliciosos identificados pela Intel® Threat</span><span class="sxs-lookup"><span data-stu-id="7fbf4-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="7fbf4-124">Este exemplo cria um firewall que permite todo o tráfego HTTP na porta 8080, a menos que seja considerado mal-intencionado pela Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="7fbf4-125">Ao executar no modo negar, ao contrário do alerta, o tráfego é considerado mal-intencionado pela ameaça, a Intel não está apenas registrada, mas também bloqueada.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="7fbf4-126">6: criar um firewall sem regras e zonas de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="7fbf4-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="7fbf4-127">Este exemplo cria um firewall com todas as zonas de disponibilidade disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="7fbf4-128">7: criar um firewall com dois ou mais endereços IP públicos</span><span class="sxs-lookup"><span data-stu-id="7fbf4-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="7fbf4-129">Este exemplo cria um firewall anexado à rede virtual "vnet" com dois endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="7fbf4-130">8: criar um firewall que permita o tráfego do MSSQL para um banco de dados SQL específico</span><span class="sxs-lookup"><span data-stu-id="7fbf4-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="7fbf4-131">Este exemplo cria um firewall que permite o tráfego do MSSQL na porta padrão 1433 para o banco de dados SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="7fbf4-132">OS</span><span class="sxs-lookup"><span data-stu-id="7fbf4-132">PARAMETERS</span></span>

### <span data-ttu-id="7fbf4-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7fbf4-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="7fbf4-134">Especifica as coleções de regras do aplicativo para o novo firewall.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="7fbf4-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fbf4-135">-AsJob</span></span>
<span data-ttu-id="7fbf4-136">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7fbf4-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fbf4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbf4-137">-DefaultProfile</span></span>
<span data-ttu-id="7fbf4-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fbf4-139">-Force</span><span class="sxs-lookup"><span data-stu-id="7fbf4-139">-Force</span></span>
<span data-ttu-id="7fbf4-140">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7fbf4-141">-Local</span><span class="sxs-lookup"><span data-stu-id="7fbf4-141">-Location</span></span>
<span data-ttu-id="7fbf4-142">Especifica a região do firewall.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="7fbf4-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fbf4-143">-Name</span></span>
<span data-ttu-id="7fbf4-144">Especifica o nome do firewall do Azure que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7fbf4-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7fbf4-145">-NatRuleCollection</span></span>
<span data-ttu-id="7fbf4-146">A lista de AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="7fbf4-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="7fbf4-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7fbf4-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="7fbf4-148">A lista de AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="7fbf4-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="7fbf4-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7fbf4-149">-PublicIpAddress</span></span>
<span data-ttu-id="7fbf4-150">Um ou mais endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="7fbf4-151">Os endereços IP públicos devem usar SKU padrão e devem pertencer ao mesmo grupo de recursos que o firewall.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="7fbf4-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="7fbf4-152">-PublicIpName</span></span>
<span data-ttu-id="7fbf4-153">Nome do IP público.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-153">Public Ip Name.</span></span> <span data-ttu-id="7fbf4-154">O IP público deve usar a SKU padrão e deve pertencer ao mesmo grupo de recursos do firewall.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="7fbf4-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fbf4-155">-ResourceGroupName</span></span>
<span data-ttu-id="7fbf4-156">Especifica o nome de um grupo de recursos para conter o firewall.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="7fbf4-157">-Zone</span><span class="sxs-lookup"><span data-stu-id="7fbf4-157">-Zone</span></span>
<span data-ttu-id="7fbf4-158">Uma lista de zonas de disponibilidade que indicam para onde o firewall precisa vir.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="7fbf4-159">-Marca</span><span class="sxs-lookup"><span data-stu-id="7fbf4-159">-Tag</span></span>
<span data-ttu-id="7fbf4-160">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7fbf4-161">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7fbf4-161">For example:</span></span>

<span data-ttu-id="7fbf4-162">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7fbf4-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7fbf4-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="7fbf4-163">-ThreatIntelMode</span></span>
<span data-ttu-id="7fbf4-164">Especifica o modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="7fbf4-165">O modo padrão é alerta, não está desligado.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="7fbf4-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fbf4-166">-VirtualNetwork</span></span>
<span data-ttu-id="7fbf4-167">Rede virtual</span><span class="sxs-lookup"><span data-stu-id="7fbf4-167">Virtual Network</span></span>

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

### <span data-ttu-id="7fbf4-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7fbf4-168">-VirtualNetworkName</span></span>
<span data-ttu-id="7fbf4-169">Especifica o nome da rede virtual para a qual o firewall será implantado.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="7fbf4-170">A rede virtual e o firewall devem pertencer ao mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="7fbf4-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7fbf4-171">-Confirm</span></span>
<span data-ttu-id="7fbf4-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fbf4-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fbf4-173">-WhatIf</span></span>
<span data-ttu-id="7fbf4-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fbf4-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fbf4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbf4-176">CommonParameters</span></span>
<span data-ttu-id="7fbf4-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fbf4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbf4-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbf4-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbf4-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fbf4-179">INPUTS</span></span>

### <span data-ttu-id="7fbf4-180">System. String</span><span class="sxs-lookup"><span data-stu-id="7fbf4-180">System.String</span></span>

### <span data-ttu-id="7fbf4-181">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7fbf4-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="7fbf4-182">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="7fbf4-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="7fbf4-183">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="7fbf4-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="7fbf4-184">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="7fbf4-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="7fbf4-185">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="7fbf4-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="7fbf4-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7fbf4-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7fbf4-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fbf4-187">OUTPUTS</span></span>

### <span data-ttu-id="7fbf4-188">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7fbf4-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="7fbf4-189">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fbf4-189">NOTES</span></span>

## <span data-ttu-id="7fbf4-190">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fbf4-190">RELATED LINKS</span></span>

[<span data-ttu-id="7fbf4-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7fbf4-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="7fbf4-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7fbf4-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="7fbf4-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7fbf4-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="7fbf4-194">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7fbf4-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="7fbf4-195">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7fbf4-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="7fbf4-196">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7fbf4-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
