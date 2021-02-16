---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113457"
---
# <span data-ttu-id="ce904-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ce904-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ce904-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce904-102">SYNOPSIS</span></span>
<span data-ttu-id="ce904-103">Remove uma configuração de peering de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ce904-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="ce904-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce904-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce904-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce904-105">DESCRIPTION</span></span>
<span data-ttu-id="ce904-106">O cmdlet **Remove-AzExpressRoute CircuitPeeringConfig** remove uma configuração de peering de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ce904-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="ce904-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ce904-107">EXAMPLES</span></span>

### <span data-ttu-id="ce904-108">Exemplo 1: Remover uma configuração de peering de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ce904-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="ce904-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce904-109">PARAMETERS</span></span>

### <span data-ttu-id="ce904-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce904-110">-DefaultProfile</span></span>
<span data-ttu-id="ce904-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ce904-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce904-112">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="ce904-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ce904-113">O circuito do ExpressRoute que contém a configuração de peering a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ce904-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ce904-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce904-114">-Name</span></span>
<span data-ttu-id="ce904-115">O nome da configuração de peering a ser removida.</span><span class="sxs-lookup"><span data-stu-id="ce904-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ce904-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ce904-116">-PeerAddressType</span></span>
<span data-ttu-id="ce904-117">A família Endereço do peering</span><span class="sxs-lookup"><span data-stu-id="ce904-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="ce904-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce904-118">CommonParameters</span></span>
<span data-ttu-id="ce904-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce904-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce904-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce904-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce904-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="ce904-121">INPUTS</span></span>

### <span data-ttu-id="ce904-122">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="ce904-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ce904-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="ce904-123">OUTPUTS</span></span>

### <span data-ttu-id="ce904-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="ce904-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ce904-125">Notas</span><span class="sxs-lookup"><span data-stu-id="ce904-125">NOTES</span></span>

## <span data-ttu-id="ce904-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce904-126">RELATED LINKS</span></span>

[<span data-ttu-id="ce904-127">Add-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ce904-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ce904-128">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="ce904-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ce904-129">New-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ce904-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ce904-130">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="ce904-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
