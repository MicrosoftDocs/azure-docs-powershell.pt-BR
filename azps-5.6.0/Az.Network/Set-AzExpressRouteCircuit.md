---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 71571d9fe6eccee73efda01015a877014c67c9ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885393"
---
# <span data-ttu-id="d3020-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="d3020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3020-102">SYNOPSIS</span></span>
<span data-ttu-id="d3020-103">Modifica um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d3020-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d3020-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3020-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3020-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3020-105">DESCRIPTION</span></span>
<span data-ttu-id="d3020-106">O cmdlet **Set-AzExpressRouteCircuit** salva o circuito ExpressRoute modificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="d3020-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="d3020-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3020-107">EXAMPLES</span></span>

### <span data-ttu-id="d3020-108">Exemplo 1: Alterar a ServiceKey de um circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d3020-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="d3020-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3020-109">PARAMETERS</span></span>

### <span data-ttu-id="d3020-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3020-110">-AsJob</span></span>
<span data-ttu-id="d3020-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d3020-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3020-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3020-112">-DefaultProfile</span></span>
<span data-ttu-id="d3020-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d3020-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3020-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d3020-115">Especifica o **objeto ExpressRouteCircuit** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d3020-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3020-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3020-116">CommonParameters</span></span>
<span data-ttu-id="d3020-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3020-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3020-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3020-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3020-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3020-119">INPUTS</span></span>

### <span data-ttu-id="d3020-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d3020-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3020-121">OUTPUTS</span></span>

### <span data-ttu-id="d3020-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d3020-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3020-123">NOTES</span></span>

## <span data-ttu-id="d3020-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3020-124">RELATED LINKS</span></span>

[<span data-ttu-id="d3020-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d3020-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="d3020-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="d3020-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d3020-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
