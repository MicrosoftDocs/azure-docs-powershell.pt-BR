---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: c52aec45b71510c508ad56359b0ea87c98bef4dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944859"
---
# <span data-ttu-id="36bde-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="36bde-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="36bde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36bde-102">SYNOPSIS</span></span>
<span data-ttu-id="36bde-103">Obtém uma conexão VPN por nome ou lista todas as conexões VPN conectadas a um VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="36bde-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="36bde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36bde-104">SYNTAX</span></span>

### <span data-ttu-id="36bde-105">ByVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="36bde-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36bde-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="36bde-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36bde-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="36bde-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36bde-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36bde-108">DESCRIPTION</span></span>
<span data-ttu-id="36bde-109">Obtém uma conexão VPN por nome ou lista todas as conexões VPN conectadas a um VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="36bde-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="36bde-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36bde-110">EXAMPLES</span></span>

### <span data-ttu-id="36bde-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36bde-111">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

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
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="36bde-112">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="36bde-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="36bde-113">Um gateway VPN será criado posteriormente no Hub virtual com duas unidades de escala.</span><span class="sxs-lookup"><span data-stu-id="36bde-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="36bde-114">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="36bde-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="36bde-115">Em seguida, ele obtém a conexão usando o nome da conexão.</span><span class="sxs-lookup"><span data-stu-id="36bde-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="36bde-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="36bde-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

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
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1

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
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
```

<span data-ttu-id="36bde-117">Este cmdlet obtém todas as conexões que começam com "Test".</span><span class="sxs-lookup"><span data-stu-id="36bde-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="36bde-118">OS</span><span class="sxs-lookup"><span data-stu-id="36bde-118">PARAMETERS</span></span>

### <span data-ttu-id="36bde-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36bde-119">-DefaultProfile</span></span>
<span data-ttu-id="36bde-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36bde-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36bde-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="36bde-121">-Name</span></span>
<span data-ttu-id="36bde-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="36bde-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bde-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36bde-123">-ParentObject</span></span>
<span data-ttu-id="36bde-124">O VpnGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="36bde-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36bde-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="36bde-125">-ParentResourceId</span></span>
<span data-ttu-id="36bde-126">A ID do recurso do VpnGateway pai dessa conexão.</span><span class="sxs-lookup"><span data-stu-id="36bde-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36bde-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="36bde-127">-ParentResourceName</span></span>
<span data-ttu-id="36bde-128">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="36bde-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bde-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36bde-129">-ResourceGroupName</span></span>
<span data-ttu-id="36bde-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36bde-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36bde-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36bde-131">CommonParameters</span></span>
<span data-ttu-id="36bde-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36bde-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36bde-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36bde-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36bde-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36bde-134">INPUTS</span></span>

### <span data-ttu-id="36bde-135">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="36bde-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="36bde-136">System. String</span><span class="sxs-lookup"><span data-stu-id="36bde-136">System.String</span></span>

## <span data-ttu-id="36bde-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36bde-137">OUTPUTS</span></span>

### <span data-ttu-id="36bde-138">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="36bde-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="36bde-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36bde-139">NOTES</span></span>

## <span data-ttu-id="36bde-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36bde-140">RELATED LINKS</span></span>

[<span data-ttu-id="36bde-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="36bde-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="36bde-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="36bde-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="36bde-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="36bde-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
