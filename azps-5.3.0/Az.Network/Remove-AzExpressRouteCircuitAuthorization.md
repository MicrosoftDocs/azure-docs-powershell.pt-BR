---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271691"
---
# <span data-ttu-id="316f8-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="316f8-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="316f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="316f8-102">SYNOPSIS</span></span>
<span data-ttu-id="316f8-103">Remove uma autorização de configuração do ExpressRoute existente.</span><span class="sxs-lookup"><span data-stu-id="316f8-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="316f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="316f8-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="316f8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="316f8-105">DESCRIPTION</span></span>
<span data-ttu-id="316f8-106">O cmdlet **Remove-AzExpressRouteCircuitAuthorization** remove uma autorização atribuída a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="316f8-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="316f8-107">Os circuitos do ExpressRoute conectam a sua rede local ao Azure usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="316f8-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="316f8-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito.</span><span class="sxs-lookup"><span data-stu-id="316f8-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="316f8-109">Só pode haver uma autorização por rede virtual.</span><span class="sxs-lookup"><span data-stu-id="316f8-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="316f8-110">No entanto, a qualquer momento, o proprietário do circuito pode usar **Remove-AzExpressRouteCircuitAuthorization** para remover a autorização atribuída a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="316f8-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="316f8-111">Quando isso acontece, a rede virtual correspondente não consegue mais usar o circuito do ExpressRoute para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="316f8-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="316f8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="316f8-112">EXAMPLES</span></span>

### <span data-ttu-id="316f8-113">Exemplo 1: remover a autorização de um circuito de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="316f8-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="316f8-114">Este exemplo remove uma autorização de circuito de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="316f8-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="316f8-115">O primeiro comando usa o cmdlet **Get-AzExpressRouteCircuit** para criar uma referência de objeto para um circuito do ExpressRoute chamado ContosoCircuit e armazena o resultado na variável chamada $Circuit.</span><span class="sxs-lookup"><span data-stu-id="316f8-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="316f8-116">O segundo comando marca a ContosoCircuitAuthorization de autorização de circuito para remoção.</span><span class="sxs-lookup"><span data-stu-id="316f8-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="316f8-117">O terceiro comando usa o cmdlet Set-AzExpressRouteCircuit para confirmar a remoção do circuito do ExpressRoute armazenado na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="316f8-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="316f8-118">OS</span><span class="sxs-lookup"><span data-stu-id="316f8-118">PARAMETERS</span></span>

### <span data-ttu-id="316f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316f8-119">-DefaultProfile</span></span>
<span data-ttu-id="316f8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="316f8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="316f8-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="316f8-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="316f8-122">Especifica o objeto ExpressRouteCircuit que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="316f8-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="316f8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="316f8-123">-Name</span></span>
<span data-ttu-id="316f8-124">Especifica o nome da autorização de circuito que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="316f8-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="316f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316f8-125">CommonParameters</span></span>
<span data-ttu-id="316f8-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316f8-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316f8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316f8-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="316f8-128">INPUTS</span></span>

### <span data-ttu-id="316f8-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="316f8-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="316f8-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="316f8-130">OUTPUTS</span></span>

### <span data-ttu-id="316f8-131">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="316f8-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="316f8-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="316f8-132">NOTES</span></span>

## <span data-ttu-id="316f8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="316f8-133">RELATED LINKS</span></span>

[<span data-ttu-id="316f8-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="316f8-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="316f8-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="316f8-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="316f8-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="316f8-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="316f8-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="316f8-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="316f8-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="316f8-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
