---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: a99b2ce5364e256f19069e1142b49abaf7f5e938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441388"
---
# <span data-ttu-id="44913-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="44913-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="44913-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44913-102">SYNOPSIS</span></span>
<span data-ttu-id="44913-103">Obtém informações sobre as autorizações de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44913-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44913-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44913-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44913-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44913-105">DESCRIPTION</span></span>
<span data-ttu-id="44913-106">O cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** Obtém informações sobre as autorizações atribuídas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44913-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="44913-107">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="44913-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="44913-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="44913-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="44913-109">As chaves de autorização, bem como outras informações sobre a autorização, podem ser visualizadas a qualquer momento ao executar **Get-AzureRmExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="44913-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="44913-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44913-110">EXAMPLES</span></span>

### <span data-ttu-id="44913-111">Exemplo 1: obter todas as autorizações do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="44913-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="44913-112">Esses comandos retornam informações sobre todas as autorizações do ExpressRoute associadas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44913-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="44913-113">O primeiro comando usa o cmdlet **Get-AzureRmExpressRouteCircuit** para criar uma referência de objeto um Circuit chamado ContosoCircuit; Essa referência de objeto é armazenada na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="44913-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="44913-114">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** para retornar informações sobre as autorizações associadas ao ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="44913-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="44913-115">Exemplo 2: obter todas as autorizações do ExpressRoute usando o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="44913-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="44913-116">Esses comandos representam uma variação nos comandos usados no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="44913-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="44913-117">Nesse caso, no entanto, as informações são retornadas apenas para as autorizações que estão disponíveis para uso (ou seja, para autorizações que não foram atribuídas a uma rede virtual).</span><span class="sxs-lookup"><span data-stu-id="44913-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="44913-118">Para fazer isso, as informações de autorização de circuito são retornadas no comando 2 e são canalizadas para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="44913-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="44913-119">Em seguida, **Object** , em seguida, escolhe apenas as autorizações em que a propriedade *AuthorizationUseStatus* está definida como available.</span><span class="sxs-lookup"><span data-stu-id="44913-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="44913-120">Para listar apenas as autorizações que não estão disponíveis, use esta sintaxe para a cláusula WHERE:</span><span class="sxs-lookup"><span data-stu-id="44913-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="44913-121">OS</span><span class="sxs-lookup"><span data-stu-id="44913-121">PARAMETERS</span></span>

### <span data-ttu-id="44913-122">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="44913-122">-ExpressRouteCircuit</span></span>
<span data-ttu-id="44913-123">Especifica a autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44913-123">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="44913-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="44913-124">-Name</span></span>
<span data-ttu-id="44913-125">Especifica o nome da autorização de circuito do ExpressRoute que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="44913-125">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="44913-126">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="44913-126">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="44913-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44913-127">-DefaultProfile</span></span>
<span data-ttu-id="44913-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44913-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44913-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44913-129">CommonParameters</span></span>
<span data-ttu-id="44913-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44913-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44913-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44913-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44913-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44913-132">INPUTS</span></span>

### <span data-ttu-id="44913-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="44913-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="44913-134">**Get-AzureRmExpressRouteCircuitAuthorization** aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="44913-134">**Get-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="44913-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44913-135">OUTPUTS</span></span>

### <span data-ttu-id="44913-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="44913-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="44913-137">**Get-AzureRmExpressRouteCircuitAuthorization** retorna instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="44913-137">**Get-AzureRmExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="44913-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44913-138">NOTES</span></span>

## <span data-ttu-id="44913-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44913-139">RELATED LINKS</span></span>

[<span data-ttu-id="44913-140">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="44913-140">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="44913-141">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="44913-141">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="44913-142">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="44913-142">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="44913-143">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="44913-143">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
