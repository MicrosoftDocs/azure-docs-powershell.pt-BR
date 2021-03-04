---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d8f77ffd6353ef55548e8ddc2a2cc4f823efe98d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892400"
---
# <span data-ttu-id="b16a3-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16a3-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="b16a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b16a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b16a3-103">Remove uma configuração IP de um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="b16a3-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="b16a3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b16a3-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b16a3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b16a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b16a3-106">Remove uma configuração IP de um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="b16a3-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="b16a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b16a3-107">EXAMPLES</span></span>

### <span data-ttu-id="b16a3-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="b16a3-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="b16a3-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b16a3-109">PARAMETERS</span></span>

### <span data-ttu-id="b16a3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16a3-110">-DefaultProfile</span></span>
<span data-ttu-id="b16a3-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b16a3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b16a3-112">-Name</span><span class="sxs-lookup"><span data-stu-id="b16a3-112">-Name</span></span>
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

### <span data-ttu-id="b16a3-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b16a3-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="b16a3-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b16a3-114">-Confirm</span></span>
<span data-ttu-id="b16a3-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b16a3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b16a3-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16a3-116">-WhatIf</span></span>
<span data-ttu-id="b16a3-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b16a3-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16a3-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b16a3-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b16a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16a3-119">CommonParameters</span></span>
<span data-ttu-id="b16a3-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b16a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16a3-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b16a3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16a3-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b16a3-122">INPUTS</span></span>

### <span data-ttu-id="b16a3-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b16a3-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b16a3-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b16a3-124">OUTPUTS</span></span>

### <span data-ttu-id="b16a3-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b16a3-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b16a3-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="b16a3-126">NOTES</span></span>

## <span data-ttu-id="b16a3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b16a3-127">RELATED LINKS</span></span>

[<span data-ttu-id="b16a3-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16a3-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="b16a3-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b16a3-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
