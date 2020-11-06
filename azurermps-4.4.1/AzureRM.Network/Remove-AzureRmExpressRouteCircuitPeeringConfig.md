---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5a7f842f172ac61722daaeb6f6f4c6d4ef6a33a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441011"
---
# <span data-ttu-id="ac805-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ac805-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ac805-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac805-102">SYNOPSIS</span></span>
<span data-ttu-id="ac805-103">Remove uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ac805-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac805-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac805-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac805-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac805-105">DESCRIPTION</span></span>
<span data-ttu-id="ac805-106">O cmdlet **Remove-AzureRmExpressRouteCircuitPeeringConfig** remove uma configuração de emparelhamento de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ac805-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="ac805-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac805-107">EXAMPLES</span></span>

### <span data-ttu-id="ac805-108">Exemplo 1: remover uma configuração de emparelhamento de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ac805-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="ac805-109">OS</span><span class="sxs-lookup"><span data-stu-id="ac805-109">PARAMETERS</span></span>

### <span data-ttu-id="ac805-110">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac805-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ac805-111">O circuito do ExpressRoute que contém a configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="ac805-111">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ac805-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac805-112">-Name</span></span>
<span data-ttu-id="ac805-113">O nome da configuração de emparelhamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="ac805-113">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="ac805-114">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ac805-114">-PeerAddressType</span></span>
<span data-ttu-id="ac805-115">A família de endereços da correspondência</span><span class="sxs-lookup"><span data-stu-id="ac805-115">The Address family of the peering</span></span>

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

### <span data-ttu-id="ac805-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac805-116">-DefaultProfile</span></span>
<span data-ttu-id="ac805-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac805-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac805-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac805-118">CommonParameters</span></span>
<span data-ttu-id="ac805-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac805-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac805-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac805-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac805-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac805-121">INPUTS</span></span>

### <span data-ttu-id="ac805-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac805-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="ac805-123">O parâmetro ' ExpressRouteCircuit ' aceita o valor do tipo ' PSExpressRouteCircuit ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ac805-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="ac805-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac805-124">OUTPUTS</span></span>

### <span data-ttu-id="ac805-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac805-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ac805-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac805-126">NOTES</span></span>

## <span data-ttu-id="ac805-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac805-127">RELATED LINKS</span></span>

[<span data-ttu-id="ac805-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ac805-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ac805-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac805-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ac805-130">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ac805-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ac805-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ac805-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)