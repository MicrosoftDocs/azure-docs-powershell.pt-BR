---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 92eab91d06a8624c00973bb35cc1a56dfd096a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889436"
---
# <span data-ttu-id="a1258-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a1258-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="a1258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1258-102">SYNOPSIS</span></span>
<span data-ttu-id="a1258-103">Cria uma conexão IPSec que conecta uma VpnGateway a uma filial de cliente remota representada no RM como um VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a1258-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="a1258-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a1258-104">SYNTAX</span></span>

### <span data-ttu-id="a1258-105">ByVpnGatewayNameByVpnSiteObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a1258-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1258-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="a1258-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1258-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="a1258-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1258-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="a1258-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1258-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="a1258-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1258-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="a1258-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1258-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a1258-111">DESCRIPTION</span></span>
<span data-ttu-id="a1258-112">Cria uma conexão IPSec que conecta uma VpnGateway a uma filial de cliente remota representada no RM como um VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a1258-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="a1258-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1258-113">EXAMPLES</span></span>

### <span data-ttu-id="a1258-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1258-114">Example 1</span></span>

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
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="a1258-115">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um VpnSite no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="a1258-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a1258-116">Um gateway VPN será criado posteriormente no Hub Virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="a1258-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a1258-117">Depois que o gateway for criado, ele será conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="a1258-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="a1258-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a1258-118">Example 2</span></span>
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

<span data-ttu-id="a1258-119">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um VpnSite com 1 VpnSiteLinks no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="a1258-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="a1258-120">Um gateway VPN será criado posteriormente no Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="a1258-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="a1258-121">Depois que o gateway for criado, ele será conectado ao VpnSite usando o comando New-AzVpnConnection com 1 VpnSiteLinkConnections para o VpnSiteLink do VpnSite.</span><span class="sxs-lookup"><span data-stu-id="a1258-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="a1258-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a1258-122">PARAMETERS</span></span>

### <span data-ttu-id="a1258-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1258-123">-AsJob</span></span>
<span data-ttu-id="a1258-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a1258-124">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="a1258-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="a1258-126">A largura de banda que precisa ser manipulada por essa conexão em mbps.</span><span class="sxs-lookup"><span data-stu-id="a1258-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1258-127">-DefaultProfile</span></span>
<span data-ttu-id="a1258-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1258-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a1258-129">-EnableBgp</span></span>
<span data-ttu-id="a1258-130">Habilitar BGP para essa conexão</span><span class="sxs-lookup"><span data-stu-id="a1258-130">Enable BGP for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a1258-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="a1258-132">Habilitar a segurança da Internet para essa conexão</span><span class="sxs-lookup"><span data-stu-id="a1258-132">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="a1258-133">-IpSecPolicy</span></span>
<span data-ttu-id="a1258-134">A largura de banda que precisa ser manipulada por essa conexão em mbps.</span><span class="sxs-lookup"><span data-stu-id="a1258-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-135">-Name</span><span class="sxs-lookup"><span data-stu-id="a1258-135">-Name</span></span>
<span data-ttu-id="a1258-136">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a1258-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a1258-137">-ParentObject</span></span>
<span data-ttu-id="a1258-138">O VpnGateway pai para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="a1258-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a1258-139">-ParentResourceId</span></span>
<span data-ttu-id="a1258-140">A id de recurso do VpnGateway pai para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="a1258-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a1258-141">-ParentResourceName</span></span>
<span data-ttu-id="a1258-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1258-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1258-143">-ResourceGroupName</span></span>
<span data-ttu-id="a1258-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1258-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1258-145">-RoutingConfiguration</span></span>
<span data-ttu-id="a1258-146">Configuração de roteamento para essa conexão</span><span class="sxs-lookup"><span data-stu-id="a1258-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="a1258-147">-SharedKey</span></span>
<span data-ttu-id="a1258-148">A chave compartilhada necessária para configurar essa conexão.</span><span class="sxs-lookup"><span data-stu-id="a1258-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1258-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="a1258-150">Use o endereço ip local do azure como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="a1258-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="a1258-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="a1258-152">Use seletores de tráfego baseados em política para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="a1258-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="a1258-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="a1258-154">Protocolo de conexão de gateway:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="a1258-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="a1258-155">-VpnSite</span></span>
<span data-ttu-id="a1258-156">O site vpn remoto ao qual essa conexão de rede virtual do hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="a1258-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="a1258-157">-VpnSiteId</span></span>
<span data-ttu-id="a1258-158">O site vpn remoto ao qual essa conexão de rede virtual do hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="a1258-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="a1258-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="a1258-160">A lista de VpnSiteLinkConnections que essa VpnConnection tem.</span><span class="sxs-lookup"><span data-stu-id="a1258-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1258-161">-Confirm</span></span>
<span data-ttu-id="a1258-162">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1258-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1258-163">-WhatIf</span></span>
<span data-ttu-id="a1258-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1258-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1258-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1258-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1258-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1258-166">CommonParameters</span></span>
<span data-ttu-id="a1258-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1258-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1258-168">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1258-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1258-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1258-169">INPUTS</span></span>

### <span data-ttu-id="a1258-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a1258-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="a1258-171">System.String</span><span class="sxs-lookup"><span data-stu-id="a1258-171">System.String</span></span>

## <span data-ttu-id="a1258-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a1258-172">OUTPUTS</span></span>

### <span data-ttu-id="a1258-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a1258-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="a1258-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="a1258-174">NOTES</span></span>

## <span data-ttu-id="a1258-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1258-175">RELATED LINKS</span></span>

[<span data-ttu-id="a1258-176">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a1258-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="a1258-177">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a1258-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="a1258-178">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a1258-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="a1258-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1258-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
