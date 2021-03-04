---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c820d44ed8c3d32feb3f1d63d2b52a487c27f0dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892398"
---
# <span data-ttu-id="62aa4-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="62aa4-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="62aa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="62aa4-103">Remove uma configuração de sub-rede de uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="62aa4-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="62aa4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="62aa4-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62aa4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="62aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="62aa4-106">O cmdlet **Remove-AzVirtualNetworkSubnetConfig** remove uma sub-rede de uma rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="62aa4-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="62aa4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="62aa4-108">1: Remover uma sub-rede de uma rede virtual e atualizar a rede virtual</span><span class="sxs-lookup"><span data-stu-id="62aa4-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
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

<span data-ttu-id="62aa4-109">Este exemplo cria um grupo de recursos e uma rede virtual com duas sub-redes.</span><span class="sxs-lookup"><span data-stu-id="62aa4-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="62aa4-110">Em seguida, ele usa o Remove-AzVirtualNetworkSubnetConfig para remover a sub-rede back-end da representação na memória da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="62aa4-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="62aa4-111">Set-AzVirtualNetwork então é chamado para modificar a rede virtual no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="62aa4-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="62aa4-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="62aa4-112">PARAMETERS</span></span>

### <span data-ttu-id="62aa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62aa4-113">-DefaultProfile</span></span>
<span data-ttu-id="62aa4-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="62aa4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62aa4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="62aa4-115">-Name</span></span>
<span data-ttu-id="62aa4-116">Especifica o nome da configuração da sub-rede a ser removido.</span><span class="sxs-lookup"><span data-stu-id="62aa4-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="62aa4-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62aa4-117">-VirtualNetwork</span></span>
<span data-ttu-id="62aa4-118">Especifica o **objeto VirtualNetwork** que contém a configuração da sub-rede a ser removido.</span><span class="sxs-lookup"><span data-stu-id="62aa4-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="62aa4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62aa4-119">CommonParameters</span></span>
<span data-ttu-id="62aa4-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62aa4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62aa4-121">Para obter mais informações, consulte [about_CommonParameters] ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62aa4-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62aa4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62aa4-122">INPUTS</span></span>

### <span data-ttu-id="62aa4-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62aa4-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="62aa4-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="62aa4-124">OUTPUTS</span></span>

### <span data-ttu-id="62aa4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62aa4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="62aa4-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="62aa4-126">NOTES</span></span>

## <span data-ttu-id="62aa4-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62aa4-127">RELATED LINKS</span></span>

[<span data-ttu-id="62aa4-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="62aa4-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="62aa4-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="62aa4-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="62aa4-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="62aa4-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="62aa4-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="62aa4-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


