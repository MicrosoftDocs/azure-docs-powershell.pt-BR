---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: 0d798c5eb70c8c472862e9af0f992d01827a750e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885645"
---
# <span data-ttu-id="434ba-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="434ba-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="434ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="434ba-102">SYNOPSIS</span></span>
<span data-ttu-id="434ba-103">Obtém um par RouteServer em um RouteServer do Azure</span><span class="sxs-lookup"><span data-stu-id="434ba-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="434ba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="434ba-104">SYNTAX</span></span>

### <span data-ttu-id="434ba-105">RouteServerNPeerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="434ba-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="434ba-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="434ba-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="434ba-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="434ba-107">DESCRIPTION</span></span>
<span data-ttu-id="434ba-108">O cmdlet **Get-AzRouteServerPeer** obtém um Peer em um RouteServer do Azure</span><span class="sxs-lookup"><span data-stu-id="434ba-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="434ba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="434ba-109">EXAMPLES</span></span>

### <span data-ttu-id="434ba-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="434ba-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="434ba-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="434ba-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="434ba-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="434ba-112">PARAMETERS</span></span>

### <span data-ttu-id="434ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434ba-113">-DefaultProfile</span></span>
<span data-ttu-id="434ba-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="434ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="434ba-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="434ba-115">-PeerName</span></span>
<span data-ttu-id="434ba-116">O nome do par de servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="434ba-116">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="434ba-118">O nome do grupo de recursos do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="434ba-118">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ba-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="434ba-119">-ResourceId</span></span>
<span data-ttu-id="434ba-120">ResourceId do ponto de servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="434ba-120">ResourceId of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ba-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="434ba-121">-RouteServerName</span></span>
<span data-ttu-id="434ba-122">O nome do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="434ba-122">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434ba-123">CommonParameters</span></span>
<span data-ttu-id="434ba-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="434ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434ba-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="434ba-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434ba-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="434ba-126">INPUTS</span></span>

### <span data-ttu-id="434ba-127">System.String</span><span class="sxs-lookup"><span data-stu-id="434ba-127">System.String</span></span>

## <span data-ttu-id="434ba-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="434ba-128">OUTPUTS</span></span>

### <span data-ttu-id="434ba-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="434ba-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="434ba-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="434ba-130">NOTES</span></span>

## <span data-ttu-id="434ba-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="434ba-131">RELATED LINKS</span></span>
