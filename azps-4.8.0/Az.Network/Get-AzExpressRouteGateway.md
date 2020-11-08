---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114154"
---
# <span data-ttu-id="eda2d-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="eda2d-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="eda2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eda2d-102">SYNOPSIS</span></span>
<span data-ttu-id="eda2d-103">Obtém um recurso ExpressRouteGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="eda2d-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="eda2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eda2d-104">SYNTAX</span></span>

### <span data-ttu-id="eda2d-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="eda2d-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eda2d-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda2d-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eda2d-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="eda2d-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eda2d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eda2d-108">DESCRIPTION</span></span>
<span data-ttu-id="eda2d-109">Obtém um recurso ExpressRouteGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="eda2d-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="eda2d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eda2d-110">EXAMPLES</span></span>

### <span data-ttu-id="eda2d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eda2d-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"

ResourceGroupName   : testRG
Name                : testExpressRoutegw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="eda2d-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro-oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="eda2d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="eda2d-113">Um gateway ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="eda2d-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="eda2d-114">Em seguida, ele obtém o ExpressRouteGateway usando seu resourceGroupName e o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="eda2d-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="eda2d-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eda2d-115">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteGateway -Name test*

ResourceGroupName   : testRG
Name                : testExpressRoutegw1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw1
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : testExpressRoutegw2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw2
Location            : West Central US
ExpressRouteGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/ExpressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="eda2d-116">Esse comando terá todos os ExpressRouteGateways que começam com "Test"</span><span class="sxs-lookup"><span data-stu-id="eda2d-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="eda2d-117">OS</span><span class="sxs-lookup"><span data-stu-id="eda2d-117">PARAMETERS</span></span>

### <span data-ttu-id="eda2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda2d-118">-DefaultProfile</span></span>
<span data-ttu-id="eda2d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eda2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eda2d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eda2d-120">-Name</span></span>
<span data-ttu-id="eda2d-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="eda2d-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, ExpressRouteGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="eda2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="eda2d-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eda2d-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="eda2d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eda2d-124">-ResourceId</span></span>
<span data-ttu-id="eda2d-125">A ID de recurso do Azure para o expressRouteGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="eda2d-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda2d-126">CommonParameters</span></span>
<span data-ttu-id="eda2d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda2d-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eda2d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda2d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eda2d-129">INPUTS</span></span>

### <span data-ttu-id="eda2d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eda2d-130">System.String</span></span>

## <span data-ttu-id="eda2d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eda2d-131">OUTPUTS</span></span>

### <span data-ttu-id="eda2d-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="eda2d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="eda2d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eda2d-133">NOTES</span></span>

## <span data-ttu-id="eda2d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eda2d-134">RELATED LINKS</span></span>
