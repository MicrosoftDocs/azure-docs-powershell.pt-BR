---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: b7ed573ed8df8086cd5cef04204020498e1413c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258765"
---
# <span data-ttu-id="9ef80-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9ef80-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="9ef80-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ef80-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef80-103">Atualiza um site VPN.</span><span class="sxs-lookup"><span data-stu-id="9ef80-103">Updates a VPN site.</span></span>

## <span data-ttu-id="9ef80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ef80-104">SYNTAX</span></span>

### <span data-ttu-id="9ef80-105">ByVpnSiteNameNoVirtualWanUpdate (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ef80-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef80-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ef80-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef80-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef80-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ef80-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9ef80-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ef80-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ef80-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef80-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef80-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ef80-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9ef80-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ef80-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="9ef80-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef80-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ef80-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef80-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef80-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef80-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="9ef80-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ef80-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="9ef80-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef80-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ef80-117">DESCRIPTION</span></span>
<span data-ttu-id="9ef80-118">O cmdlet **Update-AzVpnSite** atualiza um site VPN.</span><span class="sxs-lookup"><span data-stu-id="9ef80-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="9ef80-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ef80-119">EXAMPLES</span></span>

### <span data-ttu-id="9ef80-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ef80-120">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "2.3.5.5"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 2.3.4.5
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="9ef80-121">A seguir, você criará um grupo de recursos, uma WAN virtual no oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef80-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="9ef80-122">Em seguida, ele cria um VpnSite para representar uma ramificação do cliente e a vincula à rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="9ef80-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="9ef80-123">Após a criação do site, ele atualiza o IpAddress do site usando o comando Set-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="9ef80-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="9ef80-124">OS</span><span class="sxs-lookup"><span data-stu-id="9ef80-124">PARAMETERS</span></span>

### <span data-ttu-id="9ef80-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="9ef80-125">-AddressSpace</span></span>
<span data-ttu-id="9ef80-126">Os prefixos de endereço da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9ef80-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="9ef80-127">Use este ou o AddressSpaceObject, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="9ef80-127">Use this or AddressSpaceObject but not both.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ef80-128">-AsJob</span></span>
<span data-ttu-id="9ef80-129">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9ef80-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ef80-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="9ef80-130">-BgpAsn</span></span>
<span data-ttu-id="9ef80-131">A ASN do BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9ef80-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="9ef80-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="9ef80-133">O endereço de emparelhamento BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9ef80-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="9ef80-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="9ef80-135">O peso de emparelhamento BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9ef80-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef80-136">-DefaultProfile</span></span>
<span data-ttu-id="9ef80-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ef80-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef80-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="9ef80-138">-DeviceModel</span></span>
<span data-ttu-id="9ef80-139">O modelo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="9ef80-139">The device model of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9ef80-140">-DeviceVendor</span></span>
<span data-ttu-id="9ef80-141">O fornecedor do dispositivo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="9ef80-141">The device vendor of the remote vpn device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ef80-142">-InputObject</span></span>
<span data-ttu-id="9ef80-143">O objeto de site VPN a ser modificado</span><span class="sxs-lookup"><span data-stu-id="9ef80-143">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObjectByVirtualWanName, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteObjectNoVirtualWanUpdate
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="9ef80-144">-IpAddress</span></span>
<span data-ttu-id="9ef80-145">Endereço IP do gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="9ef80-145">IP address of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="9ef80-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="9ef80-147">O modelo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="9ef80-147">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ef80-148">-Name</span></span>
<span data-ttu-id="9ef80-149">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9ef80-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="9ef80-150">-O365Policy</span></span>
<span data-ttu-id="9ef80-151">A política de debates de tráfego do Office 365 para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="9ef80-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef80-152">-ResourceGroupName</span></span>
<span data-ttu-id="9ef80-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ef80-153">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameNoVirtualWanUpdate, ByVpnSiteNameByVirtualWanName, ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteNameByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef80-154">-ResourceId</span></span>
<span data-ttu-id="9ef80-155">A ID de recurso do Azure para o site VPN.</span><span class="sxs-lookup"><span data-stu-id="9ef80-155">The Azure resource ID for the vpn site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceIdByVirtualWanName, ByVpnSiteResourceIdByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanObject, ByVpnSiteResourceIdNoVirtualWanUpdate
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="9ef80-156">-Tag</span></span>
<span data-ttu-id="9ef80-157">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ef80-157">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="9ef80-158">-VirtualWan</span></span>
<span data-ttu-id="9ef80-159">O VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="9ef80-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVpnSiteNameByVirtualWanObject, ByVpnSiteObjectByVirtualWanObject, ByVpnSiteResourceIdByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="9ef80-160">-VirtualWanId</span></span>
<span data-ttu-id="9ef80-161">O ResourceId VirtualWan que este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="9ef80-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanResourceId, ByVpnSiteObjectByVirtualWanResourceId, ByVpnSiteResourceIdByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="9ef80-162">-VirtualWanName</span></span>
<span data-ttu-id="9ef80-163">O nome do VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="9ef80-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef80-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="9ef80-165">O nome do grupo de recursos do VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="9ef80-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteNameByVirtualWanName, ByVpnSiteObjectByVirtualWanName, ByVpnSiteResourceIdByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="9ef80-166">-VpnSiteLink</span></span>
<span data-ttu-id="9ef80-167">A lista de VpnSiteLinks que esta VpnSite tem.</span><span class="sxs-lookup"><span data-stu-id="9ef80-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ef80-168">-Confirm</span></span>
<span data-ttu-id="9ef80-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef80-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef80-170">-WhatIf</span></span>
<span data-ttu-id="9ef80-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ef80-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef80-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ef80-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef80-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef80-173">CommonParameters</span></span>
<span data-ttu-id="9ef80-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef80-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef80-175">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ef80-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef80-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ef80-176">INPUTS</span></span>

### <span data-ttu-id="9ef80-177">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="9ef80-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="9ef80-178">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef80-178">System.String</span></span>

## <span data-ttu-id="9ef80-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ef80-179">OUTPUTS</span></span>

### <span data-ttu-id="9ef80-180">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="9ef80-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="9ef80-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ef80-181">NOTES</span></span>

## <span data-ttu-id="9ef80-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ef80-182">RELATED LINKS</span></span>

[<span data-ttu-id="9ef80-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9ef80-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="9ef80-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9ef80-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="9ef80-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9ef80-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
