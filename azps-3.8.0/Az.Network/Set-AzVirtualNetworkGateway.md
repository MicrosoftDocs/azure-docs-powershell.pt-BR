---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: e5216d3a5727c32bd5e9f185cd48ace068a890b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940663"
---
# <span data-ttu-id="d6d56-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6d56-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d6d56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6d56-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d56-103">Atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6d56-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="d6d56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6d56-104">SYNTAX</span></span>

### <span data-ttu-id="d6d56-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6d56-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6d56-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6d56-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6d56-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="d6d56-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6d56-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6d56-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6d56-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="d6d56-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6d56-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6d56-110">DESCRIPTION</span></span>
<span data-ttu-id="d6d56-111">O cmdlet **set-AzVirtualNetworkGateway** atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6d56-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="d6d56-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6d56-112">EXAMPLES</span></span>

### <span data-ttu-id="d6d56-113">Exemplo 1: atualizar uma ASN do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6d56-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="d6d56-114">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual armazenado no $Gateway variável.</span><span class="sxs-lookup"><span data-stu-id="d6d56-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d6d56-115">O comando também define o ASN para o 1337.</span><span class="sxs-lookup"><span data-stu-id="d6d56-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="d6d56-116">Exemplo 2: adicionar a política IPsec a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6d56-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="d6d56-117">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando cria o objeto da política IPSec de VPN de acordo com os parâmetros de IPSec especificados.</span><span class="sxs-lookup"><span data-stu-id="d6d56-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="d6d56-118">O terceiro comando atualiza o gateway de rede virtual armazenado em variável $Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6d56-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d6d56-119">O comando também define a política IPSec VPN personalizada especificada no objeto $vpnclientipsecpolicy no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6d56-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="d6d56-120">Exemplo 3: Adicionar/atualizar marcas para um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="d6d56-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="d6d56-121">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual Gateway01 com as marcas @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="d6d56-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="d6d56-122">Exemplo 4: Adicionar/atualizar a configuração de autenticação do AAD para o VpnClient de um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="d6d56-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="d6d56-123">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual Gateway01 com os parâmetros de configuração de autenticação do AAD: aadTenantUri, aadAudienceId, aadIssuerUri para VpnClient.</span><span class="sxs-lookup"><span data-stu-id="d6d56-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="d6d56-124">O terceiro comando Remove a configuração de autenticação do AAD do VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6d56-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="d6d56-125">Exemplo 5: Adicionar/atualizar o IpConfigurationBgpPeeringAddresses a um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="d6d56-125">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="d6d56-126">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atribui o valor do gateway de rede virtual Gateway01 a ID da IpConfiguration à variável ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="d6d56-126">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="d6d56-127">O terceiro comando atribui a lista de endereços ao AddressList1.</span><span class="sxs-lookup"><span data-stu-id="d6d56-127">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="d6d56-128">O quarto comando criou um objeto PSIpConfigurationBgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="d6d56-128">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="d6d56-129">O quinto comando define esse novo PSIpConfigurationBgpPeeringAddress criado para IpConfigurationBgpPeeringAddresses e atualizar o gateway.</span><span class="sxs-lookup"><span data-stu-id="d6d56-129">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="d6d56-130">OS</span><span class="sxs-lookup"><span data-stu-id="d6d56-130">PARAMETERS</span></span>

