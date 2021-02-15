---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115211"
---
# <span data-ttu-id="46f7d-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="46f7d-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="46f7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="46f7d-103">Adiciona uma autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="46f7d-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="46f7d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46f7d-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46f7d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="46f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="46f7d-106">O **cmdlet Add-AzExpressRoute CircuitAuthorization** adiciona uma autorização a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="46f7d-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="46f7d-107">Os circuitos do ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="46f7d-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="46f7d-108">O proprietário de um circuito do ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="46f7d-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="46f7d-109">**O Add-AzExpressRoute CircuitAuthorization** adiciona uma nova autorização a um circuito e, ao mesmo tempo, gera a chave de autorização correspondente.</span><span class="sxs-lookup"><span data-stu-id="46f7d-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="46f7d-110">Essas teclas podem ser exibidas a qualquer momento executando o cmdlet Get-AzExpressRouteCircuitAuthorization e, conforme necessário, podem ser copiadas e encaminhadas para o proprietário da rede apropriado.</span><span class="sxs-lookup"><span data-stu-id="46f7d-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="46f7d-111">Observe que, depois de executar **o Add-AzExpressRoute CircuitAuthorization,** você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a chave.</span><span class="sxs-lookup"><span data-stu-id="46f7d-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="46f7d-112">Se você não ligar para **Set-AzExpressRoute Circuit,** a autorização será adicionada ao circuito, mas não será habilitada para uso.</span><span class="sxs-lookup"><span data-stu-id="46f7d-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="46f7d-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46f7d-113">EXAMPLES</span></span>

### <span data-ttu-id="46f7d-114">Exemplo 1: Adicionar uma autorização ao circuito do ExpressRoute especificado</span><span class="sxs-lookup"><span data-stu-id="46f7d-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="46f7d-115">Os comandos neste exemplo adicionam uma nova autorização a um circuito do ExpressRoute existente.</span><span class="sxs-lookup"><span data-stu-id="46f7d-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="46f7d-116">O primeiro comando usa **Get-AzExpressRoute Circuit** para criar uma referência de objeto a um circuito chamado Contoso Circuit.</span><span class="sxs-lookup"><span data-stu-id="46f7d-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="46f7d-117">Essa referência de objeto é armazenada em uma variável chamada $Circuit.</span><span class="sxs-lookup"><span data-stu-id="46f7d-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="46f7d-118">No segundo comando, o cmdlet **Add-AzExpressRoute CircuitAuthorization** é usado para adicionar uma nova autorização (Contoso CircuitAuthorization) ao circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="46f7d-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="46f7d-119">Esse comando adiciona a autorização, mas não ativa essa autorização.</span><span class="sxs-lookup"><span data-stu-id="46f7d-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="46f7d-120">A ativação de uma autorização requer **o Set-AzExpressRoute Circuit** mostrado no comando final no exemplo.</span><span class="sxs-lookup"><span data-stu-id="46f7d-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="46f7d-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46f7d-121">PARAMETERS</span></span>

### <span data-ttu-id="46f7d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f7d-122">-DefaultProfile</span></span>
<span data-ttu-id="46f7d-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="46f7d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46f7d-124">-ExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="46f7d-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="46f7d-125">Especifica o circuito do ExpressRoute ao que este cmdlet adiciona a autorização.</span><span class="sxs-lookup"><span data-stu-id="46f7d-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="46f7d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="46f7d-126">-Name</span></span>
<span data-ttu-id="46f7d-127">Especifica o nome da autorização de circuito a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="46f7d-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="46f7d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f7d-128">CommonParameters</span></span>
<span data-ttu-id="46f7d-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f7d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f7d-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f7d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f7d-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="46f7d-131">INPUTS</span></span>

### <span data-ttu-id="46f7d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="46f7d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="46f7d-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="46f7d-133">OUTPUTS</span></span>

### <span data-ttu-id="46f7d-134">Microsoft.Azure.Commands.Network.Models.PSExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="46f7d-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="46f7d-135">Notas</span><span class="sxs-lookup"><span data-stu-id="46f7d-135">NOTES</span></span>

## <span data-ttu-id="46f7d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46f7d-136">RELATED LINKS</span></span>

[<span data-ttu-id="46f7d-137">Get-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="46f7d-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="46f7d-138">Get-AzExpressRoute CircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="46f7d-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="46f7d-139">New-AzExpressRoute CircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="46f7d-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="46f7d-140">Remove-AzExpressRoute CircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="46f7d-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="46f7d-141">Set-AzExpressRoute Circuit</span><span class="sxs-lookup"><span data-stu-id="46f7d-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
