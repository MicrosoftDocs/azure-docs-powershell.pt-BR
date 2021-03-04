---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2adb971d2e44f844fe52bb83a9ce834bbebe1897
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891153"
---
# <span data-ttu-id="e69e2-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e69e2-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="e69e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e69e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e69e2-103">Remove uma autorização de configuração do ExpressRoute existente.</span><span class="sxs-lookup"><span data-stu-id="e69e2-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="e69e2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e69e2-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e69e2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e69e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e69e2-106">O cmdlet **Remove-AzExpressRouteCircuitAuthorization** remove uma autorização atribuída a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e69e2-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="e69e2-107">Os circuitos ExpressRoute conectam sua rede local ao Azure usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="e69e2-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="e69e2-108">O proprietário de um circuito ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito.</span><span class="sxs-lookup"><span data-stu-id="e69e2-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="e69e2-109">Só pode haver uma autorização por rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e69e2-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="e69e2-110">No entanto, a qualquer momento, o proprietário do circuito pode usar **Remove-AzExpressRouteCircuitAuthorization** para remover a autorização atribuída a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e69e2-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="e69e2-111">Quando isso acontece, a rede virtual correspondente não é mais capaz de usar o circuito ExpressRoute para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="e69e2-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="e69e2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e69e2-112">EXAMPLES</span></span>

### <span data-ttu-id="e69e2-113">Exemplo 1: Remover uma autorização de circuito de um circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e69e2-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="e69e2-114">Este exemplo remove uma autorização de circuito de um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e69e2-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="e69e2-115">O primeiro comando usa o cmdlet **Get-AzExpressRouteCircuit** para criar uma referência de objeto a um circuito ExpressRoute chamado ContosoCircuit e armazena o resultado na variável denominada $Circuit.</span><span class="sxs-lookup"><span data-stu-id="e69e2-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="e69e2-116">O segundo comando marca a autorização de circuito ContosoCircuitAuthorization para remoção.</span><span class="sxs-lookup"><span data-stu-id="e69e2-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="e69e2-117">O terceiro comando usa o cmdlet Set-AzExpressRouteCircuit para confirmar a remoção do circuito ExpressRoute armazenado na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="e69e2-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="e69e2-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e69e2-118">PARAMETERS</span></span>

### <span data-ttu-id="e69e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69e2-119">-DefaultProfile</span></span>
<span data-ttu-id="e69e2-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e69e2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e69e2-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e69e2-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e69e2-122">Especifica o objeto ExpressRouteCircuit que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e69e2-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e69e2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e69e2-123">-Name</span></span>
<span data-ttu-id="e69e2-124">Especifica o nome da autorização de circuito que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="e69e2-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69e2-125">CommonParameters</span></span>
<span data-ttu-id="e69e2-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e69e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69e2-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e69e2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69e2-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e69e2-128">INPUTS</span></span>

### <span data-ttu-id="e69e2-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e69e2-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e69e2-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e69e2-130">OUTPUTS</span></span>

### <span data-ttu-id="e69e2-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e69e2-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e69e2-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="e69e2-132">NOTES</span></span>

## <span data-ttu-id="e69e2-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e69e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="e69e2-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e69e2-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e69e2-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e69e2-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e69e2-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e69e2-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e69e2-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="e69e2-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="e69e2-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e69e2-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
