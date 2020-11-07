---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772737"
---
# <span data-ttu-id="d7648-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d7648-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7648-102">SYNOPSIS</span></span>
<span data-ttu-id="d7648-103">Atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7648-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="d7648-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7648-104">SYNTAX</span></span>

### <span data-ttu-id="d7648-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7648-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7648-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7648-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7648-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="d7648-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7648-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7648-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7648-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="d7648-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7648-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7648-110">DESCRIPTION</span></span>
<span data-ttu-id="d7648-111">O cmdlet **set-AzVirtualNetworkGateway** atualiza um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7648-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="d7648-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7648-112">EXAMPLES</span></span>

### <span data-ttu-id="d7648-113">Exemplo 1: atualizar uma ASN do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d7648-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="d7648-114">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual armazenado no $Gateway variável.</span><span class="sxs-lookup"><span data-stu-id="d7648-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d7648-115">O comando também define o ASN para o 1337.</span><span class="sxs-lookup"><span data-stu-id="d7648-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="d7648-116">Exemplo 2: adicionar a política IPsec a um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d7648-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="d7648-117">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando cria o objeto da política IPSec de VPN de acordo com os parâmetros de IPSec especificados.</span><span class="sxs-lookup"><span data-stu-id="d7648-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="d7648-118">O terceiro comando atualiza o gateway de rede virtual armazenado em variável $Gateway.</span><span class="sxs-lookup"><span data-stu-id="d7648-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d7648-119">O comando também define a política IPSec VPN personalizada especificada no objeto $vpnclientipsecpolicy no gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7648-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="d7648-120">Exemplo 3: Adicionar/atualizar marcas para um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="d7648-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="d7648-121">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual Gateway01 com as marcas @ {testtagKey = "SomeTagKey"; testtagValue = "SomeKeyValue"}.</span><span class="sxs-lookup"><span data-stu-id="d7648-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="d7648-122">Exemplo 4: Adicionar/atualizar a configuração de autenticação do AAD para o VpnClient de um gateway de rede virtual existente</span><span class="sxs-lookup"><span data-stu-id="d7648-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="d7648-123">O primeiro comando obtém um gateway de rede virtual chamado Gateway01 que pertence à ResourceGroup001 do grupo de recursos e o armazena na variável chamada $Gateway o segundo comando atualiza o gateway de rede virtual Gateway01 com os parâmetros de configuração de autenticação do AAD: aadTenantUri, aadAudienceId, aadIssuerUri para VpnClient.</span><span class="sxs-lookup"><span data-stu-id="d7648-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="d7648-124">O terceiro comando Remove a configuração de autenticação do AAD do VpnClient do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7648-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="d7648-125">OS</span><span class="sxs-lookup"><span data-stu-id="d7648-125">PARAMETERS</span></span>

### <span data-ttu-id="d7648-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="d7648-126">-AadAudienceId</span></span>
<span data-ttu-id="d7648-127">Opção de autenticação AAD do P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="d7648-127">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="d7648-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="d7648-128">-AadIssuerUri</span></span>
<span data-ttu-id="d7648-129">Opção de autenticação AAD do P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="d7648-129">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="d7648-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="d7648-130">-AadTenantUri</span></span>
<span data-ttu-id="d7648-131">Opção de autenticação AAD do P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="d7648-131">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="d7648-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7648-132">-AsJob</span></span>
<span data-ttu-id="d7648-133">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7648-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7648-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="d7648-134">-Asn</span></span>
<span data-ttu-id="d7648-135">Especifica o número de sistema autônomo do gateway de rede virtual (ASN) que é usado para configurar sessões do BGP (Border Gateway Protocol) dentro de túneis IPsec.</span><span class="sxs-lookup"><span data-stu-id="d7648-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="d7648-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="d7648-136">-CustomRoute</span></span>
<span data-ttu-id="d7648-137">AddressPool de rotas personalizadas especificado pelo cliente</span><span class="sxs-lookup"><span data-stu-id="d7648-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="d7648-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7648-138">-DefaultProfile</span></span>
<span data-ttu-id="d7648-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7648-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7648-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d7648-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="d7648-141">Desabilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="d7648-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="d7648-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d7648-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="d7648-143">Habilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="d7648-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="d7648-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d7648-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="d7648-145">Especifica o site padrão a ser usado para o tunelamento forçado.</span><span class="sxs-lookup"><span data-stu-id="d7648-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="d7648-146">Se um site padrão for especificado, todo o tráfego da Internet da VPN (rede virtual privada) do gateway será roteado para esse site.</span><span class="sxs-lookup"><span data-stu-id="d7648-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="d7648-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d7648-147">-GatewaySku</span></span>
<span data-ttu-id="d7648-148">Especifica a SKU (unidade de manutenção de estoque) do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7648-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="d7648-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d7648-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7648-150">Basic</span><span class="sxs-lookup"><span data-stu-id="d7648-150">Basic</span></span>
- <span data-ttu-id="d7648-151">Oficial</span><span class="sxs-lookup"><span data-stu-id="d7648-151">Standard</span></span>
- <span data-ttu-id="d7648-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="d7648-152">HighPerformance</span></span>
- <span data-ttu-id="d7648-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="d7648-153">VpnGw1</span></span>
- <span data-ttu-id="d7648-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="d7648-154">VpnGw2</span></span>
- <span data-ttu-id="d7648-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="d7648-155">VpnGw3</span></span>
- <span data-ttu-id="d7648-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d7648-156">VpnGw1AZ</span></span>
- <span data-ttu-id="d7648-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d7648-157">VpnGw2AZ</span></span>
- <span data-ttu-id="d7648-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d7648-158">VpnGw3AZ</span></span>
- <span data-ttu-id="d7648-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d7648-159">ErGw1AZ</span></span>
- <span data-ttu-id="d7648-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d7648-160">ErGw2AZ</span></span>
- <span data-ttu-id="d7648-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d7648-161">ErGw3AZ</span></span>

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

