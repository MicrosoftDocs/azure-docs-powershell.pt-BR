---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775463"
---
# <span data-ttu-id="413da-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="413da-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="413da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="413da-102">SYNOPSIS</span></span>
<span data-ttu-id="413da-103">Obtém o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="413da-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="413da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="413da-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="413da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="413da-105">DESCRIPTION</span></span>
<span data-ttu-id="413da-106">O cmdlet **Get-AzVirtualNetworkPeering** Obtém o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="413da-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="413da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="413da-107">EXAMPLES</span></span>

### <span data-ttu-id="413da-108">Exemplo 1: obter um emparelhamento entre duas redes virtuais</span><span class="sxs-lookup"><span data-stu-id="413da-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="413da-109">OS</span><span class="sxs-lookup"><span data-stu-id="413da-109">PARAMETERS</span></span>

### <span data-ttu-id="413da-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413da-110">-DefaultProfile</span></span>
<span data-ttu-id="413da-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="413da-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="413da-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="413da-112">-Name</span></span>
<span data-ttu-id="413da-113">Especifica o nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="413da-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413da-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413da-114">-ResourceGroupName</span></span>
<span data-ttu-id="413da-115">Especifica o nome do grupo de recursos ao qual o emparelhamento de rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="413da-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413da-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="413da-116">-VirtualNetworkName</span></span>
<span data-ttu-id="413da-117">Especifica o nome da rede virtual que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="413da-117">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413da-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413da-118">CommonParameters</span></span>
<span data-ttu-id="413da-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413da-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413da-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413da-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413da-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="413da-121">INPUTS</span></span>

## <span data-ttu-id="413da-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="413da-122">OUTPUTS</span></span>

### <span data-ttu-id="413da-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="413da-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="413da-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="413da-124">NOTES</span></span>

## <span data-ttu-id="413da-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="413da-125">RELATED LINKS</span></span>

[<span data-ttu-id="413da-126">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="413da-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="413da-127">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="413da-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="413da-128">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="413da-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


