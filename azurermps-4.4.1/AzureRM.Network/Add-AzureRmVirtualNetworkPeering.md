---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 7a26e563c8416f31178855acb2d97f318001f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433073"
---
# <span data-ttu-id="2fb8e-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2fb8e-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="2fb8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fb8e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb8e-103">Cria um emparelhamento entre duas redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fb8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fb8e-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fb8e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2fb8e-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb8e-106">O cmdlet **Add-AzureRmVirtualNetworkPeering** cria um emparelhamento entre duas redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="2fb8e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fb8e-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb8e-108">Exemplo 1: criar um emparelhamento entre duas redes virtuais na mesma região</span><span class="sxs-lookup"><span data-stu-id="2fb8e-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="2fb8e-109">Observe que um link de emparelhamento deve ser criado a partir de vnet1 para vnet2 e vice-versa para que o emparelhamento funcione.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="2fb8e-110">Exemplo 2: criar um emparelhamento entre duas redes virtuais em diferentes regiões</span><span class="sxs-lookup"><span data-stu-id="2fb8e-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="2fb8e-111">Aqui, "myVnet1" no centro dos EUA, o centro dos EUA está emparelhado com "myVnet2" na central do Canadá.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="2fb8e-112">OS</span><span class="sxs-lookup"><span data-stu-id="2fb8e-112">PARAMETERS</span></span>

### <span data-ttu-id="2fb8e-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="2fb8e-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="2fb8e-114">Indica que esse cmdlet permite o tráfego encaminhado das máquinas virtuais na rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="2fb8e-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="2fb8e-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="2fb8e-116">Sinalizador para permitir que o gatewayLinks seja usado no link da rede virtual remota para esta rede virtual</span><span class="sxs-lookup"><span data-stu-id="2fb8e-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb8e-117">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2fb8e-117">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="2fb8e-118">Indica que esse cmdlet bloqueia as máquinas virtuais no espaço da rede virtual vinculada para acessar todas as máquinas virtuais no espaço da rede virtual local.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-118">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="2fb8e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fb8e-119">-Name</span></span>
<span data-ttu-id="2fb8e-120">Especifica o nome do emparelhamento de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-120">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="2fb8e-121">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2fb8e-121">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="2fb8e-122">Especifica a ID da rede virtual remota.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-122">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="2fb8e-123">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="2fb8e-123">-UseRemoteGateways</span></span>
<span data-ttu-id="2fb8e-124">Indica que esse cmdlet permite gateways remotos nesta rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-124">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="2fb8e-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fb8e-125">-VirtualNetwork</span></span>
<span data-ttu-id="2fb8e-126">Especifica a rede virtual pai.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-126">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="2fb8e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb8e-127">-DefaultProfile</span></span>
<span data-ttu-id="2fb8e-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fb8e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb8e-129">CommonParameters</span></span>
<span data-ttu-id="2fb8e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb8e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb8e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb8e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2fb8e-132">INPUTS</span></span>

### <span data-ttu-id="2fb8e-133">String</span><span class="sxs-lookup"><span data-stu-id="2fb8e-133">String</span></span>
<span data-ttu-id="2fb8e-134">O parâmetro ' RemoteVirtualNetworkId ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2fb8e-134">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2fb8e-135">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fb8e-135">PSVirtualNetwork</span></span>
<span data-ttu-id="2fb8e-136">O parâmetro ' VirtualNetwork ' aceita o valor do tipo ' PSVirtualNetwork ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="2fb8e-136">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="2fb8e-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2fb8e-137">OUTPUTS</span></span>

### <span data-ttu-id="2fb8e-138">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2fb8e-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="2fb8e-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2fb8e-139">NOTES</span></span>

## <span data-ttu-id="2fb8e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fb8e-140">RELATED LINKS</span></span>

[<span data-ttu-id="2fb8e-141">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2fb8e-141">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2fb8e-142">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2fb8e-142">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="2fb8e-143">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2fb8e-143">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="2fb8e-144">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2fb8e-144">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


