---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: d2be2927be03895f80a537f70e80c53e246e16f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432193"
---
# <span data-ttu-id="d5f83-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d5f83-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="d5f83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5f83-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f83-103">Obtém uma tabela de rota de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d5f83-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5f83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5f83-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5f83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5f83-105">DESCRIPTION</span></span>
<span data-ttu-id="d5f83-106">O cmdlet **Get-AzureRmExpressRouteCircuitRouteTable** recupera uma tabela de rotas detalhadas de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d5f83-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="d5f83-107">A tabela de rota mostrará todas as rotas ou poderá ser filtrada para mostrar rotas para um tipo de emparelhamento específico.</span><span class="sxs-lookup"><span data-stu-id="d5f83-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="d5f83-108">Você pode usar a tabela de rotas para validar a configuração e a conectividade de pares.</span><span class="sxs-lookup"><span data-stu-id="d5f83-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="d5f83-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5f83-109">EXAMPLES</span></span>

### <span data-ttu-id="d5f83-110">Exemplo 1: exibir a tabela de rota para o caminho principal</span><span class="sxs-lookup"><span data-stu-id="d5f83-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="d5f83-111">OS</span><span class="sxs-lookup"><span data-stu-id="d5f83-111">PARAMETERS</span></span>

### <span data-ttu-id="d5f83-112">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="d5f83-112">-DevicePath</span></span>
<span data-ttu-id="d5f83-113">Os valores aceitáveis para esse parâmetro são: `Primary` ou `Secondary`</span><span class="sxs-lookup"><span data-stu-id="d5f83-113">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="d5f83-114">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="d5f83-114">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="d5f83-115">O nome do circuito do ExpressRoute sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="d5f83-115">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="d5f83-116">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d5f83-116">-PeeringType</span></span>
<span data-ttu-id="d5f83-117">Os valores aceitáveis para esse parâmetro são: `AzurePrivatePeering` , `AzurePublicPeering` , e `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d5f83-117">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d5f83-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f83-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5f83-119">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d5f83-119">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="d5f83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f83-120">-DefaultProfile</span></span>
<span data-ttu-id="d5f83-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f83-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f83-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f83-122">CommonParameters</span></span>
<span data-ttu-id="d5f83-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f83-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f83-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f83-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f83-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5f83-125">INPUTS</span></span>

## <span data-ttu-id="d5f83-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5f83-126">OUTPUTS</span></span>

### <span data-ttu-id="d5f83-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="d5f83-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="d5f83-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5f83-128">NOTES</span></span>

## <span data-ttu-id="d5f83-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5f83-129">RELATED LINKS</span></span>

[<span data-ttu-id="d5f83-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d5f83-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="d5f83-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d5f83-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="d5f83-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="d5f83-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)