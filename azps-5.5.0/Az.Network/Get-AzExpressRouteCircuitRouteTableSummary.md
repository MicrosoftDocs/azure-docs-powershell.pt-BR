---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115190"
---
# <span data-ttu-id="990da-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="990da-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="990da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="990da-102">SYNOPSIS</span></span>
<span data-ttu-id="990da-103">Obtém um resumo da tabela de rota de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="990da-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="990da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="990da-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="990da-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="990da-105">DESCRIPTION</span></span>
<span data-ttu-id="990da-106">O cmdlet **Get-AzExpressRoute CircuitRouteTableSummary** recupera um resumo das informações do vizinhos BGP para um contexto de roteamento específico.</span><span class="sxs-lookup"><span data-stu-id="990da-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="990da-107">Essas informações são úteis para determinar por quanto tempo um contexto de roteamento foi estabelecido e o número de prefixos de rota anunciados pelo roteador de paridade.</span><span class="sxs-lookup"><span data-stu-id="990da-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="990da-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="990da-108">EXAMPLES</span></span>

### <span data-ttu-id="990da-109">Exemplo 1: Exibir o resumo da rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="990da-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="990da-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="990da-110">PARAMETERS</span></span>

### <span data-ttu-id="990da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="990da-111">-DefaultProfile</span></span>
<span data-ttu-id="990da-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="990da-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="990da-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="990da-113">-DevicePath</span></span>
<span data-ttu-id="990da-114">Os valores aceitáveis para este parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="990da-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="990da-115">-ExpressRoute CircuitName</span><span class="sxs-lookup"><span data-stu-id="990da-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="990da-116">O nome do circuito do ExpressRoute que está sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="990da-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="990da-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="990da-117">-PeeringType</span></span>
<span data-ttu-id="990da-118">Os valores aceitáveis para este parâmetro são: `AzurePrivatePeering` `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="990da-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="990da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="990da-119">-ResourceGroupName</span></span>
<span data-ttu-id="990da-120">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="990da-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="990da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="990da-121">CommonParameters</span></span>
<span data-ttu-id="990da-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="990da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="990da-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="990da-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="990da-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="990da-124">INPUTS</span></span>

### <span data-ttu-id="990da-125">System.String</span><span class="sxs-lookup"><span data-stu-id="990da-125">System.String</span></span>

## <span data-ttu-id="990da-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="990da-126">OUTPUTS</span></span>

### <span data-ttu-id="990da-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoute CircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="990da-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="990da-128">Notas</span><span class="sxs-lookup"><span data-stu-id="990da-128">NOTES</span></span>

## <span data-ttu-id="990da-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="990da-129">RELATED LINKS</span></span>

[<span data-ttu-id="990da-130">Tabela Get-AzExpressRoute CircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="990da-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="990da-131">Get-AzExpressRoute CircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="990da-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="990da-132">Get-AzExpressRoute CircuitStat</span><span class="sxs-lookup"><span data-stu-id="990da-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
