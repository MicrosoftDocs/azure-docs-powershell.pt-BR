---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111701"
---
# <span data-ttu-id="16e46-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="16e46-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="16e46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16e46-102">SYNOPSIS</span></span>
<span data-ttu-id="16e46-103">Adiciona uma configuração IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="16e46-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="16e46-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16e46-104">SYNTAX</span></span>

### <span data-ttu-id="16e46-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="16e46-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16e46-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="16e46-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16e46-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="16e46-107">DESCRIPTION</span></span>
<span data-ttu-id="16e46-108">O **cmdlet Add-AzVirtualNetworkGatewayIpConfig** adiciona uma configuração IP a um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="16e46-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="16e46-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16e46-109">EXAMPLES</span></span>

### <span data-ttu-id="16e46-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16e46-110">Example 1</span></span>
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

## <span data-ttu-id="16e46-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16e46-111">PARAMETERS</span></span>

### <span data-ttu-id="16e46-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e46-112">-DefaultProfile</span></span>
<span data-ttu-id="16e46-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="16e46-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e46-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="16e46-114">-Name</span></span>
<span data-ttu-id="16e46-115">Especifica o nome da configuração IP do gateway a ser adicionar.</span><span class="sxs-lookup"><span data-stu-id="16e46-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="16e46-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="16e46-116">-PrivateIpAddress</span></span>
<span data-ttu-id="16e46-117">Especifica o endereço IP particular.</span><span class="sxs-lookup"><span data-stu-id="16e46-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="16e46-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="16e46-118">-PublicIpAddress</span></span>
<span data-ttu-id="16e46-119">Especifica o endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="16e46-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="16e46-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="16e46-120">-PublicIpAddressId</span></span>
<span data-ttu-id="16e46-121">Especifica a ID do endereço IP público.</span><span class="sxs-lookup"><span data-stu-id="16e46-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="16e46-122">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="16e46-122">-Subnet</span></span>
<span data-ttu-id="16e46-123">Especifica um **objeto PSSubnet.**</span><span class="sxs-lookup"><span data-stu-id="16e46-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="16e46-124">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="16e46-124">-SubnetId</span></span>
<span data-ttu-id="16e46-125">Especifica a ID da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="16e46-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="16e46-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="16e46-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="16e46-127">Especifica um **objeto PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="16e46-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="16e46-128">Esse cmdlet modifica o **objeto PSVirtualNetworkGateway** especificado por você.</span><span class="sxs-lookup"><span data-stu-id="16e46-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="16e46-129">Você pode usar o cmdlet Get-AzVirtualNetworkGateway para recuperar um objeto **PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="16e46-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="16e46-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16e46-130">-Confirm</span></span>
<span data-ttu-id="16e46-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e46-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e46-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e46-132">-WhatIf</span></span>
<span data-ttu-id="16e46-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16e46-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e46-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16e46-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e46-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e46-135">CommonParameters</span></span>
<span data-ttu-id="16e46-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e46-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e46-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e46-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e46-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="16e46-138">INPUTS</span></span>

### <span data-ttu-id="16e46-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="16e46-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="16e46-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="16e46-140">OUTPUTS</span></span>

### <span data-ttu-id="16e46-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="16e46-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="16e46-142">Notas</span><span class="sxs-lookup"><span data-stu-id="16e46-142">NOTES</span></span>

## <span data-ttu-id="16e46-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16e46-143">RELATED LINKS</span></span>

[<span data-ttu-id="16e46-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="16e46-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="16e46-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="16e46-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="16e46-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="16e46-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
