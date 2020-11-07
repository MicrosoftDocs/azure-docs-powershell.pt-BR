---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775550"
---
# <span data-ttu-id="42221-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42221-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="42221-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42221-102">SYNOPSIS</span></span>
<span data-ttu-id="42221-103">Obtém uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42221-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="42221-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42221-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42221-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42221-105">DESCRIPTION</span></span>
<span data-ttu-id="42221-106">O cmdlet **Get-AzExpressRouteCircuitPeeringConfig** recupera a configuração de uma relação de emparelhamento para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="42221-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="42221-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42221-107">EXAMPLES</span></span>

### <span data-ttu-id="42221-108">Exemplo 1: exibir a configuração de emparelhamento para um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="42221-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="42221-109">OS</span><span class="sxs-lookup"><span data-stu-id="42221-109">PARAMETERS</span></span>

### <span data-ttu-id="42221-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42221-110">-DefaultProfile</span></span>
<span data-ttu-id="42221-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42221-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42221-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42221-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="42221-113">O objeto de circuito do ExpressRoute que contém a configuração de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="42221-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="42221-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="42221-114">-Name</span></span>
<span data-ttu-id="42221-115">O nome da configuração de emparelhamento a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="42221-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="42221-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42221-116">CommonParameters</span></span>
<span data-ttu-id="42221-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42221-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42221-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42221-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42221-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42221-119">INPUTS</span></span>

### <span data-ttu-id="42221-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42221-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="42221-121">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="42221-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="42221-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42221-122">OUTPUTS</span></span>

### <span data-ttu-id="42221-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="42221-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="42221-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42221-124">NOTES</span></span>

## <span data-ttu-id="42221-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42221-125">RELATED LINKS</span></span>

[<span data-ttu-id="42221-126">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42221-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="42221-127">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42221-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="42221-128">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="42221-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="42221-129">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="42221-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
