---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: bbe047def99ef2300c2002a2e8d5beedef26fd4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772727"
---
# <span data-ttu-id="2e33e-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e33e-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="2e33e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e33e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e33e-103">Configura um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2e33e-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="2e33e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e33e-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e33e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e33e-105">DESCRIPTION</span></span>
<span data-ttu-id="2e33e-106">O cmdlet **set-AzVirtualNetworkPeering** configura um emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2e33e-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="2e33e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e33e-107">EXAMPLES</span></span>

### <span data-ttu-id="2e33e-108">Exemplo 1: alterar a configuração de tráfego encaminhado de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2e33e-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="2e33e-109">Exemplo 2: alterar o acesso à rede virtual de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2e33e-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="2e33e-110">Exemplo 3: alterar a configuração da propriedade Transit do gateway de um emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2e33e-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="2e33e-111">Exemplo 4: usar gateways remotos em emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2e33e-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="2e33e-112">Ao alterar essa propriedade para $True, o gateway da VNet do seu par pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="2e33e-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="2e33e-113">No entanto, a VNet de par deve ter um gateway configurado e **AllowGatewayTransit** deve ter um valor de $true.</span><span class="sxs-lookup"><span data-stu-id="2e33e-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="2e33e-114">Esta propriedade não poderá ser usada se um gateway já tiver sido configurado.</span><span class="sxs-lookup"><span data-stu-id="2e33e-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="2e33e-115">OS</span><span class="sxs-lookup"><span data-stu-id="2e33e-115">PARAMETERS</span></span>

### <span data-ttu-id="2e33e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e33e-116">-AsJob</span></span>
<span data-ttu-id="2e33e-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2e33e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e33e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e33e-118">-DefaultProfile</span></span>
<span data-ttu-id="2e33e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e33e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e33e-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e33e-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="2e33e-121">Especifica o emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2e33e-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="2e33e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e33e-122">CommonParameters</span></span>
<span data-ttu-id="2e33e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e33e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e33e-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e33e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e33e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e33e-125">INPUTS</span></span>

### <span data-ttu-id="2e33e-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e33e-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="2e33e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e33e-127">OUTPUTS</span></span>

### <span data-ttu-id="2e33e-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e33e-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="2e33e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e33e-129">NOTES</span></span>

## <span data-ttu-id="2e33e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e33e-130">RELATED LINKS</span></span>

[<span data-ttu-id="2e33e-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e33e-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2e33e-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e33e-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="2e33e-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2e33e-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)