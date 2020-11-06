---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: d5314453be4d2f9042fd5034cc864d94caf1dbd1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600578"
---
# <span data-ttu-id="6fd56-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="6fd56-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="6fd56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fd56-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd56-103">Obtém um recurso ExpressRouteGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="6fd56-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="6fd56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fd56-104">SYNTAX</span></span>

### <span data-ttu-id="6fd56-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="6fd56-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fd56-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd56-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fd56-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd56-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fd56-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fd56-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd56-109">Obtém um recurso ExpressRouteGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="6fd56-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="6fd56-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fd56-110">EXAMPLES</span></span>

### <span data-ttu-id="6fd56-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fd56-111">Example 1</span></span>

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

<span data-ttu-id="6fd56-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no centro-oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd56-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="6fd56-113">Um gateway ExpressRoute será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="6fd56-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="6fd56-114">Em seguida, ele obtém o ExpressRouteGateway usando seu resourceGroupName e o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="6fd56-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="6fd56-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6fd56-115">Example 2</span></span>

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

<span data-ttu-id="6fd56-116">Esse comando terá todos os ExpressRouteGateways que começam com "Test"</span><span class="sxs-lookup"><span data-stu-id="6fd56-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="6fd56-117">OS</span><span class="sxs-lookup"><span data-stu-id="6fd56-117">PARAMETERS</span></span>

### <span data-ttu-id="6fd56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd56-118">-DefaultProfile</span></span>
<span data-ttu-id="6fd56-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd56-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fd56-120">-Name</span></span>
<span data-ttu-id="6fd56-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="6fd56-121">The resource name.</span></span>

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

### <span data-ttu-id="6fd56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd56-122">-ResourceGroupName</span></span>
<span data-ttu-id="6fd56-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6fd56-123">The resource group name.</span></span>

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

### <span data-ttu-id="6fd56-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd56-124">-ResourceId</span></span>
<span data-ttu-id="6fd56-125">A ID de recurso do Azure para o expressRouteGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6fd56-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="6fd56-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd56-126">CommonParameters</span></span>
<span data-ttu-id="6fd56-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd56-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd56-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fd56-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd56-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fd56-129">INPUTS</span></span>

### <span data-ttu-id="6fd56-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6fd56-130">System.String</span></span>

## <span data-ttu-id="6fd56-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fd56-131">OUTPUTS</span></span>

### <span data-ttu-id="6fd56-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="6fd56-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="6fd56-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fd56-133">NOTES</span></span>

## <span data-ttu-id="6fd56-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fd56-134">RELATED LINKS</span></span>
