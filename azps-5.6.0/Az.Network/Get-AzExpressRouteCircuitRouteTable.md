---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 28a61e18f01f550f1b1ffd924119da3323905ad1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891004"
---
# <span data-ttu-id="f201a-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f201a-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="f201a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f201a-102">SYNOPSIS</span></span>
<span data-ttu-id="f201a-103">Obtém uma tabela de rota de um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f201a-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f201a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f201a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f201a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f201a-105">DESCRIPTION</span></span>
<span data-ttu-id="f201a-106">O cmdlet **Get-AzExpressRouteCircuitRouteTable** recupera uma tabela de rota detalhada de um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f201a-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="f201a-107">A tabela de rota mostrará todas as rotas ou poderá ser filtrada para mostrar rotas para um tipo de paração específico.</span><span class="sxs-lookup"><span data-stu-id="f201a-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="f201a-108">Você pode usar a tabela de rota para validar sua configuração de par e conectividade.</span><span class="sxs-lookup"><span data-stu-id="f201a-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="f201a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f201a-109">EXAMPLES</span></span>

### <span data-ttu-id="f201a-110">Exemplo 1: Exibir a tabela de rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="f201a-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="f201a-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f201a-111">PARAMETERS</span></span>

### <span data-ttu-id="f201a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f201a-112">-DefaultProfile</span></span>
<span data-ttu-id="f201a-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f201a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f201a-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f201a-114">-DevicePath</span></span>
<span data-ttu-id="f201a-115">Os valores aceitáveis para este parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f201a-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f201a-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="f201a-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="f201a-117">O nome do circuito ExpressRoute que está sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="f201a-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f201a-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f201a-118">-PeeringType</span></span>
<span data-ttu-id="f201a-119">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f201a-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f201a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f201a-120">-ResourceGroupName</span></span>
<span data-ttu-id="f201a-121">O nome do grupo de recursos que contém o circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f201a-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f201a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f201a-122">CommonParameters</span></span>
<span data-ttu-id="f201a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f201a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f201a-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f201a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f201a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f201a-125">INPUTS</span></span>

### <span data-ttu-id="f201a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f201a-126">System.String</span></span>

## <span data-ttu-id="f201a-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f201a-127">OUTPUTS</span></span>

### <span data-ttu-id="f201a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="f201a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="f201a-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="f201a-129">NOTES</span></span>

## <span data-ttu-id="f201a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f201a-130">RELATED LINKS</span></span>

[<span data-ttu-id="f201a-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f201a-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f201a-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f201a-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f201a-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="f201a-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
