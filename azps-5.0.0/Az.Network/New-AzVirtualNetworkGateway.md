---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118317"
---
# <span data-ttu-id="23627-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23627-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="23627-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23627-102">SYNOPSIS</span></span>
<span data-ttu-id="23627-103">Cria um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="23627-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="23627-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23627-104">SYNTAX</span></span>

### <span data-ttu-id="23627-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="23627-105">Default (Default)</span></span>
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

### <span data-ttu-id="23627-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="23627-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23627-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="23627-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="23627-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="23627-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="23627-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23627-109">DESCRIPTION</span></span>
<span data-ttu-id="23627-110">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="23627-111">O cmdlet **New-AzVirtualNetworkGateway** cria o objeto do seu gateway no Azure com base no nome, nome do grupo de recursos, localização e configuração de IP, bem como o tipo de gateway e se VPN, o tipo de VPN.</span><span class="sxs-lookup"><span data-stu-id="23627-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="23627-112">Você também pode nomear o SKU do gateway.</span><span class="sxs-lookup"><span data-stu-id="23627-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="23627-113">Se esse gateway estiver sendo usado para conexões de ponto a site, você também precisará incluir o pool de endereços do cliente VPN do qual atribuir endereços para clientes de conexão e o certificado raiz do cliente VPN usado para autenticar clientes VPN que se conectam ao gateway.</span><span class="sxs-lookup"><span data-stu-id="23627-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="23627-114">Você também pode optar por incluir outros recursos como BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="23627-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="23627-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23627-115">EXAMPLES</span></span>

### <span data-ttu-id="23627-116">Exemplo 1: criar um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="23627-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="23627-117">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="23627-118">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="23627-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="23627-119">Exemplo 2: criar um gateway de rede virtual com configuração RADIUS externa</span><span class="sxs-lookup"><span data-stu-id="23627-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="23627-120">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="23627-121">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="23627-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="23627-122">Ele também adiciona um servidor RADIUS externo com o endereço "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="23627-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="23627-123">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="23627-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="23627-124">Exemplo 3: criar um gateway de rede virtual com configurações do P2S</span><span class="sxs-lookup"><span data-stu-id="23627-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
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

<span data-ttu-id="23627-125">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway de rede virtual com as configurações do P2S, por exemplo, VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy etc. no Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="23627-126">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="23627-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="23627-127">As configurações de VPN serão definidas no gateway como VpnProtocol definido como Ikev2, VpnClientAddressPool como "201.169.0.0/16", VpnClientRootCertificate definido como aprovado: clientRootCertName e a política IPSec VPN personalizada passada no objeto: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="23627-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="23627-128">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="23627-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="23627-129">Exemplo 4: criar um gateway de rede virtual com a configuração de autenticação AAD para VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="23627-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="23627-130">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="23627-131">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="23627-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="23627-132">Ele também configura as configurações de autenticação do AAD: AadTenantUri, AadIssuerUri e AadAudienceId para VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="23627-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="23627-133">Exemplo 5: criar um gateway de rede virtual com VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="23627-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="23627-134">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="23627-135">O gateway será chamado de "myNGW" dentro do grupo de recursos "VPN-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway "VPN", o tipo de VPN "RouteBased", o SKU "VpnGw4" e VpnGatewayGeneration Generation2 habilitados.</span><span class="sxs-lookup"><span data-stu-id="23627-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="23627-136">Exemplo 6: criar um gateway de rede virtual com o IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="23627-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
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

<span data-ttu-id="23627-137">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="23627-138">ipconfigurationId1 de ipconfiguration de gateway recém-criado e armazenado no ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="23627-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="23627-139">O gateway será chamado de "gateway1" dentro do grupo de recursos "resourcegroup1resourcegroup1", no local "Reino Unido", com o endereço de Bgppeering de configurações de IP criado anteriormente salvo na variável "gw1ipconfBgp1", o tipo de gateway de "VPN", o tipo de VPN "RouteBased", o SKU "VpnGw4" e VpnGatewayGeneration Generation2 habilitados.</span><span class="sxs-lookup"><span data-stu-id="23627-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="23627-140">OS</span><span class="sxs-lookup"><span data-stu-id="23627-140">PARAMETERS</span></span>

