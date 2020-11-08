---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111598"
---
# <span data-ttu-id="6dc35-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6dc35-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="6dc35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6dc35-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc35-103">Obtém o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6dc35-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="6dc35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dc35-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dc35-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6dc35-105">DESCRIPTION</span></span>
<span data-ttu-id="6dc35-106">O cmdlet **Get-AzVirtualNetworkPeering** Obtém o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6dc35-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="6dc35-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6dc35-107">EXAMPLES</span></span>

### <span data-ttu-id="6dc35-108">Exemplo 1: obter um emparelhamento entre duas redes virtuais</span><span class="sxs-lookup"><span data-stu-id="6dc35-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="6dc35-109">Exemplo 2: obter todos os pares na rede virtual</span><span class="sxs-lookup"><span data-stu-id="6dc35-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="6dc35-110">OS</span><span class="sxs-lookup"><span data-stu-id="6dc35-110">PARAMETERS</span></span>

### <span data-ttu-id="6dc35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc35-111">-DefaultProfile</span></span>
<span data-ttu-id="6dc35-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dc35-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dc35-113">-Name</span></span>
<span data-ttu-id="6dc35-114">Especifica o nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6dc35-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6dc35-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc35-115">-ResourceGroupName</span></span>
<span data-ttu-id="6dc35-116">Especifica o nome do grupo de recursos ao qual o emparelhamento de rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="6dc35-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc35-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6dc35-117">-VirtualNetworkName</span></span>
<span data-ttu-id="6dc35-118">Especifica o nome da rede virtual que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6dc35-118">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dc35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc35-119">CommonParameters</span></span>
<span data-ttu-id="6dc35-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc35-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dc35-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc35-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6dc35-122">INPUTS</span></span>

### <span data-ttu-id="6dc35-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc35-123">System.String</span></span>

## <span data-ttu-id="6dc35-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6dc35-124">OUTPUTS</span></span>

### <span data-ttu-id="6dc35-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6dc35-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="6dc35-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6dc35-126">NOTES</span></span>

## <span data-ttu-id="6dc35-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dc35-127">RELATED LINKS</span></span>

[<span data-ttu-id="6dc35-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6dc35-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="6dc35-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6dc35-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="6dc35-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6dc35-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
