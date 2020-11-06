---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427832"
---
# <span data-ttu-id="5e47e-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e47e-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="5e47e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e47e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e47e-103">Configura um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5e47e-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e47e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e47e-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e47e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e47e-105">DESCRIPTION</span></span>
<span data-ttu-id="5e47e-106">O cmdlet **set-AzureRmVirtualNetworkPeering** configura um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5e47e-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="5e47e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e47e-107">EXAMPLES</span></span>

### <span data-ttu-id="5e47e-108">Exemplo 1: alterar a configuração de tráfego encaminhado de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5e47e-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="5e47e-109">Exemplo 2: alterar o acesso à rede virtual de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5e47e-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="5e47e-110">Exemplo 3: alterar a configuração da propriedade Transit do gateway de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5e47e-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="5e47e-111">Exemplo 4: usar gateways remotos em emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5e47e-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="5e47e-112">Ao alterar essa propriedade para $True, o gateway da VNet do seu par pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="5e47e-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="5e47e-113">No entanto, a VNet de par deve ter um gateway configurado e **AllowGatewayTransit** deve ter um valor de $true.</span><span class="sxs-lookup"><span data-stu-id="5e47e-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="5e47e-114">Esta propriedade não poderá ser usada se um gateway já tiver sido configurado.</span><span class="sxs-lookup"><span data-stu-id="5e47e-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="5e47e-115">OS</span><span class="sxs-lookup"><span data-stu-id="5e47e-115">PARAMETERS</span></span>

### <span data-ttu-id="5e47e-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e47e-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="5e47e-117">Especifica o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5e47e-117">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e47e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e47e-118">-DefaultProfile</span></span>
<span data-ttu-id="5e47e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e47e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e47e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e47e-120">CommonParameters</span></span>
<span data-ttu-id="5e47e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e47e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e47e-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e47e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e47e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e47e-123">INPUTS</span></span>

### <span data-ttu-id="5e47e-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e47e-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="5e47e-125">O parâmetro ' VirtualNetworkPeering ' aceita o valor do tipo ' PSVirtualNetworkPeering ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5e47e-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="5e47e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e47e-126">OUTPUTS</span></span>

### <span data-ttu-id="5e47e-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e47e-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="5e47e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e47e-128">NOTES</span></span>

## <span data-ttu-id="5e47e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e47e-129">RELATED LINKS</span></span>

[<span data-ttu-id="5e47e-130">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e47e-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="5e47e-131">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e47e-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="5e47e-132">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5e47e-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


