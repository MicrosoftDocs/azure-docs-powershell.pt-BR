---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113436"
---
# <span data-ttu-id="94187-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="94187-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="94187-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94187-102">SYNOPSIS</span></span>
<span data-ttu-id="94187-103">Modifica um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="94187-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="94187-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94187-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94187-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="94187-105">DESCRIPTION</span></span>
<span data-ttu-id="94187-106">O cmdlet **Set-AzExpressRoute Circuit** salva o circuito do ExpressRoute modificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="94187-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="94187-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94187-107">EXAMPLES</span></span>

### <span data-ttu-id="94187-108">Exemplo 1: Alterar a ServiceKey de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="94187-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="94187-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94187-109">PARAMETERS</span></span>

### <span data-ttu-id="94187-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94187-110">-AsJob</span></span>
<span data-ttu-id="94187-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="94187-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94187-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94187-112">-DefaultProfile</span></span>
<span data-ttu-id="94187-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="94187-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94187-114">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="94187-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="94187-115">Especifica o **objeto ExpressRoute Circuit** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="94187-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="94187-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94187-116">CommonParameters</span></span>
<span data-ttu-id="94187-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94187-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94187-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94187-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94187-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="94187-119">INPUTS</span></span>

### <span data-ttu-id="94187-120">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="94187-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="94187-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="94187-121">OUTPUTS</span></span>

### <span data-ttu-id="94187-122">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="94187-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="94187-123">Notas</span><span class="sxs-lookup"><span data-stu-id="94187-123">NOTES</span></span>

## <span data-ttu-id="94187-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94187-124">RELATED LINKS</span></span>

[<span data-ttu-id="94187-125">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="94187-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="94187-126">Move-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="94187-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="94187-127">New-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="94187-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="94187-128">Remove-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="94187-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
