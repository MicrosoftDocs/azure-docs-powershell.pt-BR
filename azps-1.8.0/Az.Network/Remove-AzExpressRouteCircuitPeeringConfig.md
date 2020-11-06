---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c7d60c3d2f69e7ea18bcd256d8ad4a943817769a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600180"
---
# <span data-ttu-id="e62da-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e62da-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="e62da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e62da-102">SYNOPSIS</span></span>
<span data-ttu-id="e62da-103">Remove uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e62da-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="e62da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e62da-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e62da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e62da-105">DESCRIPTION</span></span>
<span data-ttu-id="e62da-106">O cmdlet **Remove-AzExpressRouteCircuitPeeringConfig** remove uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e62da-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="e62da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e62da-107">EXAMPLES</span></span>

### <span data-ttu-id="e62da-108">Exemplo 1: remover uma configuração de emparelhamento de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e62da-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="e62da-109">OS</span><span class="sxs-lookup"><span data-stu-id="e62da-109">PARAMETERS</span></span>

### <span data-ttu-id="e62da-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62da-110">-DefaultProfile</span></span>
<span data-ttu-id="e62da-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e62da-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e62da-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e62da-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e62da-113">O circuito do ExpressRoute que contém a configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="e62da-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="e62da-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e62da-114">-Name</span></span>
<span data-ttu-id="e62da-115">O nome da configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="e62da-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="e62da-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e62da-116">-PeerAddressType</span></span>
<span data-ttu-id="e62da-117">A família de endereços da correspondência</span><span class="sxs-lookup"><span data-stu-id="e62da-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="e62da-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62da-118">CommonParameters</span></span>
<span data-ttu-id="e62da-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62da-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62da-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e62da-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62da-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e62da-121">INPUTS</span></span>

### <span data-ttu-id="e62da-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e62da-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e62da-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e62da-123">OUTPUTS</span></span>

### <span data-ttu-id="e62da-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e62da-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e62da-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e62da-125">NOTES</span></span>

## <span data-ttu-id="e62da-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e62da-126">RELATED LINKS</span></span>

[<span data-ttu-id="e62da-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e62da-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e62da-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e62da-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e62da-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="e62da-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="e62da-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e62da-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
