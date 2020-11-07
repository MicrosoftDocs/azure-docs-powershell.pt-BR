---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941107"
---
# <span data-ttu-id="640c0-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="640c0-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="640c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="640c0-102">SYNOPSIS</span></span>
<span data-ttu-id="640c0-103">Adiciona uma autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="640c0-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="640c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="640c0-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="640c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="640c0-105">DESCRIPTION</span></span>
<span data-ttu-id="640c0-106">O cmdlet **Add-AzExpressRouteCircuitAuthorization** adiciona uma autorização a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="640c0-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="640c0-107">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="640c0-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="640c0-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="640c0-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="640c0-109">**Add-AzExpressRouteCircuitAuthorization** adiciona uma nova autorização a um circuito e, ao mesmo tempo, gera a chave de autorização correspondente.</span><span class="sxs-lookup"><span data-stu-id="640c0-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="640c0-110">Essas chaves podem ser visualizadas a qualquer momento executando o cmdlet Get-AzExpressRouteCircuitAuthorization e, conforme necessário, podem ser copiados e encaminhados para o proprietário da rede apropriado.</span><span class="sxs-lookup"><span data-stu-id="640c0-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="640c0-111">Observe que, depois de executar **Add-AzExpressRouteCircuitAuthorization** , você deve chamar o cmdlet Set-AzExpressRouteCircuit para ativar a chave.</span><span class="sxs-lookup"><span data-stu-id="640c0-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="640c0-112">Se você não chamar **set-AzExpressRouteCircuit** , a autorização será adicionada ao circuito, mas não será habilitada para uso.</span><span class="sxs-lookup"><span data-stu-id="640c0-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="640c0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="640c0-113">EXAMPLES</span></span>

### <span data-ttu-id="640c0-114">Exemplo 1: adicionar uma autorização ao circuito do ExpressRoute especificado</span><span class="sxs-lookup"><span data-stu-id="640c0-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="640c0-115">Os comandos neste exemplo adicionam uma nova autorização a um circuito ExpressRoute existente.</span><span class="sxs-lookup"><span data-stu-id="640c0-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="640c0-116">O primeiro comando usa **Get-AzExpressRouteCircuit** para criar uma referência de objeto para um circuito chamado ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="640c0-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="640c0-117">Essa referência de objeto é armazenada em uma variável chamada $Circuit.</span><span class="sxs-lookup"><span data-stu-id="640c0-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="640c0-118">No segundo comando, o cmdlet **Add-AzExpressRouteCircuitAuthorization** é usado para adicionar uma nova autorização (ContosoCircuitAuthorization) ao circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="640c0-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="640c0-119">Esse comando adiciona a autorização, mas não ativa essa autorização.</span><span class="sxs-lookup"><span data-stu-id="640c0-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="640c0-120">Ativar uma autorização requer o **set-AzExpressRouteCircuit** mostrado no comando final do exemplo.</span><span class="sxs-lookup"><span data-stu-id="640c0-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="640c0-121">OS</span><span class="sxs-lookup"><span data-stu-id="640c0-121">PARAMETERS</span></span>

### <span data-ttu-id="640c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640c0-122">-DefaultProfile</span></span>
<span data-ttu-id="640c0-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="640c0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="640c0-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="640c0-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="640c0-125">Especifica o circuito do ExpressRoute ao qual esse cmdlet adiciona a autorização.</span><span class="sxs-lookup"><span data-stu-id="640c0-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="640c0-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="640c0-126">-Name</span></span>
<span data-ttu-id="640c0-127">Especifica o nome da autorização de circuito a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="640c0-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="640c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640c0-128">CommonParameters</span></span>
<span data-ttu-id="640c0-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640c0-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="640c0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640c0-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="640c0-131">INPUTS</span></span>

### <span data-ttu-id="640c0-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="640c0-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="640c0-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="640c0-133">OUTPUTS</span></span>

### <span data-ttu-id="640c0-134">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="640c0-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="640c0-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="640c0-135">NOTES</span></span>

## <span data-ttu-id="640c0-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="640c0-136">RELATED LINKS</span></span>

[<span data-ttu-id="640c0-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="640c0-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="640c0-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="640c0-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="640c0-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="640c0-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="640c0-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="640c0-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="640c0-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="640c0-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
