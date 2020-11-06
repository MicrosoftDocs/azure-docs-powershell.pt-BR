---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: f2e0bb88df867da0a110422debea4d6688ad3af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433061"
---
# <span data-ttu-id="52f6d-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="52f6d-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="52f6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="52f6d-103">Remove uma configuração de sub-rede de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52f6d-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52f6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52f6d-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52f6d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="52f6d-106">O cmdlet **Remove-AzureRmVirtualNetworkSubnetConfig** remove uma sub-rede de uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="52f6d-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="52f6d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52f6d-107">EXAMPLES</span></span>

### <span data-ttu-id="52f6d-108">1: remover uma sub-rede de uma rede virtual e atualizar a rede virtual</span><span class="sxs-lookup"><span data-stu-id="52f6d-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="52f6d-109">Este exemplo cria um grupo de recursos e uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="52f6d-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="52f6d-110">Em seguida, ele usa o comando Remove-AzureRmVirtualNetworkSubnetConfig para remover a sub-rede back-end da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52f6d-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="52f6d-111">Set-AzureRmVirtualNetwork, em seguida, é chamado para modificar a rede virtual no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="52f6d-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="52f6d-112">OS</span><span class="sxs-lookup"><span data-stu-id="52f6d-112">PARAMETERS</span></span>

### <span data-ttu-id="52f6d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="52f6d-113">-Name</span></span>
<span data-ttu-id="52f6d-114">Especifica o nome da configuração de sub-rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="52f6d-114">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="52f6d-115">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="52f6d-115">-VirtualNetwork</span></span>
<span data-ttu-id="52f6d-116">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="52f6d-116">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="52f6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f6d-117">-DefaultProfile</span></span>
<span data-ttu-id="52f6d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52f6d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f6d-119">CommonParameters</span></span>
<span data-ttu-id="52f6d-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f6d-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f6d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f6d-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52f6d-122">INPUTS</span></span>

### <span data-ttu-id="52f6d-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="52f6d-123">PSVirtualNetwork</span></span>
<span data-ttu-id="52f6d-124">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="52f6d-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="52f6d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52f6d-125">OUTPUTS</span></span>

### <span data-ttu-id="52f6d-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="52f6d-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="52f6d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52f6d-127">NOTES</span></span>

## <span data-ttu-id="52f6d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52f6d-128">RELATED LINKS</span></span>

[<span data-ttu-id="52f6d-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="52f6d-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="52f6d-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="52f6d-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="52f6d-131">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="52f6d-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="52f6d-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="52f6d-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)

