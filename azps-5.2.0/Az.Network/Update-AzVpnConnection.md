---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261161"
---
# <span data-ttu-id="d6042-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6042-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="d6042-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6042-102">SYNOPSIS</span></span>
<span data-ttu-id="d6042-103">Atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="d6042-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="d6042-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6042-104">SYNTAX</span></span>

### <span data-ttu-id="d6042-105">ByVpnConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6042-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6042-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="d6042-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6042-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="d6042-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6042-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6042-108">DESCRIPTION</span></span>
<span data-ttu-id="d6042-109">O cmdlet **Update-AzVpnConnection** atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="d6042-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="d6042-110">A conexão VPN cria uma conexão IPsec que conecta um gateway VPN a uma ramificação de cliente remoto representada no Azure como um site de VPN.</span><span class="sxs-lookup"><span data-stu-id="d6042-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="d6042-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6042-111">EXAMPLES</span></span>

### <span data-ttu-id="d6042-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6042-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="d6042-113">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6042-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d6042-114">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="d6042-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d6042-115">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="d6042-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="d6042-116">A conexão é atualizada para ter um novo IpSecPolicy usando o comando Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="d6042-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="d6042-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d6042-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="d6042-118">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6042-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d6042-119">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="d6042-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="d6042-120">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="d6042-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="d6042-121">A conexão é atualizada para ter uma nova chave compartilhada usando a construção de cadeia de caracteres segura.</span><span class="sxs-lookup"><span data-stu-id="d6042-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="d6042-122">OS</span><span class="sxs-lookup"><span data-stu-id="d6042-122">PARAMETERS</span></span>

### <span data-ttu-id="d6042-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6042-123">-AsJob</span></span>
<span data-ttu-id="d6042-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d6042-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6042-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="d6042-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="d6042-126">A largura de banda que precisa ser manipulada por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="d6042-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="d6042-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6042-127">-DefaultProfile</span></span>
<span data-ttu-id="d6042-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6042-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6042-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d6042-129">-EnableBgp</span></span>
<span data-ttu-id="d6042-130">Habilitar o BGP para esta conexão</span><span class="sxs-lookup"><span data-stu-id="d6042-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d6042-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="d6042-132">Habilitar a segurança da Internet para esta conexão</span><span class="sxs-lookup"><span data-stu-id="d6042-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6042-133">-InputObject</span></span>
<span data-ttu-id="d6042-134">O objeto VpnConnection a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d6042-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="d6042-135">-IpSecPolicy</span></span>
<span data-ttu-id="d6042-136">A largura de banda que precisa ser manipulada por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="d6042-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="d6042-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6042-137">-Name</span></span>
<span data-ttu-id="d6042-138">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d6042-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d6042-139">-ParentResourceName</span></span>
<span data-ttu-id="d6042-140">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="d6042-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6042-141">-ResourceGroupName</span></span>
<span data-ttu-id="d6042-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6042-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6042-143">-ResourceId</span></span>
<span data-ttu-id="d6042-144">A ID do recurso do objeto VpnConnection a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d6042-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6042-145">-RoutingConfiguration</span></span>
<span data-ttu-id="d6042-146">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="d6042-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="d6042-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d6042-147">-SharedKey</span></span>
<span data-ttu-id="d6042-148">A chave compartilhada necessária para definir essa conexão.</span><span class="sxs-lookup"><span data-stu-id="d6042-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="d6042-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6042-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="d6042-150">Usar o endereço IP do Azure local como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="d6042-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d6042-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="d6042-152">Use seletores de tráfego baseado em política para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="d6042-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6042-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d6042-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="d6042-154">A lista de VpnSiteLinkConnections que esse VpnConnection precisa ter.</span><span class="sxs-lookup"><span data-stu-id="d6042-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="d6042-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6042-155">-Confirm</span></span>
<span data-ttu-id="d6042-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6042-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6042-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6042-157">-WhatIf</span></span>
<span data-ttu-id="d6042-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6042-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6042-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6042-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6042-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6042-160">CommonParameters</span></span>
<span data-ttu-id="d6042-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6042-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6042-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6042-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6042-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6042-163">INPUTS</span></span>

### <span data-ttu-id="d6042-164">System. String</span><span class="sxs-lookup"><span data-stu-id="d6042-164">System.String</span></span>

### <span data-ttu-id="d6042-165">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6042-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="d6042-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6042-166">OUTPUTS</span></span>

### <span data-ttu-id="d6042-167">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6042-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="d6042-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6042-168">NOTES</span></span>

## <span data-ttu-id="d6042-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6042-169">RELATED LINKS</span></span>

[<span data-ttu-id="d6042-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6042-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="d6042-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6042-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="d6042-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6042-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="d6042-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6042-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
