---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 1bde6608f5dd87c2c102f3f2957832a2eb41e50a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771951"
---
# <span data-ttu-id="f1829-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1829-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="f1829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1829-102">SYNOPSIS</span></span>
<span data-ttu-id="f1829-103">Cria um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-103">Creates an application gateway.</span></span>

## <span data-ttu-id="f1829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1829-104">SYNTAX</span></span>

### <span data-ttu-id="f1829-105">IdentityByUserAssignedIdentityId (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1829-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1829-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1829-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1829-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f1829-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1829-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="f1829-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity> [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1829-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1829-109">DESCRIPTION</span></span>
<span data-ttu-id="f1829-110">O cmdlet **New-AzApplicationGateway** cria um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1829-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="f1829-111">Um gateway de aplicativo requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f1829-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="f1829-112">Um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1829-112">A resource group.</span></span>
- <span data-ttu-id="f1829-113">Uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f1829-113">A virtual network.</span></span>
- <span data-ttu-id="f1829-114">Um pool de servidores back-end que contém os endereços IP dos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="f1829-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="f1829-115">Configurações de pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="f1829-115">Back-end server pool settings.</span></span> <span data-ttu-id="f1829-116">Cada pool tem configurações como portabilidade baseada em protocolo e porta, que são aplicadas a todos os servidores dentro do pool.</span><span class="sxs-lookup"><span data-stu-id="f1829-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="f1829-117">Endereços IP front-end, que são os endereços IP abertos no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="f1829-118">Um endereço IP front-end pode ser um endereço IP público ou um endereço IP interno.</span><span class="sxs-lookup"><span data-stu-id="f1829-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="f1829-119">Portas de front-end, que são as portas públicas abertas no Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1829-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="f1829-120">O tráfego que atinge essas portas é redirecionado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="f1829-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="f1829-121">Uma regra de roteamento de solicitação que associa o ouvinte e o pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="f1829-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="f1829-122">A regra define qual pool de servidores back-end o tráfego deve ser direcionado quando ele atinge um ouvinte específico.</span><span class="sxs-lookup"><span data-stu-id="f1829-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="f1829-123">Um ouvinte tem uma porta de front-end, endereço IP front-end, protocolo (HTTP ou HTTPS) e nome de certificado SSL (se estiver configurando o descarregamento de SSL).</span><span class="sxs-lookup"><span data-stu-id="f1829-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="f1829-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1829-124">EXAMPLES</span></span>

### <span data-ttu-id="f1829-125">Exemplo 1: criar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1829-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="f1829-126">O exemplo a seguir cria um aplicativo gateway criando primeiro um grupo de recursos e uma rede virtual, bem como os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f1829-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="f1829-127">Um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="f1829-127">A back-end server pool</span></span>
- <span data-ttu-id="f1829-128">Configurações de pool de servidor back-end</span><span class="sxs-lookup"><span data-stu-id="f1829-128">Back-end server pool settings</span></span>
- <span data-ttu-id="f1829-129">Portas de front-end</span><span class="sxs-lookup"><span data-stu-id="f1829-129">Front-end ports</span></span>
- <span data-ttu-id="f1829-130">Endereços IP front-end</span><span class="sxs-lookup"><span data-stu-id="f1829-130">Front-end IP addresses</span></span>
- <span data-ttu-id="f1829-131">Uma regra de roteamento de solicitação estes quatro comandos criam uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f1829-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="f1829-132">O primeiro comando cria uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f1829-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="f1829-133">O segundo comando cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f1829-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="f1829-134">O terceiro comando verifica a configuração de sub-rede e o quarto comando verifica se a rede virtual foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="f1829-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="f1829-135">Os comandos a seguir criam o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1829-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="f1829-136">O primeiro comando cria uma configuração de IP chamada GatewayIp01 para a sub-rede criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f1829-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="f1829-137">O segundo comando cria um pool de servidores back-end chamado Pool01 com uma lista de endereços IP back-end e armazena o pool na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="f1829-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="f1829-138">O terceiro comando cria as configurações do pool de servidores back-end e armazena as configurações na variável $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="f1829-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="f1829-139">O comando avançar cria uma porta de front-end na porta 80, nomeia-a FrontEndPort01 e armazena a porta na variável $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="f1829-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="f1829-140">O quinto comando cria um endereço IP público usando New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="f1829-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="f1829-141">O sexto comando cria uma configuração de IP de front-end usando $PublicIp, nomeia-a FrontEndPortConfig01 e a armazena na variável $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="f1829-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="f1829-142">O sétimo comando cria um ouvinte usando o $FrontEndPort de $FrontEndIpConfig criadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f1829-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="f1829-143">O oitavo comando cria uma regra para o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="f1829-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="f1829-144">O nono comando define a SKU.</span><span class="sxs-lookup"><span data-stu-id="f1829-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="f1829-145">O comando décimo cria o gateway usando os objetos definidos pelos comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="f1829-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="f1829-146">Exemplo 2: criar um gateway de aplicativo com identidade atribuída pelo</span><span class="sxs-lookup"><span data-stu-id="f1829-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="f1829-147">OS</span><span class="sxs-lookup"><span data-stu-id="f1829-147">PARAMETERS</span></span>