### <span data-ttu-id="23627-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="23627-141">-AadAudienceId</span></span>
<span data-ttu-id="23627-142">Opção de autenticação AAD do P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="23627-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="23627-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="23627-143">-AadIssuerUri</span></span>
<span data-ttu-id="23627-144">Opção de autenticação AAD do P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="23627-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="23627-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="23627-145">-AadTenantUri</span></span>
<span data-ttu-id="23627-146">Opção de autenticação AAD do P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="23627-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="23627-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23627-147">-AsJob</span></span>
<span data-ttu-id="23627-148">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="23627-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23627-149">-ASN</span><span class="sxs-lookup"><span data-stu-id="23627-149">-Asn</span></span>
<span data-ttu-id="23627-150">O ASN do gateway de rede virtual para BGP em VPN</span><span class="sxs-lookup"><span data-stu-id="23627-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="23627-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="23627-151">-CustomRoute</span></span>
<span data-ttu-id="23627-152">AddressPool de rotas personalizadas especificado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="23627-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="23627-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23627-153">-DefaultProfile</span></span>
<span data-ttu-id="23627-154">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23627-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23627-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="23627-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="23627-156">Sinalizar para habilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="23627-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="23627-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="23627-157">-EnableBgp</span></span>
<span data-ttu-id="23627-158">Sinalizador EnableBgp</span><span class="sxs-lookup"><span data-stu-id="23627-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="23627-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="23627-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="23627-160">Sinalizar para habilitar o IPAddress privado no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="23627-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="23627-161">-Force</span><span class="sxs-lookup"><span data-stu-id="23627-161">-Force</span></span>
<span data-ttu-id="23627-162">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="23627-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="23627-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="23627-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="23627-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="23627-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="23627-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="23627-165">-GatewaySku</span></span>
<span data-ttu-id="23627-166">A camada SKU do gateway</span><span class="sxs-lookup"><span data-stu-id="23627-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="23627-167">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="23627-167">-GatewayType</span></span>
<span data-ttu-id="23627-168">O tipo deste gateway de rede virtual: VPN, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="23627-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="23627-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="23627-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="23627-170">O BgpPeeringAddresses para o bgpsettings do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="23627-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="23627-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="23627-171">-IpConfigurations</span></span>
<span data-ttu-id="23627-172">As IpConfigurations do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="23627-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="23627-173">-Local</span><span class="sxs-lookup"><span data-stu-id="23627-173">-Location</span></span>
<span data-ttu-id="23627-174">ponto.</span><span class="sxs-lookup"><span data-stu-id="23627-174">location.</span></span>

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

### <span data-ttu-id="23627-175">-Nome</span><span class="sxs-lookup"><span data-stu-id="23627-175">-Name</span></span>
<span data-ttu-id="23627-176">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="23627-176">The resource name.</span></span>

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

### <span data-ttu-id="23627-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="23627-177">-PeerWeight</span></span>
<span data-ttu-id="23627-178">A espessura adicionada a rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="23627-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="23627-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="23627-179">-RadiusServerAddress</span></span>
<span data-ttu-id="23627-180">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="23627-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="23627-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="23627-181">-RadiusServerList</span></span>
<span data-ttu-id="23627-182">P2S vários servidores de servidor RADIUS externos.</span><span class="sxs-lookup"><span data-stu-id="23627-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23627-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="23627-183">-RadiusServerSecret</span></span>
<span data-ttu-id="23627-184">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="23627-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="23627-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23627-185">-ResourceGroupName</span></span>
<span data-ttu-id="23627-186">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23627-186">The resource group name.</span></span>

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

### <span data-ttu-id="23627-187">-Marca</span><span class="sxs-lookup"><span data-stu-id="23627-187">-Tag</span></span>
<span data-ttu-id="23627-188">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="23627-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="23627-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="23627-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="23627-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="23627-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="23627-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="23627-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="23627-192">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="23627-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="23627-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="23627-193">-VpnClientProtocol</span></span>
<span data-ttu-id="23627-194">A lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="23627-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="23627-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="23627-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="23627-196">A lista de VpnClientCertificates a ser revogada.</span><span class="sxs-lookup"><span data-stu-id="23627-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="23627-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="23627-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="23627-198">A lista de VpnClientRootCertificates a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="23627-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="23627-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="23627-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="23627-200">A geração desse gateway de VPN VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="23627-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="23627-201">Deve ser nenhum se Gatewaytype não for VPN.</span><span class="sxs-lookup"><span data-stu-id="23627-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="23627-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="23627-202">-VpnType</span></span>
<span data-ttu-id="23627-203">O tipo da VPN: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="23627-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="23627-204">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23627-204">-Confirm</span></span>
<span data-ttu-id="23627-205">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23627-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23627-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23627-206">-WhatIf</span></span>
<span data-ttu-id="23627-207">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23627-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23627-208">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23627-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23627-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23627-209">CommonParameters</span></span>
<span data-ttu-id="23627-210">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23627-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23627-211">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23627-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23627-212">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23627-212">INPUTS</span></span>

### <span data-ttu-id="23627-213">System. String</span><span class="sxs-lookup"><span data-stu-id="23627-213">System.String</span></span>

### <span data-ttu-id="23627-214">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="23627-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="23627-215">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23627-215">System.Boolean</span></span>

### <span data-ttu-id="23627-216">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23627-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="23627-217">System. String []</span><span class="sxs-lookup"><span data-stu-id="23627-217">System.String[]</span></span>

### <span data-ttu-id="23627-218">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="23627-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="23627-219">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="23627-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="23627-220">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="23627-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="23627-221">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="23627-221">System.UInt32</span></span>

### <span data-ttu-id="23627-222">System. Int32</span><span class="sxs-lookup"><span data-stu-id="23627-222">System.Int32</span></span>

### <span data-ttu-id="23627-223">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="23627-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="23627-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="23627-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="23627-225">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="23627-225">System.Security.SecureString</span></span>

## <span data-ttu-id="23627-226">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23627-226">OUTPUTS</span></span>

### <span data-ttu-id="23627-227">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23627-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="23627-228">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23627-228">NOTES</span></span>

## <span data-ttu-id="23627-229">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23627-229">RELATED LINKS</span></span>
