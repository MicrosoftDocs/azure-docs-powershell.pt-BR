---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777450"
---
# <span data-ttu-id="d5568-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d5568-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="d5568-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5568-102">SYNOPSIS</span></span> 
<span data-ttu-id="d5568-103">Desconecte as conexões de cliente VPN conectadas a um determinado gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d5568-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="d5568-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5568-104">SYNTAX</span></span>
### <span data-ttu-id="d5568-105">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5568-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="d5568-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d5568-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="d5568-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d5568-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="d5568-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5568-108">DESCRIPTION</span></span>
<span data-ttu-id="d5568-109">O cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** permite que você desconecte determinada conexão de cliente VPN conectada.</span><span class="sxs-lookup"><span data-stu-id="d5568-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="d5568-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5568-110">EXAMPLES</span></span>

### <span data-ttu-id="d5568-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d5568-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="d5568-112">OS</span><span class="sxs-lookup"><span data-stu-id="d5568-112">PARAMETERS</span></span>

### <span data-ttu-id="d5568-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5568-113">-ResourceGroupName</span></span>
<span data-ttu-id="d5568-114">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d5568-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d5568-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d5568-115">-ResourceName</span></span>
<span data-ttu-id="d5568-116">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d5568-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="d5568-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5568-117">-ResourceId</span></span>
<span data-ttu-id="d5568-118">ID do recurso do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d5568-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="d5568-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="d5568-119">-VpnConnectionId</span></span>
<span data-ttu-id="d5568-120">IDs de conexão VPN</span><span class="sxs-lookup"><span data-stu-id="d5568-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="d5568-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5568-121">-InputObject</span></span>
<span data-ttu-id="d5568-122">Objeto de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d5568-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="d5568-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5568-123">-AsJob</span></span>
<span data-ttu-id="d5568-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d5568-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5568-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5568-125">CommonParameters</span></span>
<span data-ttu-id="d5568-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5568-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5568-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5568-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5568-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5568-128">INPUTS</span></span>

### <span data-ttu-id="d5568-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d5568-129">System.String</span></span>

## <span data-ttu-id="d5568-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5568-130">OUTPUTS</span></span>

### <span data-ttu-id="d5568-131">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5568-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d5568-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5568-132">NOTES</span></span>

## <span data-ttu-id="d5568-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5568-133">RELATED LINKS</span></span>
