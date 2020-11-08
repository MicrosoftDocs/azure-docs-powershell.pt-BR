---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111104"
---
# <span data-ttu-id="2d8b4-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d8b4-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="2d8b4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8b4-103">Obtém um resumo da tabela de rota de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2d8b4-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2d8b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d8b4-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d8b4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="2d8b4-106">O cmdlet **Get-AzExpressRouteCircuitRouteTableSummary** recupera um resumo das informações de vizinho BGP para um contexto de roteamento específico.</span><span class="sxs-lookup"><span data-stu-id="2d8b4-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="2d8b4-107">Essas informações são úteis para determinar por quanto tempo um contexto de roteamento foi estabelecido e o número de prefixos de rota anunciados pelo roteador de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="2d8b4-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="2d8b4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d8b4-108">EXAMPLES</span></span>

### <span data-ttu-id="2d8b4-109">Exemplo 1: exibir o resumo da rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="2d8b4-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="2d8b4-110">OS</span><span class="sxs-lookup"><span data-stu-id="2d8b4-110">PARAMETERS</span></span>

### <span data-ttu-id="2d8b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d8b4-111">-DefaultProfile</span></span>
<span data-ttu-id="2d8b4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d8b4-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="2d8b4-113">-DevicePath</span></span>
<span data-ttu-id="2d8b4-114">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="2d8b4-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="2d8b4-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="2d8b4-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="2d8b4-116">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="2d8b4-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="2d8b4-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2d8b4-117">-PeeringType</span></span>
<span data-ttu-id="2d8b4-118">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2d8b4-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2d8b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d8b4-120">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2d8b4-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2d8b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8b4-121">CommonParameters</span></span>
<span data-ttu-id="2d8b4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d8b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8b4-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d8b4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8b4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d8b4-124">INPUTS</span></span>

### <span data-ttu-id="2d8b4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2d8b4-125">System.String</span></span>

## <span data-ttu-id="2d8b4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d8b4-126">OUTPUTS</span></span>

### <span data-ttu-id="2d8b4-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d8b4-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="2d8b4-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d8b4-128">NOTES</span></span>

## <span data-ttu-id="2d8b4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d8b4-129">RELATED LINKS</span></span>

[<span data-ttu-id="2d8b4-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2d8b4-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="2d8b4-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d8b4-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="2d8b4-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="2d8b4-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
