---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: c27ac0c2a56000465b70810ca1e957b882fa3357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886006"
---
# <span data-ttu-id="4ca7f-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="4ca7f-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="4ca7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ca7f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca7f-103">Obtém uma lista de provedores de serviços ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="4ca7f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4ca7f-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca7f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4ca7f-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca7f-106">O cmdlet **Get-AzExpressRouteServiceProvider** recupera uma lista de provedores de serviços ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="4ca7f-107">O atributo inclui opções de localização e largura de banda.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="4ca7f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ca7f-108">EXAMPLES</span></span>

### <span data-ttu-id="4ca7f-109">Exemplo 1: Obter uma lista de provedor de serviços com locais em "Vale do Silício"</span><span class="sxs-lookup"><span data-stu-id="4ca7f-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="4ca7f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4ca7f-110">PARAMETERS</span></span>

### <span data-ttu-id="4ca7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca7f-111">-DefaultProfile</span></span>
<span data-ttu-id="4ca7f-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ca7f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca7f-113">CommonParameters</span></span>
<span data-ttu-id="4ca7f-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca7f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca7f-115">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ca7f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca7f-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ca7f-116">INPUTS</span></span>

### <span data-ttu-id="4ca7f-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4ca7f-117">None</span></span>

## <span data-ttu-id="4ca7f-118">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4ca7f-118">OUTPUTS</span></span>

### <span data-ttu-id="4ca7f-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="4ca7f-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="4ca7f-120">NOTES</span><span class="sxs-lookup"><span data-stu-id="4ca7f-120">NOTES</span></span>

## <span data-ttu-id="4ca7f-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ca7f-121">RELATED LINKS</span></span>

[<span data-ttu-id="4ca7f-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4ca7f-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="4ca7f-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ca7f-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="4ca7f-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4ca7f-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="4ca7f-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="4ca7f-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
