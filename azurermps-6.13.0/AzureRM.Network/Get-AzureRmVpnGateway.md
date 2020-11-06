---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnGateway.md
ms.openlocfilehash: f1e7b829856558f438793a921154aa3f04666ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429480"
---
# <span data-ttu-id="84573-101">Get-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="84573-101">Get-AzureRmVpnGateway</span></span>

## <span data-ttu-id="84573-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84573-102">SYNOPSIS</span></span>
<span data-ttu-id="84573-103">Obtém um recurso VpnGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="84573-103">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84573-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84573-104">SYNTAX</span></span>

### <span data-ttu-id="84573-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="84573-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84573-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84573-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnGateway -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84573-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84573-107">DESCRIPTION</span></span>
<span data-ttu-id="84573-108">Obtém um recurso VpnGateway usando ResourceGroupName e GATEWAYNAME ou lista todos os gateways por ResourceGroupName ou SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="84573-108">Gets a VpnGateway resource using ResourceGroupName and GatewayName OR lists all gateways by ResourceGroupName or SubscriptionId.</span></span>

## <span data-ttu-id="84573-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84573-109">EXAMPLES</span></span>

### <span data-ttu-id="84573-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84573-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

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

<span data-ttu-id="84573-111">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual no oeste dos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="84573-111">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="84573-112">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="84573-112">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="84573-113">Em seguida, ele obtém o VpnGateway usando seu resourceGroupName e o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="84573-113">It then gets the VpnGateway using its resourceGroupName and the gateway name.</span></span>

## <span data-ttu-id="84573-114">OS</span><span class="sxs-lookup"><span data-stu-id="84573-114">PARAMETERS</span></span>

### <span data-ttu-id="84573-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84573-115">-DefaultProfile</span></span>
<span data-ttu-id="84573-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84573-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84573-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="84573-117">-Name</span></span>
<span data-ttu-id="84573-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="84573-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84573-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84573-119">-ResourceGroupName</span></span>
<span data-ttu-id="84573-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84573-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84573-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84573-121">CommonParameters</span></span>
<span data-ttu-id="84573-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84573-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84573-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84573-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84573-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84573-124">INPUTS</span></span>

### <span data-ttu-id="84573-125">System. String</span><span class="sxs-lookup"><span data-stu-id="84573-125">System.String</span></span>

## <span data-ttu-id="84573-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84573-126">OUTPUTS</span></span>

### <span data-ttu-id="84573-127">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="84573-127">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="84573-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84573-128">NOTES</span></span>

## <span data-ttu-id="84573-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84573-129">RELATED LINKS</span></span>
