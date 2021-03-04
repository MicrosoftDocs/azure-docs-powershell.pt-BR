---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2c58549ee79cd24d29c1e3549d729995313c5748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887367"
---
# <span data-ttu-id="ddd78-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ddd78-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="ddd78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd78-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd78-103">Obtém informações sobre autorizações de circuitos ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ddd78-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="ddd78-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ddd78-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddd78-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddd78-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd78-106">O cmdlet **Get-AzExpressRouteCircuitAuthorization** obtém informações sobre as autorizações atribuídas a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ddd78-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="ddd78-107">Os circuitos ExpressRoute conectam sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="ddd78-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="ddd78-108">O proprietário de um circuito ExpressRoute pode criar até 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="ddd78-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="ddd78-109">As chaves de autorização, bem como outras informações sobre a autorização, podem ser exibidas a qualquer momento executando **Get-AzExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="ddd78-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="ddd78-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddd78-110">EXAMPLES</span></span>

### <span data-ttu-id="ddd78-111">Exemplo 1: Obter todas as autorizações do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ddd78-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="ddd78-112">Esses comandos retornam informações sobre todas as autorizações do ExpressRoute associadas a um circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ddd78-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="ddd78-113">O primeiro comando usa o cmdlet **Get-AzExpressRouteCircuit** para criar uma referência de objeto a um circuito chamado ContosoCircuit; essa referência de objeto é armazenada na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="ddd78-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="ddd78-114">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzExpressRouteCircuitAuthorization** para retornar informações sobre as autorizações associadas à ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="ddd78-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="ddd78-115">Exemplo 2: Obter todas as autorizações do ExpressRoute usando o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="ddd78-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="ddd78-116">Esses comandos representam uma variação nos comandos usados no Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="ddd78-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="ddd78-117">Nesse caso, no entanto, as informações são retornadas apenas para as autorizações que estão disponíveis para uso (ou seja, para autorizações que não foram atribuídas a uma rede virtual).</span><span class="sxs-lookup"><span data-stu-id="ddd78-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="ddd78-118">Para fazer isso, as informações de autorização do circuito são retornadas no comando 2 e são canaldas para o cmdlet **Where-Object.**</span><span class="sxs-lookup"><span data-stu-id="ddd78-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="ddd78-119">**Where-Object,** em seguida, escolhe apenas as autorizações em que *a propriedade AuthorizationUseStatus* está definida como Disponível.</span><span class="sxs-lookup"><span data-stu-id="ddd78-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="ddd78-120">Para listar apenas as autorizações que não estão disponíveis, use esta sintaxe para a cláusula Where: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="ddd78-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="ddd78-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ddd78-121">PARAMETERS</span></span>

### <span data-ttu-id="ddd78-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd78-122">-DefaultProfile</span></span>
<span data-ttu-id="ddd78-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ddd78-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd78-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ddd78-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ddd78-125">Especifica a autorização do circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ddd78-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="ddd78-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ddd78-126">-Name</span></span>
<span data-ttu-id="ddd78-127">Especifica o nome da autorização de circuito ExpressRoute que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="ddd78-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="ddd78-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="ddd78-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="ddd78-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd78-129">CommonParameters</span></span>
<span data-ttu-id="ddd78-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd78-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd78-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddd78-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd78-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddd78-132">INPUTS</span></span>

### <span data-ttu-id="ddd78-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ddd78-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ddd78-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ddd78-134">OUTPUTS</span></span>

### <span data-ttu-id="ddd78-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ddd78-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="ddd78-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ddd78-136">NOTES</span></span>

## <span data-ttu-id="ddd78-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddd78-137">RELATED LINKS</span></span>

[<span data-ttu-id="ddd78-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ddd78-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ddd78-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ddd78-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ddd78-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ddd78-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ddd78-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ddd78-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
