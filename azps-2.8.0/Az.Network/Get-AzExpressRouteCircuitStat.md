---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 463c1bf9e97d3e438b89cee1e87279ad4bf06ad9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772029"
---
# <span data-ttu-id="74cc9-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="74cc9-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="74cc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="74cc9-103">Obtém estatísticas de uso de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="74cc9-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="74cc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74cc9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74cc9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="74cc9-106">O cmdlet **Get-AzExpressRouteCircuitStat** recupera estatísticas de tráfego para um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="74cc9-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="74cc9-107">As estatísticas incluem o número de bytes enviados e recebidos por rotas primárias e secundárias.</span><span class="sxs-lookup"><span data-stu-id="74cc9-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="74cc9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74cc9-108">EXAMPLES</span></span>

### <span data-ttu-id="74cc9-109">Exemplo 1: exibir as estatísticas de tráfego para um par ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="74cc9-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="74cc9-110">OS</span><span class="sxs-lookup"><span data-stu-id="74cc9-110">PARAMETERS</span></span>

### <span data-ttu-id="74cc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74cc9-111">-DefaultProfile</span></span>
<span data-ttu-id="74cc9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74cc9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74cc9-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="74cc9-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="74cc9-114">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="74cc9-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="74cc9-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="74cc9-115">-PeeringType</span></span>
<span data-ttu-id="74cc9-116">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="74cc9-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="74cc9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74cc9-117">-ResourceGroupName</span></span>
<span data-ttu-id="74cc9-118">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="74cc9-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="74cc9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74cc9-119">CommonParameters</span></span>
<span data-ttu-id="74cc9-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74cc9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74cc9-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74cc9-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74cc9-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74cc9-122">INPUTS</span></span>

### <span data-ttu-id="74cc9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="74cc9-123">System.String</span></span>

## <span data-ttu-id="74cc9-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74cc9-124">OUTPUTS</span></span>

### <span data-ttu-id="74cc9-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="74cc9-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="74cc9-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74cc9-126">NOTES</span></span>

## <span data-ttu-id="74cc9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74cc9-127">RELATED LINKS</span></span>

[<span data-ttu-id="74cc9-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="74cc9-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="74cc9-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="74cc9-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="74cc9-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="74cc9-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
