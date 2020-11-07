---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
ms.openlocfilehash: 68579ea2adecbf7ad6a97fd11f4f32da9adeb48f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786309"
---
# <span data-ttu-id="3369f-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="3369f-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="3369f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3369f-102">SYNOPSIS</span></span>
<span data-ttu-id="3369f-103">Obtém estatísticas de uso de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3369f-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3369f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3369f-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3369f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3369f-105">DESCRIPTION</span></span>
<span data-ttu-id="3369f-106">O cmdlet **Get-AzureRmExpressRouteCircuitStats** recupera estatísticas de tráfego para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3369f-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="3369f-107">As estatísticas incluem o número de bytes enviados e recebidos por rotas primárias e secundárias.</span><span class="sxs-lookup"><span data-stu-id="3369f-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="3369f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3369f-108">EXAMPLES</span></span>

### <span data-ttu-id="3369f-109">Exemplo 1: exibir as estatísticas de tráfego para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3369f-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="3369f-110">OS</span><span class="sxs-lookup"><span data-stu-id="3369f-110">PARAMETERS</span></span>

### <span data-ttu-id="3369f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3369f-111">-DefaultProfile</span></span>
<span data-ttu-id="3369f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3369f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3369f-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="3369f-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="3369f-114">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="3369f-114">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3369f-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3369f-115">-PeeringType</span></span>
<span data-ttu-id="3369f-116">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3369f-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3369f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3369f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3369f-118">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3369f-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3369f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3369f-119">CommonParameters</span></span>
<span data-ttu-id="3369f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3369f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3369f-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3369f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3369f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3369f-122">INPUTS</span></span>

## <span data-ttu-id="3369f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3369f-123">OUTPUTS</span></span>

### <span data-ttu-id="3369f-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="3369f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="3369f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3369f-125">NOTES</span></span>

## <span data-ttu-id="3369f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3369f-126">RELATED LINKS</span></span>

[<span data-ttu-id="3369f-127">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3369f-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="3369f-128">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3369f-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="3369f-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3369f-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
