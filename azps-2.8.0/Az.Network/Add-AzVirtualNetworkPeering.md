---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: c4dbac761b9dd73a7d8d2b73f3d62975f1d7611f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771822"
---
# <span data-ttu-id="52721-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="52721-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="52721-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52721-102">SYNOPSIS</span></span>
<span data-ttu-id="52721-103">Cria um emparelhamento entre duas redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="52721-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="52721-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52721-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52721-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52721-105">DESCRIPTION</span></span>
<span data-ttu-id="52721-106">O cmdlet **Add-AzVirtualNetworkPeering** cria um emparelhamento entre duas redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="52721-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="52721-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52721-107">EXAMPLES</span></span>

### <span data-ttu-id="52721-108">Exemplo 1: criar um emparelhamento entre duas redes virtuais na mesma região</span><span class="sxs-lookup"><span data-stu-id="52721-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="52721-109">Observe que um link de emparelhamento deve ser criado a partir de vnet1 para vnet2 e vice-versa para que o emparelhamento funcione.</span><span class="sxs-lookup"><span data-stu-id="52721-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="52721-110">Exemplo 2: criar um emparelhamento entre duas redes virtuais em diferentes regiões</span><span class="sxs-lookup"><span data-stu-id="52721-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="52721-111">Aqui, "myVnet1" no centro dos EUA, o centro dos EUA está emparelhado com "myVnet2" na central do Canadá.</span><span class="sxs-lookup"><span data-stu-id="52721-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="52721-112">OS</span><span class="sxs-lookup"><span data-stu-id="52721-112">PARAMETERS</span></span>

### <span data-ttu-id="52721-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="52721-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="52721-114">Indica que esse cmdlet permite o tráfego encaminhado das máquinas virtuais na rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="52721-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="52721-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="52721-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="52721-116">Sinalizador para permitir que o gatewayLinks seja usado no link da rede virtual remota para esta rede virtual</span><span class="sxs-lookup"><span data-stu-id="52721-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="52721-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52721-117">-AsJob</span></span>
<span data-ttu-id="52721-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="52721-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52721-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="52721-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="52721-120">Indica que esse cmdlet bloqueia as máquinas virtuais no espaço da rede virtual vinculada para acessar todas as máquinas virtuais no espaço da rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="52721-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="52721-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52721-121">-DefaultProfile</span></span>
<span data-ttu-id="52721-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52721-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52721-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="52721-123">-Name</span></span>
<span data-ttu-id="52721-124">Especifica o nome do emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52721-124">Specifies the name of the virtual network peering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52721-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="52721-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="52721-126">Especifica a ID da rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="52721-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52721-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="52721-127">-UseRemoteGateways</span></span>
<span data-ttu-id="52721-128">Indica que esse cmdlet permite gateways remotos nesta rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52721-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="52721-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="52721-129">-VirtualNetwork</span></span>
<span data-ttu-id="52721-130">Especifica a rede virtual pai.</span><span class="sxs-lookup"><span data-stu-id="52721-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="52721-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52721-131">CommonParameters</span></span>
<span data-ttu-id="52721-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52721-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52721-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52721-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52721-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52721-134">INPUTS</span></span>

### <span data-ttu-id="52721-135">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="52721-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="52721-136">System. String</span><span class="sxs-lookup"><span data-stu-id="52721-136">System.String</span></span>

## <span data-ttu-id="52721-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52721-137">OUTPUTS</span></span>

### <span data-ttu-id="52721-138">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="52721-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="52721-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52721-139">NOTES</span></span>

## <span data-ttu-id="52721-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52721-140">RELATED LINKS</span></span>

[<span data-ttu-id="52721-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="52721-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="52721-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="52721-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="52721-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="52721-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="52721-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="52721-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
