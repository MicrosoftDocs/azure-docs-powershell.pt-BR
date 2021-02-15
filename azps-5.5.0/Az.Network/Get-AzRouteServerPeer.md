---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteServerPeer.md
ms.openlocfilehash: d36a919adfbf1a7a2e2b7a10313433e820cc478a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112884"
---
# <span data-ttu-id="fe706-101">Get-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="fe706-101">Get-AzRouteServerPeer</span></span>

## <span data-ttu-id="fe706-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe706-102">SYNOPSIS</span></span>
<span data-ttu-id="fe706-103">Obtém um ponto de RouteServer em um Servidor de Rota do Azure</span><span class="sxs-lookup"><span data-stu-id="fe706-103">Gets a RouteServer peer in an Azure RouteServer</span></span>

## <span data-ttu-id="fe706-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe706-104">SYNTAX</span></span>

### <span data-ttu-id="fe706-105">RouteServerNPeerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fe706-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Get-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe706-106">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe706-106">RouteServerNPeerResourceIdParameterSet</span></span>
```
Get-AzRouteServerPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe706-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe706-107">DESCRIPTION</span></span>
<span data-ttu-id="fe706-108">O cmdlet **Get-AzRouteServerPeer** obtém um Ponto em um Servidor de Rota do Azure</span><span class="sxs-lookup"><span data-stu-id="fe706-108">The **Get-AzRouteServerPeer** cmdlet gets a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="fe706-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fe706-109">EXAMPLES</span></span>

### <span data-ttu-id="fe706-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe706-110">Example 1</span></span>
```powershell
Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
```

### <span data-ttu-id="fe706-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fe706-111">Example 2</span></span>
```powershell
$routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Get-AzRouteServerPeer -ResourceId $routeServerPeerId
```

## <span data-ttu-id="fe706-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe706-112">PARAMETERS</span></span>

### <span data-ttu-id="fe706-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe706-113">-DefaultProfile</span></span>
<span data-ttu-id="fe706-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe706-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe706-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="fe706-115">-PeerName</span></span>
<span data-ttu-id="fe706-116">O nome do ponto do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="fe706-116">The name of the route server peer.</span></span>

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

### <span data-ttu-id="fe706-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe706-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe706-118">O nome do grupo de recursos do servidor de rotação.</span><span class="sxs-lookup"><span data-stu-id="fe706-118">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="fe706-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe706-119">-ResourceId</span></span>
<span data-ttu-id="fe706-120">ResourceId do ponto de servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="fe706-120">ResourceId of the route server peer.</span></span>

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

### <span data-ttu-id="fe706-121">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="fe706-121">-RouteServerName</span></span>
<span data-ttu-id="fe706-122">O nome do servidor de rota.</span><span class="sxs-lookup"><span data-stu-id="fe706-122">The name of the route server.</span></span>

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

### <span data-ttu-id="fe706-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe706-123">CommonParameters</span></span>
<span data-ttu-id="fe706-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe706-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe706-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe706-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe706-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="fe706-126">INPUTS</span></span>

### <span data-ttu-id="fe706-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fe706-127">System.String</span></span>

## <span data-ttu-id="fe706-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="fe706-128">OUTPUTS</span></span>

### <span data-ttu-id="fe706-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="fe706-129">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="fe706-130">Notas</span><span class="sxs-lookup"><span data-stu-id="fe706-130">NOTES</span></span>

## <span data-ttu-id="fe706-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe706-131">RELATED LINKS</span></span>
