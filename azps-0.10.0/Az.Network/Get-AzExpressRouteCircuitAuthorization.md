---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3b51a16d6ff2de8292b1bbb66f7f5ab24cc17b93
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775548"
---
# <span data-ttu-id="23ddd-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23ddd-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="23ddd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="23ddd-103">Obtém informações sobre as autorizações de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23ddd-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="23ddd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23ddd-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23ddd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="23ddd-106">O cmdlet **Get-AzExpressRouteCircuitAuthorization** Obtém informações sobre as autorizações atribuídas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23ddd-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="23ddd-107">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="23ddd-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="23ddd-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="23ddd-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="23ddd-109">As chaves de autorização, bem como outras informações sobre a autorização, podem ser visualizadas a qualquer momento ao executar **Get-AzExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="23ddd-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="23ddd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23ddd-110">EXAMPLES</span></span>

### <span data-ttu-id="23ddd-111">Exemplo 1: obter todas as autorizações do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="23ddd-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="23ddd-112">Esses comandos retornam informações sobre todas as autorizações do ExpressRoute associadas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23ddd-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="23ddd-113">O primeiro comando usa o cmdlet **Get-AzExpressRouteCircuit** para criar uma referência de objeto um Circuit chamado ContosoCircuit; Essa referência de objeto é armazenada na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="23ddd-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="23ddd-114">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzExpressRouteCircuitAuthorization** para retornar informações sobre as autorizações associadas ao ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="23ddd-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="23ddd-115">Exemplo 2: obter todas as autorizações do ExpressRoute usando o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="23ddd-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="23ddd-116">Esses comandos representam uma variação nos comandos usados no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="23ddd-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="23ddd-117">Nesse caso, no entanto, as informações são retornadas apenas para as autorizações que estão disponíveis para uso (ou seja, para autorizações que não foram atribuídas a uma rede virtual).</span><span class="sxs-lookup"><span data-stu-id="23ddd-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="23ddd-118">Para fazer isso, as informações de autorização de circuito são retornadas no comando 2 e são canalizadas para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="23ddd-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="23ddd-119">Em seguida, **Object** , em seguida, escolhe apenas as autorizações em que a propriedade *AuthorizationUseStatus* está definida como available.</span><span class="sxs-lookup"><span data-stu-id="23ddd-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="23ddd-120">Para listar apenas as autorizações que não estão disponíveis, use esta sintaxe para a cláusula WHERE:</span><span class="sxs-lookup"><span data-stu-id="23ddd-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="23ddd-121">OS</span><span class="sxs-lookup"><span data-stu-id="23ddd-121">PARAMETERS</span></span>

### <span data-ttu-id="23ddd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ddd-122">-DefaultProfile</span></span>
<span data-ttu-id="23ddd-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23ddd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23ddd-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23ddd-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="23ddd-125">Especifica a autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23ddd-125">Specifies the ExpressRoute circuit authorization.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ddd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="23ddd-126">-Name</span></span>
<span data-ttu-id="23ddd-127">Especifica o nome da autorização de circuito do ExpressRoute que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="23ddd-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="23ddd-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="23ddd-128">-Name "ContosoCircuitAuthorization"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ddd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ddd-129">CommonParameters</span></span>
<span data-ttu-id="23ddd-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ddd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ddd-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ddd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ddd-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23ddd-132">INPUTS</span></span>

### <span data-ttu-id="23ddd-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23ddd-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="23ddd-134">**Get-AzExpressRouteCircuitAuthorization** aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="23ddd-134">**Get-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="23ddd-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23ddd-135">OUTPUTS</span></span>

### <span data-ttu-id="23ddd-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23ddd-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="23ddd-137">**Get-AzExpressRouteCircuitAuthorization** retorna instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .</span><span class="sxs-lookup"><span data-stu-id="23ddd-137">**Get-AzExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="23ddd-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23ddd-138">NOTES</span></span>

## <span data-ttu-id="23ddd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23ddd-139">RELATED LINKS</span></span>

[<span data-ttu-id="23ddd-140">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23ddd-140">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="23ddd-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23ddd-141">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="23ddd-142">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23ddd-142">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="23ddd-143">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="23ddd-143">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
