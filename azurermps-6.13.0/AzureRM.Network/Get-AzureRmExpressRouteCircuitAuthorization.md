---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 5b277ca35071c3639a3c7b341451cea78c024901
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440766"
---
# <span data-ttu-id="eac5a-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eac5a-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="eac5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eac5a-102">SYNOPSIS</span></span>
<span data-ttu-id="eac5a-103">Obtém informações sobre as autorizações de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eac5a-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eac5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eac5a-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eac5a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eac5a-105">DESCRIPTION</span></span>
<span data-ttu-id="eac5a-106">O cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** Obtém informações sobre as autorizações atribuídas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eac5a-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="eac5a-107">Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública.</span><span class="sxs-lookup"><span data-stu-id="eac5a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="eac5a-108">O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual).</span><span class="sxs-lookup"><span data-stu-id="eac5a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="eac5a-109">As chaves de autorização, bem como outras informações sobre a autorização, podem ser visualizadas a qualquer momento ao executar **Get-AzureRmExpressRouteCircuitAuthorization**.</span><span class="sxs-lookup"><span data-stu-id="eac5a-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="eac5a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eac5a-110">EXAMPLES</span></span>

### <span data-ttu-id="eac5a-111">Exemplo 1: obter todas as autorizações do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="eac5a-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="eac5a-112">Esses comandos retornam informações sobre todas as autorizações do ExpressRoute associadas a um circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eac5a-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="eac5a-113">O primeiro comando usa o cmdlet **Get-AzureRmExpressRouteCircuit** para criar uma referência de objeto um Circuit chamado ContosoCircuit; Essa referência de objeto é armazenada na variável $Circuit.</span><span class="sxs-lookup"><span data-stu-id="eac5a-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="eac5a-114">Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** para retornar informações sobre as autorizações associadas ao ContosoCircuit.</span><span class="sxs-lookup"><span data-stu-id="eac5a-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="eac5a-115">Exemplo 2: obter todas as autorizações do ExpressRoute usando o cmdlet Where-Object</span><span class="sxs-lookup"><span data-stu-id="eac5a-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="eac5a-116">Esses comandos representam uma variação nos comandos usados no exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="eac5a-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="eac5a-117">Nesse caso, no entanto, as informações são retornadas apenas para as autorizações que estão disponíveis para uso (ou seja, para autorizações que não foram atribuídas a uma rede virtual).</span><span class="sxs-lookup"><span data-stu-id="eac5a-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="eac5a-118">Para fazer isso, as informações de autorização de circuito são retornadas no comando 2 e são canalizadas para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="eac5a-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="eac5a-119">Em seguida, **Object** , em seguida, escolhe apenas as autorizações em que a propriedade *AuthorizationUseStatus* está definida como available.</span><span class="sxs-lookup"><span data-stu-id="eac5a-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="eac5a-120">Para listar apenas as autorizações que não estão disponíveis, use esta sintaxe para a cláusula WHERE: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="eac5a-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="eac5a-121">OS</span><span class="sxs-lookup"><span data-stu-id="eac5a-121">PARAMETERS</span></span>

### <span data-ttu-id="eac5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac5a-122">-DefaultProfile</span></span>
<span data-ttu-id="eac5a-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eac5a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac5a-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac5a-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="eac5a-125">Especifica a autorização de circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eac5a-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="eac5a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="eac5a-126">-Name</span></span>
<span data-ttu-id="eac5a-127">Especifica o nome da autorização de circuito do ExpressRoute que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="eac5a-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="eac5a-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="eac5a-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="eac5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac5a-129">CommonParameters</span></span>
<span data-ttu-id="eac5a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eac5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac5a-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac5a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac5a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eac5a-132">INPUTS</span></span>

### <span data-ttu-id="eac5a-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac5a-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="eac5a-134">Parâmetros: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eac5a-134">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="eac5a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eac5a-135">OUTPUTS</span></span>

### <span data-ttu-id="eac5a-136">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eac5a-136">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="eac5a-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eac5a-137">NOTES</span></span>

## <span data-ttu-id="eac5a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eac5a-138">RELATED LINKS</span></span>

[<span data-ttu-id="eac5a-139">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eac5a-139">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="eac5a-140">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eac5a-140">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="eac5a-141">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eac5a-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="eac5a-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="eac5a-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)