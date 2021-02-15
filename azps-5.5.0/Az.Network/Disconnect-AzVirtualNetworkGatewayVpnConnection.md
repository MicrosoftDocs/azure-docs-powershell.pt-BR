---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114199"
---
# <span data-ttu-id="46c45-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="46c45-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="46c45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46c45-102">SYNOPSIS</span></span> 
<span data-ttu-id="46c45-103">Desconecte determinadas conexões de cliente vpn conectadas com um determinado gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="46c45-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="46c45-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46c45-104">SYNTAX</span></span>
### <span data-ttu-id="46c45-105">ByVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46c45-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="46c45-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="46c45-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="46c45-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="46c45-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="46c45-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="46c45-108">DESCRIPTION</span></span>
<span data-ttu-id="46c45-109">O cmdlet **Disconnect-AzVirtualNetworkGatewayVpnConnection** permite que você desconecte determinada conexão de cliente vpn conectada.</span><span class="sxs-lookup"><span data-stu-id="46c45-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="46c45-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46c45-110">EXAMPLES</span></span>

### <span data-ttu-id="46c45-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="46c45-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="46c45-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46c45-112">PARAMETERS</span></span>

### <span data-ttu-id="46c45-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c45-113">-ResourceGroupName</span></span>
<span data-ttu-id="46c45-114">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="46c45-114">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="46c45-115">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="46c45-115">-ResourceName</span></span>
<span data-ttu-id="46c45-116">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="46c45-116">Virtual network gateway name</span></span>

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

### <span data-ttu-id="46c45-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46c45-117">-ResourceId</span></span>
<span data-ttu-id="46c45-118">ID de recurso do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="46c45-118">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="46c45-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="46c45-119">-VpnConnectionId</span></span>
<span data-ttu-id="46c45-120">Ids de conexão vpn</span><span class="sxs-lookup"><span data-stu-id="46c45-120">Vpn Connection Ids</span></span>

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

### <span data-ttu-id="46c45-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46c45-121">-InputObject</span></span>
<span data-ttu-id="46c45-122">Objeto de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="46c45-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="46c45-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46c45-123">-AsJob</span></span>
<span data-ttu-id="46c45-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="46c45-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46c45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c45-125">CommonParameters</span></span>
<span data-ttu-id="46c45-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c45-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46c45-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c45-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="46c45-128">INPUTS</span></span>

### <span data-ttu-id="46c45-129">System.String</span><span class="sxs-lookup"><span data-stu-id="46c45-129">System.String</span></span>

## <span data-ttu-id="46c45-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="46c45-130">OUTPUTS</span></span>

### <span data-ttu-id="46c45-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46c45-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="46c45-132">Notas</span><span class="sxs-lookup"><span data-stu-id="46c45-132">NOTES</span></span>

## <span data-ttu-id="46c45-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46c45-133">RELATED LINKS</span></span>
