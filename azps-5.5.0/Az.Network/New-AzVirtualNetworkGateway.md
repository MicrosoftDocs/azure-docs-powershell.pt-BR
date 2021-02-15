---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117379"
---
# <span data-ttu-id="aa164-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aa164-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="aa164-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa164-102">SYNOPSIS</span></span>
<span data-ttu-id="aa164-103">Cria um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="aa164-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="aa164-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa164-104">SYNTAX</span></span>

### <span data-ttu-id="aa164-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aa164-105">Default (Default)</span></span>
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

### <span data-ttu-id="aa164-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa164-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="aa164-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa164-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="aa164-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa164-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="aa164-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa164-109">DESCRIPTION</span></span>
<span data-ttu-id="aa164-110">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="aa164-111">O cmdlet **New-AzVirtualNetworkGateway** cria o objeto do gateway no Azure com base na configuração Nome, Nome do Grupo de Recursos, Local e IP, bem como o Tipo de Gateway e se VPN, o Tipo VPN.</span><span class="sxs-lookup"><span data-stu-id="aa164-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="aa164-112">Você também pode nomear a SKU do Gateway.</span><span class="sxs-lookup"><span data-stu-id="aa164-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="aa164-113">Se esse Gateway estiver sendo usado para conexões ponto a site, você também precisará incluir o Pool de Endereços do Cliente VPN do qual atribuir endereços para conectar clientes e o Certificado Raiz do Cliente VPN usado para autenticar clientes VPN que se conectam ao Gateway.</span><span class="sxs-lookup"><span data-stu-id="aa164-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="aa164-114">Você também pode optar por incluir outros recursos, como BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="aa164-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="aa164-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa164-115">EXAMPLES</span></span>

### <span data-ttu-id="aa164-116">Exemplo 1: Criar um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="aa164-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="aa164-117">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="aa164-118">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Oeste do Reino Unido" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e a sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="aa164-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="aa164-119">Exemplo 2: Criar um Gateway de Rede Virtual com Configuração de Raio Externo</span><span class="sxs-lookup"><span data-stu-id="aa164-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="aa164-120">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="aa164-121">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Oeste do Reino Unido" com as configurações DE IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e a sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="aa164-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="aa164-122">Ele também adiciona um servidor de raio externo com o endereço "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="aa164-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="aa164-123">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="aa164-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="aa164-124">Exemplo 3: Criar um Gateway de Rede Virtual com configurações P2S</span><span class="sxs-lookup"><span data-stu-id="aa164-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="aa164-125">O exemplo acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual com configurações P2S, por exemplo, VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy etc. no Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="aa164-126">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Oeste do Reino Unido" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e a sku "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="aa164-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="aa164-127">As configurações de VPN serão definidas no Gateway, como VpnProtocol definidas como Ikev2, VpnClientAddressPool como "201.169.0.0/16", VpnClientRootCertificate definido como aprovado: clientRootCertName e política ipsec vpn personalizada passada em objeto:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="aa164-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="aa164-128">Ele também definirá rotas personalizadas especificadas pelos clientes no gateway.</span><span class="sxs-lookup"><span data-stu-id="aa164-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="aa164-129">Exemplo 4: Criar um Gateway de Rede Virtual com a configuração de autenticação AAD para VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="aa164-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="aa164-130">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="aa164-131">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Oeste do Reino Unido" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased" e a sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="aa164-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="aa164-132">Ele também configura configurações de autenticação do AAD: AadTenantUri, AadIssuerUri e AadAudienceId para VpnClient de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="aa164-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="aa164-133">Exemplo 5: Criar um Gateway de Rede Virtual com o VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="aa164-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="aa164-134">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="aa164-135">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Oeste do Reino Unido" com as configurações IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo vpn "RouteBased", a sku "VpnGw4" e VpnGatewayGeneration Generation2 habilitada.</span><span class="sxs-lookup"><span data-stu-id="aa164-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="aa164-136">Exemplo 6: Criar um Gateway de Rede Virtual com IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="aa164-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="aa164-137">O acima criará um grupo de recursos, solicitará um Endereço IP Público, criará uma Rede Virtual e uma sub-rede e criará um Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="aa164-138">ipconfigurationId1 de ipconfiguration do gateway acabou de criar e armazenar no ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="aa164-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="aa164-139">O gateway será chamado de "gateway1" dentro do grupo de recursos "resourcegroup1resourcegroup1" no local "Uk West" com as configurações IP criadas anteriormente. O endereço Bgappering salvo na variável "gw1ipconfBgp1", o tipo de gateway de "VPN", o tipo de vpn "RouteBased", a sku "VpnGw4" e VpnGatewayGeneration Generation2 habilitado.</span><span class="sxs-lookup"><span data-stu-id="aa164-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="aa164-140">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa164-140">PARAMETERS</span></span>