### <span data-ttu-id="d7648-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d7648-162">-PeerWeight</span></span>
<span data-ttu-id="d7648-163">Especifica a espessura adicionada às rotas aprendidas em BGP deste gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d7648-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="d7648-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d7648-164">-RadiusServerAddress</span></span>
<span data-ttu-id="d7648-165">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="d7648-165">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="d7648-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d7648-166">-RadiusServerSecret</span></span>
<span data-ttu-id="d7648-167">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="d7648-167">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="d7648-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="d7648-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="d7648-169">Sinalizador para remover a autenticação AAD do cliente P2S do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7648-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="d7648-170">-Marca</span><span class="sxs-lookup"><span data-stu-id="d7648-170">-Tag</span></span>
<span data-ttu-id="d7648-171">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7648-171">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d7648-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d7648-173">Especifica o objeto de gateway de rede virtual para basear as modificações de.</span><span class="sxs-lookup"><span data-stu-id="d7648-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="d7648-174">Você pode usar o cmdlet Get-AzVirtualNetworkGateway para obter o objeto do gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d7648-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="d7648-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d7648-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="d7648-176">Especifica o espaço de endereço que esse cmdlet usa para atribuir endereços IP do cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="d7648-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="d7648-177">Isso não deve sobrepor a rede virtual ou intervalos locais.</span><span class="sxs-lookup"><span data-stu-id="d7648-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="d7648-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d7648-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d7648-179">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="d7648-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d7648-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d7648-180">-VpnClientProtocol</span></span>
<span data-ttu-id="d7648-181">Uma lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="d7648-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="d7648-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="d7648-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="d7648-183">Especifica uma lista de certificados de cliente VPN revogados.</span><span class="sxs-lookup"><span data-stu-id="d7648-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="d7648-184">Um cliente VPN apresentando um certificado que corresponda a um deles é removido.</span><span class="sxs-lookup"><span data-stu-id="d7648-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="d7648-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d7648-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="d7648-186">Especifica uma lista de certificados raiz de cliente VPN a serem usados para autenticação de cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="d7648-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="d7648-187">A conexão de clientes VPN deve apresentar certificados gerados a partir de um desses certificados raiz.</span><span class="sxs-lookup"><span data-stu-id="d7648-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="d7648-188">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7648-188">-Confirm</span></span>
<span data-ttu-id="d7648-189">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7648-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7648-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7648-190">-WhatIf</span></span>
<span data-ttu-id="d7648-191">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7648-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7648-192">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7648-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7648-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7648-193">CommonParameters</span></span>
<span data-ttu-id="d7648-194">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7648-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7648-195">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7648-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7648-196">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7648-196">INPUTS</span></span>

### <span data-ttu-id="d7648-197">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d7648-198">System. String</span><span class="sxs-lookup"><span data-stu-id="d7648-198">System.String</span></span>

### <span data-ttu-id="d7648-199">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="d7648-200">System. String []</span><span class="sxs-lookup"><span data-stu-id="d7648-200">System.String[]</span></span>

### <span data-ttu-id="d7648-201">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="d7648-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="d7648-202">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="d7648-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="d7648-203">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d7648-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d7648-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="d7648-204">System.UInt32</span></span>

### <span data-ttu-id="d7648-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d7648-205">System.Int32</span></span>

### <span data-ttu-id="d7648-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d7648-206">System.Security.SecureString</span></span>

## <span data-ttu-id="d7648-207">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7648-207">OUTPUTS</span></span>

### <span data-ttu-id="d7648-208">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d7648-209">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7648-209">NOTES</span></span>
* <span data-ttu-id="d7648-210">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="d7648-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d7648-211">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7648-211">RELATED LINKS</span></span>

[<span data-ttu-id="d7648-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d7648-213">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d7648-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d7648-215">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d7648-216">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d7648-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
