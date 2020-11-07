---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785912"
---
# <span data-ttu-id="f14b3-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f14b3-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="f14b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f14b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f14b3-103">Obtém uma tabela de rota de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f14b3-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f14b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f14b3-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f14b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f14b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f14b3-106">O cmdlet **Get-AzureRmExpressRouteCircuitRouteTable** recupera uma tabela de rotas detalhadas de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f14b3-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="f14b3-107">A tabela de rota mostrará todas as rotas ou poderá ser filtrada para mostrar rotas para um tipo de emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="f14b3-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="f14b3-108">Você pode usar a tabela de rotas para validar a configuração e a conectividade de pares.</span><span class="sxs-lookup"><span data-stu-id="f14b3-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="f14b3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f14b3-109">EXAMPLES</span></span>

### <span data-ttu-id="f14b3-110">Exemplo 1: exibir a tabela de rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="f14b3-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="f14b3-111">OS</span><span class="sxs-lookup"><span data-stu-id="f14b3-111">PARAMETERS</span></span>

### <span data-ttu-id="f14b3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14b3-112">-DefaultProfile</span></span>
<span data-ttu-id="f14b3-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f14b3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f14b3-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f14b3-114">-DevicePath</span></span>
<span data-ttu-id="f14b3-115">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f14b3-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f14b3-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f14b3-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f14b3-117">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="f14b3-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="f14b3-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f14b3-118">-PeeringType</span></span>
<span data-ttu-id="f14b3-119">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f14b3-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f14b3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14b3-120">-ResourceGroupName</span></span>
<span data-ttu-id="f14b3-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f14b3-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="f14b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14b3-122">CommonParameters</span></span>
<span data-ttu-id="f14b3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f14b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14b3-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14b3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14b3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f14b3-125">INPUTS</span></span>

## <span data-ttu-id="f14b3-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f14b3-126">OUTPUTS</span></span>

### <span data-ttu-id="f14b3-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="f14b3-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="f14b3-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f14b3-128">NOTES</span></span>

## <span data-ttu-id="f14b3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f14b3-129">RELATED LINKS</span></span>

[<span data-ttu-id="f14b3-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f14b3-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f14b3-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f14b3-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f14b3-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="f14b3-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
