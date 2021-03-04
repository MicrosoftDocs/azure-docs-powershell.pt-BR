---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885424"
---
# <span data-ttu-id="febe0-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="febe0-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="febe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="febe0-102">SYNOPSIS</span></span>
<span data-ttu-id="febe0-103">Adiciona uma autorização de circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="febe0-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="febe0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="febe0-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="febe0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="febe0-105">DESCRIPTION</span></span>
<span data-ttu-id="febe0-106">O cmdlet **Add-AzExpressRouteCircuitAuthorization** adiciona uma autorização a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="febe0-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="febe0-107">Os circuitos ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="febe0-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="febe0-108">O proprietário de um circuito ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="febe0-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="febe0-109">**Add-AzExpressRouteCircuitAuthorization** adiciona uma nova autorização a um circuito e, ao mesmo tempo, gera a chave de autorização correspondente.</span><span class="sxs-lookup"><span data-stu-id="febe0-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="febe0-110">Essas chaves podem ser exibidas a qualquer momento executando o cmdlet Get-AzExpressRouteCircuitAuthorization e, conforme necessário, podem ser copiadas e encaminhadas para o proprietário da rede apropriado.</span><span class="sxs-lookup"><span data-stu-id="febe0-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="febe0-111">Observe que, depois de executar **Add-AzExpressRouteCircuitAuthorization,** você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a chave.</span><span class="sxs-lookup"><span data-stu-id="febe0-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="febe0-112">Se você não chamar **Set-AzExpressRouteCircuit,** a autorização será adicionada ao circuito, mas não estará habilitada para uso.</span><span class="sxs-lookup"><span data-stu-id="febe0-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="febe0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="febe0-113">EXAMPLES</span></span>

### <span data-ttu-id="febe0-114">Exemplo 1: Adicionar uma autorização ao circuito ExpressRoute especificado</span><span class="sxs-lookup"><span data-stu-id="febe0-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="febe0-115">Os comandos neste exemplo adicionam uma nova autorização a um circuito ExpressRoute existente.</span><span class="sxs-lookup"><span data-stu-id="febe0-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="febe0-116">O primeiro comando usa **Get-AzExpressRouteCircuit** para criar uma referência de objeto a um circuito chamado ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="febe0-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="febe0-117">Essa referência de objeto é armazenada em uma variável chamada $Circuit.</span><span class="sxs-lookup"><span data-stu-id="febe0-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="febe0-118">No segundo comando, o cmdlet **Add-AzExpressRouteCircuitAuthorization** é usado para adicionar uma nova autorização (ContosoCircuitAuthorization) ao circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="febe0-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="febe0-119">Este comando adiciona a autorização, mas não ativa essa autorização.</span><span class="sxs-lookup"><span data-stu-id="febe0-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="febe0-120">A ativação de uma autorização requer **o Set-AzExpressRouteCircuit** mostrado no comando final no exemplo.</span><span class="sxs-lookup"><span data-stu-id="febe0-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="febe0-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="febe0-121">PARAMETERS</span></span>

### <span data-ttu-id="febe0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febe0-122">-DefaultProfile</span></span>
<span data-ttu-id="febe0-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="febe0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="febe0-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="febe0-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="febe0-125">Especifica o circuito ExpressRoute ao que este cmdlet adiciona a autorização.</span><span class="sxs-lookup"><span data-stu-id="febe0-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="febe0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="febe0-126">-Name</span></span>
<span data-ttu-id="febe0-127">Especifica o nome da autorização do circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="febe0-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febe0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febe0-128">CommonParameters</span></span>
<span data-ttu-id="febe0-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febe0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febe0-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febe0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febe0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="febe0-131">INPUTS</span></span>

### <span data-ttu-id="febe0-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="febe0-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="febe0-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="febe0-133">OUTPUTS</span></span>

### <span data-ttu-id="febe0-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="febe0-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="febe0-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="febe0-135">NOTES</span></span>

## <span data-ttu-id="febe0-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="febe0-136">RELATED LINKS</span></span>

[<span data-ttu-id="febe0-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="febe0-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="febe0-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="febe0-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="febe0-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="febe0-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="febe0-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="febe0-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="febe0-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="febe0-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
