---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 5f91f333cf7983d50ba2984fcf01845a6c555e83
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281761"
---
# <span data-ttu-id="42b7c-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42b7c-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="42b7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="42b7c-103">Cria um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-103">Creates an application gateway.</span></span>

## <span data-ttu-id="42b7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42b7c-104">SYNTAX</span></span>

### <span data-ttu-id="42b7c-105">IdentityByUserAssignedIdentityId (padrão)</span><span class="sxs-lookup"><span data-stu-id="42b7c-105">IdentityByUserAssignedIdentityId (Default)</span></span>
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
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42b7c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="42b7c-106">SetByResourceId</span></span>
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
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42b7c-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="42b7c-107">SetByResource</span></span>
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
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42b7c-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="42b7c-108">IdentityByIdentityObject</span></span>
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
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42b7c-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42b7c-109">DESCRIPTION</span></span>
<span data-ttu-id="42b7c-110">O cmdlet **New-AzApplicationGateway** cria um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="42b7c-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="42b7c-111">Um gateway de aplicativo requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="42b7c-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="42b7c-112">Um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42b7c-112">A resource group.</span></span>
- <span data-ttu-id="42b7c-113">Uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="42b7c-113">A virtual network.</span></span>
- <span data-ttu-id="42b7c-114">Um pool de servidores back-end que contém os endereços IP dos servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="42b7c-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="42b7c-115">Configurações de pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="42b7c-115">Back-end server pool settings.</span></span> <span data-ttu-id="42b7c-116">Cada pool tem configurações como portabilidade baseada em protocolo e porta, que são aplicadas a todos os servidores dentro do pool.</span><span class="sxs-lookup"><span data-stu-id="42b7c-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="42b7c-117">Endereços IP front-end, que são os endereços IP abertos no gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="42b7c-118">Um endereço IP front-end pode ser um endereço IP público ou um endereço IP interno.</span><span class="sxs-lookup"><span data-stu-id="42b7c-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="42b7c-119">Portas de front-end, que são as portas públicas abertas no Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="42b7c-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="42b7c-120">O tráfego que atinge essas portas é redirecionado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="42b7c-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="42b7c-121">Uma regra de roteamento de solicitação que associa o ouvinte e o pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="42b7c-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="42b7c-122">A regra define qual pool de servidores back-end o tráfego deve ser direcionado quando ele atinge um ouvinte específico.</span><span class="sxs-lookup"><span data-stu-id="42b7c-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="42b7c-123">Um ouvinte tem uma porta de front-end, endereço IP front-end, protocolo (HTTP ou HTTPS) e nome de certificado SSL (se estiver configurando o descarregamento de SSL).</span><span class="sxs-lookup"><span data-stu-id="42b7c-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="42b7c-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42b7c-124">EXAMPLES</span></span>

### <span data-ttu-id="42b7c-125">Exemplo 1: criar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="42b7c-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="42b7c-126">O exemplo a seguir cria um aplicativo gateway criando primeiro um grupo de recursos e uma rede virtual, bem como os seguintes:</span><span class="sxs-lookup"><span data-stu-id="42b7c-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="42b7c-127">Um pool de servidores back-end</span><span class="sxs-lookup"><span data-stu-id="42b7c-127">A back-end server pool</span></span>
- <span data-ttu-id="42b7c-128">Configurações de pool de servidor back-end</span><span class="sxs-lookup"><span data-stu-id="42b7c-128">Back-end server pool settings</span></span>
- <span data-ttu-id="42b7c-129">Portas de front-end</span><span class="sxs-lookup"><span data-stu-id="42b7c-129">Front-end ports</span></span>
- <span data-ttu-id="42b7c-130">Endereços IP front-end</span><span class="sxs-lookup"><span data-stu-id="42b7c-130">Front-end IP addresses</span></span>
- <span data-ttu-id="42b7c-131">Uma regra de roteamento de solicitação estes quatro comandos criam uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="42b7c-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="42b7c-132">O primeiro comando cria uma configuração de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="42b7c-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="42b7c-133">O segundo comando cria uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="42b7c-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="42b7c-134">O terceiro comando verifica a configuração de sub-rede e o quarto comando verifica se a rede virtual foi criada com êxito.</span><span class="sxs-lookup"><span data-stu-id="42b7c-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="42b7c-135">Os comandos a seguir criam o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="42b7c-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="42b7c-136">O primeiro comando cria uma configuração de IP chamada GatewayIp01 para a sub-rede criada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="42b7c-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="42b7c-137">O segundo comando cria um pool de servidores back-end chamado Pool01 com uma lista de endereços IP back-end e armazena o pool na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="42b7c-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="42b7c-138">O terceiro comando cria as configurações do pool de servidores back-end e armazena as configurações na variável $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="42b7c-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="42b7c-139">O comando avançar cria uma porta de front-end na porta 80, nomeia-a FrontEndPort01 e armazena a porta na variável $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="42b7c-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="42b7c-140">O quinto comando cria um endereço IP público usando New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="42b7c-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="42b7c-141">O sexto comando cria uma configuração de IP de front-end usando $PublicIp, nomeia-a FrontEndPortConfig01 e a armazena na variável $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="42b7c-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="42b7c-142">O sétimo comando cria um ouvinte usando o $FrontEndPort de $FrontEndIpConfig criadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="42b7c-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="42b7c-143">O oitavo comando cria uma regra para o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="42b7c-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="42b7c-144">O nono comando define a SKU.</span><span class="sxs-lookup"><span data-stu-id="42b7c-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="42b7c-145">O comando décimo cria o gateway usando os objetos definidos pelos comandos anteriores.</span><span class="sxs-lookup"><span data-stu-id="42b7c-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="42b7c-146">Exemplo 2: criar um gateway de aplicativo com identidade atribuída pelo</span><span class="sxs-lookup"><span data-stu-id="42b7c-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="42b7c-147">OS</span><span class="sxs-lookup"><span data-stu-id="42b7c-147">PARAMETERS</span></span>

