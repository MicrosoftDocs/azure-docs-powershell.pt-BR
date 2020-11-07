---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: d6f258bf15ac89dc0321c61ab592ef9fc6e58a7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785153"
---
# <span data-ttu-id="c38a7-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c38a7-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="c38a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c38a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c38a7-103">Configura um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c38a7-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c38a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c38a7-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c38a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c38a7-105">DESCRIPTION</span></span>
<span data-ttu-id="c38a7-106">O cmdlet **set-AzureRmVirtualNetworkPeering** configura um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c38a7-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="c38a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c38a7-107">EXAMPLES</span></span>

### <span data-ttu-id="c38a7-108">Exemplo 1: alterar a configuração de tráfego encaminhado de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c38a7-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="c38a7-109">Exemplo 2: alterar o acesso à rede virtual de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c38a7-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="c38a7-110">Exemplo 3: alterar a configuração da propriedade Transit do gateway de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c38a7-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="c38a7-111">Exemplo 4: usar gateways remotos em emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="c38a7-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="c38a7-112">Ao alterar essa propriedade para $True, o gateway da VNet do seu par pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="c38a7-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="c38a7-113">No entanto, a VNet de par deve ter um gateway configurado e **AllowGatewayTransit** deve ter um valor de $true.</span><span class="sxs-lookup"><span data-stu-id="c38a7-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="c38a7-114">Esta propriedade não poderá ser usada se um gateway já tiver sido configurado.</span><span class="sxs-lookup"><span data-stu-id="c38a7-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="c38a7-115">OS</span><span class="sxs-lookup"><span data-stu-id="c38a7-115">PARAMETERS</span></span>

### <span data-ttu-id="c38a7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c38a7-116">-AsJob</span></span>
<span data-ttu-id="c38a7-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c38a7-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38a7-118">-DefaultProfile</span></span>
<span data-ttu-id="c38a7-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c38a7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c38a7-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c38a7-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="c38a7-121">Especifica o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c38a7-121">Specifies the virtual network peering.</span></span>

```yaml
Type: PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38a7-122">CommonParameters</span></span>
<span data-ttu-id="c38a7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38a7-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c38a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38a7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c38a7-125">INPUTS</span></span>

### <span data-ttu-id="c38a7-126">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c38a7-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="c38a7-127">O parâmetro ' VirtualNetworkPeering ' aceita o valor do tipo ' PSVirtualNetworkPeering ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c38a7-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="c38a7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c38a7-128">OUTPUTS</span></span>

### <span data-ttu-id="c38a7-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c38a7-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="c38a7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c38a7-130">NOTES</span></span>

## <span data-ttu-id="c38a7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c38a7-131">RELATED LINKS</span></span>

[<span data-ttu-id="c38a7-132">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c38a7-132">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="c38a7-133">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c38a7-133">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="c38a7-134">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c38a7-134">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


