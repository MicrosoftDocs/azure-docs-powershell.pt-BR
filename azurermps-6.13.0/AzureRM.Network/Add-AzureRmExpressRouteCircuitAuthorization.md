---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 108ea2b0262c34e38ffd7ed2961e3cba9a8d59ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602600"
---
# <span data-ttu-id="9609b-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9609b-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="9609b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9609b-102">SYNOPSIS</span></span>
<span data-ttu-id="9609b-103">Adiciona uma autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9609b-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9609b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9609b-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9609b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9609b-105">DESCRIPTION</span></span>
<span data-ttu-id="9609b-106">O cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** adiciona uma autorização a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9609b-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="9609b-107">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="9609b-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="9609b-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="9609b-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="9609b-109">**Add-AzureRmExpressRouteCircuitAuthorization** adiciona uma nova autorização a um circuito e, ao mesmo tempo, gera a chave de autorização correspondente.</span><span class="sxs-lookup"><span data-stu-id="9609b-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="9609b-110">Essas chaves podem ser visualizadas a qualquer momento executando o cmdlet Get-AzureRmExpressRouteCircuitAuthorization e, conforme necessário, podem ser copiados e encaminhados para o proprietário da rede apropriado.</span><span class="sxs-lookup"><span data-stu-id="9609b-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="9609b-111">Observe que, depois de executar **Add-AzureRmExpressRouteCircuitAuthorization** , você deve chamar o cmdlet Set-AzureRmExpressRouteCircuit para ativar a chave.</span><span class="sxs-lookup"><span data-stu-id="9609b-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="9609b-112">Se você não chamar **set-AzureRmExpressRouteCircuit** , a autorização será adicionada ao circuito, mas não será habilitada para uso.</span><span class="sxs-lookup"><span data-stu-id="9609b-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="9609b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9609b-113">EXAMPLES</span></span>

### <span data-ttu-id="9609b-114">Exemplo 1: adicionar uma autorização ao circuito do ExpressRoute especificado</span><span class="sxs-lookup"><span data-stu-id="9609b-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="9609b-115">Os comandos neste exemplo adicionam uma nova autorização a um circuito ExpressRoute existente.</span><span class="sxs-lookup"><span data-stu-id="9609b-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="9609b-116">O primeiro comando usa **Get-AzureRmExpressRouteCircuit** para criar uma referência de objeto para um circuito chamado ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="9609b-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="9609b-117">Essa referência de objeto é armazenada em uma variável chamada $Circuit.</span><span class="sxs-lookup"><span data-stu-id="9609b-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="9609b-118">No segundo comando, o cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** é usado para adicionar uma nova autorização (ContosoCircuitAuthorization) ao circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9609b-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="9609b-119">Esse comando adiciona a autorização, mas não ativa essa autorização.</span><span class="sxs-lookup"><span data-stu-id="9609b-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="9609b-120">Ativar uma autorização requer o **set-AzureRmExpressRouteCircuit** mostrado no comando final do exemplo.</span><span class="sxs-lookup"><span data-stu-id="9609b-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="9609b-121">OS</span><span class="sxs-lookup"><span data-stu-id="9609b-121">PARAMETERS</span></span>

### <span data-ttu-id="9609b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9609b-122">-DefaultProfile</span></span>
<span data-ttu-id="9609b-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9609b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9609b-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9609b-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9609b-125">Especifica o circuito do ExpressRoute ao qual esse cmdlet adiciona a autorização.</span><span class="sxs-lookup"><span data-stu-id="9609b-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="9609b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9609b-126">-Name</span></span>
<span data-ttu-id="9609b-127">Especifica o nome da autorização de circuito a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="9609b-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="9609b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9609b-128">CommonParameters</span></span>
<span data-ttu-id="9609b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9609b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9609b-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9609b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9609b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9609b-131">INPUTS</span></span>

### <span data-ttu-id="9609b-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9609b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="9609b-133">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9609b-133">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="9609b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9609b-134">OUTPUTS</span></span>

### <span data-ttu-id="9609b-135">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9609b-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9609b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9609b-136">NOTES</span></span>

## <span data-ttu-id="9609b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9609b-137">RELATED LINKS</span></span>

[<span data-ttu-id="9609b-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9609b-138">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9609b-139">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9609b-139">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9609b-140">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9609b-140">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9609b-141">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="9609b-141">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="9609b-142">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9609b-142">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