### <span data-ttu-id="aa164-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="aa164-141">-AadAudienceId</span></span>
<span data-ttu-id="aa164-142">Opção de autenticação P2S AAD:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="aa164-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="aa164-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="aa164-143">-AadIssuerUri</span></span>
<span data-ttu-id="aa164-144">Opção de autenticação P2S AAD:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="aa164-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="aa164-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="aa164-145">-AadTenantUri</span></span>
<span data-ttu-id="aa164-146">Opção de autenticação P2S AAD:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="aa164-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="aa164-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa164-147">-AsJob</span></span>
<span data-ttu-id="aa164-148">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aa164-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa164-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="aa164-149">-Asn</span></span>
<span data-ttu-id="aa164-150">AsN do gateway de rede virtual para BGP por VPN</span><span class="sxs-lookup"><span data-stu-id="aa164-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="aa164-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="aa164-151">-CustomRoute</span></span>
<span data-ttu-id="aa164-152">Rotas personalizadas, AddressPool especificadas pelo cliente</span><span class="sxs-lookup"><span data-stu-id="aa164-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="aa164-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa164-153">-DefaultProfile</span></span>
<span data-ttu-id="aa164-154">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa164-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa164-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="aa164-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="aa164-156">Sinalizar para habilitar o recurso Ativo Ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="aa164-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="aa164-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="aa164-157">-EnableBgp</span></span>
<span data-ttu-id="aa164-158">Sinalizador EnableBgp</span><span class="sxs-lookup"><span data-stu-id="aa164-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="aa164-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa164-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="aa164-160">Sinalizar para habilitar o IPAddress particular no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="aa164-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="aa164-161">-Forçar</span><span class="sxs-lookup"><span data-stu-id="aa164-161">-Force</span></span>
<span data-ttu-id="aa164-162">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="aa164-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="aa164-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="aa164-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="aa164-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="aa164-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="aa164-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="aa164-165">-GatewaySku</span></span>
<span data-ttu-id="aa164-166">A camada SKU do Gateway</span><span class="sxs-lookup"><span data-stu-id="aa164-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="aa164-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="aa164-167">-GatewayType</span></span>
<span data-ttu-id="aa164-168">O tipo deste gateway de rede virtual: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="aa164-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="aa164-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="aa164-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="aa164-170">O BgpPeeringAddresses para gateway de rede virtual bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="aa164-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="aa164-171">-IpConfigurações</span><span class="sxs-lookup"><span data-stu-id="aa164-171">-IpConfigurations</span></span>
<span data-ttu-id="aa164-172">O gateway de rede IpConfigurations para Virtual.</span><span class="sxs-lookup"><span data-stu-id="aa164-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="aa164-173">-Local</span><span class="sxs-lookup"><span data-stu-id="aa164-173">-Location</span></span>
<span data-ttu-id="aa164-174">Localização.</span><span class="sxs-lookup"><span data-stu-id="aa164-174">location.</span></span>

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

### <span data-ttu-id="aa164-175">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa164-175">-Name</span></span>
<span data-ttu-id="aa164-176">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="aa164-176">The resource name.</span></span>

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

