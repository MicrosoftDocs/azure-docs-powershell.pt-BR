---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnSite.md
ms.openlocfilehash: bd9b0b2a61edf70dfb4cebf392bb64fa742c0417
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885315"
---
# <span data-ttu-id="ae3c2-101">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ae3c2-101">Update-AzVpnSite</span></span>

## <span data-ttu-id="ae3c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3c2-103">Atualiza um site VPN.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-103">Updates a VPN site.</span></span>

## <span data-ttu-id="ae3c2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae3c2-104">SYNTAX</span></span>

### <span data-ttu-id="ae3c2-105">ByVpnSiteNameNoVirtualWanUpdate (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae3c2-105">ByVpnSiteNameNoVirtualWanUpdate (Default)</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-106">ByVpnSiteNameByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="ae3c2-106">ByVpnSiteNameByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanResourceGroupName <String>
 -VirtualWanName <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-107">ByVpnSiteNameByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3c2-107">ByVpnSiteNameByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-108">ByVpnSiteNameByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ae3c2-108">ByVpnSiteNameByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceGroupName <String> -Name <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-109">ByVpnSiteObjectByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="ae3c2-109">ByVpnSiteObjectByVirtualWanName</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-110">ByVpnSiteObjectByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3c2-110">ByVpnSiteObjectByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWanId <String> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-111">ByVpnSiteObjectByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ae3c2-111">ByVpnSiteObjectByVirtualWanObject</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-112">ByVpnSiteObjectNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="ae3c2-112">ByVpnSiteObjectNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -InputObject <PSVpnSite> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-113">ByVpnSiteResourceIdByVirtualWanName</span><span class="sxs-lookup"><span data-stu-id="ae3c2-113">ByVpnSiteResourceIdByVirtualWanName</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanResourceGroupName <String> -VirtualWanName <String>
 [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-114">ByVpnSiteResourceIdByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3c2-114">ByVpnSiteResourceIdByVirtualWanResourceId</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWanId <String> [-IpAddress <String>] [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-115">ByVpnSiteResourceIdByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="ae3c2-115">ByVpnSiteResourceIdByVirtualWanObject</span></span>
```
Update-AzVpnSite -ResourceId <String> -VirtualWan <PSVirtualWan> [-IpAddress <String>]
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>]
 [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae3c2-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span><span class="sxs-lookup"><span data-stu-id="ae3c2-116">ByVpnSiteResourceIdNoVirtualWanUpdate</span></span>
```
Update-AzVpnSite -ResourceId <String> [-IpAddress <String>] [-AddressSpace <String[]>] [-DeviceModel <String>]
 [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>]
 [-BgpPeeringWeight <UInt32>] [-VpnSiteLink <PSVpnSiteLink[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae3c2-117">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae3c2-117">DESCRIPTION</span></span>
<span data-ttu-id="ae3c2-118">O cmdlet **Update-AzVpnSite** atualiza um site VPN.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-118">The **Update-AzVpnSite** cmdlet updates a VPN site.</span></span>

## <span data-ttu-id="ae3c2-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae3c2-119">EXAMPLES</span></span>

### <span data-ttu-id="ae3c2-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae3c2-120">Example 1</span></span>

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

<span data-ttu-id="ae3c2-121">O acima criará um grupo de recursos, a WAN Virtual no Oeste dos EUA, no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-121">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="ae3c2-122">Em seguida, ele cria um VpnSite para representar uma filial de cliente e o vincula à WAN Virtual.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-122">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="ae3c2-123">Depois que o site é criado, ele atualiza o IpAddress do site usando o Set-AzVpnSite comando.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-123">Once the site is created, it updates the IpAddress of the site using the Set-AzVpnSite command.</span></span>

## <span data-ttu-id="ae3c2-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae3c2-124">PARAMETERS</span></span>

### <span data-ttu-id="ae3c2-125">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="ae3c2-125">-AddressSpace</span></span>
<span data-ttu-id="ae3c2-126">Os prefixos de endereço da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-126">The address prefixes of the virtual network.</span></span>
<span data-ttu-id="ae3c2-127">Use isso ou AddressSpaceObject, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-127">Use this or AddressSpaceObject but not both.</span></span>

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

### <span data-ttu-id="ae3c2-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae3c2-128">-AsJob</span></span>
<span data-ttu-id="ae3c2-129">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae3c2-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae3c2-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="ae3c2-130">-BgpAsn</span></span>
<span data-ttu-id="ae3c2-131">O ASN BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="ae3c2-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="ae3c2-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="ae3c2-133">O Endereço de Peering BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="ae3c2-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="ae3c2-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="ae3c2-135">O peso de paração BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="ae3c2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3c2-136">-DefaultProfile</span></span>
<span data-ttu-id="ae3c2-137">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae3c2-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="ae3c2-138">-DeviceModel</span></span>
<span data-ttu-id="ae3c2-139">O modelo de dispositivo do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="ae3c2-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="ae3c2-140">-DeviceVendor</span></span>
<span data-ttu-id="ae3c2-141">O fornecedor de dispositivos do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="ae3c2-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae3c2-142">-InputObject</span></span>
<span data-ttu-id="ae3c2-143">O objeto de site vpn a ser modificado</span><span class="sxs-lookup"><span data-stu-id="ae3c2-143">The vpn site object to be modified</span></span>

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

### <span data-ttu-id="ae3c2-144">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ae3c2-144">-IpAddress</span></span>
<span data-ttu-id="ae3c2-145">Endereço IP do gateway de rede local.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-145">IP address of local network gateway.</span></span>

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

### <span data-ttu-id="ae3c2-146">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="ae3c2-146">-LinkSpeedInMbps</span></span>
<span data-ttu-id="ae3c2-147">O modelo de dispositivo do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-147">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="ae3c2-148">-Name</span><span class="sxs-lookup"><span data-stu-id="ae3c2-148">-Name</span></span>
<span data-ttu-id="ae3c2-149">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-149">The resource name.</span></span>

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

### <span data-ttu-id="ae3c2-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="ae3c2-150">-O365Policy</span></span>
<span data-ttu-id="ae3c2-151">A política de quebra de tráfego do office 365 para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="ae3c2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3c2-152">-ResourceGroupName</span></span>
<span data-ttu-id="ae3c2-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-153">The resource group name.</span></span>

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

### <span data-ttu-id="ae3c2-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3c2-154">-ResourceId</span></span>
<span data-ttu-id="ae3c2-155">A ID de recurso do Azure para o site vpn.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-155">The Azure resource ID for the vpn site.</span></span>

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

### <span data-ttu-id="ae3c2-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae3c2-156">-Tag</span></span>
<span data-ttu-id="ae3c2-157">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-157">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ae3c2-158">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="ae3c2-158">-VirtualWan</span></span>
<span data-ttu-id="ae3c2-159">O VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-159">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="ae3c2-160">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="ae3c2-160">-VirtualWanId</span></span>
<span data-ttu-id="ae3c2-161">O ResourceId VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-161">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="ae3c2-162">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="ae3c2-162">-VirtualWanName</span></span>
<span data-ttu-id="ae3c2-163">O nome do VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-163">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="ae3c2-164">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3c2-164">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="ae3c2-165">O nome do grupo de recursos do VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-165">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="ae3c2-166">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ae3c2-166">-VpnSiteLink</span></span>
<span data-ttu-id="ae3c2-167">A lista de VpnSiteLinks que este VpnSite tem.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-167">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="ae3c2-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae3c2-168">-Confirm</span></span>
<span data-ttu-id="ae3c2-169">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae3c2-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3c2-170">-WhatIf</span></span>
<span data-ttu-id="ae3c2-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae3c2-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae3c2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3c2-173">CommonParameters</span></span>
<span data-ttu-id="ae3c2-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae3c2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3c2-175">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae3c2-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3c2-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae3c2-176">INPUTS</span></span>

### <span data-ttu-id="ae3c2-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="ae3c2-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="ae3c2-178">System.String</span><span class="sxs-lookup"><span data-stu-id="ae3c2-178">System.String</span></span>

## <span data-ttu-id="ae3c2-179">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae3c2-179">OUTPUTS</span></span>

### <span data-ttu-id="ae3c2-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="ae3c2-180">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="ae3c2-181">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae3c2-181">NOTES</span></span>

## <span data-ttu-id="ae3c2-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae3c2-182">RELATED LINKS</span></span>

[<span data-ttu-id="ae3c2-183">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ae3c2-183">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="ae3c2-184">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ae3c2-184">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="ae3c2-185">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ae3c2-185">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)