### <span data-ttu-id="f1829-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1829-148">-AsJob</span></span>
<span data-ttu-id="f1829-149">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f1829-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1829-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="f1829-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="f1829-151">Especifica certificados de autenticação para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1829-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="f1829-153">Configuração de autoescala</span><span class="sxs-lookup"><span data-stu-id="f1829-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="f1829-154">-BackendAddressPools</span></span>
<span data-ttu-id="f1829-155">Especifica a lista de pools de endereços back-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="f1829-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="f1829-157">Especifica a lista de configurações HTTP de back-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1829-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="f1829-159">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f1829-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1829-160">-DefaultProfile</span></span>
<span data-ttu-id="f1829-161">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1829-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1829-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="f1829-162">-EnableFIPS</span></span>
<span data-ttu-id="f1829-163">Se o FIPS está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f1829-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="f1829-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="f1829-164">-EnableHttp2</span></span>
<span data-ttu-id="f1829-165">Se o HTTP2 está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f1829-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="f1829-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f1829-166">-FirewallPolicy</span></span>
<span data-ttu-id="f1829-167">Configuração de firewall</span><span class="sxs-lookup"><span data-stu-id="f1829-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f1829-168">-FirewallPolicyId</span></span>
<span data-ttu-id="f1829-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f1829-169">FirewallPolicyId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-170">-Force</span><span class="sxs-lookup"><span data-stu-id="f1829-170">-Force</span></span>
<span data-ttu-id="f1829-171">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1829-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1829-172">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="f1829-172">-FrontendIPConfigurations</span></span>
<span data-ttu-id="f1829-173">Especifica uma lista de configurações de IP de front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-173">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-174">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="f1829-174">-FrontendPorts</span></span>
<span data-ttu-id="f1829-175">Especifica uma lista de portas front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-175">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-176">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="f1829-176">-GatewayIPConfigurations</span></span>
<span data-ttu-id="f1829-177">Especifica uma lista de configurações de IP para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-177">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-178">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="f1829-178">-HttpListeners</span></span>
<span data-ttu-id="f1829-179">Especifica uma lista de ouvintes HTTP para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1829-179">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-180">-Identidade</span><span class="sxs-lookup"><span data-stu-id="f1829-180">-Identity</span></span>
<span data-ttu-id="f1829-181">Identidade do gateway do aplicativo a ser atribuída ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1829-181">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-182">-Local</span><span class="sxs-lookup"><span data-stu-id="f1829-182">-Location</span></span>
<span data-ttu-id="f1829-183">Especifica a região na qual criar o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-183">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="f1829-184">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1829-184">-Name</span></span>
<span data-ttu-id="f1829-185">Especifica o nome do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-185">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="f1829-186">-Testes</span><span class="sxs-lookup"><span data-stu-id="f1829-186">-Probes</span></span>
<span data-ttu-id="f1829-187">Especifica os testes do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-187">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-188">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="f1829-188">-RedirectConfigurations</span></span>
<span data-ttu-id="f1829-189">A lista de configurações de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="f1829-189">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-190">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="f1829-190">-RequestRoutingRules</span></span>
<span data-ttu-id="f1829-191">Especifica uma lista de regras de roteamento de solicitações para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-191">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1829-192">-ResourceGroupName</span></span>
<span data-ttu-id="f1829-193">Especifica o nome do grupo de recursos no qual o Application Gateway será criado.</span><span class="sxs-lookup"><span data-stu-id="f1829-193">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="f1829-194">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1829-194">-RewriteRuleSet</span></span>
<span data-ttu-id="f1829-195">A lista de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f1829-195">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-196">-SKU</span><span class="sxs-lookup"><span data-stu-id="f1829-196">-Sku</span></span>
<span data-ttu-id="f1829-197">Especifica a SKU (unidade de manutenção de estoque) do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-197">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-198">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="f1829-198">-SslCertificates</span></span>
<span data-ttu-id="f1829-199">Especifica a lista de certificados SSL (Secure Sockets Layer) para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1829-199">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-200">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="f1829-200">-SslPolicy</span></span>
<span data-ttu-id="f1829-201">Especifica uma política SSL para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1829-201">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-202">-Marca</span><span class="sxs-lookup"><span data-stu-id="f1829-202">-Tag</span></span>
<span data-ttu-id="f1829-203">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f1829-203">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f1829-204">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f1829-204">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f1829-205">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f1829-205">-TrustedRootCertificate</span></span>
<span data-ttu-id="f1829-206">A lista de certificados raiz confiáveis</span><span class="sxs-lookup"><span data-stu-id="f1829-206">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-207">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="f1829-207">-UrlPathMaps</span></span>
<span data-ttu-id="f1829-208">Especifica mapas de caminho de URL para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1829-208">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-209">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f1829-209">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f1829-210">ResourceId da identidade atribuída pelo usuário a ser atribuído ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f1829-210">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-211">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1829-211">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="f1829-212">Especifica uma configuração de firewall de aplicativo Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="f1829-212">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="f1829-213">Você pode usar o cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration para obter um WAF.</span><span class="sxs-lookup"><span data-stu-id="f1829-213">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1829-214">-Zone</span><span class="sxs-lookup"><span data-stu-id="f1829-214">-Zone</span></span>
<span data-ttu-id="f1829-215">Uma lista de zonas de disponibilidade que indicam para onde o gateway do aplicativo precisa vir.</span><span class="sxs-lookup"><span data-stu-id="f1829-215">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="f1829-216">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1829-216">-Confirm</span></span>
<span data-ttu-id="f1829-217">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1829-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1829-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1829-218">-WhatIf</span></span>
<span data-ttu-id="f1829-219">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1829-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1829-220">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1829-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1829-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1829-221">CommonParameters</span></span>
<span data-ttu-id="f1829-222">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1829-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1829-223">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1829-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1829-224">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1829-224">INPUTS</span></span>

