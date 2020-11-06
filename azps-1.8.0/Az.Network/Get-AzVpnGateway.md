---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGateway.md
ms.openlocfilehash: fa91ce991a109c91b27560b0b969d1af0f4342d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600445"
---
# <span data-ttu-id="12fe0-101">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fe0-101">Get-AzVpnGateway</span></span>

## <span data-ttu-id="12fe0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="12fe0-103">Obtém um recurso VpnGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="12fe0-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="12fe0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12fe0-104">SYNTAX</span></span>

### <span data-ttu-id="12fe0-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="12fe0-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12fe0-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fe0-106">ListByResourceGroupName</span></span>
```
Get-AzVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12fe0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12fe0-107">DESCRIPTION</span></span>
<span data-ttu-id="12fe0-108">Obtém um recurso VpnGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="12fe0-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="12fe0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12fe0-109">EXAMPLES</span></span>

### <span data-ttu-id="12fe0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12fe0-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="12fe0-111">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="12fe0-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="12fe0-112">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="12fe0-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="12fe0-113">Em seguida, ele obtém o VpnGateway usando seu resourceGroupName e o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="12fe0-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

### <span data-ttu-id="12fe0-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="12fe0-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnGateway -Name test*

ResourceGroupName   : testRG
Name                : test1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test1
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded

ResourceGroupName   : testRG
Name                : test2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/test2
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="12fe0-115">Este cmdlet obtém todos os gateways que começam com "Test".</span><span class="sxs-lookup"><span data-stu-id="12fe0-115">This cmdlet gets all Gateways that start with "test".</span></span>

## <span data-ttu-id="12fe0-116">OS</span><span class="sxs-lookup"><span data-stu-id="12fe0-116">PARAMETERS</span></span>

### <span data-ttu-id="12fe0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12fe0-117">-DefaultProfile</span></span>
<span data-ttu-id="12fe0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12fe0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12fe0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="12fe0-119">-Name</span></span>
<span data-ttu-id="12fe0-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="12fe0-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="12fe0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12fe0-121">-ResourceGroupName</span></span>
<span data-ttu-id="12fe0-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12fe0-122">The resource group name.</span></span>

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

### <span data-ttu-id="12fe0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12fe0-123">CommonParameters</span></span>
<span data-ttu-id="12fe0-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12fe0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12fe0-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12fe0-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12fe0-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12fe0-126">INPUTS</span></span>

### <span data-ttu-id="12fe0-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12fe0-127">None</span></span>

## <span data-ttu-id="12fe0-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12fe0-128">OUTPUTS</span></span>

### <span data-ttu-id="12fe0-129">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fe0-129">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="12fe0-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12fe0-130">NOTES</span></span>

## <span data-ttu-id="12fe0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12fe0-131">RELATED LINKS</span></span>

[<span data-ttu-id="12fe0-132">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fe0-132">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="12fe0-133">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fe0-133">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="12fe0-134">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="12fe0-134">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
