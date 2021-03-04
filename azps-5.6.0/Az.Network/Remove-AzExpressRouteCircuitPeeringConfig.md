---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 187921598b21747764436dd4ae6f988961d4a951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891151"
---
# <span data-ttu-id="a592e-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a592e-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a592e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a592e-102">SYNOPSIS</span></span>
<span data-ttu-id="a592e-103">Remove uma configuração de paração de circuitos ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a592e-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a592e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a592e-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a592e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a592e-105">DESCRIPTION</span></span>
<span data-ttu-id="a592e-106">O cmdlet **Remove-AzExpressRouteCircuitPeeringConfig** remove uma configuração de paração de circuitos ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a592e-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a592e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a592e-107">EXAMPLES</span></span>

### <span data-ttu-id="a592e-108">Exemplo 1: Remover uma configuração de peering de um circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a592e-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="a592e-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a592e-109">PARAMETERS</span></span>

### <span data-ttu-id="a592e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a592e-110">-DefaultProfile</span></span>
<span data-ttu-id="a592e-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a592e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a592e-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a592e-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a592e-113">O circuito ExpressRoute que contém a configuração de paração a ser removida.</span><span class="sxs-lookup"><span data-stu-id="a592e-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a592e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a592e-114">-Name</span></span>
<span data-ttu-id="a592e-115">O nome da configuração de paração a ser removida.</span><span class="sxs-lookup"><span data-stu-id="a592e-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a592e-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a592e-116">-PeerAddressType</span></span>
<span data-ttu-id="a592e-117">A família address do paring</span><span class="sxs-lookup"><span data-stu-id="a592e-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a592e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a592e-118">CommonParameters</span></span>
<span data-ttu-id="a592e-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a592e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a592e-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a592e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a592e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a592e-121">INPUTS</span></span>

### <span data-ttu-id="a592e-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a592e-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a592e-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a592e-123">OUTPUTS</span></span>

### <span data-ttu-id="a592e-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a592e-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a592e-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="a592e-125">NOTES</span></span>

## <span data-ttu-id="a592e-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a592e-126">RELATED LINKS</span></span>

[<span data-ttu-id="a592e-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a592e-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a592e-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a592e-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a592e-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a592e-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a592e-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a592e-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