### <span data-ttu-id="42b7c-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42b7c-148">-AsJob</span></span>
<span data-ttu-id="42b7c-149">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="42b7c-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42b7c-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="42b7c-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="42b7c-151">Especifica certificados de autenticação para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="42b7c-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="42b7c-153">Configuração de autoescala</span><span class="sxs-lookup"><span data-stu-id="42b7c-153">Autoscale Configuration</span></span>

```yaml
Type: PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="42b7c-154">-BackendAddressPools</span></span>
<span data-ttu-id="42b7c-155">Especifica a lista de pools de endereços back-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="42b7c-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="42b7c-157">Especifica a lista de configurações HTTP de back-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="42b7c-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="42b7c-159">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="42b7c-159">Customer error of an application gateway</span></span>

```yaml
Type: PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b7c-160">-DefaultProfile</span></span>
<span data-ttu-id="42b7c-161">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42b7c-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42b7c-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="42b7c-162">-EnableFIPS</span></span>
<span data-ttu-id="42b7c-163">Se o FIPS está habilitado.</span><span class="sxs-lookup"><span data-stu-id="42b7c-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="42b7c-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="42b7c-164">-EnableHttp2</span></span>
<span data-ttu-id="42b7c-165">Se o HTTP2 está habilitado.</span><span class="sxs-lookup"><span data-stu-id="42b7c-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="42b7c-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="42b7c-166">-FirewallPolicy</span></span>
<span data-ttu-id="42b7c-167">Configuração de firewall</span><span class="sxs-lookup"><span data-stu-id="42b7c-167">Firewall configuration</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="42b7c-168">-FirewallPolicyId</span></span>
<span data-ttu-id="42b7c-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="42b7c-169">FirewallPolicyId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-170">-Force</span><span class="sxs-lookup"><span data-stu-id="42b7c-170">-Force</span></span>
<span data-ttu-id="42b7c-171">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="42b7c-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42b7c-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="42b7c-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="42b7c-173">Se forçar Associação firewallPolicy estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="42b7c-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="42b7c-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="42b7c-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="42b7c-175">Especifica uma lista de configurações de IP de front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="42b7c-176">-FrontendPorts</span></span>
<span data-ttu-id="42b7c-177">Especifica uma lista de portas front-end para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="42b7c-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="42b7c-179">Especifica uma lista de configurações de IP para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="42b7c-180">-HttpListeners</span></span>
<span data-ttu-id="42b7c-181">Especifica uma lista de ouvintes HTTP para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="42b7c-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-182">-Identidade</span><span class="sxs-lookup"><span data-stu-id="42b7c-182">-Identity</span></span>
<span data-ttu-id="42b7c-183">Identidade do gateway do aplicativo a ser atribuída ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="42b7c-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-184">-Local</span><span class="sxs-lookup"><span data-stu-id="42b7c-184">-Location</span></span>
<span data-ttu-id="42b7c-185">Especifica a região na qual criar o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="42b7c-186">-Nome</span><span class="sxs-lookup"><span data-stu-id="42b7c-186">-Name</span></span>
<span data-ttu-id="42b7c-187">Especifica o nome do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="42b7c-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="42b7c-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="42b7c-189">A lista de configuração do privateLink</span><span class="sxs-lookup"><span data-stu-id="42b7c-189">The list of privateLink Configuration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-190">-Testes</span><span class="sxs-lookup"><span data-stu-id="42b7c-190">-Probes</span></span>
<span data-ttu-id="42b7c-191">Especifica os testes do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="42b7c-192">-RedirectConfigurations</span></span>
<span data-ttu-id="42b7c-193">A lista de configurações de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="42b7c-193">The list of redirect configuration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="42b7c-194">-RequestRoutingRules</span></span>
<span data-ttu-id="42b7c-195">Especifica uma lista de regras de roteamento de solicitações para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b7c-196">-ResourceGroupName</span></span>
<span data-ttu-id="42b7c-197">Especifica o nome do grupo de recursos no qual o Application Gateway será criado.</span><span class="sxs-lookup"><span data-stu-id="42b7c-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="42b7c-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42b7c-198">-RewriteRuleSet</span></span>
<span data-ttu-id="42b7c-199">A lista de RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="42b7c-199">The list of RewriteRuleSet</span></span>

