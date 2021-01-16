---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260128"
---
# <span data-ttu-id="f5ab5-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f5ab5-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="f5ab5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ab5-103">Obtém uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="f5ab5-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="f5ab5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5ab5-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5ab5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ab5-106">O cmdlet **Get-AzExpressRouteServiceProvider** recupera uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="f5ab5-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="f5ab5-107">Inclua as opções de localização e largura de banda.</span><span class="sxs-lookup"><span data-stu-id="f5ab5-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="f5ab5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5ab5-108">EXAMPLES</span></span>

### <span data-ttu-id="f5ab5-109">Exemplo 1: obter uma lista de provedores de serviços com locais em "vale do silício"</span><span class="sxs-lookup"><span data-stu-id="f5ab5-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="f5ab5-110">OS</span><span class="sxs-lookup"><span data-stu-id="f5ab5-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ab5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ab5-111">-DefaultProfile</span></span>
<span data-ttu-id="f5ab5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ab5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5ab5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ab5-113">CommonParameters</span></span>
<span data-ttu-id="f5ab5-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ab5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ab5-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5ab5-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ab5-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5ab5-116">INPUTS</span></span>

### <span data-ttu-id="f5ab5-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f5ab5-117">None</span></span>

## <span data-ttu-id="f5ab5-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5ab5-118">OUTPUTS</span></span>

### <span data-ttu-id="f5ab5-119">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="f5ab5-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="f5ab5-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5ab5-120">NOTES</span></span>

## <span data-ttu-id="f5ab5-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5ab5-121">RELATED LINKS</span></span>

[<span data-ttu-id="f5ab5-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f5ab5-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="f5ab5-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f5ab5-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="f5ab5-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f5ab5-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="f5ab5-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="f5ab5-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
