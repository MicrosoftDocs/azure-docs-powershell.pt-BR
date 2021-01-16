---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272595"
---
# <span data-ttu-id="c4c3d-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c3d-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c4c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c3d-103">Atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="c4c3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4c3d-104">SYNTAX</span></span>

### <span data-ttu-id="c4c3d-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4c3d-105">Default (Default)</span></span>
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

### <span data-ttu-id="c4c3d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4c3d-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="c4c3d-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="c4c3d-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
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

### <span data-ttu-id="c4c3d-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4c3d-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c3d-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4c3d-109">AadAuthenticationConfiguration</span></span>
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

### <span data-ttu-id="c4c3d-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="c4c3d-110">UpdateResourceWithTags</span></span>
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

## <span data-ttu-id="c4c3d-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4c3d-111">DESCRIPTION</span></span>
<span data-ttu-id="c4c3d-112">O cmdlet **set-AzVirtualNetworkGateway** atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="c4c3d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4c3d-113">EXAMPLES</span></span>

### <span data-ttu-id="c4c3d-114">Exemplo 1: atualizar uma ASN do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4c3d-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="c4c3d-115">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual armazenado no $Gateway variável.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c4c3d-116">O comando também define o ASN para o 1337.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="c4c3d-117">Exemplo 2: adicionar a política IPsec a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4c3d-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="c4c3d-118">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando cria o objeto da política IPSec de VPN de acordo com os parâmetros de IPSec especificados.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="c4c3d-119">O terceiro comando atualiza o gateway de rede virtual armazenado em variável $Gateway.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c4c3d-120">O comando também define a política IPSec VPN personalizada especificada no objeto $vpnclientipsecpolicy no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="c4c3d-121">Exemplo 3: Adicionar/atualizar marcas para um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="c4c3d-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="c4c3d-122">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual Gateway01 com as marcas @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="c4c3d-123">Exemplo 4: Adicionar/atualizar a configuração de autenticação do AAD para o VpnClient de um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="c4c3d-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="c4c3d-124">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual Gateway01 com os parâmetros de configuração de autenticação do AAD: aadTenantUri, aadAudienceId, aadIssuerUri para VpnClient.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="c4c3d-125">O terceiro comando Remove a configuração de autenticação do AAD do VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="c4c3d-126">Exemplo 5: Adicionar/atualizar o IpConfigurationBgpPeeringAddresses a um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="c4c3d-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
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

<span data-ttu-id="c4c3d-127">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atribui o valor do gateway de rede virtual Gateway01 a ID da IpConfiguration à variável ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="c4c3d-128">O terceiro comando atribui a lista de endereços ao AddressList1.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="c4c3d-129">O quarto comando criou um objeto PSIpConfigurationBgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="c4c3d-130">O quinto comando define esse novo PSIpConfigurationBgpPeeringAddress criado para IpConfigurationBgpPeeringAddresses e atualizar o gateway.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="c4c3d-131">OS</span><span class="sxs-lookup"><span data-stu-id="c4c3d-131">PARAMETERS</span></span>

