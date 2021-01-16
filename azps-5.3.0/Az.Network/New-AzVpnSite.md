---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271710"
---
# <span data-ttu-id="e2833-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e2833-101">New-AzVpnSite</span></span>

## <span data-ttu-id="e2833-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2833-102">SYNOPSIS</span></span>
<span data-ttu-id="e2833-103">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="e2833-104">Trata-se de uma representação RM de ramificações de cliente que são carregadas para o Azure para a conectividade S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="e2833-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="e2833-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2833-105">SYNTAX</span></span>

### <span data-ttu-id="e2833-106">ByVirtualWanNameByVpnSiteIpAddress (padrão)</span><span class="sxs-lookup"><span data-stu-id="e2833-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2833-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="e2833-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2833-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2833-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2833-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="e2833-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2833-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2833-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2833-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="e2833-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2833-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2833-112">DESCRIPTION</span></span>
<span data-ttu-id="e2833-113">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="e2833-114">Trata-se de uma representação RM de ramificações de cliente que são carregadas para o Azure para a conectividade S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="e2833-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="e2833-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2833-115">EXAMPLES</span></span>

### <span data-ttu-id="e2833-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2833-116">Example 1</span></span>

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

<span data-ttu-id="e2833-117">A seguir, você criará um grupo de recursos, a WAN virtual no leste dos EUA no grupo de recursos "nonlinkSite" do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2833-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="e2833-118">Em seguida, ele cria um VpnSite para representar uma ramificação do cliente e a vincula à rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="e2833-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="e2833-119">Uma conexão IPSec pode ser configurada com essa ramificação e uma VpnGateway usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="e2833-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="e2833-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e2833-120">Example 2</span></span>
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

<span data-ttu-id="e2833-121">A seguir, você criará um grupo de recursos, uma rede de longa distância virtual e uma VpnSite com 1 VpnSiteLinks no leste dos EUA no grupo de recursos "conexões múltiplas" do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2833-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="e2833-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e2833-122">Example 3</span></span>

<span data-ttu-id="e2833-123">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="e2833-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e2833-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="e2833-125">OS</span><span class="sxs-lookup"><span data-stu-id="e2833-125">PARAMETERS</span></span>

### <span data-ttu-id="e2833-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="e2833-126">-AddressSpace</span></span>
<span data-ttu-id="e2833-127">Os prefixos de endereço da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e2833-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="e2833-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2833-128">-AsJob</span></span>
<span data-ttu-id="e2833-129">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e2833-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2833-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="e2833-130">-BgpAsn</span></span>
<span data-ttu-id="e2833-131">A ASN do BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="e2833-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e2833-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="e2833-133">O endereço de emparelhamento BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="e2833-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="e2833-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="e2833-135">O peso de emparelhamento BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="e2833-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2833-136">-DefaultProfile</span></span>
<span data-ttu-id="e2833-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2833-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2833-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="e2833-138">-DeviceModel</span></span>
<span data-ttu-id="e2833-139">O modelo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="e2833-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="e2833-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="e2833-140">-DeviceVendor</span></span>
<span data-ttu-id="e2833-141">O fornecedor do dispositivo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="e2833-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="e2833-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e2833-142">-IpAddress</span></span>
<span data-ttu-id="e2833-143">O IPAddress para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="e2833-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="e2833-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="e2833-145">O modelo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="e2833-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="e2833-146">-Local</span><span class="sxs-lookup"><span data-stu-id="e2833-146">-Location</span></span>
<span data-ttu-id="e2833-147">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2833-147">The resource location.</span></span>

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

### <span data-ttu-id="e2833-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2833-148">-Name</span></span>
<span data-ttu-id="e2833-149">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2833-149">The resource name.</span></span>

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

### <span data-ttu-id="e2833-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="e2833-150">-O365Policy</span></span>
<span data-ttu-id="e2833-151">A política de debates de tráfego do Office 365 para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="e2833-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="e2833-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2833-152">-ResourceGroupName</span></span>
<span data-ttu-id="e2833-153">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e2833-153">The resource name.</span></span>

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

### <span data-ttu-id="e2833-154">-Marca</span><span class="sxs-lookup"><span data-stu-id="e2833-154">-Tag</span></span>
<span data-ttu-id="e2833-155">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2833-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e2833-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="e2833-156">-VirtualWan</span></span>
<span data-ttu-id="e2833-157">O VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="e2833-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="e2833-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="e2833-158">-VirtualWanId</span></span>
<span data-ttu-id="e2833-159">O ResourceId VirtualWan que este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="e2833-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="e2833-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="e2833-160">-VirtualWanName</span></span>
<span data-ttu-id="e2833-161">O nome do VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="e2833-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="e2833-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2833-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="e2833-163">O nome do grupo de recursos do VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="e2833-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="e2833-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e2833-164">-VpnSiteLink</span></span>
<span data-ttu-id="e2833-165">A lista de VpnSiteLinks que esta VpnSite tem.</span><span class="sxs-lookup"><span data-stu-id="e2833-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="e2833-166">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2833-166">-Confirm</span></span>
<span data-ttu-id="e2833-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2833-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2833-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2833-168">-WhatIf</span></span>
<span data-ttu-id="e2833-169">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2833-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2833-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2833-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2833-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2833-171">CommonParameters</span></span>
<span data-ttu-id="e2833-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2833-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2833-173">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2833-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2833-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2833-174">INPUTS</span></span>

### <span data-ttu-id="e2833-175">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e2833-175">None</span></span>

## <span data-ttu-id="e2833-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2833-176">OUTPUTS</span></span>

### <span data-ttu-id="e2833-177">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="e2833-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="e2833-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2833-178">NOTES</span></span>

## <span data-ttu-id="e2833-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2833-179">RELATED LINKS</span></span>

[<span data-ttu-id="e2833-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e2833-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="e2833-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e2833-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="e2833-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="e2833-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
