---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: f0e66c1e601ab63eec6d2540edd3ba0235727e9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785675"
---
# <span data-ttu-id="23535-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23535-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="23535-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23535-102">SYNOPSIS</span></span>
<span data-ttu-id="23535-103">Cria uma autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23535-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23535-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23535-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23535-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23535-105">DESCRIPTION</span></span>
<span data-ttu-id="23535-106">O cmdlet **New-AzureRmExpressRouteCircuitAuthorization** cria uma autorização de circuito que pode ser adicionada a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23535-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="23535-107">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="23535-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="23535-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar uma rede ao circuito.</span><span class="sxs-lookup"><span data-stu-id="23535-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="23535-109">Só pode haver uma autorização por rede virtual.</span><span class="sxs-lookup"><span data-stu-id="23535-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="23535-110">Depois de criar um circuito do ExpressRoute, você pode usar **Add-AzureRmExpressRouteCircuitAuthorization** para adicionar uma autorização para esse circuito.</span><span class="sxs-lookup"><span data-stu-id="23535-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="23535-111">Você também pode usar **New-AzureRmExpressRouteCircuitAuthorization** para criar uma autorização que pode ser adicionada a um novo circuito ao mesmo tempo em que o circuito é criado.</span><span class="sxs-lookup"><span data-stu-id="23535-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="23535-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23535-112">EXAMPLES</span></span>

### <span data-ttu-id="23535-113">Exemplo 1: criar uma nova autorização de circuito</span><span class="sxs-lookup"><span data-stu-id="23535-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="23535-114">Esse comando cria uma nova autorização de circuito chamada ContosoCircuitAuthorization e, em seguida, armazena esse objeto em uma variável chamada $Authorization.</span><span class="sxs-lookup"><span data-stu-id="23535-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="23535-115">Salvar o objeto em uma variável é importante: embora **New-AzureRmExpressRouteCircuitAuthorization** possa criar uma autorização de circuito, ele não pode adicionar essa autorização a uma rota de circuito.</span><span class="sxs-lookup"><span data-stu-id="23535-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="23535-116">Em vez disso, o $Authorization variável é usado New-AzureRmExpressRouteCircuit durante a criação de um circuito do ExpressRoute com nova marca.</span><span class="sxs-lookup"><span data-stu-id="23535-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="23535-117">Para obter mais informações, consulte a documentação do cmdlet New-AzureRmExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="23535-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="23535-118">OS</span><span class="sxs-lookup"><span data-stu-id="23535-118">PARAMETERS</span></span>

### <span data-ttu-id="23535-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23535-119">-DefaultProfile</span></span>
<span data-ttu-id="23535-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23535-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23535-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="23535-121">-Name</span></span>
<span data-ttu-id="23535-122">Especifica um nome exclusivo para a nova autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23535-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23535-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23535-123">CommonParameters</span></span>
<span data-ttu-id="23535-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23535-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23535-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23535-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23535-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23535-126">INPUTS</span></span>

### <span data-ttu-id="23535-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="23535-127">None</span></span>
<span data-ttu-id="23535-128">Esse cmdlet não aceita entrada em pipeline.</span><span class="sxs-lookup"><span data-stu-id="23535-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="23535-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23535-129">OUTPUTS</span></span>

### <span data-ttu-id="23535-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23535-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="23535-131">Esse cmdlet cria instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="23535-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="23535-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23535-132">NOTES</span></span>

## <span data-ttu-id="23535-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23535-133">RELATED LINKS</span></span>

[<span data-ttu-id="23535-134">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23535-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="23535-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23535-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="23535-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23535-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

