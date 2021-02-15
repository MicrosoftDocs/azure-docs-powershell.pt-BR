---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: ac203d499674e97080edd645f9643b12291873d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114670"
---
# <span data-ttu-id="a7f31-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7f31-101">New-AzVpnSite</span></span>

## <span data-ttu-id="a7f31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7f31-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f31-103">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a7f31-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="a7f31-104">Esta é uma representação rm das ramificações do cliente que são carregadas para a conectividade do Azure para S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="a7f31-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="a7f31-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7f31-105">SYNTAX</span></span>

### <span data-ttu-id="a7f31-106">ByVirtualWanNameByVpnSiteIpAddress (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7f31-106">ByVirtualWanNameByVpnSiteIpAddress (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f31-107">ByVirtualWanNameByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="a7f31-107">ByVirtualWanNameByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f31-108">ByVirtualWanObjectByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7f31-108">ByVirtualWanObjectByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7f31-109">ByVirtualWanObjectByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="a7f31-109">ByVirtualWanObjectByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7f31-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7f31-110">ByVirtualWanResourceIdByVpnSiteIpAddress</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7f31-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span><span class="sxs-lookup"><span data-stu-id="a7f31-111">ByVirtualWanResourceIdByVpnSiteLinkObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>] -VpnSiteLink <PSVpnSiteLink[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7f31-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7f31-112">DESCRIPTION</span></span>
<span data-ttu-id="a7f31-113">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a7f31-113">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="a7f31-114">Esta é uma representação rm das ramificações do cliente que são carregadas para a conectividade do Azure para S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="a7f31-114">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="a7f31-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7f31-115">EXAMPLES</span></span>

### <span data-ttu-id="a7f31-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7f31-116">Example 1</span></span>

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

<span data-ttu-id="a7f31-117">O acima criará um grupo de recursos, Wan Virtual no Leste dos EUA, no grupo de recursos "nonlinkSite" no Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f31-117">The above will create a resource group, Virtual WAN in East US in "nonlinkSite" resource group in Azure.</span></span> 

<span data-ttu-id="a7f31-118">Em seguida, ele cria um VpnSite para representar uma ramificação de cliente e a vincula à WAN Virtual.</span><span class="sxs-lookup"><span data-stu-id="a7f31-118">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="a7f31-119">Uma conexão IPSec pode ser configurada com essa ramificação e uma VpnGateway usando o comando New-AzVpnConnection usuário.</span><span class="sxs-lookup"><span data-stu-id="a7f31-119">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="a7f31-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a7f31-120">Example 2</span></span>
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

<span data-ttu-id="a7f31-121">O exemplo acima criará um grupo de recursos, WAN Virtual e um Site Vpn com 1 VpnSiteLinks no Leste dos EUA em um grupo de recursos "multilink" no Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f31-121">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in East US in "multilink" resource group in Azure.</span></span>

### <span data-ttu-id="a7f31-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a7f31-122">Example 3</span></span>