### <span data-ttu-id="f1829-225">System. String</span><span class="sxs-lookup"><span data-stu-id="f1829-225">System.String</span></span>

### <span data-ttu-id="f1829-226">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f1829-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="f1829-227">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="f1829-227">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="f1829-228">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f1829-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="f1829-229">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="f1829-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="f1829-230">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="f1829-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="f1829-231">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="f1829-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="f1829-232">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f1829-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="f1829-233">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="f1829-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="f1829-234">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="f1829-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="f1829-235">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="f1829-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="f1829-236">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="f1829-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="f1829-237">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="f1829-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="f1829-238">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="f1829-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="f1829-239">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="f1829-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="f1829-240">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="f1829-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="f1829-241">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f1829-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="f1829-242">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1829-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="f1829-243">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1829-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="f1829-244">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1829-244">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f1829-245">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1829-245">OUTPUTS</span></span>

### <span data-ttu-id="f1829-246">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f1829-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f1829-247">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1829-247">NOTES</span></span>

## <span data-ttu-id="f1829-248">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1829-248">RELATED LINKS</span></span>

[<span data-ttu-id="f1829-249">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f1829-249">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f1829-250">New-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f1829-250">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="f1829-251">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f1829-251">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f1829-252">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f1829-252">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f1829-253">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f1829-253">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f1829-254">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1829-254">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f1829-255">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f1829-255">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f1829-256">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f1829-256">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="f1829-257">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f1829-257">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f1829-258">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f1829-258">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)