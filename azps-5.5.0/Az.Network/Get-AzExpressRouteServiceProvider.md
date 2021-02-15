---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115189"
---
# <span data-ttu-id="e6b15-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="e6b15-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="e6b15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6b15-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b15-103">Obtém uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="e6b15-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="e6b15-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6b15-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b15-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6b15-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b15-106">O cmdlet **Get-AzExpressRouteServiceProvider** recupera uma lista de provedores de serviços do ExpressRoute e seus atributos.</span><span class="sxs-lookup"><span data-stu-id="e6b15-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="e6b15-107">O atributo inclui opções de localização e largura de banda.</span><span class="sxs-lookup"><span data-stu-id="e6b15-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="e6b15-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6b15-108">EXAMPLES</span></span>

### <span data-ttu-id="e6b15-109">Exemplo 1: Obter uma lista de provedor de serviços com locais no "Vale do Silício"</span><span class="sxs-lookup"><span data-stu-id="e6b15-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="e6b15-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6b15-110">PARAMETERS</span></span>

### <span data-ttu-id="e6b15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b15-111">-DefaultProfile</span></span>
<span data-ttu-id="e6b15-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e6b15-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6b15-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b15-113">CommonParameters</span></span>
<span data-ttu-id="e6b15-114">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b15-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b15-115">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6b15-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b15-116">Entradas</span><span class="sxs-lookup"><span data-stu-id="e6b15-116">INPUTS</span></span>

### <span data-ttu-id="e6b15-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e6b15-117">None</span></span>

## <span data-ttu-id="e6b15-118">Saídas</span><span class="sxs-lookup"><span data-stu-id="e6b15-118">OUTPUTS</span></span>

### <span data-ttu-id="e6b15-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="e6b15-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="e6b15-120">Notas</span><span class="sxs-lookup"><span data-stu-id="e6b15-120">NOTES</span></span>

## <span data-ttu-id="e6b15-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6b15-121">RELATED LINKS</span></span>

[<span data-ttu-id="e6b15-122">Tabela Get-AzExpressRoute CircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e6b15-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="e6b15-123">Get-AzExpressRoute CircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e6b15-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="e6b15-124">Get-AzExpressRoute CircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e6b15-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="e6b15-125">Get-AzExpressRoute CircuitStat</span><span class="sxs-lookup"><span data-stu-id="e6b15-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
