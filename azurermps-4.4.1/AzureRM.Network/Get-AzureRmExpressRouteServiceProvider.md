---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: b321e55160d3a88c04e3a0587efb845c70028a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429260"
---
# <span data-ttu-id="abc8d-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="abc8d-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="abc8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="abc8d-103">Obtém uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="abc8d-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abc8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abc8d-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abc8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abc8d-105">DESCRIPTION</span></span>
<span data-ttu-id="abc8d-106">O cmdlet **Get-AzureRmExpressRouteServiceProvider** recupera uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="abc8d-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="abc8d-107">Inclua as opções de localização e largura de banda.</span><span class="sxs-lookup"><span data-stu-id="abc8d-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="abc8d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abc8d-108">EXAMPLES</span></span>

### <span data-ttu-id="abc8d-109">Exemplo 1: obter uma lista de provedores de serviços com locais em "vale do silício"</span><span class="sxs-lookup"><span data-stu-id="abc8d-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="abc8d-110">OS</span><span class="sxs-lookup"><span data-stu-id="abc8d-110">PARAMETERS</span></span>

### <span data-ttu-id="abc8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc8d-111">-DefaultProfile</span></span>
<span data-ttu-id="abc8d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abc8d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc8d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc8d-113">CommonParameters</span></span>
<span data-ttu-id="abc8d-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc8d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc8d-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc8d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc8d-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abc8d-116">INPUTS</span></span>

## <span data-ttu-id="abc8d-117">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abc8d-117">OUTPUTS</span></span>

### <span data-ttu-id="abc8d-118">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="abc8d-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="abc8d-119">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abc8d-119">NOTES</span></span>

## <span data-ttu-id="abc8d-120">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abc8d-120">RELATED LINKS</span></span>

[<span data-ttu-id="abc8d-121">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="abc8d-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="abc8d-122">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="abc8d-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="abc8d-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="abc8d-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="abc8d-124">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="abc8d-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
