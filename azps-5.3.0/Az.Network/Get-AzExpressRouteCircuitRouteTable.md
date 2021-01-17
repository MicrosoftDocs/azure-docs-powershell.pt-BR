---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 3067df10f3cd1d49b519d6c83defe304fbcf0296
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427030"
---
# <span data-ttu-id="018a6-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="018a6-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="018a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="018a6-102">SYNOPSIS</span></span>
<span data-ttu-id="018a6-103">Obtém uma tabela de rota de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="018a6-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="018a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="018a6-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="018a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="018a6-105">DESCRIPTION</span></span>
<span data-ttu-id="018a6-106">O cmdlet **Get-AzExpressRouteCircuitRouteTable** recupera uma tabela de rotas detalhadas de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="018a6-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="018a6-107">A tabela de rota mostrará todas as rotas ou poderá ser filtrada para mostrar rotas para um tipo de emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="018a6-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="018a6-108">Você pode usar a tabela de rotas para validar a configuração e a conectividade de pares.</span><span class="sxs-lookup"><span data-stu-id="018a6-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="018a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="018a6-109">EXAMPLES</span></span>

### <span data-ttu-id="018a6-110">Exemplo 1: exibir a tabela de rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="018a6-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="018a6-111">OS</span><span class="sxs-lookup"><span data-stu-id="018a6-111">PARAMETERS</span></span>

### <span data-ttu-id="018a6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018a6-112">-DefaultProfile</span></span>
<span data-ttu-id="018a6-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="018a6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="018a6-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="018a6-114">-DevicePath</span></span>
<span data-ttu-id="018a6-115">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="018a6-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="018a6-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="018a6-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="018a6-117">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="018a6-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="018a6-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="018a6-118">-PeeringType</span></span>
<span data-ttu-id="018a6-119">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="018a6-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="018a6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018a6-120">-ResourceGroupName</span></span>
<span data-ttu-id="018a6-121">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="018a6-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="018a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018a6-122">CommonParameters</span></span>
<span data-ttu-id="018a6-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018a6-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="018a6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018a6-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="018a6-125">INPUTS</span></span>

### <span data-ttu-id="018a6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="018a6-126">System.String</span></span>

## <span data-ttu-id="018a6-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="018a6-127">OUTPUTS</span></span>

### <span data-ttu-id="018a6-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="018a6-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="018a6-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="018a6-129">NOTES</span></span>

## <span data-ttu-id="018a6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="018a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="018a6-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="018a6-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="018a6-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="018a6-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="018a6-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="018a6-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
