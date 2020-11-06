---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSite.md
ms.openlocfilehash: 980b84fd1b23cb7e4b034dee485b785b96893f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600237"
---
# <span data-ttu-id="4b5d4-101">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4b5d4-101">New-AzVpnSite</span></span>

## <span data-ttu-id="4b5d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5d4-103">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-103">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="4b5d4-104">Trata-se de uma representação RM de ramificações de cliente que são carregadas para o Azure para a conectividade S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="4b5d4-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b5d4-105">SYNTAX</span></span>

### <span data-ttu-id="4b5d4-106">ByVirtualWanName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b5d4-106">ByVirtualWanName (Default)</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String>
 -VirtualWanResourceGroupName <String> -VirtualWanName <String> -IpAddress <String> [-AddressSpace <String[]>]
 [-DeviceModel <String>] [-DeviceVendor <String>] [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>]
 [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b5d4-107">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="4b5d4-107">ByVirtualWanObject</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWan <PSVirtualWan>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b5d4-108">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="4b5d4-108">ByVirtualWanResourceId</span></span>
```
New-AzVpnSite -ResourceGroupName <String> -Name <String> -Location <String> -VirtualWanId <String>
 -IpAddress <String> [-AddressSpace <String[]>] [-DeviceModel <String>] [-DeviceVendor <String>]
 [-LinkSpeedInMbps <UInt32>] [-BgpAsn <UInt32>] [-BgpPeeringAddress <String>] [-BgpPeeringWeight <UInt32>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b5d4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b5d4-109">DESCRIPTION</span></span>
<span data-ttu-id="4b5d4-110">Cria um novo recurso do Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-110">Creates a new Azure VpnSite resource.</span></span> <span data-ttu-id="4b5d4-111">Trata-se de uma representação RM de ramificações de cliente que são carregadas para o Azure para a conectividade S2S com um hub virtual Cortex.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-111">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="4b5d4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b5d4-112">EXAMPLES</span></span>

### <span data-ttu-id="4b5d4-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b5d4-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="4b5d4-114">A seguir, você criará um grupo de recursos, uma WAN virtual no oeste do grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-114">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="4b5d4-115">Em seguida, ele cria um VpnSite para representar uma ramificação do cliente e a vincula à rede de longa distância virtual.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-115">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="4b5d4-116">Uma conexão IPSec pode ser configurada com essa ramificação e uma VpnGateway usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-116">An IPSec connection can then be setup with this branch and a VpnGateway using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="4b5d4-117">OS</span><span class="sxs-lookup"><span data-stu-id="4b5d4-117">PARAMETERS</span></span>

### <span data-ttu-id="4b5d4-118">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="4b5d4-118">-AddressSpace</span></span>
<span data-ttu-id="4b5d4-119">Os prefixos de endereço da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-119">The address prefixes of the virtual network.</span></span>

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

### <span data-ttu-id="4b5d4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b5d4-120">-AsJob</span></span>
<span data-ttu-id="4b5d4-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4b5d4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b5d4-122">-BgpAsn</span><span class="sxs-lookup"><span data-stu-id="4b5d4-122">-BgpAsn</span></span>
<span data-ttu-id="4b5d4-123">A ASN do BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-123">The BGP ASN for this VpnSite.</span></span>

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

### <span data-ttu-id="4b5d4-124">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="4b5d4-124">-BgpPeeringAddress</span></span>
<span data-ttu-id="4b5d4-125">O endereço de emparelhamento BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-125">The BGP Peering Address for this VpnSite.</span></span>

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

### <span data-ttu-id="4b5d4-126">-BgpPeeringWeight</span><span class="sxs-lookup"><span data-stu-id="4b5d4-126">-BgpPeeringWeight</span></span>
<span data-ttu-id="4b5d4-127">O peso de emparelhamento BGP para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-127">The BGP Peering weight for this VpnSite.</span></span>

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

### <span data-ttu-id="4b5d4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5d4-128">-DefaultProfile</span></span>
<span data-ttu-id="4b5d4-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b5d4-130">-DeviceModel</span><span class="sxs-lookup"><span data-stu-id="4b5d4-130">-DeviceModel</span></span>
<span data-ttu-id="4b5d4-131">O modelo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-131">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="4b5d4-132">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="4b5d4-132">-DeviceVendor</span></span>
<span data-ttu-id="4b5d4-133">O fornecedor do dispositivo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-133">The device vendor of the remote vpn device.</span></span>

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

### <span data-ttu-id="4b5d4-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4b5d4-134">-IpAddress</span></span>
<span data-ttu-id="4b5d4-135">O IPAddress para este VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-135">The IPAddress for this VpnSite.</span></span>

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

### <span data-ttu-id="4b5d4-136">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="4b5d4-136">-LinkSpeedInMbps</span></span>
<span data-ttu-id="4b5d4-137">O modelo do dispositivo VPN remoto.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-137">The device model of the remote vpn device.</span></span>

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

### <span data-ttu-id="4b5d4-138">-Local</span><span class="sxs-lookup"><span data-stu-id="4b5d4-138">-Location</span></span>
<span data-ttu-id="4b5d4-139">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-139">The resource location.</span></span>

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

### <span data-ttu-id="4b5d4-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b5d4-140">-Name</span></span>
<span data-ttu-id="4b5d4-141">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-141">The resource name.</span></span>

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

### <span data-ttu-id="4b5d4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5d4-142">-ResourceGroupName</span></span>
<span data-ttu-id="4b5d4-143">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-143">The resource name.</span></span>

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

### <span data-ttu-id="4b5d4-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="4b5d4-144">-Tag</span></span>
<span data-ttu-id="4b5d4-145">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4b5d4-146">-VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4b5d4-146">-VirtualWan</span></span>
<span data-ttu-id="4b5d4-147">O VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-147">The VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-148">-VirtualWanId</span><span class="sxs-lookup"><span data-stu-id="4b5d4-148">-VirtualWanId</span></span>
<span data-ttu-id="4b5d4-149">O ResourceId VirtualWan que este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-149">The ResourceId VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-150">-VirtualWanName</span><span class="sxs-lookup"><span data-stu-id="4b5d4-150">-VirtualWanName</span></span>
<span data-ttu-id="4b5d4-151">O nome do VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-151">The name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-152">-VirtualWanResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5d4-152">-VirtualWanResourceGroupName</span></span>
<span data-ttu-id="4b5d4-153">O nome do grupo de recursos do VirtualWan para o qual este VpnSite precisa estar conectado.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-153">The resource group name of the VirtualWan this VpnSite needs to be connected to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b5d4-154">-Confirm</span></span>
<span data-ttu-id="4b5d4-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b5d4-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b5d4-156">-WhatIf</span></span>
<span data-ttu-id="4b5d4-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b5d4-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b5d4-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5d4-159">CommonParameters</span></span>
<span data-ttu-id="4b5d4-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5d4-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5d4-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5d4-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b5d4-162">INPUTS</span></span>

### <span data-ttu-id="4b5d4-163">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4b5d4-163">None</span></span>

## <span data-ttu-id="4b5d4-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b5d4-164">OUTPUTS</span></span>

### <span data-ttu-id="4b5d4-165">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="4b5d4-165">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="4b5d4-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b5d4-166">NOTES</span></span>

## <span data-ttu-id="4b5d4-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b5d4-167">RELATED LINKS</span></span>

[<span data-ttu-id="4b5d4-168">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4b5d4-168">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="4b5d4-169">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4b5d4-169">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="4b5d4-170">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="4b5d4-170">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
