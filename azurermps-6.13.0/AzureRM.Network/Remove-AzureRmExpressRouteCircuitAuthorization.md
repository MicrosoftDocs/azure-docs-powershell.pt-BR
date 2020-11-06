---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 6a8c81f8c130f322e868c91e18c7fff7b1175d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440350"
---
# <span data-ttu-id="de8b5-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="de8b5-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="de8b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="de8b5-103">Remove uma autorização de configuração do ExpressRoute existente.</span><span class="sxs-lookup"><span data-stu-id="de8b5-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de8b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de8b5-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de8b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="de8b5-106">O cmdlet **Remove-AzureRmExpressRouteCircuitAuthorization** remove uma autorização atribuída a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="de8b5-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="de8b5-107">Os circuitos do ExpressRoute conectam a sua rede local ao Azure usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="de8b5-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="de8b5-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito.</span><span class="sxs-lookup"><span data-stu-id="de8b5-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="de8b5-109">Só pode haver uma autorização por rede virtual.</span><span class="sxs-lookup"><span data-stu-id="de8b5-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="de8b5-110">No entanto, a qualquer momento, o proprietário do circuito pode usar **Remove-AzureRmExpressRouteCircuitAuthorization** para remover a autorização atribuída a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="de8b5-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="de8b5-111">Quando isso acontece, a rede virtual correspondente não consegue mais usar o circuito do ExpressRoute para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="de8b5-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="de8b5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de8b5-112">EXAMPLES</span></span>

### <span data-ttu-id="de8b5-113">Exemplo 1: remover a autorização de um circuito de um circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="de8b5-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="de8b5-114">Este exemplo remove uma autorização de circuito de um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="de8b5-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="de8b5-115">O primeiro comando usa o cmdlet **Get-AzureRmExpressRouteCircuit** para criar uma referência de objeto para um circuito do ExpressRoute chamado ContosoCircuit e armazena o resultado na variável chamada $Circuit.</span><span class="sxs-lookup"><span data-stu-id="de8b5-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="de8b5-116">O segundo comando marca a ContosoCircuitAuthorization de autorização de circuito para remoção.</span><span class="sxs-lookup"><span data-stu-id="de8b5-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="de8b5-117">O terceiro comando usa o cmdlet Set-AzureRmExpressRouteCircuit para confirmar a remoção do circuito do ExpressRoute armazenado na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="de8b5-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="de8b5-118">OS</span><span class="sxs-lookup"><span data-stu-id="de8b5-118">PARAMETERS</span></span>

### <span data-ttu-id="de8b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8b5-119">-DefaultProfile</span></span>
<span data-ttu-id="de8b5-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de8b5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de8b5-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de8b5-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="de8b5-122">Especifica o objeto ExpressRouteCircuit que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="de8b5-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="de8b5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="de8b5-123">-Name</span></span>
<span data-ttu-id="de8b5-124">Especifica o nome da autorização de circuito que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="de8b5-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="de8b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8b5-125">CommonParameters</span></span>
<span data-ttu-id="de8b5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8b5-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de8b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8b5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de8b5-128">INPUTS</span></span>

### <span data-ttu-id="de8b5-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de8b5-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="de8b5-130">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="de8b5-130">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="de8b5-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de8b5-131">OUTPUTS</span></span>

### <span data-ttu-id="de8b5-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de8b5-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="de8b5-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de8b5-133">NOTES</span></span>

## <span data-ttu-id="de8b5-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de8b5-134">RELATED LINKS</span></span>

[<span data-ttu-id="de8b5-135">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="de8b5-135">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="de8b5-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de8b5-136">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="de8b5-137">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="de8b5-137">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="de8b5-138">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="de8b5-138">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="de8b5-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="de8b5-139">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
