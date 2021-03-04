---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 1f24dd8cff058b49c9661da1d2f5f2ae927e1a0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885390"
---
# <span data-ttu-id="10c44-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="10c44-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="10c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10c44-102">SYNOPSIS</span></span>
<span data-ttu-id="10c44-103">Configura um par de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="10c44-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="10c44-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10c44-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c44-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10c44-105">DESCRIPTION</span></span>
<span data-ttu-id="10c44-106">O cmdlet **Set-AzVirtualNetworkPeering** configura um par de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="10c44-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="10c44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10c44-107">EXAMPLES</span></span>

### <span data-ttu-id="10c44-108">Exemplo 1: Alterar a configuração de tráfego encaminhado de uma peering de rede virtual</span><span class="sxs-lookup"><span data-stu-id="10c44-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="10c44-109">Exemplo 2: Alterar o acesso à rede virtual de uma peering de rede virtual</span><span class="sxs-lookup"><span data-stu-id="10c44-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="10c44-110">Exemplo 3: Alterar a configuração da propriedade de trânsito do gateway de um paring de rede virtual</span><span class="sxs-lookup"><span data-stu-id="10c44-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="10c44-111">Exemplo 4: usar gateways remotos no peering de rede virtual</span><span class="sxs-lookup"><span data-stu-id="10c44-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="10c44-112">Ao alterar essa propriedade para $True, o gateway VNet do seu par pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="10c44-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="10c44-113">No entanto, a VNet de par deve ter um gateway configurado e **AllowGatewayTransit** deve ter um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="10c44-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="10c44-114">Essa propriedade não poderá ser usada se um gateway já tiver sido configurado.</span><span class="sxs-lookup"><span data-stu-id="10c44-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="10c44-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10c44-115">PARAMETERS</span></span>

### <span data-ttu-id="10c44-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10c44-116">-AsJob</span></span>
<span data-ttu-id="10c44-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="10c44-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c44-118">-DefaultProfile</span></span>
<span data-ttu-id="10c44-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="10c44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10c44-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="10c44-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="10c44-121">Especifica o paring de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="10c44-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="10c44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c44-122">CommonParameters</span></span>
<span data-ttu-id="10c44-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c44-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c44-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c44-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10c44-125">INPUTS</span></span>

### <span data-ttu-id="10c44-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="10c44-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="10c44-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10c44-127">OUTPUTS</span></span>

### <span data-ttu-id="10c44-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="10c44-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="10c44-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="10c44-129">NOTES</span></span>

## <span data-ttu-id="10c44-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10c44-130">RELATED LINKS</span></span>

[<span data-ttu-id="10c44-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="10c44-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="10c44-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="10c44-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="10c44-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="10c44-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
