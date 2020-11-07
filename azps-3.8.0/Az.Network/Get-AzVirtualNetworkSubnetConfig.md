---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941368"
---
# <span data-ttu-id="7c562-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7c562-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="7c562-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c562-102">SYNOPSIS</span></span>
<span data-ttu-id="7c562-103">Obtém uma sub-rede em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7c562-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="7c562-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c562-104">SYNTAX</span></span>

### <span data-ttu-id="7c562-105">GetByVirtualNetwork (padrão)</span><span class="sxs-lookup"><span data-stu-id="7c562-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c562-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c562-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c562-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c562-107">DESCRIPTION</span></span>
<span data-ttu-id="7c562-108">O cmdlet **Get-AzVirtualNetworkSubnetConfig** Obtém uma ou mais configurações de sub-rede em uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c562-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="7c562-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c562-109">EXAMPLES</span></span>

### <span data-ttu-id="7c562-110">1: obter uma sub-rede em uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="7c562-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="7c562-111">Este exemplo cria um grupo de recursos e uma rede virtual com uma única sub-rede nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c562-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="7c562-112">Em seguida, ele recupera dados sobre essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7c562-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="7c562-113">OS</span><span class="sxs-lookup"><span data-stu-id="7c562-113">PARAMETERS</span></span>

### <span data-ttu-id="7c562-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c562-114">-DefaultProfile</span></span>
<span data-ttu-id="7c562-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c562-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c562-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c562-116">-Name</span></span>
<span data-ttu-id="7c562-117">Especifica o nome da configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c562-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7c562-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c562-118">-ResourceId</span></span>
<span data-ttu-id="7c562-119">Especifica a ID do recurso da sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c562-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7c562-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c562-120">-VirtualNetwork</span></span>
<span data-ttu-id="7c562-121">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c562-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7c562-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c562-122">CommonParameters</span></span>
<span data-ttu-id="7c562-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c562-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c562-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c562-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c562-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c562-125">INPUTS</span></span>

### <span data-ttu-id="7c562-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c562-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="7c562-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7c562-127">System.String</span></span>

## <span data-ttu-id="7c562-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c562-128">OUTPUTS</span></span>

### <span data-ttu-id="7c562-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7c562-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7c562-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c562-130">NOTES</span></span>

## <span data-ttu-id="7c562-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c562-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c562-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7c562-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7c562-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7c562-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7c562-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7c562-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7c562-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7c562-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
