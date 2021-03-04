---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: c92033fa0ed907aab4c36f7dd980fb977a47be73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888836"
---
# <span data-ttu-id="8f063-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8f063-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="8f063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f063-102">SYNOPSIS</span></span>
<span data-ttu-id="8f063-103">Obtém uma tabela de rota de uma conexão cruzada ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8f063-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="8f063-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f063-104">SYNTAX</span></span>

### <span data-ttu-id="8f063-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="8f063-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f063-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="8f063-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f063-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f063-107">DESCRIPTION</span></span>
<span data-ttu-id="8f063-108">O cmdlet **Get-AzExpressRouteCrossConnectionRouteTable** recupera uma tabela de rota detalhada de um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8f063-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="8f063-109">A tabela de rota mostrará todas as rotas ou poderá ser filtrada para mostrar rotas para um tipo de paração específico.</span><span class="sxs-lookup"><span data-stu-id="8f063-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="8f063-110">Você pode usar a tabela de rota para validar sua configuração de par e conectividade.</span><span class="sxs-lookup"><span data-stu-id="8f063-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="8f063-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f063-111">EXAMPLES</span></span>

### <span data-ttu-id="8f063-112">Exemplo 1: Exibir a tabela de rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="8f063-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="8f063-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f063-113">PARAMETERS</span></span>

### <span data-ttu-id="8f063-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="8f063-114">-CrossConnectionName</span></span>
<span data-ttu-id="8f063-115">O nome da conexão entre rotas expressas</span><span class="sxs-lookup"><span data-stu-id="8f063-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f063-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f063-116">-DefaultProfile</span></span>
<span data-ttu-id="8f063-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8f063-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f063-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="8f063-118">-DevicePath</span></span>
<span data-ttu-id="8f063-119">Os valores aceitáveis para este parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="8f063-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="8f063-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8f063-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="8f063-121">A Conexão Entre Rota Expressa</span><span class="sxs-lookup"><span data-stu-id="8f063-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f063-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8f063-122">-PeeringType</span></span>
<span data-ttu-id="8f063-123">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8f063-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8f063-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f063-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f063-125">O nome do grupo de recursos que contém a conexão cruzada ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8f063-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f063-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f063-126">CommonParameters</span></span>
<span data-ttu-id="8f063-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f063-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f063-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f063-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f063-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f063-129">INPUTS</span></span>

### <span data-ttu-id="8f063-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8f063-130">None</span></span>
<span data-ttu-id="8f063-131">Este cmdlet não aceita qualquer entrada.</span><span class="sxs-lookup"><span data-stu-id="8f063-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f063-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f063-132">OUTPUTS</span></span>

### <span data-ttu-id="8f063-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="8f063-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="8f063-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f063-134">NOTES</span></span>

## <span data-ttu-id="8f063-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f063-135">RELATED LINKS</span></span>

[<span data-ttu-id="8f063-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="8f063-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="8f063-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8f063-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
