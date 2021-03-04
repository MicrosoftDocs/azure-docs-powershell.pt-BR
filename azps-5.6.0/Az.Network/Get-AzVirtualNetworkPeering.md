---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 5648fe6049a7686d5f3930de6ea780598e2c0b06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887644"
---
# <span data-ttu-id="19230-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="19230-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="19230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19230-102">SYNOPSIS</span></span>
<span data-ttu-id="19230-103">Obtém o paring de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19230-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="19230-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="19230-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19230-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="19230-105">DESCRIPTION</span></span>
<span data-ttu-id="19230-106">O cmdlet **Get-AzVirtualNetworkPeering** obtém o paring de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19230-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="19230-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19230-107">EXAMPLES</span></span>

### <span data-ttu-id="19230-108">Exemplo 1: obter um par entre duas redes virtuais</span><span class="sxs-lookup"><span data-stu-id="19230-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="19230-109">Exemplo 2: Obter todos os pares na rede virtual</span><span class="sxs-lookup"><span data-stu-id="19230-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="19230-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="19230-110">PARAMETERS</span></span>

### <span data-ttu-id="19230-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19230-111">-DefaultProfile</span></span>
<span data-ttu-id="19230-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="19230-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19230-113">-Name</span><span class="sxs-lookup"><span data-stu-id="19230-113">-Name</span></span>
<span data-ttu-id="19230-114">Especifica o nome de paração de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19230-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="19230-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19230-115">-ResourceGroupName</span></span>
<span data-ttu-id="19230-116">Especifica o nome do grupo de recursos ao que o paring de rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="19230-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="19230-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="19230-117">-VirtualNetworkName</span></span>
<span data-ttu-id="19230-118">Especifica o nome da rede virtual que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="19230-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="19230-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19230-119">CommonParameters</span></span>
<span data-ttu-id="19230-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19230-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19230-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19230-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19230-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19230-122">INPUTS</span></span>

### <span data-ttu-id="19230-123">System.String</span><span class="sxs-lookup"><span data-stu-id="19230-123">System.String</span></span>

## <span data-ttu-id="19230-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="19230-124">OUTPUTS</span></span>

### <span data-ttu-id="19230-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="19230-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="19230-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="19230-126">NOTES</span></span>

## <span data-ttu-id="19230-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19230-127">RELATED LINKS</span></span>

[<span data-ttu-id="19230-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="19230-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="19230-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="19230-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="19230-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="19230-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
