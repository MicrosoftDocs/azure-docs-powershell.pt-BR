---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: e37c8fdded8fa5e141138903e502e2e1b0f1a0f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600604"
---
# <span data-ttu-id="4e956-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e956-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="4e956-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e956-102">SYNOPSIS</span></span>
<span data-ttu-id="4e956-103">Obtém um circuito do Azure ExpressRoute do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e956-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="4e956-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e956-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e956-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e956-105">DESCRIPTION</span></span>
<span data-ttu-id="4e956-106">O cmdlet **Get-AzExpressRouteCircuit** é usado para recuperar um objeto de circuito do ExpressRoute da sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="4e956-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="4e956-107">O objeto de circuito retornado pode ser usado como entrada para outros cmdlets que operam em circuitos do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4e956-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="4e956-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e956-108">EXAMPLES</span></span>

### <span data-ttu-id="4e956-109">Exemplo 1: obter o circuito do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4e956-109">Example 1: Get the ExpressRoute circuit</span></span>
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

<span data-ttu-id="4e956-110">Obter um circuito do ExpressRoute específico com o nome "testrg" e ResourceGroupName "teste"</span><span class="sxs-lookup"><span data-stu-id="4e956-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="4e956-111">Exemplo 2: listar os circuitos do ExpressRoute usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="4e956-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
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

<span data-ttu-id="4e956-112">Obter todos os circuitos do ExpressRoute cujo nome começa com "Test".</span><span class="sxs-lookup"><span data-stu-id="4e956-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="4e956-113">OS</span><span class="sxs-lookup"><span data-stu-id="4e956-113">PARAMETERS</span></span>

### <span data-ttu-id="4e956-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e956-114">-DefaultProfile</span></span>
<span data-ttu-id="4e956-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e956-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e956-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e956-116">-Name</span></span>
<span data-ttu-id="4e956-117">O nome do circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4e956-117">The name of the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="4e956-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e956-118">-ResourceGroupName</span></span>
<span data-ttu-id="4e956-119">O nome do grupo de recursos que contém o circuito do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4e956-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="4e956-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e956-120">CommonParameters</span></span>
<span data-ttu-id="4e956-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e956-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e956-122">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e956-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e956-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e956-123">INPUTS</span></span>

### <span data-ttu-id="4e956-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4e956-124">System.String</span></span>

## <span data-ttu-id="4e956-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e956-125">OUTPUTS</span></span>

### <span data-ttu-id="4e956-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e956-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4e956-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e956-127">NOTES</span></span>

## <span data-ttu-id="4e956-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e956-128">RELATED LINKS</span></span>

[<span data-ttu-id="4e956-129">Mover-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e956-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e956-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e956-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e956-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e956-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="4e956-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4e956-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
