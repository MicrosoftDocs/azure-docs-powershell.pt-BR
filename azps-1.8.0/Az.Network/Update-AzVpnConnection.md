---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 5161dfcb843310ad372739438e63adb6c81f1935
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599922"
---
# <span data-ttu-id="39c0b-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="39c0b-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="39c0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="39c0b-103">Atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="39c0b-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="39c0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39c0b-104">SYNTAX</span></span>

### <span data-ttu-id="39c0b-105">ByVpnConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="39c0b-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39c0b-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="39c0b-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c0b-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="39c0b-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c0b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39c0b-108">DESCRIPTION</span></span>
<span data-ttu-id="39c0b-109">O cmdlet **Update-AzVpnConnection** atualiza uma conexão VPN.</span><span class="sxs-lookup"><span data-stu-id="39c0b-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="39c0b-110">A conexão VPN cria uma conexão IPsec que conecta um gateway VPN a uma ramificação de cliente remoto representada no Azure como um site de VPN.</span><span class="sxs-lookup"><span data-stu-id="39c0b-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="39c0b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39c0b-111">EXAMPLES</span></span>

### <span data-ttu-id="39c0b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39c0b-112">Example 1</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="39c0b-113">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="39c0b-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="39c0b-114">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="39c0b-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="39c0b-115">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="39c0b-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="39c0b-116">A conexão é atualizada para ter um novo IpSecPolicy usando o comando Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="39c0b-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="39c0b-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="39c0b-117">Example 2</span></span>

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
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="39c0b-118">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="39c0b-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="39c0b-119">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="39c0b-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="39c0b-120">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="39c0b-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="39c0b-121">A conexão é atualizada para ter uma nova chave compartilhada usando a construção de cadeia de caracteres segura.</span><span class="sxs-lookup"><span data-stu-id="39c0b-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="39c0b-122">OS</span><span class="sxs-lookup"><span data-stu-id="39c0b-122">PARAMETERS</span></span>

### <span data-ttu-id="39c0b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39c0b-123">-AsJob</span></span>
<span data-ttu-id="39c0b-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="39c0b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39c0b-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="39c0b-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="39c0b-126">O banda que precisa ser manipulado por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="39c0b-126">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="39c0b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c0b-127">-DefaultProfile</span></span>
<span data-ttu-id="39c0b-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39c0b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c0b-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="39c0b-129">-EnableBgp</span></span>
<span data-ttu-id="39c0b-130">Habilitar o BGP para esta conexão</span><span class="sxs-lookup"><span data-stu-id="39c0b-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="39c0b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39c0b-131">-InputObject</span></span>
<span data-ttu-id="39c0b-132">O objeto VpnConenction a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="39c0b-132">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="39c0b-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="39c0b-133">-IpSecPolicy</span></span>
<span data-ttu-id="39c0b-134">O banda que precisa ser manipulado por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="39c0b-134">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="39c0b-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="39c0b-135">-Name</span></span>
<span data-ttu-id="39c0b-136">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="39c0b-136">The resource name.</span></span>

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

### <span data-ttu-id="39c0b-137">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="39c0b-137">-ParentResourceName</span></span>
<span data-ttu-id="39c0b-138">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="39c0b-138">The parent resource name.</span></span>

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

### <span data-ttu-id="39c0b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c0b-139">-ResourceGroupName</span></span>
<span data-ttu-id="39c0b-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39c0b-140">The resource group name.</span></span>

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

### <span data-ttu-id="39c0b-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39c0b-141">-ResourceId</span></span>
<span data-ttu-id="39c0b-142">A ID do recurso do objeto VpnConenction a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="39c0b-142">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="39c0b-143">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="39c0b-143">-SharedKey</span></span>
<span data-ttu-id="39c0b-144">A chave compartilhada necessária para definir essa conexão.</span><span class="sxs-lookup"><span data-stu-id="39c0b-144">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="39c0b-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="39c0b-145">-Confirm</span></span>
<span data-ttu-id="39c0b-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39c0b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c0b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c0b-147">-WhatIf</span></span>
<span data-ttu-id="39c0b-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39c0b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c0b-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39c0b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c0b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c0b-150">CommonParameters</span></span>
<span data-ttu-id="39c0b-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c0b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c0b-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c0b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c0b-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39c0b-153">INPUTS</span></span>

### <span data-ttu-id="39c0b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="39c0b-154">System.String</span></span>

### <span data-ttu-id="39c0b-155">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="39c0b-155">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="39c0b-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39c0b-156">OUTPUTS</span></span>

### <span data-ttu-id="39c0b-157">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="39c0b-157">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="39c0b-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39c0b-158">NOTES</span></span>

## <span data-ttu-id="39c0b-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39c0b-159">RELATED LINKS</span></span>

[<span data-ttu-id="39c0b-160">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="39c0b-160">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="39c0b-161">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="39c0b-161">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="39c0b-162">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="39c0b-162">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