```yaml
Type: PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="42b7c-200">-Sku</span></span>
<span data-ttu-id="42b7c-201">Especifica a SKU (unidade de manutenção de estoque) do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="42b7c-202">-SslCertificates</span></span>
<span data-ttu-id="42b7c-203">Especifica a lista de certificados SSL (Secure Sockets Layer) para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="42b7c-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="42b7c-204">-SslPolicy</span></span>
<span data-ttu-id="42b7c-205">Especifica uma política SSL para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="42b7c-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-206">-Marca</span><span class="sxs-lookup"><span data-stu-id="42b7c-206">-Tag</span></span>
<span data-ttu-id="42b7c-207">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="42b7c-207">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42b7c-208">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="42b7c-208">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="42b7c-209">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="42b7c-209">-TrustedRootCertificate</span></span>
<span data-ttu-id="42b7c-210">A lista de certificados raiz confiáveis</span><span class="sxs-lookup"><span data-stu-id="42b7c-210">The list of trusted root certificates</span></span>

```yaml
Type: PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-211">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="42b7c-211">-UrlPathMaps</span></span>
<span data-ttu-id="42b7c-212">Especifica mapas de caminho de URL para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42b7c-212">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-213">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="42b7c-213">-UserAssignedIdentityId</span></span>
<span data-ttu-id="42b7c-214">ResourceId da identidade atribuída pelo usuário a ser atribuído ao Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="42b7c-214">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-215">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="42b7c-215">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="42b7c-216">Especifica uma configuração de firewall de aplicativo Web (WAF).</span><span class="sxs-lookup"><span data-stu-id="42b7c-216">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="42b7c-217">Você pode usar o cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration para obter um WAF.</span><span class="sxs-lookup"><span data-stu-id="42b7c-217">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b7c-218">-Zone</span><span class="sxs-lookup"><span data-stu-id="42b7c-218">-Zone</span></span>
<span data-ttu-id="42b7c-219">Uma lista de zonas de disponibilidade que indicam para onde o gateway do aplicativo precisa vir.</span><span class="sxs-lookup"><span data-stu-id="42b7c-219">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="42b7c-220">-Confirme</span><span class="sxs-lookup"><span data-stu-id="42b7c-220">-Confirm</span></span>
<span data-ttu-id="42b7c-221">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b7c-221">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42b7c-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b7c-222">-WhatIf</span></span>
<span data-ttu-id="42b7c-223">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42b7c-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42b7c-224">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42b7c-224">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42b7c-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b7c-225">CommonParameters</span></span>
<span data-ttu-id="42b7c-226">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b7c-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b7c-227">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42b7c-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b7c-228">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42b7c-228">INPUTS</span></span>

### <span data-ttu-id="42b7c-229">System. String</span><span class="sxs-lookup"><span data-stu-id="42b7c-229">System.String</span></span>

### <span data-ttu-id="42b7c-230">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="42b7c-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="42b7c-231">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="42b7c-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="42b7c-232">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="42b7c-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="42b7c-233">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="42b7c-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="42b7c-234">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="42b7c-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="42b7c-235">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="42b7c-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="42b7c-236">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="42b7c-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="42b7c-237">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="42b7c-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="42b7c-238">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="42b7c-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="42b7c-239">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="42b7c-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="42b7c-240">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="42b7c-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="42b7c-241">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="42b7c-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="42b7c-242">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="42b7c-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="42b7c-243">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="42b7c-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="42b7c-244">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="42b7c-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="42b7c-245">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="42b7c-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="42b7c-246">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="42b7c-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="42b7c-247">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="42b7c-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="42b7c-248">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="42b7c-248">System.Collections.Hashtable</span></span>

### <span data-ttu-id="42b7c-249">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="42b7c-249">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="42b7c-250">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42b7c-250">OUTPUTS</span></span>

### <span data-ttu-id="42b7c-251">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42b7c-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="42b7c-252">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42b7c-252">NOTES</span></span>

## <span data-ttu-id="42b7c-253">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42b7c-253">RELATED LINKS</span></span>

[<span data-ttu-id="42b7c-254">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="42b7c-254">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="42b7c-255">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="42b7c-255">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="42b7c-256">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="42b7c-256">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="42b7c-257">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42b7c-257">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="42b7c-258">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="42b7c-258">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="42b7c-259">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="42b7c-259">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="42b7c-260">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="42b7c-260">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="42b7c-261">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="42b7c-261">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="42b7c-262">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="42b7c-262">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="42b7c-263">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="42b7c-263">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
