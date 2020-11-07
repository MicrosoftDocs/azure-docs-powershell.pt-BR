---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: ceb009dba1984f69e7da3e04a9ae57a9da14c067
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786445"
---
# <span data-ttu-id="56b1d-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="56b1d-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="56b1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="56b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="56b1d-103">Obtém uma sub-rede em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="56b1d-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56b1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56b1d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b1d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="56b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="56b1d-106">O cmdlet **Get-AzureRmVirtualNetworkSubnetConfig** Obtém uma ou mais configurações de sub-rede em uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="56b1d-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="56b1d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56b1d-107">EXAMPLES</span></span>

### <span data-ttu-id="56b1d-108">1: obter uma sub-rede em uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="56b1d-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="56b1d-109">Este exemplo cria um grupo de recursos e uma rede virtual com uma única sub-rede nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="56b1d-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="56b1d-110">Em seguida, ele recupera dados sobre essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="56b1d-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="56b1d-111">OS</span><span class="sxs-lookup"><span data-stu-id="56b1d-111">PARAMETERS</span></span>

### <span data-ttu-id="56b1d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b1d-112">-DefaultProfile</span></span>
<span data-ttu-id="56b1d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56b1d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b1d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="56b1d-114">-Name</span></span>
<span data-ttu-id="56b1d-115">Especifica o nome da configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b1d-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56b1d-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56b1d-116">-VirtualNetwork</span></span>
<span data-ttu-id="56b1d-117">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b1d-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56b1d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b1d-118">CommonParameters</span></span>
<span data-ttu-id="56b1d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b1d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b1d-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b1d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b1d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="56b1d-121">INPUTS</span></span>

### <span data-ttu-id="56b1d-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56b1d-122">PSVirtualNetwork</span></span>
<span data-ttu-id="56b1d-123">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="56b1d-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="56b1d-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="56b1d-124">OUTPUTS</span></span>

### <span data-ttu-id="56b1d-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="56b1d-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="56b1d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="56b1d-126">NOTES</span></span>

## <span data-ttu-id="56b1d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56b1d-127">RELATED LINKS</span></span>

[<span data-ttu-id="56b1d-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="56b1d-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="56b1d-129">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="56b1d-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="56b1d-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="56b1d-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="56b1d-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="56b1d-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


