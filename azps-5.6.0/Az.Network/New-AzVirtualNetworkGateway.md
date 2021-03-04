---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c9729dd81dc5ff287ab032fdce6ad937c282e1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888621"
---
# <span data-ttu-id="0b4cf-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0b4cf-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="0b4cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4cf-103">Cria um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="0b4cf-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="0b4cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0b4cf-104">SYNTAX</span></span>

### <span data-ttu-id="0b4cf-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b4cf-105">Default (Default)</span></span>
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

### <span data-ttu-id="0b4cf-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4cf-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="0b4cf-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4cf-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="0b4cf-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b4cf-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="0b4cf-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0b4cf-109">DESCRIPTION</span></span>
<span data-ttu-id="0b4cf-110">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="0b4cf-111">O cmdlet **New-AzVirtualNetworkGateway** cria o objeto do gateway no Azure com base na configuração Nome, Nome do Grupo de Recursos, Local e IP, bem como o Tipo de Gateway e se VPN, o Tipo VPN.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="0b4cf-112">Você também pode nomear o SKU do Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="0b4cf-113">Se esse Gateway estiver sendo usado para conexões ponto a site, você também precisará incluir o Pool de Endereços do Cliente VPN do qual atribuir endereços para conectar clientes e o Certificado Raiz do Cliente VPN usado para autenticar clientes VPN que se conectam ao Gateway.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="0b4cf-114">Você também pode optar por incluir outros recursos, como BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="0b4cf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b4cf-115">EXAMPLES</span></span>

### <span data-ttu-id="0b4cf-116">Exemplo 1: Criar um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="0b4cf-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="0b4cf-117">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0b4cf-118">O gateway será chamado de "myNGW" dentro do grupo de recursos "vnet-gateway" no local "Uk West" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e o sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="0b4cf-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="0b4cf-119">Exemplo 2: Criar um gateway de rede virtual com configuração de raio externo</span><span class="sxs-lookup"><span data-stu-id="0b4cf-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="0b4cf-120">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0b4cf-121">O gateway será chamado de "myNGW" dentro do grupo de recursos "vnet-gateway" no local "Uk West" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e o sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="0b4cf-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="0b4cf-122">Ele também adiciona um servidor de raio externo com o endereço "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="0b4cf-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="0b4cf-123">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="0b4cf-124">Exemplo 3: Criar um Gateway de Rede Virtual com configurações P2S</span><span class="sxs-lookup"><span data-stu-id="0b4cf-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="0b4cf-125">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual com configurações P2S, por exemplo, VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="0b4cf-126">O gateway será chamado de "myNGW" dentro do grupo de recursos "vnet-gateway" no local "Uk West" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e o sku "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="0b4cf-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="0b4cf-127">As configurações de VPN serão definidas no Gateway, como VpnProtocol definido como Ikev2, VpnClientAddressPool como "201.169.0.0/16", VpnClientRootCertificate definido como passado um: clientRootCertName e política ipsec vpn personalizada passada em object:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="0b4cf-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="0b4cf-128">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="0b4cf-129">Exemplo 4: Criar um Gateway de Rede Virtual com a configuração de autenticação AAD para VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="0b4cf-130">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0b4cf-131">O gateway será chamado de "myNGW" dentro do grupo de recursos "vnet-gateway" no local "Uk West" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e o sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="0b4cf-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="0b4cf-132">Ele também configura configurações de autenticação AAD: AadTenantUri, AadIssuerUri e AadAudienceId para VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="0b4cf-133">Exemplo 5: Criar um Gateway de Rede Virtual com VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="0b4cf-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="0b4cf-134">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0b4cf-135">O gateway será chamado de "myNGW" dentro do grupo de recursos "vnet-gateway" no local "Uk West" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased", o sku "VpnGw4" e VpnGatewayGeneration Generation2 habilitado.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="0b4cf-136">Exemplo 6: Criar um Gateway de Rede Virtual com IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="0b4cf-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="0b4cf-137">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0b4cf-138">ipconfigurationId1 do gateway ipconfiguration acabou de ser criado e armazenado no ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="0b4cf-139">O gateway será chamado de "gateway1" dentro do grupo de recursos "resourcegroup1resourcegroup1" no local "Uk West" com as configurações IP criadas anteriormente Endereço Bgppeering salvo na variável "gw1ipconfBgp1", o tipo de gateway de "VPN", o tipo vpn "RouteBased", o sku "VpnGw4" e VpnGatewayGeneration Generation2 habilitado.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="0b4cf-140">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0b4cf-140">PARAMETERS</span></span>