### <span data-ttu-id="aa164-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="aa164-177">-PeerWeight</span></span>
<span data-ttu-id="aa164-178">A peso adicionada às rotas aprendidas sobre bGP neste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="aa164-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="aa164-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="aa164-179">-RadiusServerAddress</span></span>
<span data-ttu-id="aa164-180">Endereço do servidor P2S External Radius.</span><span class="sxs-lookup"><span data-stu-id="aa164-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="aa164-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="aa164-181">-RadiusServerList</span></span>
<span data-ttu-id="aa164-182">Vários servidores externos de servidor Raio P2S.</span><span class="sxs-lookup"><span data-stu-id="aa164-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="aa164-183">-RadiusServerSecsec</span><span class="sxs-lookup"><span data-stu-id="aa164-183">-RadiusServerSecret</span></span>
<span data-ttu-id="aa164-184">Segredo do servidor P2S External Radius.</span><span class="sxs-lookup"><span data-stu-id="aa164-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="aa164-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa164-185">-ResourceGroupName</span></span>
<span data-ttu-id="aa164-186">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa164-186">The resource group name.</span></span>

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

### <span data-ttu-id="aa164-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa164-187">-Tag</span></span>
<span data-ttu-id="aa164-188">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="aa164-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="aa164-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="aa164-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="aa164-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="aa164-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="aa164-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="aa164-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="aa164-192">Uma lista de políticas IPSec para protocolos de túnel de cliente P2S VPN.</span><span class="sxs-lookup"><span data-stu-id="aa164-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="aa164-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="aa164-193">-VpnClientProtocol</span></span>
<span data-ttu-id="aa164-194">A lista de protocolos de túnel do cliente P2S VPN</span><span class="sxs-lookup"><span data-stu-id="aa164-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="aa164-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="aa164-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="aa164-196">A lista de VpnClientCertificates a ser revogada.</span><span class="sxs-lookup"><span data-stu-id="aa164-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="aa164-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="aa164-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="aa164-198">A lista de VpnClientRootCertificates a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="aa164-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="aa164-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="aa164-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="aa164-200">A geração desse gateway VPN virtualnetwork.</span><span class="sxs-lookup"><span data-stu-id="aa164-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="aa164-201">Deve ser Nenhum se GatewayType não for VPN.</span><span class="sxs-lookup"><span data-stu-id="aa164-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="aa164-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="aa164-202">-VpnType</span></span>
<span data-ttu-id="aa164-203">O tipo de Vpn:PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="aa164-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="aa164-204">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aa164-204">-Confirm</span></span>
<span data-ttu-id="aa164-205">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa164-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa164-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa164-206">-WhatIf</span></span>
<span data-ttu-id="aa164-207">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aa164-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa164-208">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa164-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa164-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa164-209">CommonParameters</span></span>
<span data-ttu-id="aa164-210">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa164-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa164-211">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa164-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa164-212">Entradas</span><span class="sxs-lookup"><span data-stu-id="aa164-212">INPUTS</span></span>

### <span data-ttu-id="aa164-213">System.String</span><span class="sxs-lookup"><span data-stu-id="aa164-213">System.String</span></span>

### <span data-ttu-id="aa164-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="aa164-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="aa164-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa164-215">System.Boolean</span></span>

### <span data-ttu-id="aa164-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aa164-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="aa164-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aa164-217">System.String[]</span></span>

### <span data-ttu-id="aa164-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="aa164-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="aa164-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="aa164-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="aa164-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="aa164-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="aa164-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="aa164-221">System.UInt32</span></span>

### <span data-ttu-id="aa164-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aa164-222">System.Int32</span></span>

### <span data-ttu-id="aa164-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="aa164-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="aa164-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aa164-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aa164-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="aa164-225">System.Security.SecureString</span></span>

## <span data-ttu-id="aa164-226">Saídas</span><span class="sxs-lookup"><span data-stu-id="aa164-226">OUTPUTS</span></span>

### <span data-ttu-id="aa164-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aa164-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="aa164-228">Notas</span><span class="sxs-lookup"><span data-stu-id="aa164-228">NOTES</span></span>

## <span data-ttu-id="aa164-229">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa164-229">RELATED LINKS</span></span>