<span data-ttu-id="a7f31-123">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a7f31-123">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="a7f31-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="a7f31-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnSite -AddressSpace <String[]> -DeviceModel 'SomeDevice' -DeviceVendor 'SomeDeviceVendor' -IpAddress '1.2.3.4' -LinkSpeedInMbps '10' -Location 'East US' -Name 'testVpnSite' -ResourceGroupName 'multilink' -VirtualWanName <String> -VirtualWanResourceGroupName <String>
```

## <span data-ttu-id="a7f31-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7f31-125">PARAMETERS</span></span>

### <span data-ttu-id="a7f31-126">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="a7f31-126">-AddressSpace</span></span>
<span data-ttu-id="a7f31-127">Os prefixos de endereço da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a7f31-127">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="a7f31-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7f31-128">-AsJob</span></span>
<span data-ttu-id="a7f31-129">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a7f31-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7f31-130">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="a7f31-130">-BgpAsn</span></span>
<span data-ttu-id="a7f31-131">O ASN BGP para este Site Vpn.</span><span class="sxs-lookup"><span data-stu-id="a7f31-131">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="a7f31-132">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="a7f31-132">-BgpPeeringAddress</span></span>
<span data-ttu-id="a7f31-133">O endereço de paridade BGP deste VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a7f31-133">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="a7f31-134">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="a7f31-134">-BgpPeeringWeight</span></span>
<span data-ttu-id="a7f31-135">A peso do peering BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a7f31-135">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="a7f31-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f31-136">-DefaultProfile</span></span>
<span data-ttu-id="a7f31-137">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7f31-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f31-138">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="a7f31-138">-DeviceModel</span></span>
<span data-ttu-id="a7f31-139">O modelo de dispositivo do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="a7f31-139">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="a7f31-140">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="a7f31-140">-DeviceVendor</span></span>
<span data-ttu-id="a7f31-141">O fornecedor de dispositivo do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="a7f31-141">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="a7f31-142">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a7f31-142">-IpAddress</span></span>
<span data-ttu-id="a7f31-143">O IPAddress para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a7f31-143">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="a7f31-144">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="a7f31-144">-LinkSpeedInMbps</span></span>
<span data-ttu-id="a7f31-145">O modelo de dispositivo do dispositivo vpn remoto.</span><span class="sxs-lookup"><span data-stu-id="a7f31-145">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="a7f31-146">-Local</span><span class="sxs-lookup"><span data-stu-id="a7f31-146">-Location</span></span>
<span data-ttu-id="a7f31-147">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7f31-147">The resource location.</span></span>

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

### <span data-ttu-id="a7f31-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7f31-148">-Name</span></span>
<span data-ttu-id="a7f31-149">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7f31-149">The resource name.</span></span>

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

### <span data-ttu-id="a7f31-150">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="a7f31-150">-O365Policy</span></span>
<span data-ttu-id="a7f31-151">A política de quebra de tráfego do Office 365 para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a7f31-151">The office 365 traffic breakout policy for this VpnSite.</span></span>

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

### <span data-ttu-id="a7f31-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f31-152">-ResourceGroupName</span></span>
<span data-ttu-id="a7f31-153">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7f31-153">The resource name.</span></span>

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

### <span data-ttu-id="a7f31-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7f31-154">-Tag</span></span>
<span data-ttu-id="a7f31-155">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a7f31-155">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a7f31-156">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="a7f31-156">-VirtualWan</span></span>
<span data-ttu-id="a7f31-157">O VirtualWan ao que este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="a7f31-157">The VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a7f31-158">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="a7f31-158">-VirtualWanId</span></span>
<span data-ttu-id="a7f31-159">O ResourceId VirtualWan a que este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="a7f31-159">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a7f31-160">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="a7f31-160">-VirtualWanName</span></span>
<span data-ttu-id="a7f31-161">O nome do VirtualWan ao que este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="a7f31-161">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a7f31-162">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f31-162">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="a7f31-163">O nome do grupo de recursos do VirtualWan ao que este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="a7f31-163">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

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

### <span data-ttu-id="a7f31-164">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="a7f31-164">-VpnSiteLink</span></span>
<span data-ttu-id="a7f31-165">A lista de VpnSiteLinks que este Site Vpn tem.</span><span class="sxs-lookup"><span data-stu-id="a7f31-165">The list of VpnSiteLinks that this VpnSite have.</span></span>

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

### <span data-ttu-id="a7f31-166">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a7f31-166">-Confirm</span></span>
<span data-ttu-id="a7f31-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7f31-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f31-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f31-168">-WhatIf</span></span>
<span data-ttu-id="a7f31-169">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a7f31-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f31-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7f31-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f31-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f31-171">CommonParameters</span></span>
<span data-ttu-id="a7f31-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f31-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f31-173">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7f31-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f31-174">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7f31-174">INPUTS</span></span>

### <span data-ttu-id="a7f31-175">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a7f31-175">None</span></span>

## <span data-ttu-id="a7f31-176">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7f31-176">OUTPUTS</span></span>

### <span data-ttu-id="a7f31-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7f31-177">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="a7f31-178">Notas</span><span class="sxs-lookup"><span data-stu-id="a7f31-178">NOTES</span></span>

## <span data-ttu-id="a7f31-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7f31-179">RELATED LINKS</span></span>

[<span data-ttu-id="a7f31-180">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7f31-180">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="a7f31-181">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7f31-181">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="a7f31-182">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a7f31-182">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
