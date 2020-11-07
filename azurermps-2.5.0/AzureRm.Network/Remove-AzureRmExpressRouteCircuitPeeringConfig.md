---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 749f1b84ed033e903d3e50652e6199f184fffa2b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785467"
---
# <span data-ttu-id="436b3-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="436b3-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="436b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="436b3-102">SYNOPSIS</span></span>
<span data-ttu-id="436b3-103">Remove uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="436b3-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="436b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="436b3-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="436b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="436b3-105">DESCRIPTION</span></span>
<span data-ttu-id="436b3-106">O cmdlet **Remove-AzureRmExpressRouteCircuitPeeringConfig** remove uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="436b3-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="436b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="436b3-107">EXAMPLES</span></span>

### <span data-ttu-id="436b3-108">Exemplo 1: remover uma configuração de emparelhamento de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="436b3-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="436b3-109">OS</span><span class="sxs-lookup"><span data-stu-id="436b3-109">PARAMETERS</span></span>

### <span data-ttu-id="436b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436b3-110">-DefaultProfile</span></span>
<span data-ttu-id="436b3-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="436b3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="436b3-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="436b3-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="436b3-113">O circuito do ExpressRoute que contém a configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="436b3-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="436b3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="436b3-114">-Name</span></span>
<span data-ttu-id="436b3-115">O nome da configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="436b3-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="436b3-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="436b3-116">-PeerAddressType</span></span>
<span data-ttu-id="436b3-117">A família de endereços da correspondência</span><span class="sxs-lookup"><span data-stu-id="436b3-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436b3-118">CommonParameters</span></span>
<span data-ttu-id="436b3-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="436b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436b3-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="436b3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436b3-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="436b3-121">INPUTS</span></span>

### <span data-ttu-id="436b3-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="436b3-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="436b3-123">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="436b3-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="436b3-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="436b3-124">OUTPUTS</span></span>

### <span data-ttu-id="436b3-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="436b3-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="436b3-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="436b3-126">NOTES</span></span>

## <span data-ttu-id="436b3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="436b3-127">RELATED LINKS</span></span>

[<span data-ttu-id="436b3-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="436b3-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="436b3-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="436b3-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="436b3-130">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="436b3-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="436b3-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="436b3-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
