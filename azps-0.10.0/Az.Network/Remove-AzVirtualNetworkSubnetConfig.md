---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 5f05672c5fd3f0866652507fd0f61f7a8b6e0fcc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776592"
---
# <span data-ttu-id="4928c-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4928c-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="4928c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4928c-102">SYNOPSIS</span></span>
<span data-ttu-id="4928c-103">Remove uma configuração de sub-rede de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4928c-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="4928c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4928c-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4928c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4928c-105">DESCRIPTION</span></span>
<span data-ttu-id="4928c-106">O cmdlet **Remove-AzVirtualNetworkSubnetConfig** remove uma sub-rede de uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4928c-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="4928c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4928c-107">EXAMPLES</span></span>

### <span data-ttu-id="4928c-108">1: remover uma sub-rede de uma rede virtual e atualizar a rede virtual</span><span class="sxs-lookup"><span data-stu-id="4928c-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="4928c-109">Este exemplo cria um grupo de recursos e uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="4928c-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="4928c-110">Em seguida, ele usa o comando Remove-AzVirtualNetworkSubnetConfig para remover a sub-rede back-end da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4928c-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="4928c-111">Set-AzVirtualNetwork, em seguida, é chamado para modificar a rede virtual no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4928c-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="4928c-112">OS</span><span class="sxs-lookup"><span data-stu-id="4928c-112">PARAMETERS</span></span>

### <span data-ttu-id="4928c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4928c-113">-DefaultProfile</span></span>
<span data-ttu-id="4928c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4928c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4928c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4928c-115">-Name</span></span>
<span data-ttu-id="4928c-116">Especifica o nome da configuração de sub-rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4928c-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="4928c-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4928c-117">-VirtualNetwork</span></span>
<span data-ttu-id="4928c-118">Especifica o objeto **VirtualNetwork** que contém a configuração de sub-rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4928c-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="4928c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4928c-119">CommonParameters</span></span>
<span data-ttu-id="4928c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4928c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4928c-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4928c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4928c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4928c-122">INPUTS</span></span>

### <span data-ttu-id="4928c-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4928c-123">PSVirtualNetwork</span></span>
<span data-ttu-id="4928c-124">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="4928c-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="4928c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4928c-125">OUTPUTS</span></span>

### <span data-ttu-id="4928c-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4928c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4928c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4928c-127">NOTES</span></span>

## <span data-ttu-id="4928c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4928c-128">RELATED LINKS</span></span>

[<span data-ttu-id="4928c-129">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4928c-129">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4928c-130">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4928c-130">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4928c-131">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4928c-131">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="4928c-132">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4928c-132">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


