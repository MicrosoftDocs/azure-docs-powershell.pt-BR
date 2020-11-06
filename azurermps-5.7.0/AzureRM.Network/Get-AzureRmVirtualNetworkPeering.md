---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 0c68886906957204ee0885a00bfc07740fb6ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602632"
---
# <span data-ttu-id="567c6-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="567c6-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="567c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="567c6-102">SYNOPSIS</span></span>
<span data-ttu-id="567c6-103">Obtém o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="567c6-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="567c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="567c6-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="567c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="567c6-105">DESCRIPTION</span></span>
<span data-ttu-id="567c6-106">O cmdlet **Get-AzureRmVirtualNetworkPeering** Obtém o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="567c6-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="567c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="567c6-107">EXAMPLES</span></span>

### <span data-ttu-id="567c6-108">Exemplo 1: obter um emparelhamento entre duas redes virtuais</span><span class="sxs-lookup"><span data-stu-id="567c6-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="567c6-109">OS</span><span class="sxs-lookup"><span data-stu-id="567c6-109">PARAMETERS</span></span>

### <span data-ttu-id="567c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567c6-110">-DefaultProfile</span></span>
<span data-ttu-id="567c6-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="567c6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="567c6-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="567c6-112">-Name</span></span>
<span data-ttu-id="567c6-113">Especifica o nome de emparelhamento da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="567c6-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="567c6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="567c6-114">-ResourceGroupName</span></span>
<span data-ttu-id="567c6-115">Especifica o nome do grupo de recursos ao qual o emparelhamento de rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="567c6-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="567c6-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="567c6-116">-VirtualNetworkName</span></span>
<span data-ttu-id="567c6-117">Especifica o nome da rede virtual que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="567c6-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="567c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567c6-118">CommonParameters</span></span>
<span data-ttu-id="567c6-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567c6-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="567c6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567c6-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="567c6-121">INPUTS</span></span>

### <span data-ttu-id="567c6-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="567c6-122">None</span></span>
<span data-ttu-id="567c6-123">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="567c6-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="567c6-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="567c6-124">OUTPUTS</span></span>

### <span data-ttu-id="567c6-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="567c6-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="567c6-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="567c6-126">NOTES</span></span>

## <span data-ttu-id="567c6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="567c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="567c6-128">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="567c6-128">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="567c6-129">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="567c6-129">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="567c6-130">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="567c6-130">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


