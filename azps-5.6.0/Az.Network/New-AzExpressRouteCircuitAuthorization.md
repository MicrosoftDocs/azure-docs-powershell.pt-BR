---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891002"
---
# <span data-ttu-id="cbed0-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cbed0-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="cbed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbed0-102">SYNOPSIS</span></span>
<span data-ttu-id="cbed0-103">Cria uma autorização de circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cbed0-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="cbed0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbed0-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbed0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbed0-105">DESCRIPTION</span></span>
<span data-ttu-id="cbed0-106">O cmdlet **New-AzExpressRouteCircuitAuthorization** cria uma autorização de circuito que pode ser adicionada a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cbed0-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="cbed0-107">Os circuitos ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="cbed0-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="cbed0-108">O proprietário de um circuito ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar uma rede ao circuito.</span><span class="sxs-lookup"><span data-stu-id="cbed0-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="cbed0-109">Só pode haver uma autorização por rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cbed0-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="cbed0-110">Depois de criar um circuito ExpressRoute, você pode usar **Add-AzExpressRouteCircuitAuthorization** para adicionar uma autorização a esse circuito.</span><span class="sxs-lookup"><span data-stu-id="cbed0-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="cbed0-111">Como alternativa, você pode usar **New-AzExpressRouteCircuitAuthorization** para criar uma autorização que pode ser adicionada a um novo circuito ao mesmo tempo em que o circuito é criado.</span><span class="sxs-lookup"><span data-stu-id="cbed0-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="cbed0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbed0-112">EXAMPLES</span></span>

### <span data-ttu-id="cbed0-113">Exemplo 1: Criar uma nova autorização de circuito</span><span class="sxs-lookup"><span data-stu-id="cbed0-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="cbed0-114">Este comando cria uma nova autorização de circuito chamada ContosoCircuitAuthorization e armazena esse objeto em uma variável chamada $Authorization.</span><span class="sxs-lookup"><span data-stu-id="cbed0-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="cbed0-115">Salvar o objeto em uma variável é importante: embora **New-AzExpressRouteCircuitAuthorization** possa criar uma autorização de circuito, ele não pode adicionar essa autorização a uma rota de circuito.</span><span class="sxs-lookup"><span data-stu-id="cbed0-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="cbed0-116">Em vez disso, a variável $Authorization é usada New-AzExpressRouteCircuit ao criar um novo circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cbed0-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="cbed0-117">Para obter mais informações, consulte a documentação do New-AzExpressRouteCircuit cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbed0-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="cbed0-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbed0-118">PARAMETERS</span></span>

### <span data-ttu-id="cbed0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbed0-119">-DefaultProfile</span></span>
<span data-ttu-id="cbed0-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="cbed0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbed0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cbed0-121">-Name</span></span>
<span data-ttu-id="cbed0-122">Especifica um nome exclusivo para a nova autorização do circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cbed0-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="cbed0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbed0-123">CommonParameters</span></span>
<span data-ttu-id="cbed0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbed0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbed0-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbed0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbed0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbed0-126">INPUTS</span></span>

### <span data-ttu-id="cbed0-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cbed0-127">None</span></span>

## <span data-ttu-id="cbed0-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbed0-128">OUTPUTS</span></span>

### <span data-ttu-id="cbed0-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cbed0-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="cbed0-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbed0-130">NOTES</span></span>

## <span data-ttu-id="cbed0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbed0-131">RELATED LINKS</span></span>

[<span data-ttu-id="cbed0-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cbed0-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="cbed0-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cbed0-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="cbed0-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cbed0-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

