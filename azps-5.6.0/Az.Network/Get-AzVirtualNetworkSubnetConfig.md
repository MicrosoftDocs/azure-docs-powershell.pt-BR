---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: bee7857751b9553314085ab3fee4f5edbadce1b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888670"
---
# <span data-ttu-id="19a69-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19a69-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="19a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19a69-102">SYNOPSIS</span></span>
<span data-ttu-id="19a69-103">Obtém uma sub-rede em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19a69-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="19a69-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="19a69-104">SYNTAX</span></span>

### <span data-ttu-id="19a69-105">GetByVirtualNetwork (Padrão)</span><span class="sxs-lookup"><span data-stu-id="19a69-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19a69-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="19a69-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19a69-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="19a69-107">DESCRIPTION</span></span>
<span data-ttu-id="19a69-108">O cmdlet **Get-AzVirtualNetworkSubnetConfig obtém** uma ou mais configurações de sub-rede em uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="19a69-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="19a69-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19a69-109">EXAMPLES</span></span>

### <span data-ttu-id="19a69-110">1: Obter uma sub-rede em uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="19a69-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="19a69-111">Este exemplo cria um grupo de recursos e uma rede virtual com uma única sub-rede nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19a69-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="19a69-112">Em seguida, ele recupera dados sobre essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="19a69-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="19a69-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="19a69-113">PARAMETERS</span></span>

### <span data-ttu-id="19a69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a69-114">-DefaultProfile</span></span>
<span data-ttu-id="19a69-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="19a69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19a69-116">-Name</span><span class="sxs-lookup"><span data-stu-id="19a69-116">-Name</span></span>
<span data-ttu-id="19a69-117">Especifica o nome da configuração de sub-rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19a69-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19a69-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19a69-118">-ResourceId</span></span>
<span data-ttu-id="19a69-119">Especifica a id de recurso da sub-rede que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19a69-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19a69-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19a69-120">-VirtualNetwork</span></span>
<span data-ttu-id="19a69-121">Especifica o **objeto VirtualNetwork** que contém a configuração de sub-rede que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19a69-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19a69-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a69-122">CommonParameters</span></span>
<span data-ttu-id="19a69-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19a69-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a69-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19a69-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a69-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19a69-125">INPUTS</span></span>

### <span data-ttu-id="19a69-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="19a69-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="19a69-127">System.String</span><span class="sxs-lookup"><span data-stu-id="19a69-127">System.String</span></span>

## <span data-ttu-id="19a69-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="19a69-128">OUTPUTS</span></span>

### <span data-ttu-id="19a69-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="19a69-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="19a69-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="19a69-130">NOTES</span></span>

## <span data-ttu-id="19a69-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19a69-131">RELATED LINKS</span></span>

[<span data-ttu-id="19a69-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19a69-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19a69-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19a69-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19a69-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19a69-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19a69-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19a69-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
