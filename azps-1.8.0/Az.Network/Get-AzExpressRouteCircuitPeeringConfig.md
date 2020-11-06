---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600599"
---
# <span data-ttu-id="e7021-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e7021-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e7021-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7021-102">SYNOPSIS</span></span>
<span data-ttu-id="e7021-103">Obtém uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e7021-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="e7021-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7021-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7021-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7021-105">DESCRIPTION</span></span>
<span data-ttu-id="e7021-106">O cmdlet **Get-AzExpressRouteCircuitPeeringConfig** recupera a configuração de uma relação de emparelhamento para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e7021-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e7021-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7021-107">EXAMPLES</span></span>

### <span data-ttu-id="e7021-108">Exemplo 1: exibir a configuração de emparelhamento para um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e7021-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="e7021-109">OS</span><span class="sxs-lookup"><span data-stu-id="e7021-109">PARAMETERS</span></span>

### <span data-ttu-id="e7021-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7021-110">-DefaultProfile</span></span>
<span data-ttu-id="e7021-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7021-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7021-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7021-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e7021-113">O objeto de circuito do ExpressRoute que contém a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="e7021-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="e7021-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7021-114">-Name</span></span>
<span data-ttu-id="e7021-115">O nome da configuração de emparelhamento a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="e7021-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="e7021-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7021-116">CommonParameters</span></span>
<span data-ttu-id="e7021-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7021-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7021-118">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7021-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7021-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7021-119">INPUTS</span></span>

### <span data-ttu-id="e7021-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7021-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e7021-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7021-121">OUTPUTS</span></span>

### <span data-ttu-id="e7021-122">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="e7021-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="e7021-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7021-123">NOTES</span></span>

## <span data-ttu-id="e7021-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7021-124">RELATED LINKS</span></span>

[<span data-ttu-id="e7021-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e7021-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e7021-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e7021-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e7021-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e7021-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e7021-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e7021-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
