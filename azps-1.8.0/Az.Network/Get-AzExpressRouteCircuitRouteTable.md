---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: c7b4f51e868522533756534b52fd0b0cf5c17f0c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401939"
---
# <span data-ttu-id="5bad2-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5bad2-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="5bad2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bad2-102">SYNOPSIS</span></span>
<span data-ttu-id="5bad2-103">Obtém uma tabela de rota de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5bad2-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="5bad2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bad2-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bad2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bad2-105">DESCRIPTION</span></span>
<span data-ttu-id="5bad2-106">O cmdlet **Get-AzExpressRoute CircuitRouteTable** recupera uma tabela de rota detalhada de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5bad2-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="5bad2-107">A tabela de rota mostrará todas as rotas ou poderá ser filtrada para mostrar rotas para um tipo de ponto específico.</span><span class="sxs-lookup"><span data-stu-id="5bad2-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="5bad2-108">Você pode usar a tabela de rota para validar a configuração de par e a conectividade.</span><span class="sxs-lookup"><span data-stu-id="5bad2-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="5bad2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5bad2-109">EXAMPLES</span></span>

### <span data-ttu-id="5bad2-110">Exemplo 1: Exibir a tabela de rota do caminho principal</span><span class="sxs-lookup"><span data-stu-id="5bad2-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="5bad2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bad2-111">PARAMETERS</span></span>

### <span data-ttu-id="5bad2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bad2-112">-DefaultProfile</span></span>
<span data-ttu-id="5bad2-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5bad2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bad2-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="5bad2-114">-DevicePath</span></span>
<span data-ttu-id="5bad2-115">Os valores aceitáveis para este parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="5bad2-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="5bad2-116">-ExpressRoute CircuitName</span><span class="sxs-lookup"><span data-stu-id="5bad2-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="5bad2-117">O nome do circuito do ExpressRoute que está sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="5bad2-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="5bad2-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5bad2-118">-PeeringType</span></span>
<span data-ttu-id="5bad2-119">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5bad2-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="5bad2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bad2-120">-ResourceGroupName</span></span>
<span data-ttu-id="5bad2-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5bad2-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="5bad2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bad2-122">CommonParameters</span></span>
<span data-ttu-id="5bad2-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bad2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bad2-124">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bad2-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bad2-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="5bad2-125">INPUTS</span></span>

### <span data-ttu-id="5bad2-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5bad2-126">System.String</span></span>

## <span data-ttu-id="5bad2-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="5bad2-127">OUTPUTS</span></span>

### <span data-ttu-id="5bad2-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoute CircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="5bad2-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="5bad2-129">Notas</span><span class="sxs-lookup"><span data-stu-id="5bad2-129">NOTES</span></span>

## <span data-ttu-id="5bad2-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bad2-130">RELATED LINKS</span></span>

[<span data-ttu-id="5bad2-131">Tabela Get-AzExpressRoute CircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5bad2-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="5bad2-132">Get-AzExpressRoute CircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5bad2-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="5bad2-133">Get-AzExpressRoute CircuitStat</span><span class="sxs-lookup"><span data-stu-id="5bad2-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
