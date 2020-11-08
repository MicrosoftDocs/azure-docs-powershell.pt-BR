---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 31679702c1499ac91f41b14057e1bc13ef2dfc32
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114351"
---
# <span data-ttu-id="c91c3-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c91c3-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="c91c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c91c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c91c3-103">Cria um objeto VpnSiteLinkConnection do Azure.</span><span class="sxs-lookup"><span data-stu-id="c91c3-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="c91c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c91c3-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c91c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c91c3-105">DESCRIPTION</span></span>
<span data-ttu-id="c91c3-106">Cria um objeto VpnSiteLinkConnection do Azure.</span><span class="sxs-lookup"><span data-stu-id="c91c3-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="c91c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c91c3-107">EXAMPLES</span></span>

### <span data-ttu-id="c91c3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c91c3-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="c91c3-109">A seguir, você criará um grupo de recursos, uma WAN virtual, uma rede virtual, um hub virtual e um VpnSite com 1 VpnSiteLinks nos EUA no grupo de recursos "testRG" do Azure.</span><span class="sxs-lookup"><span data-stu-id="c91c3-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="c91c3-110">Um gateway VPN será criado posteriormente no Hub virtual.</span><span class="sxs-lookup"><span data-stu-id="c91c3-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="c91c3-111">Após a criação do gateway, ele é conectado ao VpnSite usando o comando New-AzVpnConnection com 1 VpnSiteLinkConnections para o VpnSiteLink do VpnSite.</span><span class="sxs-lookup"><span data-stu-id="c91c3-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="c91c3-112">OS</span><span class="sxs-lookup"><span data-stu-id="c91c3-112">PARAMETERS</span></span>

### <span data-ttu-id="c91c3-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="c91c3-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="c91c3-114">A largura de banda que precisa ser manipulada por essa conexão de link em Mbps.</span><span class="sxs-lookup"><span data-stu-id="c91c3-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="c91c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91c3-115">-DefaultProfile</span></span>
<span data-ttu-id="c91c3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c91c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c91c3-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c91c3-117">-EnableBgp</span></span>
<span data-ttu-id="c91c3-118">Habilitar o BGP para esta conexão de link</span><span class="sxs-lookup"><span data-stu-id="c91c3-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="c91c3-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="c91c3-119">-IpSecPolicy</span></span>
<span data-ttu-id="c91c3-120">Política IpSec a ser considerada para esta conexão de link.</span><span class="sxs-lookup"><span data-stu-id="c91c3-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="c91c3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c91c3-121">-Name</span></span>
<span data-ttu-id="c91c3-122">Sobrenome</span><span class="sxs-lookup"><span data-stu-id="c91c3-122">Name</span></span>

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

### <span data-ttu-id="c91c3-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="c91c3-123">-RoutingWeight</span></span>
<span data-ttu-id="c91c3-124">Peso do roteamento</span><span class="sxs-lookup"><span data-stu-id="c91c3-124">Routing Weight</span></span>

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

### <span data-ttu-id="c91c3-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c91c3-125">-SharedKey</span></span>
<span data-ttu-id="c91c3-126">A chave compartilhada necessária para definir essa conexão de link.</span><span class="sxs-lookup"><span data-stu-id="c91c3-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="c91c3-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="c91c3-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="c91c3-128">Use o endereço IP do Azure local como IP de origem para esta conexão de link.</span><span class="sxs-lookup"><span data-stu-id="c91c3-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="c91c3-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="c91c3-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="c91c3-130">Use seletores de tráfego baseado em política para esta conexão de link.</span><span class="sxs-lookup"><span data-stu-id="c91c3-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="c91c3-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="c91c3-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="c91c3-132">Protocolo de conexão de gateway: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="c91c3-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="c91c3-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c91c3-133">-VpnSiteLink</span></span>
<span data-ttu-id="c91c3-134">O objeto de link de site VPN ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="c91c3-134">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c91c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91c3-135">CommonParameters</span></span>
<span data-ttu-id="c91c3-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c91c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91c3-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c91c3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91c3-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c91c3-138">INPUTS</span></span>

### <span data-ttu-id="c91c3-139">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="c91c3-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="c91c3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c91c3-140">OUTPUTS</span></span>

### <span data-ttu-id="c91c3-141">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c91c3-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="c91c3-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c91c3-142">NOTES</span></span>

## <span data-ttu-id="c91c3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c91c3-143">RELATED LINKS</span></span>

[<span data-ttu-id="c91c3-144">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c91c3-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)