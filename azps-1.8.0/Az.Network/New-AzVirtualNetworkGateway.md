---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9b8ee02cbe28784ff1fd5789881dd62add62d674
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600261"
---
# <span data-ttu-id="0c70d-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="0c70d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c70d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c70d-103">Cria um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0c70d-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="0c70d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c70d-104">SYNTAX</span></span>

### <span data-ttu-id="0c70d-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="0c70d-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c70d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c70d-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c70d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c70d-107">DESCRIPTION</span></span>
<span data-ttu-id="0c70d-108">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="0c70d-108">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="0c70d-109">O cmdlet **New-AzVirtualNetworkGateway** cria o objeto do seu gateway no Azure com base no nome, nome do grupo de recursos, localização e configuração de IP, bem como o tipo de gateway e se VPN, o tipo de VPN.</span><span class="sxs-lookup"><span data-stu-id="0c70d-109">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="0c70d-110">Você também pode nomear o SKU do gateway.</span><span class="sxs-lookup"><span data-stu-id="0c70d-110">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="0c70d-111">Se esse gateway estiver sendo usado para conexões de ponto a site, você também precisará incluir o pool de endereços do cliente VPN do qual atribuir endereços para clientes de conexão e o certificado raiz do cliente VPN usado para autenticar clientes VPN que se conectam ao gateway.</span><span class="sxs-lookup"><span data-stu-id="0c70d-111">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="0c70d-112">Você também pode optar por incluir outros recursos como BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="0c70d-112">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="0c70d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c70d-113">EXAMPLES</span></span>

### <span data-ttu-id="0c70d-114">1: criar um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0c70d-114">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="0c70d-115">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="0c70d-115">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0c70d-116">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="0c70d-116">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="0c70d-117">2: criar um gateway de rede virtual com configuração RADIUS externa</span><span class="sxs-lookup"><span data-stu-id="0c70d-117">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="0c70d-118">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="0c70d-118">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="0c70d-119">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="0c70d-119">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="0c70d-120">Ele também adiciona um servidor RADIUS externo com o endereço "TestRadiusServer"</span><span class="sxs-lookup"><span data-stu-id="0c70d-120">It also adds an external radius server with address "TestRadiusServer"</span></span>

### <span data-ttu-id="0c70d-121">1: criar um gateway de rede virtual com configurações do P2S</span><span class="sxs-lookup"><span data-stu-id="0c70d-121">1: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="0c70d-122">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway de rede virtual com as configurações do P2S, por exemplo, VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy etc. no Azure.</span><span class="sxs-lookup"><span data-stu-id="0c70d-122">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="0c70d-123">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="0c70d-123">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="0c70d-124">As configurações de VPN serão definidas no gateway como VpnProtocol definido como Ikev2, VpnClientAddressPool como "201.169.0.0/16", VpnClientRootCertificate definido como aprovado: clientRootCertName e a política IPSec VPN personalizada passada no objeto: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="0c70d-124">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  

## <span data-ttu-id="0c70d-125">OS</span><span class="sxs-lookup"><span data-stu-id="0c70d-125">PARAMETERS</span></span>

### <span data-ttu-id="0c70d-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c70d-126">-AsJob</span></span>
<span data-ttu-id="0c70d-127">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0c70d-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c70d-128">-ASN</span><span class="sxs-lookup"><span data-stu-id="0c70d-128">-Asn</span></span>

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

### <span data-ttu-id="0c70d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c70d-129">-DefaultProfile</span></span>
<span data-ttu-id="0c70d-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c70d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c70d-131">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="0c70d-131">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="0c70d-132">Habilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="0c70d-132">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="0c70d-133">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="0c70d-133">-EnableBgp</span></span>

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

### <span data-ttu-id="0c70d-134">-Force</span><span class="sxs-lookup"><span data-stu-id="0c70d-134">-Force</span></span>
<span data-ttu-id="0c70d-135">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0c70d-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c70d-136">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0c70d-136">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="0c70d-137">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="0c70d-137">-GatewaySku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c70d-138">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="0c70d-138">-GatewayType</span></span>

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

### <span data-ttu-id="0c70d-139">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="0c70d-139">-IpConfigurations</span></span>

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

### <span data-ttu-id="0c70d-140">-Local</span><span class="sxs-lookup"><span data-stu-id="0c70d-140">-Location</span></span>

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

### <span data-ttu-id="0c70d-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c70d-141">-Name</span></span>

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

### <span data-ttu-id="0c70d-142">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="0c70d-142">-PeerWeight</span></span>

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

### <span data-ttu-id="0c70d-143">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="0c70d-143">-RadiusServerAddress</span></span>
<span data-ttu-id="0c70d-144">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="0c70d-144">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="0c70d-145">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="0c70d-145">-RadiusServerSecret</span></span>
<span data-ttu-id="0c70d-146">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="0c70d-146">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="0c70d-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c70d-147">-ResourceGroupName</span></span>

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

### <span data-ttu-id="0c70d-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="0c70d-148">-Tag</span></span>
<span data-ttu-id="0c70d-149">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0c70d-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c70d-150">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0c70d-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0c70d-151">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="0c70d-151">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="0c70d-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="0c70d-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="0c70d-153">Uma lista de diretivas IPSec para protocolos de encapsulamento de cliente VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="0c70d-153">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="0c70d-154">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="0c70d-154">-VpnClientProtocol</span></span>
<span data-ttu-id="0c70d-155">A lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="0c70d-155">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="0c70d-156">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="0c70d-156">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="0c70d-157">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="0c70d-157">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="0c70d-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="0c70d-158">-VpnType</span></span>

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

### <span data-ttu-id="0c70d-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0c70d-159">-Confirm</span></span>
<span data-ttu-id="0c70d-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c70d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c70d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c70d-161">-WhatIf</span></span>
<span data-ttu-id="0c70d-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c70d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c70d-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c70d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c70d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c70d-164">CommonParameters</span></span>
<span data-ttu-id="0c70d-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c70d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c70d-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c70d-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c70d-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c70d-167">INPUTS</span></span>

### <span data-ttu-id="0c70d-168">System. String</span><span class="sxs-lookup"><span data-stu-id="0c70d-168">System.String</span></span>

### <span data-ttu-id="0c70d-169">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="0c70d-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="0c70d-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c70d-170">System.Boolean</span></span>

### <span data-ttu-id="0c70d-171">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-171">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="0c70d-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="0c70d-172">System.String[]</span></span>

### <span data-ttu-id="0c70d-173">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="0c70d-173">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="0c70d-174">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="0c70d-174">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="0c70d-175">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="0c70d-175">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="0c70d-176">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="0c70d-176">System.UInt32</span></span>

### <span data-ttu-id="0c70d-177">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0c70d-177">System.Int32</span></span>

### <span data-ttu-id="0c70d-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0c70d-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0c70d-179">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0c70d-179">System.Security.SecureString</span></span>

## <span data-ttu-id="0c70d-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c70d-180">OUTPUTS</span></span>

### <span data-ttu-id="0c70d-181">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0c70d-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c70d-182">NOTES</span></span>

## <span data-ttu-id="0c70d-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c70d-183">RELATED LINKS</span></span>

[<span data-ttu-id="0c70d-184">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-184">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0c70d-185">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-185">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0c70d-186">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-186">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0c70d-187">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-187">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0c70d-188">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0c70d-188">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
