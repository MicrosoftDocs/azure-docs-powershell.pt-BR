---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113419"
---
# <span data-ttu-id="778c4-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778c4-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="778c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="778c4-102">SYNOPSIS</span></span>
<span data-ttu-id="778c4-103">Atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="778c4-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="778c4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="778c4-104">SYNTAX</span></span>

### <span data-ttu-id="778c4-105">ByVpnConnectionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="778c4-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="778c4-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="778c4-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="778c4-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="778c4-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="778c4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="778c4-108">DESCRIPTION</span></span>
<span data-ttu-id="778c4-109">O cmdlet **Update-AzVpnConnection** atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="778c4-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="778c4-110">A conexão VPN cria uma conexão IPsec que conecta um gateway VPN a uma ramificação de cliente remota representada no Azure como um site VPN.</span><span class="sxs-lookup"><span data-stu-id="778c4-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="778c4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="778c4-111">EXAMPLES</span></span>

### <span data-ttu-id="778c4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="778c4-112">Example 1</span></span>

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

<span data-ttu-id="778c4-113">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um VpnSite no oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="778c4-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="778c4-114">Um gateway VPN será criado posteriormente no Hub Virtual com 2 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="778c4-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="778c4-115">Depois que o gateway for criado, ele será conectado ao VpnSite usando o comando New-AzVpnConnection usuário.</span><span class="sxs-lookup"><span data-stu-id="778c4-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="778c4-116">A conexão é atualizada para ter um novo IpSecPolicy usando o comando Set-AzVpnConnection usuário.</span><span class="sxs-lookup"><span data-stu-id="778c4-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="778c4-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="778c4-117">Example 2</span></span>

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

<span data-ttu-id="778c4-118">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um VpnSite no oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="778c4-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="778c4-119">Um gateway VPN será criado posteriormente no Hub Virtual com 2 unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="778c4-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="778c4-120">Depois que o gateway for criado, ele será conectado ao VpnSite usando o comando New-AzVpnConnection usuário.</span><span class="sxs-lookup"><span data-stu-id="778c4-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="778c4-121">A conexão é atualizada para ter uma nova chave compartilhada usando a construção de cadeia de caracteres segura.</span><span class="sxs-lookup"><span data-stu-id="778c4-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="778c4-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="778c4-122">PARAMETERS</span></span>

### <span data-ttu-id="778c4-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="778c4-123">-AsJob</span></span>
<span data-ttu-id="778c4-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="778c4-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="778c4-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="778c4-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="778c4-126">A largura de banda que precisa ser tratada por essa conexão em mbps.</span><span class="sxs-lookup"><span data-stu-id="778c4-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="778c4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778c4-127">-DefaultProfile</span></span>
<span data-ttu-id="778c4-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="778c4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="778c4-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="778c4-129">-EnableBgp</span></span>
<span data-ttu-id="778c4-130">Habilitar BGP para esta conexão</span><span class="sxs-lookup"><span data-stu-id="778c4-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="778c4-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="778c4-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="778c4-132">Habilitar a segurança da Internet para esta conexão</span><span class="sxs-lookup"><span data-stu-id="778c4-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="778c4-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="778c4-133">-InputObject</span></span>
<span data-ttu-id="778c4-134">O objeto VpnConnection a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="778c4-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="778c4-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="778c4-135">-IpSecPolicy</span></span>
<span data-ttu-id="778c4-136">A largura de banda que precisa ser tratada por essa conexão em mbps.</span><span class="sxs-lookup"><span data-stu-id="778c4-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="778c4-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="778c4-137">-Name</span></span>
<span data-ttu-id="778c4-138">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="778c4-138">The resource name.</span></span>

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

### <span data-ttu-id="778c4-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="778c4-139">-ParentResourceName</span></span>
<span data-ttu-id="778c4-140">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="778c4-140">The parent resource name.</span></span>

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

### <span data-ttu-id="778c4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778c4-141">-ResourceGroupName</span></span>
<span data-ttu-id="778c4-142">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="778c4-142">The resource group name.</span></span>

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

### <span data-ttu-id="778c4-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="778c4-143">-ResourceId</span></span>
<span data-ttu-id="778c4-144">A ID do recurso do objeto VpnConnection a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="778c4-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="778c4-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="778c4-145">-RoutingConfiguration</span></span>
<span data-ttu-id="778c4-146">Configuração de roteamento para esta conexão</span><span class="sxs-lookup"><span data-stu-id="778c4-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="778c4-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="778c4-147">-SharedKey</span></span>
<span data-ttu-id="778c4-148">A chave compartilhada necessária para configurar essa conexão.</span><span class="sxs-lookup"><span data-stu-id="778c4-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="778c4-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="778c4-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="778c4-150">Use o endereço ip local do azure como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="778c4-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="778c4-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="778c4-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="778c4-152">Use seletores de tráfego baseados em política para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="778c4-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="778c4-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="778c4-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="778c4-154">A lista de VpnSiteLinkConnections que esta VpnConnection precisa ter.</span><span class="sxs-lookup"><span data-stu-id="778c4-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="778c4-155">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="778c4-155">-Confirm</span></span>
<span data-ttu-id="778c4-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="778c4-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="778c4-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778c4-157">-WhatIf</span></span>
<span data-ttu-id="778c4-158">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="778c4-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="778c4-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="778c4-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="778c4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778c4-160">CommonParameters</span></span>
<span data-ttu-id="778c4-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="778c4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778c4-162">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="778c4-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778c4-163">Entradas</span><span class="sxs-lookup"><span data-stu-id="778c4-163">INPUTS</span></span>

### <span data-ttu-id="778c4-164">System.String</span><span class="sxs-lookup"><span data-stu-id="778c4-164">System.String</span></span>

### <span data-ttu-id="778c4-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778c4-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="778c4-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="778c4-166">OUTPUTS</span></span>

### <span data-ttu-id="778c4-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778c4-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="778c4-168">Notas</span><span class="sxs-lookup"><span data-stu-id="778c4-168">NOTES</span></span>

## <span data-ttu-id="778c4-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="778c4-169">RELATED LINKS</span></span>

[<span data-ttu-id="778c4-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778c4-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="778c4-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778c4-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="778c4-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="778c4-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="778c4-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="778c4-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