### <span data-ttu-id="0b4cf-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="0b4cf-141">-AadAudienceId</span></span>
<span data-ttu-id="0b4cf-142">Opção de autenticação AAD P2S:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="0b4cf-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="0b4cf-143">-AadIssuerUri</span></span>
<span data-ttu-id="0b4cf-144">Opção de autenticação AAD P2S:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="0b4cf-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="0b4cf-145">-AadTenantUri</span></span>
<span data-ttu-id="0b4cf-146">Opção de autenticação AAD P2S:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="0b4cf-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b4cf-147">-AsJob</span></span>
<span data-ttu-id="0b4cf-148">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0b4cf-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b4cf-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="0b4cf-149">-Asn</span></span>
<span data-ttu-id="0b4cf-150">ASN do gateway de rede virtual para BGP por VPN</span><span class="sxs-lookup"><span data-stu-id="0b4cf-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="0b4cf-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="0b4cf-151">-CustomRoute</span></span>
<span data-ttu-id="0b4cf-152">Rotas personalizadas AddressPool especificadas pelo cliente</span><span class="sxs-lookup"><span data-stu-id="0b4cf-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="0b4cf-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4cf-153">-DefaultProfile</span></span>
<span data-ttu-id="0b4cf-154">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b4cf-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="0b4cf-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="0b4cf-156">Sinalizador para habilitar o recurso Ativo Ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0b4cf-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="0b4cf-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="0b4cf-157">-EnableBgp</span></span>
<span data-ttu-id="0b4cf-158">Sinalizador EnableBgp</span><span class="sxs-lookup"><span data-stu-id="0b4cf-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="0b4cf-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="0b4cf-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="0b4cf-160">Sinalizador para habilitar IPAddress privado no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0b4cf-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="0b4cf-161">-Force</span><span class="sxs-lookup"><span data-stu-id="0b4cf-161">-Force</span></span>
<span data-ttu-id="0b4cf-162">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="0b4cf-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0b4cf-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0b4cf-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="0b4cf-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0b4cf-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="0b4cf-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="0b4cf-165">-GatewaySku</span></span>
<span data-ttu-id="0b4cf-166">A Camada Sku do Gateway</span><span class="sxs-lookup"><span data-stu-id="0b4cf-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="0b4cf-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="0b4cf-167">-GatewayType</span></span>
<span data-ttu-id="0b4cf-168">O tipo desse gateway de rede virtual: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0b4cf-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="0b4cf-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="0b4cf-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="0b4cf-170">BgpPeeringAddresses for Virtual network gateway bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="0b4cf-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="0b4cf-171">-IpConfigurations</span></span>
<span data-ttu-id="0b4cf-172">IpConfigurations for Virtual network gateway.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="0b4cf-173">-Location</span><span class="sxs-lookup"><span data-stu-id="0b4cf-173">-Location</span></span>
<span data-ttu-id="0b4cf-174">location.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-174">location.</span></span>

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

### <span data-ttu-id="0b4cf-175">-Name</span><span class="sxs-lookup"><span data-stu-id="0b4cf-175">-Name</span></span>
<span data-ttu-id="0b4cf-176">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-176">The resource name.</span></span>

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

### <span data-ttu-id="0b4cf-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="0b4cf-177">-PeerWeight</span></span>
<span data-ttu-id="0b4cf-178">O peso adicionado às rotas aprendidas sobre o BGP a partir deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0b4cf-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="0b4cf-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="0b4cf-179">-RadiusServerAddress</span></span>
<span data-ttu-id="0b4cf-180">Endereço do servidor raio externo P2S.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="0b4cf-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="0b4cf-181">-RadiusServerList</span></span>
<span data-ttu-id="0b4cf-182">P2S vários servidores de servidores Radius externos.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="0b4cf-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="0b4cf-183">-RadiusServerSecret</span></span>
<span data-ttu-id="0b4cf-184">Segredo do servidor raio externo P2S.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="0b4cf-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b4cf-185">-ResourceGroupName</span></span>
<span data-ttu-id="0b4cf-186">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-186">The resource group name.</span></span>

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

### <span data-ttu-id="0b4cf-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b4cf-187">-Tag</span></span>
<span data-ttu-id="0b4cf-188">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0b4cf-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="0b4cf-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="0b4cf-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="0b4cf-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="0b4cf-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="0b4cf-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="0b4cf-192">Uma lista de políticas IPSec para protocolos de túnel de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="0b4cf-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="0b4cf-193">-VpnClientProtocol</span></span>
<span data-ttu-id="0b4cf-194">A lista de protocolos de túnel de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="0b4cf-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="0b4cf-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="0b4cf-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="0b4cf-196">A lista de VpnClientCertificates a ser revogada.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="0b4cf-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="0b4cf-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="0b4cf-198">A lista de VpnClientRootCertificates a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="0b4cf-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="0b4cf-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="0b4cf-200">A geração desse gateway VPN virtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="0b4cf-201">Deve ser None se GatewayType não for VPN.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="0b4cf-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="0b4cf-202">-VpnType</span></span>
<span data-ttu-id="0b4cf-203">O tipo de Vpn:PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="0b4cf-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="0b4cf-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b4cf-204">-Confirm</span></span>
<span data-ttu-id="0b4cf-205">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b4cf-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4cf-206">-WhatIf</span></span>
<span data-ttu-id="0b4cf-207">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b4cf-208">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b4cf-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4cf-209">CommonParameters</span></span>
<span data-ttu-id="0b4cf-210">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4cf-211">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b4cf-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4cf-212">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b4cf-212">INPUTS</span></span>

### <span data-ttu-id="0b4cf-213">System.String</span><span class="sxs-lookup"><span data-stu-id="0b4cf-213">System.String</span></span>

### <span data-ttu-id="0b4cf-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="0b4cf-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="0b4cf-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b4cf-215">System.Boolean</span></span>

### <span data-ttu-id="0b4cf-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0b4cf-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="0b4cf-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0b4cf-217">System.String[]</span></span>

### <span data-ttu-id="0b4cf-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="0b4cf-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="0b4cf-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="0b4cf-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="0b4cf-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="0b4cf-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="0b4cf-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="0b4cf-221">System.UInt32</span></span>

### <span data-ttu-id="0b4cf-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0b4cf-222">System.Int32</span></span>

### <span data-ttu-id="0b4cf-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="0b4cf-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="0b4cf-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b4cf-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0b4cf-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="0b4cf-225">System.Security.SecureString</span></span>

## <span data-ttu-id="0b4cf-226">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0b4cf-226">OUTPUTS</span></span>

### <span data-ttu-id="0b4cf-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0b4cf-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0b4cf-228">NOTES</span><span class="sxs-lookup"><span data-stu-id="0b4cf-228">NOTES</span></span>

## <span data-ttu-id="0b4cf-229">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b4cf-229">RELATED LINKS</span></span>
