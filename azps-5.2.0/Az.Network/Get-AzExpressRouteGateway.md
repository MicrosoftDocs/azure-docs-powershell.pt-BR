---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263357"
---
# <span data-ttu-id="2c8fb-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="2c8fb-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="2c8fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8fb-103">Obtém um recurso ExpressRouteGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="2c8fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c8fb-104">SYNTAX</span></span>

### <span data-ttu-id="2c8fb-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c8fb-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c8fb-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8fb-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c8fb-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2c8fb-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c8fb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c8fb-108">DESCRIPTION</span></span>
<span data-ttu-id="2c8fb-109">Obtém um recurso ExpressRouteGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="2c8fb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c8fb-110">EXAMPLES</span></span>

### <span data-ttu-id="2c8fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2c8fb-111">Example 1</span></span>

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

<span data-ttu-id="2c8fb-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro-oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="2c8fb-113">Um gateway ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="2c8fb-114">Em seguida, ele obtém o ExpressRouteGateway usando seu resourceGroupName e o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="2c8fb-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2c8fb-115">Example 2</span></span>

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

<span data-ttu-id="2c8fb-116">Esse comando terá todos os ExpressRouteGateways que começam com "Test"</span><span class="sxs-lookup"><span data-stu-id="2c8fb-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="2c8fb-117">OS</span><span class="sxs-lookup"><span data-stu-id="2c8fb-117">PARAMETERS</span></span>

### <span data-ttu-id="2c8fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8fb-118">-DefaultProfile</span></span>
<span data-ttu-id="2c8fb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c8fb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c8fb-120">-Name</span></span>
<span data-ttu-id="2c8fb-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-121">The resource name.</span></span>

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

### <span data-ttu-id="2c8fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="2c8fb-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-123">The resource group name.</span></span>

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

### <span data-ttu-id="2c8fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c8fb-124">-ResourceId</span></span>
<span data-ttu-id="2c8fb-125">A ID de recurso do Azure para o expressRouteGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="2c8fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8fb-126">CommonParameters</span></span>
<span data-ttu-id="2c8fb-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8fb-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c8fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8fb-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c8fb-129">INPUTS</span></span>

### <span data-ttu-id="2c8fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2c8fb-130">System.String</span></span>

## <span data-ttu-id="2c8fb-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c8fb-131">OUTPUTS</span></span>

### <span data-ttu-id="2c8fb-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="2c8fb-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="2c8fb-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c8fb-133">NOTES</span></span>

## <span data-ttu-id="2c8fb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c8fb-134">RELATED LINKS</span></span>
