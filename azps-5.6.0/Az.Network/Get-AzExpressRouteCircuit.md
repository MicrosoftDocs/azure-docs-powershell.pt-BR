---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 8961948970843873f337fd1625aabfdf878ba15d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887374"
---
# <span data-ttu-id="c6b73-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6b73-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="c6b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6b73-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b73-103">Obtém um circuito do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b73-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="c6b73-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c6b73-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6b73-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c6b73-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b73-106">O cmdlet **Get-AzExpressRouteCircuit** é usado para recuperar um objeto de circuito ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="c6b73-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="c6b73-107">O objeto circuit retornado pode ser usado como entrada para outros cmdlets que operam em circuitos ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c6b73-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="c6b73-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6b73-108">EXAMPLES</span></span>

### <span data-ttu-id="c6b73-109">Exemplo 1: Obter o circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c6b73-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="c6b73-110">Obter um circuito ExpressRoute específico com Nome "testrg" e ResourceGroupName "test"</span><span class="sxs-lookup"><span data-stu-id="c6b73-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="c6b73-111">Exemplo 2: listar os circuitos ExpressRoute usando filtragem</span><span class="sxs-lookup"><span data-stu-id="c6b73-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="c6b73-112">Obter todos os circuitos ExpressRoute cujo nome começa com "test".</span><span class="sxs-lookup"><span data-stu-id="c6b73-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="c6b73-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c6b73-113">PARAMETERS</span></span>

### <span data-ttu-id="c6b73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b73-114">-DefaultProfile</span></span>
<span data-ttu-id="c6b73-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c6b73-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6b73-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c6b73-116">-Name</span></span>
<span data-ttu-id="c6b73-117">O nome do circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c6b73-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c6b73-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b73-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6b73-119">O nome do grupo de recursos que contém o circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c6b73-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c6b73-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b73-120">CommonParameters</span></span>
<span data-ttu-id="c6b73-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6b73-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b73-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6b73-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b73-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6b73-123">INPUTS</span></span>

### <span data-ttu-id="c6b73-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c6b73-124">System.String</span></span>

## <span data-ttu-id="c6b73-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c6b73-125">OUTPUTS</span></span>

### <span data-ttu-id="c6b73-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6b73-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c6b73-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="c6b73-127">NOTES</span></span>

## <span data-ttu-id="c6b73-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6b73-128">RELATED LINKS</span></span>

[<span data-ttu-id="c6b73-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6b73-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="c6b73-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6b73-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="c6b73-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6b73-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="c6b73-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c6b73-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
