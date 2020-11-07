---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a0e7775a85196a7a3ba709f284b58e57c46c4cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772686"
---
# <span data-ttu-id="38bfe-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="38bfe-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="38bfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="38bfe-103">Atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="38bfe-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="38bfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38bfe-104">SYNTAX</span></span>

### <span data-ttu-id="38bfe-105">ByVpnConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="38bfe-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bfe-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="38bfe-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bfe-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="38bfe-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38bfe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38bfe-108">DESCRIPTION</span></span>
<span data-ttu-id="38bfe-109">O cmdlet **Update-AzVpnConnection** atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="38bfe-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="38bfe-110">A conexão VPN cria uma conexão IPsec que conecta um gateway VPN a uma ramificação de cliente remoto representada no Azure como um site de VPN.</span><span class="sxs-lookup"><span data-stu-id="38bfe-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="38bfe-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38bfe-111">EXAMPLES</span></span>

### <span data-ttu-id="38bfe-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38bfe-112">Example 1</span></span>

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
```

<span data-ttu-id="38bfe-113">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="38bfe-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="38bfe-114">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="38bfe-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="38bfe-115">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="38bfe-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="38bfe-116">A conexão é atualizada para ter um novo IpSecPolicy usando o comando Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="38bfe-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="38bfe-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="38bfe-117">Example 2</span></span>

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
```

<span data-ttu-id="38bfe-118">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="38bfe-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="38bfe-119">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="38bfe-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="38bfe-120">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="38bfe-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="38bfe-121">A conexão é atualizada para ter uma nova chave compartilhada usando a construção de cadeia de caracteres segura.</span><span class="sxs-lookup"><span data-stu-id="38bfe-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="38bfe-122">OS</span><span class="sxs-lookup"><span data-stu-id="38bfe-122">PARAMETERS</span></span>

### <span data-ttu-id="38bfe-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38bfe-123">-AsJob</span></span>
<span data-ttu-id="38bfe-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="38bfe-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38bfe-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="38bfe-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="38bfe-126">A largura de banda que precisa ser manipulada por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="38bfe-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="38bfe-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bfe-127">-DefaultProfile</span></span>
<span data-ttu-id="38bfe-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38bfe-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bfe-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="38bfe-129">-EnableBgp</span></span>
<span data-ttu-id="38bfe-130">Habilitar o BGP para esta conexão</span><span class="sxs-lookup"><span data-stu-id="38bfe-130">Enable BGP for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38bfe-131">-InputObject</span></span>
<span data-ttu-id="38bfe-132">O objeto VpnConnection a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="38bfe-132">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="38bfe-133">-IpSecPolicy</span></span>
<span data-ttu-id="38bfe-134">A largura de banda que precisa ser manipulada por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="38bfe-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="38bfe-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="38bfe-135">-Name</span></span>
<span data-ttu-id="38bfe-136">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="38bfe-136">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="38bfe-137">-ParentResourceName</span></span>
<span data-ttu-id="38bfe-138">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="38bfe-138">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bfe-139">-ResourceGroupName</span></span>
<span data-ttu-id="38bfe-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38bfe-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38bfe-141">-ResourceId</span></span>
<span data-ttu-id="38bfe-142">A ID do recurso do objeto VpnConnection a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="38bfe-142">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="38bfe-143">-SharedKey</span></span>
<span data-ttu-id="38bfe-144">A chave compartilhada necessária para definir essa conexão.</span><span class="sxs-lookup"><span data-stu-id="38bfe-144">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="38bfe-145">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="38bfe-145">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="38bfe-146">Usar o endereço IP do Azure local como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="38bfe-146">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-147">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="38bfe-147">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="38bfe-148">Use seletores de tráfego baseado em política para esta conexão.</span><span class="sxs-lookup"><span data-stu-id="38bfe-148">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bfe-149">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="38bfe-149">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="38bfe-150">A lista de VpnSiteLinkConnections que esse VpnConnection precisa ter.</span><span class="sxs-lookup"><span data-stu-id="38bfe-150">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="38bfe-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38bfe-151">-Confirm</span></span>
<span data-ttu-id="38bfe-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38bfe-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38bfe-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bfe-153">-WhatIf</span></span>
<span data-ttu-id="38bfe-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38bfe-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bfe-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38bfe-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38bfe-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bfe-156">CommonParameters</span></span>
<span data-ttu-id="38bfe-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bfe-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bfe-158">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38bfe-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bfe-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38bfe-159">INPUTS</span></span>

### <span data-ttu-id="38bfe-160">System. String</span><span class="sxs-lookup"><span data-stu-id="38bfe-160">System.String</span></span>

### <span data-ttu-id="38bfe-161">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="38bfe-161">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="38bfe-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38bfe-162">OUTPUTS</span></span>

### <span data-ttu-id="38bfe-163">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="38bfe-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="38bfe-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38bfe-164">NOTES</span></span>

## <span data-ttu-id="38bfe-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38bfe-165">RELATED LINKS</span></span>

[<span data-ttu-id="38bfe-166">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="38bfe-166">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="38bfe-167">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="38bfe-167">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="38bfe-168">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="38bfe-168">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
