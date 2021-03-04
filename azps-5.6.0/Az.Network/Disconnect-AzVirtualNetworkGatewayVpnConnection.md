---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: 1cbbfcbc87ed1d9be869066f8ec6dd288ba3d4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892115"
---
# <span data-ttu-id="7d42e-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="7d42e-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="7d42e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d42e-102">SYNOPSIS</span></span> 
<span data-ttu-id="7d42e-103">Desconecte determinadas conexões de cliente vpn conectadas com um determinado gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7d42e-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="7d42e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7d42e-104">SYNTAX</span></span>
### <span data-ttu-id="7d42e-105">ByVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7d42e-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="7d42e-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7d42e-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="7d42e-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7d42e-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="7d42e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7d42e-108">DESCRIPTION</span></span>
<span data-ttu-id="7d42e-109">O cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** permite desconectar determinada conexão de cliente vpn conectada.</span><span class="sxs-lookup"><span data-stu-id="7d42e-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="7d42e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d42e-110">EXAMPLES</span></span>

### <span data-ttu-id="7d42e-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7d42e-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="7d42e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7d42e-112">PARAMETERS</span></span>

### <span data-ttu-id="7d42e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d42e-113">-ResourceGroupName</span></span>
<span data-ttu-id="7d42e-114">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7d42e-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d42e-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7d42e-115">-ResourceName</span></span>
<span data-ttu-id="7d42e-116">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7d42e-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d42e-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d42e-117">-ResourceId</span></span>
<span data-ttu-id="7d42e-118">ID do recurso do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7d42e-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d42e-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="7d42e-119">-VpnConnectionId</span></span>
<span data-ttu-id="7d42e-120">Ids de conexão vpn</span><span class="sxs-lookup"><span data-stu-id="7d42e-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d42e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d42e-121">-InputObject</span></span>
<span data-ttu-id="7d42e-122">Objeto gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7d42e-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d42e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d42e-123">-AsJob</span></span>
<span data-ttu-id="7d42e-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7d42e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d42e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d42e-125">CommonParameters</span></span>
<span data-ttu-id="7d42e-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d42e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d42e-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d42e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d42e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d42e-128">INPUTS</span></span>

### <span data-ttu-id="7d42e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7d42e-129">System.String</span></span>

## <span data-ttu-id="7d42e-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7d42e-130">OUTPUTS</span></span>

### <span data-ttu-id="7d42e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7d42e-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7d42e-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="7d42e-132">NOTES</span></span>

## <span data-ttu-id="7d42e-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d42e-133">RELATED LINKS</span></span>
