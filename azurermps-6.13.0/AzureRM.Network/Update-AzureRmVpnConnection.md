---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430124"
---
# <span data-ttu-id="3eedf-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3eedf-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="3eedf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3eedf-102">SYNOPSIS</span></span>
<span data-ttu-id="3eedf-103">Atualiza um objeto VpnConnection para um estado de meta.</span><span class="sxs-lookup"><span data-stu-id="3eedf-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eedf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3eedf-104">SYNTAX</span></span>

### <span data-ttu-id="3eedf-105">ByVpnConnectionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3eedf-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eedf-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="3eedf-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eedf-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="3eedf-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eedf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3eedf-108">DESCRIPTION</span></span>
<span data-ttu-id="3eedf-109">Cria uma conexão IPSec que conecta um VpnGateway a uma ramificação de cliente remoto representada no RM como um VpnSite.</span><span class="sxs-lookup"><span data-stu-id="3eedf-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="3eedf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3eedf-110">EXAMPLES</span></span>

### <span data-ttu-id="3eedf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3eedf-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

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

<span data-ttu-id="3eedf-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="3eedf-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3eedf-113">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="3eedf-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3eedf-114">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="3eedf-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="3eedf-115">A conexão é atualizada para ter um novo IpSecPolicy usando o comando Set-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="3eedf-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="3eedf-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3eedf-116">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

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

<span data-ttu-id="3eedf-117">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="3eedf-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3eedf-118">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="3eedf-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3eedf-119">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="3eedf-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="3eedf-120">A conexão é atualizada para ter uma nova chave compartilhada usando a construção de cadeia de caracteres segura.</span><span class="sxs-lookup"><span data-stu-id="3eedf-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="3eedf-121">OS</span><span class="sxs-lookup"><span data-stu-id="3eedf-121">PARAMETERS</span></span>

### <span data-ttu-id="3eedf-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eedf-122">-AsJob</span></span>
<span data-ttu-id="3eedf-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3eedf-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eedf-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3eedf-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="3eedf-125">O banda que precisa ser manipulado por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="3eedf-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="3eedf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eedf-126">-DefaultProfile</span></span>
<span data-ttu-id="3eedf-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3eedf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eedf-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="3eedf-128">-EnableBgp</span></span>
<span data-ttu-id="3eedf-129">Habilitar o BGP para esta conexão</span><span class="sxs-lookup"><span data-stu-id="3eedf-129">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="3eedf-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eedf-130">-InputObject</span></span>
<span data-ttu-id="3eedf-131">O objeto VpnConenction a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="3eedf-131">The VpnConenction object to update.</span></span>

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

### <span data-ttu-id="3eedf-132">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="3eedf-132">-IpSecPolicy</span></span>
<span data-ttu-id="3eedf-133">O banda que precisa ser manipulado por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="3eedf-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="3eedf-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eedf-134">-Name</span></span>
<span data-ttu-id="3eedf-135">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3eedf-135">The resource name.</span></span>

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

### <span data-ttu-id="3eedf-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3eedf-136">-ParentResourceName</span></span>
<span data-ttu-id="3eedf-137">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="3eedf-137">The parent resource name.</span></span>

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

### <span data-ttu-id="3eedf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eedf-138">-ResourceGroupName</span></span>
<span data-ttu-id="3eedf-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3eedf-139">The resource group name.</span></span>

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

### <span data-ttu-id="3eedf-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eedf-140">-ResourceId</span></span>
<span data-ttu-id="3eedf-141">A ID do recurso do objeto VpnConenction a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="3eedf-141">The resource id of the VpnConenction object to delete.</span></span>

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

### <span data-ttu-id="3eedf-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3eedf-142">-SharedKey</span></span>
<span data-ttu-id="3eedf-143">A chave compartilhada necessária para definir essa conexão.</span><span class="sxs-lookup"><span data-stu-id="3eedf-143">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="3eedf-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3eedf-144">-Confirm</span></span>
<span data-ttu-id="3eedf-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eedf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eedf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eedf-146">-WhatIf</span></span>
<span data-ttu-id="3eedf-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3eedf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eedf-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3eedf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eedf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eedf-149">CommonParameters</span></span>
<span data-ttu-id="3eedf-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eedf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eedf-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eedf-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eedf-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3eedf-152">INPUTS</span></span>

### <span data-ttu-id="3eedf-153">System. String</span><span class="sxs-lookup"><span data-stu-id="3eedf-153">System.String</span></span>

### <span data-ttu-id="3eedf-154">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3eedf-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="3eedf-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3eedf-155">OUTPUTS</span></span>

### <span data-ttu-id="3eedf-156">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="3eedf-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="3eedf-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3eedf-157">NOTES</span></span>

## <span data-ttu-id="3eedf-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3eedf-158">RELATED LINKS</span></span>
