---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: e0f4b24581860f17024c9b01e62b3c84616c6f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891341"
---
# <span data-ttu-id="6d583-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="6d583-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="6d583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d583-102">SYNOPSIS</span></span>
<span data-ttu-id="6d583-103">Obtém estatísticas de uso de um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6d583-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6d583-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6d583-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d583-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6d583-105">DESCRIPTION</span></span>
<span data-ttu-id="6d583-106">O cmdlet **Get-AzExpressRouteCircuitStat** recupera estatísticas de tráfego para um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6d583-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="6d583-107">As estatísticas incluem o número de bytes enviados e recebidos nas rotas primária e secundária.</span><span class="sxs-lookup"><span data-stu-id="6d583-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="6d583-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d583-108">EXAMPLES</span></span>

### <span data-ttu-id="6d583-109">Exemplo 1: Exibir as estatísticas de tráfego para um par expressRoute</span><span class="sxs-lookup"><span data-stu-id="6d583-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="6d583-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6d583-110">PARAMETERS</span></span>

### <span data-ttu-id="6d583-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d583-111">-DefaultProfile</span></span>
<span data-ttu-id="6d583-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6d583-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d583-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="6d583-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="6d583-114">O nome do circuito ExpressRoute que está sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="6d583-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="6d583-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="6d583-115">-PeeringType</span></span>
<span data-ttu-id="6d583-116">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="6d583-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d583-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d583-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d583-118">O nome do grupo de recursos que contém o circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6d583-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6d583-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d583-119">CommonParameters</span></span>
<span data-ttu-id="6d583-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d583-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d583-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d583-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d583-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d583-122">INPUTS</span></span>

### <span data-ttu-id="6d583-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6d583-123">System.String</span></span>

## <span data-ttu-id="6d583-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6d583-124">OUTPUTS</span></span>

### <span data-ttu-id="6d583-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="6d583-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="6d583-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="6d583-126">NOTES</span></span>

## <span data-ttu-id="6d583-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d583-127">RELATED LINKS</span></span>

[<span data-ttu-id="6d583-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6d583-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="6d583-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d583-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="6d583-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6d583-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
