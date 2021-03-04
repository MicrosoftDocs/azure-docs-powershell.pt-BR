---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 578835b000b6efecb3a1429b884ad2416f6c289d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889428"
---
# <span data-ttu-id="52eb8-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="52eb8-101">New-AzVpnSite</span></span>

## <span data-ttu-id="52eb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="52eb8-103">Cria um novo recurso vpnSite do Azure.</span><span class="sxs-lookup"><span data-stu-id="52eb8-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="52eb8-104">Esta é uma representação rm de filiais do cliente que são carregadas para a conectividade do Azure para S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="52eb8-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="52eb8-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52eb8-105">SYNTAX</span></span>

### <span data-ttu-id="52eb8-106">ByVirtualWanNameByVpnSiteIpAddress (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52eb8-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52eb8-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="52eb8-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52eb8-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="52eb8-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52eb8-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="52eb8-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52eb8-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="52eb8-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52eb8-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="52eb8-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52eb8-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52eb8-112">DESCRIPTION</span></span>
<span data-ttu-id="52eb8-113">Cria um novo recurso vpnSite do Azure.</span><span class="sxs-lookup"><span data-stu-id="52eb8-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="52eb8-114">Esta é uma representação rm de filiais do cliente que são carregadas para a conectividade do Azure para S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="52eb8-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="52eb8-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52eb8-115">EXAMPLES</span></span>

### <span data-ttu-id="52eb8-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52eb8-116">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "nonlinkSite"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "nonlinkSite" -Name myVirtualWAN -Location "East US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "nonlinkSite" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : nonlinkSite
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/nonlinkSite/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="52eb8-117">O acima criará um grupo de recursos, a WAN Virtual no Leste dos EUA, no grupo de recursos "nonlinkSite" no Azure.</span><span class="sxs-lookup"><span data-stu-id="52eb8-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="52eb8-118">Em seguida, ele cria um VpnSite para representar uma filial de cliente e o vincula à WAN Virtual.</span><span class="sxs-lookup"><span data-stu-id="52eb8-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="52eb8-119">Em seguida, uma conexão IPSec pode ser configurada com essa ramificação e uma VpnGateway usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="52eb8-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="52eb8-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="52eb8-120">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "East US" -Name "multilink"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName multilink -Name myVirtualWAN -Location "East US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "multilink" -Name "testVpnSite" -Location "East US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)
```

<span data-ttu-id="52eb8-121">O acima criará um grupo de recursos, a WAN Virtual e um VpnSite com 1 VpnSiteLinks no Leste dos EUA no grupo de recursos "multilink" no Azure.</span><span class="sxs-lookup"><span data-stu-id="52eb8-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="52eb8-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="52eb8-122">Example 3</span></span>

<span data-ttu-id="52eb8-123">Cria um novo recurso vpnSite do Azure.</span><span class="sxs-lookup"><span data-stu-id="52eb8-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="52eb8-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="52eb8-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="52eb8-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52eb8-125">PARAMETERS</span></span>

### <span data-ttu-id="52eb8-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="52eb8-126">-AddressSpace</span></span>
<span data-ttu-id="52eb8-127">Os prefixos de endereço da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="52eb8-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="52eb8-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52eb8-128">-AsJob</span></span>
<span data-ttu-id="52eb8-129">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="52eb8-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52eb8-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="52eb8-130">-BgpAsn</span></span>
<span data-ttu-id="52eb8-131">O ASN BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="52eb8-131">The BGP ASN for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="52eb8-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="52eb8-133">O Endereço de Peering BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="52eb8-133">The BGP Peering Address for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="52eb8-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="52eb8-135">O peso de paração BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="52eb8-135">The BGP Peering weight for this VpnSite.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52eb8-136">-DefaultProfile</span></span>
<span data-ttu-id="52eb8-137">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52eb8-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52eb8-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="52eb8-138">-DeviceModel</span></span>
<span data-ttu-id="52eb8-139">O modelo de dispositivo do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="52eb8-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="52eb8-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="52eb8-140">-DeviceVendor</span></span>
<span data-ttu-id="52eb8-141">O fornecedor de dispositivos do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="52eb8-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="52eb8-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="52eb8-142">-IpAddress</span></span>
<span data-ttu-id="52eb8-143">O IPAddress para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="52eb8-143">The IPAddress for this VpnSite.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="52eb8-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="52eb8-145">O modelo de dispositivo do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="52eb8-145">The device model of the remote vpn device.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-146">-Location</span><span class="sxs-lookup"><span data-stu-id="52eb8-146">-Location</span></span>
<span data-ttu-id="52eb8-147">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="52eb8-147">The resource location.</span></span>

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

### <span data-ttu-id="52eb8-148">-Name</span><span class="sxs-lookup"><span data-stu-id="52eb8-148">-Name</span></span>
<span data-ttu-id="52eb8-149">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="52eb8-149">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="52eb8-150">-O365Policy</span></span>
<span data-ttu-id="52eb8-151">A política de quebra de tráfego do office 365 para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="52eb8-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="52eb8-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52eb8-152">-ResourceGroupName</span></span>
<span data-ttu-id="52eb8-153">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="52eb8-153">The resource name.</span></span>

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

### <span data-ttu-id="52eb8-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="52eb8-154">-Tag</span></span>
<span data-ttu-id="52eb8-155">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="52eb8-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="52eb8-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="52eb8-156">-VirtualWan</span></span>
<span data-ttu-id="52eb8-157">O VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="52eb8-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteIpAddress, ByVirtualWanObjectByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="52eb8-158">-VirtualWanId</span></span>
<span data-ttu-id="52eb8-159">O ResourceId VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="52eb8-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteIpAddress, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="52eb8-160">-VirtualWanName</span></span>
<span data-ttu-id="52eb8-161">O nome do VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="52eb8-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52eb8-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="52eb8-163">O nome do grupo de recursos do VirtualWan ao que o VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="52eb8-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteIpAddress, ByVirtualWanNameByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="52eb8-164">-VpnSiteLink</span></span>
<span data-ttu-id="52eb8-165">A lista de VpnSiteLinks que este VpnSite tem.</span><span class="sxs-lookup"><span data-stu-id="52eb8-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink[]
Parameter Sets: ByVirtualWanNameByVpnSiteLinkObject, ByVirtualWanObjectByVpnSiteLinkObject, ByVirtualWanResourceIdByVpnSiteLinkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52eb8-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52eb8-166">-Confirm</span></span>
<span data-ttu-id="52eb8-167">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52eb8-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52eb8-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52eb8-168">-WhatIf</span></span>
<span data-ttu-id="52eb8-169">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52eb8-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52eb8-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52eb8-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52eb8-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52eb8-171">CommonParameters</span></span>
<span data-ttu-id="52eb8-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52eb8-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52eb8-173">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52eb8-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52eb8-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52eb8-174">INPUTS</span></span>

### <span data-ttu-id="52eb8-175">Nenhum</span><span class="sxs-lookup"><span data-stu-id="52eb8-175">None</span></span>

## <span data-ttu-id="52eb8-176">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52eb8-176">OUTPUTS</span></span>

### <span data-ttu-id="52eb8-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="52eb8-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="52eb8-178">NOTES</span><span class="sxs-lookup"><span data-stu-id="52eb8-178">NOTES</span></span>

## <span data-ttu-id="52eb8-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52eb8-179">RELATED LINKS</span></span>

[<span data-ttu-id="52eb8-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="52eb8-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="52eb8-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="52eb8-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="52eb8-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="52eb8-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
