---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteGateway.md
ms.openlocfilehash: 597b6fcff647b1b2032f0a1ac5d11961b9d1e959
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113509"
---
# <span data-ttu-id="857ed-101">Get-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="857ed-101">Get-AzExpressRouteGateway</span></span>

## <span data-ttu-id="857ed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="857ed-102">SYNOPSIS</span></span>
<span data-ttu-id="857ed-103">Obtém um recurso do ExpressRouteGateway usando ResourceGroupName e GatewayName OR lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="857ed-103">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="857ed-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="857ed-104">SYNTAX</span></span>

### <span data-ttu-id="857ed-105">ListBySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="857ed-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzExpressRouteGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="857ed-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857ed-106">ListByResourceGroupName</span></span>
```
Get-AzExpressRouteGateway [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="857ed-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="857ed-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="857ed-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="857ed-108">DESCRIPTION</span></span>
<span data-ttu-id="857ed-109">Obtém um recurso do ExpressRouteGateway usando ResourceGroupName e GatewayName OR lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="857ed-109">Gets a ExpressRouteGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="857ed-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="857ed-110">EXAMPLES</span></span>

### <span data-ttu-id="857ed-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="857ed-111">Example 1</span></span>

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

<span data-ttu-id="857ed-112">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual no Centro Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="857ed-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="857ed-113">Um gateway do ExpressRoute será criado posteriormente no Hub Virtual com 2 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="857ed-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="857ed-114">Em seguida, ele obtém o ExpressRouteGateway usando seu resourceGroupName e o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="857ed-114">It then gets the ExpressRouteGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="857ed-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="857ed-115">Example 2</span></span>

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

<span data-ttu-id="857ed-116">Esse comando obterá todos os ExpressRouteGateways que começam com "teste"</span><span class="sxs-lookup"><span data-stu-id="857ed-116">This command will get all ExpressRouteGateways that start with "test"</span></span>

## <span data-ttu-id="857ed-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="857ed-117">PARAMETERS</span></span>

### <span data-ttu-id="857ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857ed-118">-DefaultProfile</span></span>
<span data-ttu-id="857ed-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="857ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="857ed-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="857ed-120">-Name</span></span>
<span data-ttu-id="857ed-121">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="857ed-121">The resource name.</span></span>

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

### <span data-ttu-id="857ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="857ed-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="857ed-123">The resource group name.</span></span>

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

### <span data-ttu-id="857ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="857ed-124">-ResourceId</span></span>
<span data-ttu-id="857ed-125">A ID de recurso do Azure para que o expressRouteGateway seja excluído.</span><span class="sxs-lookup"><span data-stu-id="857ed-125">The Azure resource ID for the expressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="857ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857ed-126">CommonParameters</span></span>
<span data-ttu-id="857ed-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="857ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857ed-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="857ed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857ed-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="857ed-129">INPUTS</span></span>

### <span data-ttu-id="857ed-130">System.String</span><span class="sxs-lookup"><span data-stu-id="857ed-130">System.String</span></span>

## <span data-ttu-id="857ed-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="857ed-131">OUTPUTS</span></span>

### <span data-ttu-id="857ed-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="857ed-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="857ed-133">Notas</span><span class="sxs-lookup"><span data-stu-id="857ed-133">NOTES</span></span>

## <span data-ttu-id="857ed-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="857ed-134">RELATED LINKS</span></span>
