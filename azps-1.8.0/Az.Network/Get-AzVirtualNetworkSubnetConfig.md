---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: e5b881547f84714e238f541948602569c773c9c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600466"
---
# <span data-ttu-id="b3515-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b3515-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b3515-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3515-102">SYNOPSIS</span></span>
<span data-ttu-id="b3515-103">Obtém uma sub-rede em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b3515-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="b3515-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3515-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3515-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3515-105">DESCRIPTION</span></span>
<span data-ttu-id="b3515-106">O cmdlet **Get-AzVirtualNetworkSubnetConfig** Obtém uma ou mais configurações de sub-rede em uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3515-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="b3515-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3515-107">EXAMPLES</span></span>

### <span data-ttu-id="b3515-108">1: obter uma sub-rede em uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="b3515-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="b3515-109">Este exemplo cria um grupo de recursos e uma rede virtual com uma única sub-rede nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b3515-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="b3515-110">Em seguida, ele recupera dados sobre essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="b3515-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="b3515-111">OS</span><span class="sxs-lookup"><span data-stu-id="b3515-111">PARAMETERS</span></span>

### <span data-ttu-id="b3515-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3515-112">-DefaultProfile</span></span>
<span data-ttu-id="b3515-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b3515-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3515-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3515-114">-Name</span></span>
<span data-ttu-id="b3515-115">Especifica o nome da configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3515-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3515-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b3515-116">-VirtualNetwork</span></span>
<span data-ttu-id="b3515-117">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3515-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3515-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3515-118">CommonParameters</span></span>
<span data-ttu-id="b3515-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3515-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3515-120">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3515-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3515-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3515-121">INPUTS</span></span>

### <span data-ttu-id="b3515-122">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b3515-122">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b3515-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3515-123">OUTPUTS</span></span>

### <span data-ttu-id="b3515-124">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b3515-124">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b3515-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3515-125">NOTES</span></span>

## <span data-ttu-id="b3515-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3515-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3515-127">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b3515-127">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b3515-128">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b3515-128">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b3515-129">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b3515-129">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b3515-130">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b3515-130">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


