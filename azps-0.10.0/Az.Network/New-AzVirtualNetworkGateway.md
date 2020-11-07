---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: a19cc1484a00b60eb27723621e05aa67634e8732
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775352"
---
# <span data-ttu-id="0f131-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f131-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="0f131-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f131-102">SYNOPSIS</span></span>
<span data-ttu-id="0f131-103">Cria um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0f131-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="0f131-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f131-104">SYNTAX</span></span>

### <span data-ttu-id="0f131-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="0f131-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f131-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f131-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f131-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0f131-107">SetByResource</span></span>
```
New-AzVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f131-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f131-108">DESCRIPTION</span></span>
<span data-ttu-id="0f131-109">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="0f131-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="0f131-110">O cmdlet **New-AzVirtualNetworkGateway** cria o objeto do seu gateway no Azure com base no nome, nome do grupo de recursos, localização e configuração de IP, bem como o tipo de gateway e se VPN, o tipo de VPN.</span><span class="sxs-lookup"><span data-stu-id="0f131-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="0f131-111">Você também pode nomear o SKU do gateway.</span><span class="sxs-lookup"><span data-stu-id="0f131-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="0f131-112">Se esse gateway estiver sendo usado para conexões de ponto a site, você também precisará incluir o pool de endereços do cliente VPN do qual atribuir endereços para clientes de conexão e o certificado raiz do cliente VPN usado para autenticar clientes VPN que se conectam ao gateway.</span><span class="sxs-lookup"><span data-stu-id="0f131-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="0f131-113">Você também pode optar por incluir outros recursos como BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="0f131-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="0f131-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f131-114">EXAMPLES</span></span>

### <span data-ttu-id="0f131-115">1: criar um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="0f131-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="0f131-116">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="0f131-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="0f131-117">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="0f131-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="0f131-118">2: criar um gateway de rede virtual com configuração RADIUS externa</span><span class="sxs-lookup"><span data-stu-id="0f131-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="0f131-119">A seguir, você criará um grupo de recursos, solicitará um endereço IP público, criará uma rede virtual e uma sub-rede e criará um gateway virtual de rede no Azure.</span><span class="sxs-lookup"><span data-stu-id="0f131-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="0f131-120">O gateway será chamado de "myNGW" no grupo de recursos "vnet-gateway" no local "Reino Unido" com as configurações de IP criadas anteriormente salvas na variável "ngwIPConfig", o tipo de gateway de "VPN", o tipo de VPN "RouteBased" e a SKU "básica".</span><span class="sxs-lookup"><span data-stu-id="0f131-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="0f131-121">Ele também adiciona um servidor RADIUS externo com o endereço "TestRadiusServer"</span><span class="sxs-lookup"><span data-stu-id="0f131-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="0f131-122">OS</span><span class="sxs-lookup"><span data-stu-id="0f131-122">PARAMETERS</span></span>

### <span data-ttu-id="0f131-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f131-123">-AsJob</span></span>
<span data-ttu-id="0f131-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f131-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f131-125">-ASN</span><span class="sxs-lookup"><span data-stu-id="0f131-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f131-126">-DefaultProfile</span></span>
<span data-ttu-id="0f131-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f131-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="0f131-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="0f131-129">Habilita o recurso ativo-ativo.</span><span class="sxs-lookup"><span data-stu-id="0f131-129">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="0f131-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="0f131-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-131">-Force</span><span class="sxs-lookup"><span data-stu-id="0f131-131">-Force</span></span>
<span data-ttu-id="0f131-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0f131-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f131-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="0f131-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="0f131-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-135">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="0f131-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="0f131-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-137">-Local</span><span class="sxs-lookup"><span data-stu-id="0f131-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f131-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="0f131-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="0f131-140">-RadiusServerAddress</span></span>
<span data-ttu-id="0f131-141">P2S endereço do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="0f131-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="0f131-142">-RadiusServerSecret</span></span>
<span data-ttu-id="0f131-143">P2S segredo do servidor RADIUS externo.</span><span class="sxs-lookup"><span data-stu-id="0f131-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f131-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="0f131-145">-Tag</span></span>
<span data-ttu-id="0f131-146">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0f131-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0f131-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0f131-147">For example:</span></span>

<span data-ttu-id="0f131-148">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0f131-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0f131-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="0f131-149">-VpnClientAddressPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="0f131-150">-VpnClientProtocol</span></span>
<span data-ttu-id="0f131-151">A lista de protocolos de encapsulamento de cliente VPN P2S</span><span class="sxs-lookup"><span data-stu-id="0f131-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="0f131-152">-VpnClientRevokedCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="0f131-153">-VpnClientRootCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="0f131-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f131-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f131-155">-Confirm</span></span>
<span data-ttu-id="0f131-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f131-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f131-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f131-157">-WhatIf</span></span>
<span data-ttu-id="0f131-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f131-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f131-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f131-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f131-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f131-160">CommonParameters</span></span>
<span data-ttu-id="0f131-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f131-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f131-162">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f131-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f131-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f131-163">INPUTS</span></span>

## <span data-ttu-id="0f131-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f131-164">OUTPUTS</span></span>

### <span data-ttu-id="0f131-165">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f131-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0f131-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f131-166">NOTES</span></span>

## <span data-ttu-id="0f131-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f131-167">RELATED LINKS</span></span>

[<span data-ttu-id="0f131-168">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f131-168">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f131-169">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f131-169">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f131-170">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f131-170">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f131-171">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f131-171">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0f131-172">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0f131-172">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
