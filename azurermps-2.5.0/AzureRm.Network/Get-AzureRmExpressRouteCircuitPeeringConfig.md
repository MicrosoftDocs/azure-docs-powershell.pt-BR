---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 187b7848dc3634ee67521e03f46f4684f23b9913
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785507"
---
# <span data-ttu-id="f862c-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f862c-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f862c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f862c-102">SYNOPSIS</span></span>
<span data-ttu-id="f862c-103">Obtém uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f862c-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f862c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f862c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f862c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f862c-105">DESCRIPTION</span></span>
<span data-ttu-id="f862c-106">O cmdlet **Get-AzureRmExpressRouteCircuitPeeringConfig** recupera a configuração de uma relação de emparelhamento para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f862c-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f862c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f862c-107">EXAMPLES</span></span>

### <span data-ttu-id="f862c-108">Exemplo 1: exibir a configuração de emparelhamento para um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f862c-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f862c-109">OS</span><span class="sxs-lookup"><span data-stu-id="f862c-109">PARAMETERS</span></span>

### <span data-ttu-id="f862c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f862c-110">-DefaultProfile</span></span>
<span data-ttu-id="f862c-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f862c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f862c-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f862c-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f862c-113">O objeto de circuito do ExpressRoute que contém a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f862c-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f862c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f862c-114">-Name</span></span>
<span data-ttu-id="f862c-115">O nome da configuração de emparelhamento a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="f862c-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f862c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f862c-116">CommonParameters</span></span>
<span data-ttu-id="f862c-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f862c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f862c-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f862c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f862c-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f862c-119">INPUTS</span></span>

### <span data-ttu-id="f862c-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f862c-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="f862c-121">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f862c-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="f862c-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f862c-122">OUTPUTS</span></span>

### <span data-ttu-id="f862c-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f862c-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f862c-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f862c-124">NOTES</span></span>

## <span data-ttu-id="f862c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f862c-125">RELATED LINKS</span></span>

[<span data-ttu-id="f862c-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f862c-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f862c-127">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f862c-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f862c-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f862c-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f862c-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f862c-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
