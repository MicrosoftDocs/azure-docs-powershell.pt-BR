---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 3c30f7a341615b7e12843f3cd745cd691fa205aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943233"
---
# <span data-ttu-id="65222-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65222-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="65222-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65222-102">SYNOPSIS</span></span>
<span data-ttu-id="65222-103">Cria um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="65222-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="65222-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65222-104">SYNTAX</span></span>

### <span data-ttu-id="65222-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="65222-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65222-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="65222-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65222-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="65222-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65222-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65222-108">DESCRIPTION</span></span>
<span data-ttu-id="65222-109">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="65222-110">O cmdlet **New-AzVirtualNetworkGateway** cria o objeto do seu gateway no Azure com base no nome, nome do grupo de recursos, localização e configuração de IP, bem como o tipo de gateway e se VPN, o tipo de VPN.</span><span class="sxs-lookup"><span data-stu-id="65222-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="65222-111">Você também pode nomear o SKU do gateway.</span><span class="sxs-lookup"><span data-stu-id="65222-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="65222-112">Se esse gateway estiver sendo usado para conexões de ponto a site, você também precisará incluir o pool de endereços do cliente VPN do qual atribuir endereços para clientes de conexão e o certificado raiz do cliente VPN usado para autenticar clientes VPN que se conectam ao gateway.</span><span class="sxs-lookup"><span data-stu-id="65222-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="65222-113">Você também pode optar por incluir outros recursos como BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="65222-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="65222-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65222-114">EXAMPLES</span></span>

### <span data-ttu-id="65222-115">1: criar um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="65222-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="65222-116">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="65222-117">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="65222-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="65222-118">2: criar um gateway de rede virtual com configuração RADIUS externa</span><span class="sxs-lookup"><span data-stu-id="65222-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="65222-119">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="65222-120">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="65222-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="65222-121">Ele também adiciona um servidor RADIUS externo com o endereço "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="65222-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="65222-122">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="65222-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="65222-123">3: criar um gateway de rede virtual com configurações do P2S</span><span class="sxs-lookup"><span data-stu-id="65222-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="65222-124">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway de rede virtual com as configurações do P2S, por exemplo, VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy etc. no Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="65222-125">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="65222-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="65222-126">As configurações de VPN serão definidas no gateway como VpnProtocol definido como Ikev2, VpnClientAddressPool como "201.169.0.0/16", VpnClientRootCertificate definido como aprovado: clientRootCertName e a política IPSec VPN personalizada passada no objeto: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="65222-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="65222-127">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="65222-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="65222-128">4: Crie um gateway de rede virtual com a configuração de autenticação AAD para VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="65222-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="65222-129">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="65222-130">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="65222-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="65222-131">Ele também configura as configurações de autenticação do AAD: AadTenantUri, AadIssuerUri e AadAudienceId para VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="65222-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="65222-132">5: criar um gateway de rede virtual com o VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="65222-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="65222-133">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="65222-134">O gateway será chamado de "myNGW" dentro do grupo de recursos "VPN-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway "VPN", o tipo de VPN "RouteBased", o SKU "VpnGw4" e VpnGatewayGeneration Generation2 habilitados.</span><span class="sxs-lookup"><span data-stu-id="65222-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="65222-135">6: criar um gateway de rede virtual com o IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="65222-135">6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="65222-136">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-136">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="65222-137">ipconfigurationId1 de ipconfiguration de gateway recém-criado e armazenado no ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="65222-137">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="65222-138">O gateway será chamado de "gateway1" dentro do grupo de recursos "resourcegroup1resourcegroup1", no local "Reino Unido", com o endereço de Bgppeering de configurações de IP criado anteriormente salvo na variável "gw1ipconfBgp1", o tipo de gateway de "VPN", o tipo de VPN "RouteBased", o SKU "VpnGw4" e VpnGatewayGeneration Generation2 habilitados.</span><span class="sxs-lookup"><span data-stu-id="65222-138">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="65222-139">OS</span><span class="sxs-lookup"><span data-stu-id="65222-139">PARAMETERS</span></span>

