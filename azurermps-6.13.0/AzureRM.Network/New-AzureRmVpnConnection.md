---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
ms.openlocfilehash: 8b7d0845e6a8fce2d6c496573a493dfd187c34af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610281"
---
# <span data-ttu-id="13f6e-101">New-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="13f6e-101">New-AzureRmVpnConnection</span></span>

## <span data-ttu-id="13f6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="13f6e-103">Cria uma conexão IPSec que conecta um VpnGateway a uma ramificação de cliente remoto representada no RM como um VpnSite.</span><span class="sxs-lookup"><span data-stu-id="13f6e-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13f6e-104">SYNTAX</span></span>

### <span data-ttu-id="13f6e-105">ByVpnGatewayNameByVpnSiteObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="13f6e-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f6e-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="13f6e-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSiteId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f6e-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="13f6e-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f6e-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="13f6e-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f6e-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="13f6e-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f6e-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="13f6e-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13f6e-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13f6e-111">DESCRIPTION</span></span>
<span data-ttu-id="13f6e-112">Cria uma conexão IPSec que conecta um VpnGateway a uma ramificação de cliente remoto representada no RM como um VpnSite.</span><span class="sxs-lookup"><span data-stu-id="13f6e-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="13f6e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13f6e-113">EXAMPLES</span></span>

### <span data-ttu-id="13f6e-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="13f6e-114">Example 1</span></span>

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

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="13f6e-115">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="13f6e-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="13f6e-116">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="13f6e-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="13f6e-117">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="13f6e-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="13f6e-118">OS</span><span class="sxs-lookup"><span data-stu-id="13f6e-118">PARAMETERS</span></span>

### <span data-ttu-id="13f6e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13f6e-119">-AsJob</span></span>
<span data-ttu-id="13f6e-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="13f6e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13f6e-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="13f6e-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="13f6e-122">O banda que precisa ser manipulado por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="13f6e-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="13f6e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f6e-123">-DefaultProfile</span></span>
<span data-ttu-id="13f6e-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13f6e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13f6e-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="13f6e-125">-EnableBgp</span></span>
<span data-ttu-id="13f6e-126">Habilitar o BGP para esta conexão</span><span class="sxs-lookup"><span data-stu-id="13f6e-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="13f6e-127">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="13f6e-127">-IpSecPolicy</span></span>
<span data-ttu-id="13f6e-128">O banda que precisa ser manipulado por essa conexão em Mbps.</span><span class="sxs-lookup"><span data-stu-id="13f6e-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="13f6e-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="13f6e-129">-Name</span></span>
<span data-ttu-id="13f6e-130">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="13f6e-130">The resource name.</span></span>

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

### <span data-ttu-id="13f6e-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="13f6e-131">-ParentObject</span></span>
<span data-ttu-id="13f6e-132">O VpnGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="13f6e-132">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="13f6e-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="13f6e-133">-ParentResourceId</span></span>
<span data-ttu-id="13f6e-134">A ID do recurso do VpnGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="13f6e-134">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="13f6e-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="13f6e-135">-ParentResourceName</span></span>
<span data-ttu-id="13f6e-136">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13f6e-136">The resource group name.</span></span>

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

### <span data-ttu-id="13f6e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f6e-137">-ResourceGroupName</span></span>
<span data-ttu-id="13f6e-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13f6e-138">The resource group name.</span></span>

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

### <span data-ttu-id="13f6e-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="13f6e-139">-SharedKey</span></span>
<span data-ttu-id="13f6e-140">A chave compartilhada necessária para definir essa conexão.</span><span class="sxs-lookup"><span data-stu-id="13f6e-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="13f6e-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="13f6e-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="13f6e-142">Protocolo de conexão de gateway: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="13f6e-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="13f6e-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="13f6e-143">-VpnSite</span></span>
<span data-ttu-id="13f6e-144">O site VPN remoto ao qual essa conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="13f6e-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="13f6e-145">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="13f6e-145">-VpnSiteId</span></span>
<span data-ttu-id="13f6e-146">O site VPN remoto ao qual essa conexão de rede virtual do Hub está conectada.</span><span class="sxs-lookup"><span data-stu-id="13f6e-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="13f6e-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="13f6e-147">-Confirm</span></span>
<span data-ttu-id="13f6e-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13f6e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13f6e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f6e-149">-WhatIf</span></span>
<span data-ttu-id="13f6e-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="13f6e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13f6e-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13f6e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13f6e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f6e-152">CommonParameters</span></span>
<span data-ttu-id="13f6e-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f6e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f6e-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f6e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f6e-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13f6e-155">INPUTS</span></span>

### <span data-ttu-id="13f6e-156">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="13f6e-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="13f6e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="13f6e-157">System.String</span></span>

## <span data-ttu-id="13f6e-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13f6e-158">OUTPUTS</span></span>

### <span data-ttu-id="13f6e-159">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="13f6e-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="13f6e-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13f6e-160">NOTES</span></span>

## <span data-ttu-id="13f6e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13f6e-161">RELATED LINKS</span></span>