### <span data-ttu-id="d6d56-131">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="d6d56-131">-AadAudienceId</span></span>
<span data-ttu-id="d6d56-132">Opção de autenticação AAD do P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="d6d56-132">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="d6d56-133">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="d6d56-133">-AadIssuerUri</span></span>
<span data-ttu-id="d6d56-134">Opção de autenticação AAD do P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="d6d56-134">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="d6d56-135">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="d6d56-135">-AadTenantUri</span></span>
<span data-ttu-id="d6d56-136">Opção de autenticação AAD do P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="d6d56-136">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="d6d56-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6d56-137">-AsJob</span></span>
<span data-ttu-id="d6d56-138">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d6d56-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6d56-139">-ASN</span><span class="sxs-lookup"><span data-stu-id="d6d56-139">-Asn</span></span>
<span data-ttu-id="d6d56-140">O ASN do gateway de rede virtual, usado para configurar sessões BGP dentro de túneis IPsec</span><span class="sxs-lookup"><span data-stu-id="d6d56-140">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="d6d56-141">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="d6d56-141">-CustomRoute</span></span>
<span data-ttu-id="d6d56-142">AddressPool de rotas personalizadas especificado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="d6d56-142">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="d6d56-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d56-143">-DefaultProfile</span></span>
<span data-ttu-id="d6d56-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d56-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6d56-145">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d6d56-145">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="d6d56-146">Sinalizar para desabilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6d56-146">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="d6d56-147">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d6d56-147">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="d6d56-148">Sinalizar para habilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6d56-148">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="d6d56-149">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6d56-149">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="d6d56-150">Sinalizar para habilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6d56-150">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6d56-151">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d6d56-151">-GatewayDefaultSite</span></span>
<span data-ttu-id="d6d56-152">O site padrão a ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="d6d56-152">The default site to use for force tunneling.</span></span>
<span data-ttu-id="d6d56-153">Se um site padrão for especificado, todo o tráfego da Internet da vnet do gateway será roteado para esse site.</span><span class="sxs-lookup"><span data-stu-id="d6d56-153">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="d6d56-154">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d6d56-154">-GatewaySku</span></span>
<span data-ttu-id="d6d56-155">O SKU do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6d56-155">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="d6d56-156">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="d6d56-156">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="d6d56-157">O BgpPeeringAddresses para o bgpsettings do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6d56-157">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="d6d56-158">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d6d56-158">-PeerWeight</span></span>
<span data-ttu-id="d6d56-159">A espessura adicionada a rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6d56-159">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="d6d56-160">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d6d56-160">-RadiusServerAddress</span></span>
<span data-ttu-id="d6d56-161">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="d6d56-161">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d56-162">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d6d56-162">-RadiusServerSecret</span></span>
<span data-ttu-id="d6d56-163">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="d6d56-163">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d56-164">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="d6d56-164">-RemoveAadAuthentication</span></span>
<span data-ttu-id="d6d56-165">Sinalizador para remover a autenticação AAD do cliente P2S do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6d56-165">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="d6d56-166">-Marca</span><span class="sxs-lookup"><span data-stu-id="d6d56-166">-Tag</span></span>
<span data-ttu-id="d6d56-167">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="d6d56-167">P2S External Radius server address.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6d56-168">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6d56-168">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d6d56-169">O objeto de gateway de rede virtual para basear as alterações a partir de.</span><span class="sxs-lookup"><span data-stu-id="d6d56-169">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="d6d56-170">Isso pode ser recuperado usando Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6d56-170">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d56-171">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d6d56-171">-VpnClientAddressPool</span></span>
<span data-ttu-id="d6d56-172">O espaço de endereço do qual os endereços IP do cliente VPN são alocados.</span><span class="sxs-lookup"><span data-stu-id="d6d56-172">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="d6d56-173">Isso não deve sobrepor a rede virtual ou intervalos locais.</span><span class="sxs-lookup"><span data-stu-id="d6d56-173">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="d6d56-174">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d6d56-174">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d6d56-175">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="d6d56-175">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d6d56-176">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d6d56-176">-VpnClientProtocol</span></span>
<span data-ttu-id="d6d56-177">Uma lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="d6d56-177">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="d6d56-178">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="d6d56-178">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="d6d56-179">Uma lista de certificados de cliente VPN revogados.</span><span class="sxs-lookup"><span data-stu-id="d6d56-179">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="d6d56-180">Um cliente VPN apresentando um certificado que corresponda a um deles será instruído a ficar ausente.</span><span class="sxs-lookup"><span data-stu-id="d6d56-180">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="d6d56-181">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d6d56-181">-VpnClientRootCertificates</span></span>
<span data-ttu-id="d6d56-182">Uma lista de certificados raiz de cliente VPN a serem usados para autenticação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="d6d56-182">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="d6d56-183">A conexão de clientes VPN deve apresentar certificados gerados a partir de um desses certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="d6d56-183">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="d6d56-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6d56-184">-Confirm</span></span>
<span data-ttu-id="d6d56-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6d56-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6d56-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6d56-186">-WhatIf</span></span>
<span data-ttu-id="d6d56-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6d56-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6d56-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6d56-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6d56-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d56-189">CommonParameters</span></span>
<span data-ttu-id="d6d56-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6d56-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d56-191">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6d56-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d56-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6d56-192">INPUTS</span></span>

### <span data-ttu-id="d6d56-193">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6d56-193">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d6d56-194">System. String</span><span class="sxs-lookup"><span data-stu-id="d6d56-194">System.String</span></span>

### <span data-ttu-id="d6d56-195">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6d56-195">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="d6d56-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="d6d56-196">System.String[]</span></span>

### <span data-ttu-id="d6d56-197">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="d6d56-197">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="d6d56-198">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="d6d56-198">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="d6d56-199">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d6d56-199">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d6d56-200">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="d6d56-200">System.UInt32</span></span>

### <span data-ttu-id="d6d56-201">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d6d56-201">System.Int32</span></span>

### <span data-ttu-id="d6d56-202">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="d6d56-202">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="d6d56-203">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d6d56-203">System.Security.SecureString</span></span>

## <span data-ttu-id="d6d56-204">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6d56-204">OUTPUTS</span></span>

### <span data-ttu-id="d6d56-205">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d6d56-205">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d6d56-206">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6d56-206">NOTES</span></span>

## <span data-ttu-id="d6d56-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6d56-207">RELATED LINKS</span></span>
