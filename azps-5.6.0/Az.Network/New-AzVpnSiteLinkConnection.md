---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 4f61bce910a2dc0f2b177423a5dc199103da378d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889424"
---
# <span data-ttu-id="d6690-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d6690-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="d6690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6690-102">SYNOPSIS</span></span>
<span data-ttu-id="d6690-103">Cria um objeto Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="d6690-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="d6690-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d6690-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6690-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d6690-105">DESCRIPTION</span></span>
<span data-ttu-id="d6690-106">Cria um objeto Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="d6690-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="d6690-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6690-107">EXAMPLES</span></span>

### <span data-ttu-id="d6690-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6690-108">Example 1</span></span>
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

<span data-ttu-id="d6690-109">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um VpnSite com 1 VpnSiteLinks no Oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="d6690-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="d6690-110">Um gateway VPN será criado posteriormente no Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="d6690-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="d6690-111">Depois que o gateway for criado, ele será conectado ao VpnSite usando o comando New-AzVpnConnection com 1 VpnSiteLinkConnections para o VpnSiteLink do VpnSite.</span><span class="sxs-lookup"><span data-stu-id="d6690-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="d6690-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d6690-112">PARAMETERS</span></span>

### <span data-ttu-id="d6690-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="d6690-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="d6690-114">A largura de banda que precisa ser manipulada por essa conexão de link em mbps.</span><span class="sxs-lookup"><span data-stu-id="d6690-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="d6690-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6690-115">-DefaultProfile</span></span>
<span data-ttu-id="d6690-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6690-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6690-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="d6690-117">-EgressNatRule</span></span>
<span data-ttu-id="d6690-118">A lista de regras NAT de saída associadas a este link Connection.</span><span class="sxs-lookup"><span data-stu-id="d6690-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6690-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d6690-119">-EnableBgp</span></span>
<span data-ttu-id="d6690-120">Habilitar BGP para essa conexão de link</span><span class="sxs-lookup"><span data-stu-id="d6690-120">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="d6690-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="d6690-121">-IngressNatRule</span></span>
<span data-ttu-id="d6690-122">A lista de regras NAT de entrada associadas a este link Connection.</span><span class="sxs-lookup"><span data-stu-id="d6690-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6690-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="d6690-123">-IpSecPolicy</span></span>
<span data-ttu-id="d6690-124">Política IpSec a ser considerada para essa conexão de link.</span><span class="sxs-lookup"><span data-stu-id="d6690-124">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="d6690-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d6690-125">-Name</span></span>
<span data-ttu-id="d6690-126">Nome</span><span class="sxs-lookup"><span data-stu-id="d6690-126">Name</span></span>

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

### <span data-ttu-id="d6690-127">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="d6690-127">-RoutingWeight</span></span>
<span data-ttu-id="d6690-128">Peso do roteamento</span><span class="sxs-lookup"><span data-stu-id="d6690-128">Routing Weight</span></span>

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

### <span data-ttu-id="d6690-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d6690-129">-SharedKey</span></span>
<span data-ttu-id="d6690-130">A chave compartilhada necessária para configurar essa conexão de link.</span><span class="sxs-lookup"><span data-stu-id="d6690-130">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="d6690-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6690-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="d6690-132">Use o endereço ip local do azure como IP de origem para esta conexão de link.</span><span class="sxs-lookup"><span data-stu-id="d6690-132">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="d6690-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d6690-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="d6690-134">Use seletores de tráfego baseados em política para essa conexão de link.</span><span class="sxs-lookup"><span data-stu-id="d6690-134">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="d6690-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="d6690-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="d6690-136">Protocolo de conexão de gateway:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="d6690-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="d6690-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d6690-137">-VpnSiteLink</span></span>
<span data-ttu-id="d6690-138">O objeto de link de site vpn ao que se conectar.</span><span class="sxs-lookup"><span data-stu-id="d6690-138">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="d6690-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6690-139">CommonParameters</span></span>
<span data-ttu-id="d6690-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6690-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6690-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6690-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6690-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6690-142">INPUTS</span></span>

### <span data-ttu-id="d6690-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d6690-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="d6690-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d6690-144">OUTPUTS</span></span>

### <span data-ttu-id="d6690-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d6690-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="d6690-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="d6690-146">NOTES</span></span>

## <span data-ttu-id="d6690-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6690-147">RELATED LINKS</span></span>

[<span data-ttu-id="d6690-148">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6690-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)