---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: fd0bb4c3035eb2def0a1d0fa64038299cee4ec48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886920"
---
# <span data-ttu-id="f87a6-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="f87a6-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="f87a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f87a6-102">SYNOPSIS</span></span>
<span data-ttu-id="f87a6-103">Lista os pares BGP de um gateway de rede virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="f87a6-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="f87a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f87a6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f87a6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f87a6-105">DESCRIPTION</span></span>
<span data-ttu-id="f87a6-106">Este comando enumera os pares BGP com os que um gateway de rede virtual do Azure está configurado para fazer par.</span><span class="sxs-lookup"><span data-stu-id="f87a6-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="f87a6-107">O status de cada par também é dado.</span><span class="sxs-lookup"><span data-stu-id="f87a6-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="f87a6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f87a6-108">EXAMPLES</span></span>

### <span data-ttu-id="f87a6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f87a6-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="f87a6-110">Recupera pares BGP para o gateway de rede virtual do Azure chamado gatewayName no resourceGroup do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f87a6-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="f87a6-111">Esta saída de exemplo mostra um par BGP conectado, com um IP de 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="f87a6-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="f87a6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f87a6-112">PARAMETERS</span></span>

### <span data-ttu-id="f87a6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f87a6-113">-AsJob</span></span>
<span data-ttu-id="f87a6-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f87a6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f87a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87a6-115">-DefaultProfile</span></span>
<span data-ttu-id="f87a6-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f87a6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f87a6-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="f87a6-117">-Peer</span></span>
<span data-ttu-id="f87a6-118">IP do par para recuperar o status</span><span class="sxs-lookup"><span data-stu-id="f87a6-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f87a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="f87a6-120">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="f87a6-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="f87a6-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f87a6-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f87a6-122">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="f87a6-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="f87a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87a6-123">CommonParameters</span></span>
<span data-ttu-id="f87a6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87a6-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f87a6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87a6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f87a6-126">INPUTS</span></span>

### <span data-ttu-id="f87a6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f87a6-127">System.String</span></span>

## <span data-ttu-id="f87a6-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f87a6-128">OUTPUTS</span></span>

### <span data-ttu-id="f87a6-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="f87a6-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="f87a6-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="f87a6-130">NOTES</span></span>

## <span data-ttu-id="f87a6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f87a6-131">RELATED LINKS</span></span>
