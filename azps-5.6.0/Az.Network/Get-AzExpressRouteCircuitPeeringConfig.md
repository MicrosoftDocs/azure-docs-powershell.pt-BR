---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7da632a1496b22e2f0be183640995a2aaa96735e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892625"
---
# <span data-ttu-id="f25f0-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f25f0-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f25f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f25f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f25f0-103">Obtém uma configuração de paração de circuitos ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f25f0-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="f25f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f25f0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f25f0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f25f0-105">DESCRIPTION</span></span>
<span data-ttu-id="f25f0-106">O cmdlet **Get-AzExpressRouteCircuitPeeringConfig** recupera a configuração de uma relação de paridade para um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f25f0-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f25f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f25f0-107">EXAMPLES</span></span>

### <span data-ttu-id="f25f0-108">Exemplo 1: Exibir a configuração de peering para um circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f25f0-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f25f0-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f25f0-109">PARAMETERS</span></span>

### <span data-ttu-id="f25f0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25f0-110">-DefaultProfile</span></span>
<span data-ttu-id="f25f0-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f25f0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f25f0-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f25f0-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f25f0-113">O objeto de circuito ExpressRoute que contém a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="f25f0-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="f25f0-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f25f0-114">-Name</span></span>
<span data-ttu-id="f25f0-115">O nome da configuração de paração a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="f25f0-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="f25f0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25f0-116">CommonParameters</span></span>
<span data-ttu-id="f25f0-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25f0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25f0-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f25f0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25f0-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f25f0-119">INPUTS</span></span>

### <span data-ttu-id="f25f0-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f25f0-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f25f0-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f25f0-121">OUTPUTS</span></span>

### <span data-ttu-id="f25f0-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="f25f0-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f25f0-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="f25f0-123">NOTES</span></span>

## <span data-ttu-id="f25f0-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f25f0-124">RELATED LINKS</span></span>

[<span data-ttu-id="f25f0-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f25f0-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f25f0-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f25f0-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f25f0-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f25f0-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f25f0-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f25f0-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