### <span data-ttu-id="65222-140">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="65222-140">-AadAudienceId</span></span>
<span data-ttu-id="65222-141">Opção de autenticação AAD do P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="65222-141">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-142">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="65222-142">-AadIssuerUri</span></span>
<span data-ttu-id="65222-143">Opção de autenticação AAD do P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="65222-143">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-144">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="65222-144">-AadTenantUri</span></span>
<span data-ttu-id="65222-145">Opção de autenticação AAD do P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="65222-145">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65222-146">-AsJob</span></span>
<span data-ttu-id="65222-147">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="65222-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65222-148">-ASN</span><span class="sxs-lookup"><span data-stu-id="65222-148">-Asn</span></span>
<span data-ttu-id="65222-149">O ASN do gateway de rede virtual para BGP em VPN</span><span class="sxs-lookup"><span data-stu-id="65222-149">The virtual network gateway's ASN for BGP over VPN</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-150">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="65222-150">-CustomRoute</span></span>
<span data-ttu-id="65222-151">AddressPool de rotas personalizadas especificado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="65222-151">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65222-152">-DefaultProfile</span></span>
<span data-ttu-id="65222-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65222-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65222-154">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="65222-154">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="65222-155">Sinalizar para habilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="65222-155">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="65222-156">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="65222-156">-EnableBgp</span></span>
<span data-ttu-id="65222-157">Sinalizador EnableBgp</span><span class="sxs-lookup"><span data-stu-id="65222-157">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-158">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="65222-158">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="65222-159">Sinalizar para habilitar o IPAddress privado no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="65222-159">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="65222-160">-Force</span><span class="sxs-lookup"><span data-stu-id="65222-160">-Force</span></span>
<span data-ttu-id="65222-161">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="65222-161">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="65222-162">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="65222-162">-GatewayDefaultSite</span></span>
<span data-ttu-id="65222-163">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="65222-163">GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-164">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="65222-164">-GatewaySku</span></span>
<span data-ttu-id="65222-165">A camada SKU do gateway</span><span class="sxs-lookup"><span data-stu-id="65222-165">The Gateway Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-166">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="65222-166">-GatewayType</span></span>
<span data-ttu-id="65222-167">O tipo deste gateway de rede virtual: VPN, ExoressRoute</span><span class="sxs-lookup"><span data-stu-id="65222-167">The type of this virtual network gateway: Vpn, ExoressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-168">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="65222-168">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="65222-169">O BgpPeeringAddresses para o bgpsettings do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="65222-169">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-170">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="65222-170">-IpConfigurations</span></span>
<span data-ttu-id="65222-171">As IpConfigurations do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="65222-171">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-172">-Local</span><span class="sxs-lookup"><span data-stu-id="65222-172">-Location</span></span>
<span data-ttu-id="65222-173">ponto.</span><span class="sxs-lookup"><span data-stu-id="65222-173">location.</span></span>

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

### <span data-ttu-id="65222-174">-Nome</span><span class="sxs-lookup"><span data-stu-id="65222-174">-Name</span></span>
<span data-ttu-id="65222-175">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="65222-175">The resource name.</span></span>

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

### <span data-ttu-id="65222-176">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="65222-176">-PeerWeight</span></span>
<span data-ttu-id="65222-177">A espessura adicionada a rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="65222-177">The weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-178">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="65222-178">-RadiusServerAddress</span></span>
<span data-ttu-id="65222-179">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="65222-179">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-180">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="65222-180">-RadiusServerSecret</span></span>
<span data-ttu-id="65222-181">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="65222-181">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65222-182">-ResourceGroupName</span></span>
<span data-ttu-id="65222-183">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65222-183">The resource group name.</span></span>

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

### <span data-ttu-id="65222-184">-Marca</span><span class="sxs-lookup"><span data-stu-id="65222-184">-Tag</span></span>
<span data-ttu-id="65222-185">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="65222-185">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="65222-186">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="65222-186">-VpnClientAddressPool</span></span>
<span data-ttu-id="65222-187">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="65222-187">P2S VpnClient AddressPool</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-188">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="65222-188">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="65222-189">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="65222-189">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-190">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="65222-190">-VpnClientProtocol</span></span>
<span data-ttu-id="65222-191">A lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="65222-191">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-192">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="65222-192">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="65222-193">A lista de VpnClientCertificates a ser revogada.</span><span class="sxs-lookup"><span data-stu-id="65222-193">The list of VpnClientCertificates to be revoked.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-194">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="65222-194">-VpnClientRootCertificates</span></span>
<span data-ttu-id="65222-195">A lista de VpnClientRootCertificates a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="65222-195">The list of VpnClientRootCertificates to be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-196">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="65222-196">-VpnGatewayGeneration</span></span>
<span data-ttu-id="65222-197">A geração desse gateway de VPN VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="65222-197">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="65222-198">Deve ser nenhum se Gatewaytype não for VPN.</span><span class="sxs-lookup"><span data-stu-id="65222-198">Must be None if GatewayType is not VPN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65222-199">-VpnType</span><span class="sxs-lookup"><span data-stu-id="65222-199">-VpnType</span></span>
<span data-ttu-id="65222-200">O tipo da VPN: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="65222-200">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65222-201">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65222-201">-Confirm</span></span>
<span data-ttu-id="65222-202">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65222-202">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65222-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65222-203">-WhatIf</span></span>
<span data-ttu-id="65222-204">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65222-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65222-205">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65222-205">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65222-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65222-206">CommonParameters</span></span>
<span data-ttu-id="65222-207">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65222-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65222-208">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65222-208">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65222-209">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65222-209">INPUTS</span></span>

### <span data-ttu-id="65222-210">System. String</span><span class="sxs-lookup"><span data-stu-id="65222-210">System.String</span></span>

### <span data-ttu-id="65222-211">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="65222-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="65222-212">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65222-212">System.Boolean</span></span>

### <span data-ttu-id="65222-213">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65222-213">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="65222-214">System. String []</span><span class="sxs-lookup"><span data-stu-id="65222-214">System.String[]</span></span>

### <span data-ttu-id="65222-215">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="65222-215">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="65222-216">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="65222-216">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="65222-217">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="65222-217">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="65222-218">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="65222-218">System.UInt32</span></span>

### <span data-ttu-id="65222-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="65222-219">System.Int32</span></span>

### <span data-ttu-id="65222-220">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="65222-220">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="65222-221">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="65222-221">System.Collections.Hashtable</span></span>

### <span data-ttu-id="65222-222">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="65222-222">System.Security.SecureString</span></span>

## <span data-ttu-id="65222-223">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65222-223">OUTPUTS</span></span>

### <span data-ttu-id="65222-224">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="65222-224">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="65222-225">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65222-225">NOTES</span></span>

## <span data-ttu-id="65222-226">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65222-226">RELATED LINKS</span></span>
