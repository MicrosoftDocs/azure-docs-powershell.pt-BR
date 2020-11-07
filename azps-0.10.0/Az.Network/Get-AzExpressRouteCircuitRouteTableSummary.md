---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 5042f7055c9d74dcabc01aa81169c9290816953c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775546"
---
# <span data-ttu-id="e09e2-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e09e2-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="e09e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e09e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e09e2-103">Obtém um resumo da tabela de rota de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e09e2-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="e09e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e09e2-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e09e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e09e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e09e2-106">O cmdlet **Get-AzExpressRouteCircuitRouteTableSummary** recupera um resumo das informações de vizinho BGP para um contexto de roteamento específico.</span><span class="sxs-lookup"><span data-stu-id="e09e2-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="e09e2-107">Essas informações são úteis para determinar por quanto tempo um contexto de roteamento foi estabelecido e o número de prefixos de rota anunciados pelo roteador de emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="e09e2-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="e09e2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e09e2-108">EXAMPLES</span></span>

### <span data-ttu-id="e09e2-109">Exemplo 1: exibir o resumo da rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="e09e2-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="e09e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="e09e2-110">PARAMETERS</span></span>

### <span data-ttu-id="e09e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09e2-111">-DefaultProfile</span></span>
<span data-ttu-id="e09e2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e09e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e09e2-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="e09e2-113">-DevicePath</span></span>
<span data-ttu-id="e09e2-114">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="e09e2-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="e09e2-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="e09e2-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="e09e2-116">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="e09e2-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="e09e2-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e09e2-117">-PeeringType</span></span>
<span data-ttu-id="e09e2-118">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e09e2-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="e09e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e09e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="e09e2-120">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e09e2-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e09e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09e2-121">CommonParameters</span></span>
<span data-ttu-id="e09e2-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e09e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09e2-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e09e2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09e2-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e09e2-124">INPUTS</span></span>

## <span data-ttu-id="e09e2-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e09e2-125">OUTPUTS</span></span>

### <span data-ttu-id="e09e2-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="e09e2-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="e09e2-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e09e2-127">NOTES</span></span>

## <span data-ttu-id="e09e2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e09e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="e09e2-129">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e09e2-129">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="e09e2-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e09e2-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="e09e2-131">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="e09e2-131">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
