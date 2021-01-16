---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256813"
---
# <span data-ttu-id="cf531-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cf531-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="cf531-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf531-102">SYNOPSIS</span></span>
<span data-ttu-id="cf531-103">Obtém informações sobre as autorizações de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cf531-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="cf531-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf531-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf531-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf531-105">DESCRIPTION</span></span>
<span data-ttu-id="cf531-106">O cmdlet **Get-AzExpressRouteCircuitAuthorization** Obtém informações sobre as autorizações atribuídas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cf531-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="cf531-107">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="cf531-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="cf531-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="cf531-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="cf531-109">As chaves de autorização, bem como outras informações sobre a autorização, podem ser visualizadas a qualquer momento ao executar **Get-AzExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="cf531-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="cf531-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf531-110">EXAMPLES</span></span>

### <span data-ttu-id="cf531-111">Exemplo 1: obter todas as autorizações do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="cf531-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="cf531-112">Esses comandos retornam informações sobre todas as autorizações do ExpressRoute associadas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cf531-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="cf531-113">O primeiro comando usa o cmdlet **Get-AzExpressRouteCircuit** para criar uma referência de objeto um Circuit chamado ContosoCircuit; Essa referência de objeto é armazenada na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="cf531-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="cf531-114">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzExpressRouteCircuitAuthorization** para retornar informações sobre as autorizações associadas ao ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="cf531-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="cf531-115">Exemplo 2: obter todas as autorizações do ExpressRoute usando o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="cf531-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="cf531-116">Esses comandos representam uma variação nos comandos usados no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="cf531-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="cf531-117">Nesse caso, no entanto, as informações são retornadas apenas para as autorizações que estão disponíveis para uso (ou seja, para autorizações que não foram atribuídas a uma rede virtual).</span><span class="sxs-lookup"><span data-stu-id="cf531-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="cf531-118">Para fazer isso, as informações de autorização de circuito são retornadas no comando 2 e são canalizadas para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="cf531-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="cf531-119">Em seguida, **Object** , em seguida, escolhe apenas as autorizações em que a propriedade *AuthorizationUseStatus* está definida como available.</span><span class="sxs-lookup"><span data-stu-id="cf531-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="cf531-120">Para listar apenas as autorizações que não estão disponíveis, use esta sintaxe para a cláusula WHERE: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="cf531-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="cf531-121">OS</span><span class="sxs-lookup"><span data-stu-id="cf531-121">PARAMETERS</span></span>

### <span data-ttu-id="cf531-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf531-122">-DefaultProfile</span></span>
<span data-ttu-id="cf531-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf531-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf531-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf531-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cf531-125">Especifica a autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cf531-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="cf531-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf531-126">-Name</span></span>
<span data-ttu-id="cf531-127">Especifica o nome da autorização de circuito do ExpressRoute que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="cf531-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="cf531-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="cf531-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="cf531-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf531-129">CommonParameters</span></span>
<span data-ttu-id="cf531-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf531-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf531-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf531-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf531-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf531-132">INPUTS</span></span>

### <span data-ttu-id="cf531-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf531-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="cf531-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf531-134">OUTPUTS</span></span>

### <span data-ttu-id="cf531-135">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cf531-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="cf531-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf531-136">NOTES</span></span>

## <span data-ttu-id="cf531-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf531-137">RELATED LINKS</span></span>

[<span data-ttu-id="cf531-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cf531-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="cf531-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cf531-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="cf531-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cf531-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="cf531-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="cf531-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
