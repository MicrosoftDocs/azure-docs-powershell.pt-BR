---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111101"
---
# <span data-ttu-id="64746-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="64746-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="64746-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64746-102">SYNOPSIS</span></span>
<span data-ttu-id="64746-103">Obtém estatísticas de uso de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64746-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="64746-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64746-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64746-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64746-105">DESCRIPTION</span></span>
<span data-ttu-id="64746-106">O cmdlet **Get-AzExpressRouteCircuitStat** recupera estatísticas de tráfego para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64746-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="64746-107">As estatísticas incluem o número de bytes enviados e recebidos por rotas primárias e secundárias.</span><span class="sxs-lookup"><span data-stu-id="64746-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="64746-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64746-108">EXAMPLES</span></span>

### <span data-ttu-id="64746-109">Exemplo 1: exibir as estatísticas de tráfego para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="64746-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="64746-110">OS</span><span class="sxs-lookup"><span data-stu-id="64746-110">PARAMETERS</span></span>

### <span data-ttu-id="64746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64746-111">-DefaultProfile</span></span>
<span data-ttu-id="64746-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64746-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64746-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="64746-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="64746-114">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="64746-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="64746-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="64746-115">-PeeringType</span></span>
<span data-ttu-id="64746-116">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="64746-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="64746-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64746-117">-ResourceGroupName</span></span>
<span data-ttu-id="64746-118">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64746-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="64746-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64746-119">CommonParameters</span></span>
<span data-ttu-id="64746-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64746-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64746-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64746-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64746-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64746-122">INPUTS</span></span>

### <span data-ttu-id="64746-123">System. String</span><span class="sxs-lookup"><span data-stu-id="64746-123">System.String</span></span>

## <span data-ttu-id="64746-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64746-124">OUTPUTS</span></span>

### <span data-ttu-id="64746-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="64746-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="64746-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64746-126">NOTES</span></span>

## <span data-ttu-id="64746-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64746-127">RELATED LINKS</span></span>

[<span data-ttu-id="64746-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="64746-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="64746-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="64746-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="64746-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="64746-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
