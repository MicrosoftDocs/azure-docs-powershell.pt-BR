---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 204d70753d3a4ae80e05dfff90d4a5b50b47ab58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440764"
---
# <span data-ttu-id="34694-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="34694-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="34694-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34694-102">SYNOPSIS</span></span>
<span data-ttu-id="34694-103">Obtém uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="34694-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34694-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34694-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34694-105">DESCRIPTION</span></span>
<span data-ttu-id="34694-106">O cmdlet **Get-AzureRmExpressRouteCircuitPeeringConfig** recupera a configuração de uma relação de emparelhamento para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="34694-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="34694-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34694-107">EXAMPLES</span></span>

### <span data-ttu-id="34694-108">Exemplo 1: exibir a configuração de emparelhamento para um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="34694-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="34694-109">OS</span><span class="sxs-lookup"><span data-stu-id="34694-109">PARAMETERS</span></span>

### <span data-ttu-id="34694-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34694-110">-DefaultProfile</span></span>
<span data-ttu-id="34694-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34694-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34694-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34694-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="34694-113">O objeto de circuito do ExpressRoute que contém a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="34694-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="34694-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="34694-114">-Name</span></span>
<span data-ttu-id="34694-115">O nome da configuração de emparelhamento a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="34694-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="34694-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34694-116">CommonParameters</span></span>
<span data-ttu-id="34694-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34694-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34694-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34694-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34694-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34694-119">INPUTS</span></span>

### <span data-ttu-id="34694-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34694-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="34694-121">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="34694-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="34694-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34694-122">OUTPUTS</span></span>

### <span data-ttu-id="34694-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="34694-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="34694-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34694-124">NOTES</span></span>

## <span data-ttu-id="34694-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34694-125">RELATED LINKS</span></span>

[<span data-ttu-id="34694-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="34694-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="34694-127">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="34694-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="34694-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="34694-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="34694-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="34694-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
