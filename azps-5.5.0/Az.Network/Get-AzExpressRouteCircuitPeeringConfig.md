---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112902"
---
# <span data-ttu-id="81e63-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="81e63-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="81e63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81e63-102">SYNOPSIS</span></span>
<span data-ttu-id="81e63-103">Obtém uma configuração de paridade de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="81e63-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="81e63-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81e63-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81e63-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="81e63-105">DESCRIPTION</span></span>
<span data-ttu-id="81e63-106">O cmdlet **Get-AzExpressRoute CircuitPeeringConfig** recupera a configuração de uma relação de pares para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="81e63-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="81e63-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="81e63-107">EXAMPLES</span></span>

### <span data-ttu-id="81e63-108">Exemplo 1: Exibir a configuração de peering de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="81e63-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="81e63-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81e63-109">PARAMETERS</span></span>

### <span data-ttu-id="81e63-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e63-110">-DefaultProfile</span></span>
<span data-ttu-id="81e63-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="81e63-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e63-112">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="81e63-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="81e63-113">O objeto de circuito do ExpressRoute que contém a configuração de peering.</span><span class="sxs-lookup"><span data-stu-id="81e63-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="81e63-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="81e63-114">-Name</span></span>
<span data-ttu-id="81e63-115">O nome da configuração de peering a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="81e63-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="81e63-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e63-116">CommonParameters</span></span>
<span data-ttu-id="81e63-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e63-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e63-118">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81e63-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e63-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="81e63-119">INPUTS</span></span>

### <span data-ttu-id="81e63-120">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="81e63-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="81e63-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="81e63-121">OUTPUTS</span></span>

### <span data-ttu-id="81e63-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="81e63-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="81e63-123">Notas</span><span class="sxs-lookup"><span data-stu-id="81e63-123">NOTES</span></span>

## <span data-ttu-id="81e63-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81e63-124">RELATED LINKS</span></span>

[<span data-ttu-id="81e63-125">Add-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="81e63-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="81e63-126">New-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="81e63-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="81e63-127">Remove-AzExpressRoute CircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="81e63-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="81e63-128">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="81e63-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
