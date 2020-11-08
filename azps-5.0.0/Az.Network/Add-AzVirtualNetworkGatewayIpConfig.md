---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125956"
---
# <span data-ttu-id="0618b-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0618b-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="0618b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0618b-102">SYNOPSIS</span></span>
<span data-ttu-id="0618b-103">Adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0618b-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="0618b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0618b-104">SYNTAX</span></span>

### <span data-ttu-id="0618b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0618b-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0618b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0618b-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0618b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0618b-107">DESCRIPTION</span></span>
<span data-ttu-id="0618b-108">O cmdlet **Add-AzVirtualNetworkGatewayIpConfig** adiciona uma configuração de IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0618b-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="0618b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0618b-109">EXAMPLES</span></span>

### <span data-ttu-id="0618b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0618b-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="0618b-111">OS</span><span class="sxs-lookup"><span data-stu-id="0618b-111">PARAMETERS</span></span>

### <span data-ttu-id="0618b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0618b-112">-DefaultProfile</span></span>
<span data-ttu-id="0618b-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0618b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0618b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0618b-114">-Name</span></span>
<span data-ttu-id="0618b-115">Especifica o nome da configuração de IP do gateway a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="0618b-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0618b-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="0618b-116">-PrivateIpAddress</span></span>
<span data-ttu-id="0618b-117">Especifica o endereço IP privado.</span><span class="sxs-lookup"><span data-stu-id="0618b-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="0618b-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0618b-118">-PublicIpAddress</span></span>
<span data-ttu-id="0618b-119">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="0618b-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0618b-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="0618b-120">-PublicIpAddressId</span></span>
<span data-ttu-id="0618b-121">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="0618b-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0618b-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="0618b-122">-Subnet</span></span>
<span data-ttu-id="0618b-123">Especifica um objeto **PSSubnet** .</span><span class="sxs-lookup"><span data-stu-id="0618b-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0618b-124">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="0618b-124">-SubnetId</span></span>
<span data-ttu-id="0618b-125">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="0618b-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0618b-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0618b-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="0618b-127">Especifica um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="0618b-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="0618b-128">Esse cmdlet modifica o objeto **PSVirtualNetworkGateway** que você especificar.</span><span class="sxs-lookup"><span data-stu-id="0618b-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="0618b-129">Você pode usar o cmdlet Get-AzVirtualNetworkGateway para recuperar um objeto **PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="0618b-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="0618b-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0618b-130">-Confirm</span></span>
<span data-ttu-id="0618b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0618b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0618b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0618b-132">-WhatIf</span></span>
<span data-ttu-id="0618b-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0618b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0618b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0618b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0618b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0618b-135">CommonParameters</span></span>
<span data-ttu-id="0618b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0618b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0618b-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0618b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0618b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0618b-138">INPUTS</span></span>

### <span data-ttu-id="0618b-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0618b-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0618b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0618b-140">OUTPUTS</span></span>

### <span data-ttu-id="0618b-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0618b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0618b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0618b-142">NOTES</span></span>

## <span data-ttu-id="0618b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0618b-143">RELATED LINKS</span></span>

[<span data-ttu-id="0618b-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0618b-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="0618b-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0618b-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="0618b-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0618b-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