### <span data-ttu-id="c4c3d-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="c4c3d-132">-AadAudienceId</span></span>
<span data-ttu-id="c4c3d-133">Opção de autenticação AAD do P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="c4c3d-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="c4c3d-134">-AadIssuerUri</span></span>
<span data-ttu-id="c4c3d-135">Opção de autenticação AAD do P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="c4c3d-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="c4c3d-136">-AadTenantUri</span></span>
<span data-ttu-id="c4c3d-137">Opção de autenticação AAD do P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="c4c3d-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4c3d-138">-AsJob</span></span>
<span data-ttu-id="c4c3d-139">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c4c3d-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4c3d-140">-ASN</span><span class="sxs-lookup"><span data-stu-id="c4c3d-140">-Asn</span></span>
<span data-ttu-id="c4c3d-141">O ASN do gateway de rede virtual, usado para configurar sessões BGP dentro de túneis IPsec</span><span class="sxs-lookup"><span data-stu-id="c4c3d-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="c4c3d-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="c4c3d-142">-CustomRoute</span></span>
<span data-ttu-id="c4c3d-143">AddressPool de rotas personalizadas especificado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="c4c3d-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="c4c3d-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c3d-144">-DefaultProfile</span></span>
<span data-ttu-id="c4c3d-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c3d-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c4c3d-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="c4c3d-147">Sinalizar para desabilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4c3d-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="c4c3d-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c4c3d-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="c4c3d-149">Sinalizar para habilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4c3d-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="c4c3d-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4c3d-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="c4c3d-151">Sinalizar para habilitar o recurso ativo ativo no gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4c3d-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="c4c3d-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c4c3d-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="c4c3d-153">O site padrão a ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="c4c3d-154">Se um site padrão for especificado, todo o tráfego da Internet da vnet do gateway será roteado para esse site.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="c4c3d-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c4c3d-155">-GatewaySku</span></span>
<span data-ttu-id="c4c3d-156">O SKU do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4c3d-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="c4c3d-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="c4c3d-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="c4c3d-158">O BgpPeeringAddresses para o bgpsettings do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="c4c3d-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c4c3d-159">-PeerWeight</span></span>
<span data-ttu-id="c4c3d-160">A espessura adicionada a rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c4c3d-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="c4c3d-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c4c3d-161">-RadiusServerAddress</span></span>
<span data-ttu-id="c4c3d-162">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="c4c3d-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="c4c3d-163">-RadiusServerList</span></span>
<span data-ttu-id="c4c3d-164">P2S vários servidores RADIUS externos.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="c4c3d-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c4c3d-165">-RadiusServerSecret</span></span>
<span data-ttu-id="c4c3d-166">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="c4c3d-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="c4c3d-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="c4c3d-168">Sinalizador para remover a autenticação AAD do cliente P2S do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="c4c3d-169">-Marca</span><span class="sxs-lookup"><span data-stu-id="c4c3d-169">-Tag</span></span>
<span data-ttu-id="c4c3d-170">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="c4c3d-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c3d-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c4c3d-172">O objeto de gateway de rede virtual para basear as alterações a partir de.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="c4c3d-173">Isso pode ser recuperado usando Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c3d-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="c4c3d-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="c4c3d-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="c4c3d-175">O espaço de endereço do qual os endereços IP do cliente VPN são alocados.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="c4c3d-176">Isso não deve sobrepor a rede virtual ou intervalos locais.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="c4c3d-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c4c3d-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c4c3d-178">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c4c3d-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c4c3d-179">-VpnClientProtocol</span></span>
<span data-ttu-id="c4c3d-180">Uma lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="c4c3d-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="c4c3d-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="c4c3d-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="c4c3d-182">Uma lista de certificados de cliente VPN revogados.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="c4c3d-183">Um cliente VPN apresentando um certificado que corresponda a um deles será instruído a ficar ausente.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="c4c3d-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="c4c3d-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="c4c3d-185">Uma lista de certificados raiz de cliente VPN a serem usados para autenticação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="c4c3d-186">A conexão de clientes VPN deve apresentar certificados gerados a partir de um desses certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="c4c3d-187">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4c3d-187">-Confirm</span></span>
<span data-ttu-id="c4c3d-188">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c3d-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c3d-189">-WhatIf</span></span>
<span data-ttu-id="c4c3d-190">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c3d-191">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c3d-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c3d-192">CommonParameters</span></span>
<span data-ttu-id="c4c3d-193">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c3d-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c3d-194">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4c3d-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c3d-195">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4c3d-195">INPUTS</span></span>

### <span data-ttu-id="c4c3d-196">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c3d-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="c4c3d-197">System. String</span><span class="sxs-lookup"><span data-stu-id="c4c3d-197">System.String</span></span>

### <span data-ttu-id="c4c3d-198">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c3d-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="c4c3d-199">System. String []</span><span class="sxs-lookup"><span data-stu-id="c4c3d-199">System.String[]</span></span>

### <span data-ttu-id="c4c3d-200">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="c4c3d-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="c4c3d-201">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="c4c3d-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="c4c3d-202">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="c4c3d-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="c4c3d-203">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="c4c3d-203">System.UInt32</span></span>

### <span data-ttu-id="c4c3d-204">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c4c3d-204">System.Int32</span></span>

### <span data-ttu-id="c4c3d-205">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="c4c3d-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="c4c3d-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c4c3d-206">System.Security.SecureString</span></span>

## <span data-ttu-id="c4c3d-207">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4c3d-207">OUTPUTS</span></span>

### <span data-ttu-id="c4c3d-208">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c4c3d-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c4c3d-209">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4c3d-209">NOTES</span></span>

## <span data-ttu-id="c4c3d-210">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4c3d-210">RELATED LINKS</span></span>
