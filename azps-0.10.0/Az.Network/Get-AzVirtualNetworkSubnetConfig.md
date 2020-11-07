---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775462"
---
# <span data-ttu-id="0c8b0-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c8b0-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="0c8b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8b0-103">Obtém uma sub-rede em uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="0c8b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c8b0-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c8b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c8b0-105">DESCRIPTION</span></span>
<span data-ttu-id="0c8b0-106">O cmdlet **Get-AzVirtualNetworkSubnetConfig** Obtém uma ou mais configurações de sub-rede em uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="0c8b0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c8b0-107">EXAMPLES</span></span>

### <span data-ttu-id="0c8b0-108">1: obter uma sub-rede em uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="0c8b0-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="0c8b0-109">Este exemplo cria um grupo de recursos e uma rede virtual com uma única sub-rede nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="0c8b0-110">Em seguida, ele recupera dados sobre essa sub-rede.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="0c8b0-111">OS</span><span class="sxs-lookup"><span data-stu-id="0c8b0-111">PARAMETERS</span></span>

### <span data-ttu-id="0c8b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8b0-112">-DefaultProfile</span></span>
<span data-ttu-id="0c8b0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c8b0-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c8b0-114">-Name</span></span>
<span data-ttu-id="0c8b0-115">Especifica o nome da configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c8b0-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c8b0-116">-VirtualNetwork</span></span>
<span data-ttu-id="0c8b0-117">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c8b0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8b0-118">CommonParameters</span></span>
<span data-ttu-id="0c8b0-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c8b0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8b0-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c8b0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8b0-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c8b0-121">INPUTS</span></span>

### <span data-ttu-id="0c8b0-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c8b0-122">PSVirtualNetwork</span></span>
<span data-ttu-id="0c8b0-123">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="0c8b0-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="0c8b0-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c8b0-124">OUTPUTS</span></span>

### <span data-ttu-id="0c8b0-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="0c8b0-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="0c8b0-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c8b0-126">NOTES</span></span>

## <span data-ttu-id="0c8b0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c8b0-127">RELATED LINKS</span></span>

[<span data-ttu-id="0c8b0-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c8b0-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0c8b0-129">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c8b0-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0c8b0-130">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c8b0-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="0c8b0-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0c8b0-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


