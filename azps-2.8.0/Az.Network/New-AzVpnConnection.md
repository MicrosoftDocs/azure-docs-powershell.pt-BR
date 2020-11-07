---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: e2506ceb8b2304b403a94c8730e262c7320ac1c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772329"
---
# <span data-ttu-id="4fedb-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fedb-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="4fedb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fedb-102">SYNOPSIS</span></span>
<span data-ttu-id="4fedb-103">Cria uma conexão IPSec que conecta um VpnGateway a uma ramificação de cliente remoto representada no RM como um VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4fedb-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="4fedb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fedb-104">SYNTAX</span></span>

### <span data-ttu-id="4fedb-105">ByVpnGatewayNameByVpnSiteObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fedb-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fedb-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="4fedb-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fedb-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="4fedb-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fedb-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="4fedb-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fedb-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="4fedb-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fedb-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="4fedb-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fedb-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fedb-111">DESCRIPTION</span></span>
<span data-ttu-id="4fedb-112">Cria uma conexão IPSec que conecta um VpnGateway a uma ramificação de cliente remoto representada no RM como um VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4fedb-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="4fedb-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fedb-113">EXAMPLES</span></span>

### <span data-ttu-id="4fedb-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4fedb-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="4fedb-115">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fedb-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="4fedb-116">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="4fedb-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="4fedb-117">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="4fedb-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="4fedb-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4fedb-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="4fedb-119">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite com 1 VpnSiteLinks nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="4fedb-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="4fedb-120">Um gateway VPN será criado posteriormente no Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="4fedb-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="4fedb-121">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection com 1 VpnSiteLinkConnections para o VpnSiteLink do VpnSite.</span><span class="sxs-lookup"><span data-stu-id="4fedb-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="4fedb-122">OS</span><span class="sxs-lookup"><span data-stu-id="4fedb-122">PARAMETERS</span></span>

### <span data-ttu-id="4fedb-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fedb-123">-AsJob</span></span>
<span data-ttu-id="4fedb-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4fedb-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fedb-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="4fedb-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="4fedb-126">A largura de banda que precisa ser manipulada por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="4fedb-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="4fedb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fedb-127">-DefaultProfile</span></span>
<span data-ttu-id="4fedb-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fedb-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fedb-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="4fedb-129">-EnableBgp</span></span>
<span data-ttu-id="4fedb-130">Habilitar o BGP para esta conexão</span><span class="sxs-lookup"><span data-stu-id="4fedb-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="4fedb-131">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="4fedb-131">-IpSecPolicy</span></span>
<span data-ttu-id="4fedb-132">A largura de banda que precisa ser manipulada por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="4fedb-132">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fedb-133">-Name</span></span>
<span data-ttu-id="4fedb-134">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4fedb-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4fedb-135">-ParentObject</span></span>
<span data-ttu-id="4fedb-136">O VpnGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="4fedb-136">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4fedb-137">-ParentResourceId</span></span>
<span data-ttu-id="4fedb-138">A ID do recurso do VpnGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="4fedb-138">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4fedb-139">-ParentResourceName</span></span>
<span data-ttu-id="4fedb-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fedb-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fedb-141">-ResourceGroupName</span></span>
<span data-ttu-id="4fedb-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4fedb-142">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="4fedb-143">-SharedKey</span></span>
<span data-ttu-id="4fedb-144">A chave compartilhada necessária para definir essa conexão.</span><span class="sxs-lookup"><span data-stu-id="4fedb-144">The shared key required to set this connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-145">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="4fedb-145">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="4fedb-146">Usar o endereço IP do Azure local como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4fedb-146">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="4fedb-147">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="4fedb-147">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="4fedb-148">Use seletores de tráfego baseado em política para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="4fedb-148">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="4fedb-149">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="4fedb-149">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="4fedb-150">Protocolo de conexão de gateway: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="4fedb-150">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-151">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4fedb-151">-VpnSite</span></span>
<span data-ttu-id="4fedb-152">O site VPN remoto ao qual essa conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="4fedb-152">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-153">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="4fedb-153">-VpnSiteId</span></span>
<span data-ttu-id="4fedb-154">O site VPN remoto ao qual essa conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="4fedb-154">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-155">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4fedb-155">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="4fedb-156">A lista de VpnSiteLinkConnections que esta VpnConnection tem.</span><span class="sxs-lookup"><span data-stu-id="4fedb-156">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fedb-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4fedb-157">-Confirm</span></span>
<span data-ttu-id="4fedb-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fedb-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fedb-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fedb-159">-WhatIf</span></span>
<span data-ttu-id="4fedb-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4fedb-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fedb-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fedb-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fedb-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fedb-162">CommonParameters</span></span>
<span data-ttu-id="4fedb-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fedb-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fedb-164">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fedb-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fedb-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fedb-165">INPUTS</span></span>

### <span data-ttu-id="4fedb-166">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4fedb-166">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="4fedb-167">System. String</span><span class="sxs-lookup"><span data-stu-id="4fedb-167">System.String</span></span>

## <span data-ttu-id="4fedb-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fedb-168">OUTPUTS</span></span>

### <span data-ttu-id="4fedb-169">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fedb-169">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="4fedb-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fedb-170">NOTES</span></span>

## <span data-ttu-id="4fedb-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fedb-171">RELATED LINKS</span></span>

[<span data-ttu-id="4fedb-172">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fedb-172">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="4fedb-173">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fedb-173">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="4fedb-174">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="4fedb-174">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)