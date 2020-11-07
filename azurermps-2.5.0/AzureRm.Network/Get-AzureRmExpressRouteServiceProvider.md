---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785712"
---
# <span data-ttu-id="62bd0-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="62bd0-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="62bd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="62bd0-103">Obtém uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="62bd0-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62bd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62bd0-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62bd0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="62bd0-106">O cmdlet **Get-AzureRmExpressRouteServiceProvider** recupera uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="62bd0-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="62bd0-107">Inclua as opções de localização e largura de banda.</span><span class="sxs-lookup"><span data-stu-id="62bd0-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="62bd0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62bd0-108">EXAMPLES</span></span>

### <span data-ttu-id="62bd0-109">Exemplo 1: obter uma lista de provedores de serviços com locais em "vale do silício"</span><span class="sxs-lookup"><span data-stu-id="62bd0-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="62bd0-110">OS</span><span class="sxs-lookup"><span data-stu-id="62bd0-110">PARAMETERS</span></span>

### <span data-ttu-id="62bd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bd0-111">-DefaultProfile</span></span>
<span data-ttu-id="62bd0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62bd0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62bd0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bd0-113">CommonParameters</span></span>
<span data-ttu-id="62bd0-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bd0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bd0-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62bd0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bd0-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62bd0-116">INPUTS</span></span>

## <span data-ttu-id="62bd0-117">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62bd0-117">OUTPUTS</span></span>

### <span data-ttu-id="62bd0-118">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="62bd0-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="62bd0-119">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62bd0-119">NOTES</span></span>

## <span data-ttu-id="62bd0-120">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62bd0-120">RELATED LINKS</span></span>

[<span data-ttu-id="62bd0-121">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="62bd0-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="62bd0-122">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="62bd0-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="62bd0-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="62bd0-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="62bd0-124">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="62bd0-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
