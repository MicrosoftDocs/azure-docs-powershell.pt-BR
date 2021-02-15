---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: d5f78bf034c46d3b07a97d642032ef0cfe6b339e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114668"
---
# <span data-ttu-id="658a0-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="658a0-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="658a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="658a0-102">SYNOPSIS</span></span>
<span data-ttu-id="658a0-103">Cria um objeto Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="658a0-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="658a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="658a0-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="658a0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="658a0-105">DESCRIPTION</span></span>
<span data-ttu-id="658a0-106">Cria um objeto Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="658a0-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="658a0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="658a0-107">EXAMPLES</span></span>

### <span data-ttu-id="658a0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="658a0-108">Example 1</span></span>
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

<span data-ttu-id="658a0-109">O acima criará um grupo de recursos, WAN Virtual, Rede Virtual, Hub Virtual e um VpnSite com 1 VpnSiteLinks no oeste dos EUA no grupo de recursos "testRG" no Azure.</span><span class="sxs-lookup"><span data-stu-id="658a0-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="658a0-110">Um gateway VPN será criado posteriormente no Hub Virtual.</span><span class="sxs-lookup"><span data-stu-id="658a0-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="658a0-111">Depois que o gateway for criado, ele será conectado ao VpnSite usando o comando New-AzVpnConnection com 1 VpnSiteLinkConnections para o VpnSiteLink do VpnSite.</span><span class="sxs-lookup"><span data-stu-id="658a0-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="658a0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="658a0-112">PARAMETERS</span></span>

### <span data-ttu-id="658a0-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="658a0-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="658a0-114">A largura de banda que precisa ser tratada por esta conexão de link em mbps.</span><span class="sxs-lookup"><span data-stu-id="658a0-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="658a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658a0-115">-DefaultProfile</span></span>
<span data-ttu-id="658a0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="658a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="658a0-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="658a0-117">-EgressNatRule</span></span>
<span data-ttu-id="658a0-118">A lista de regras NAT de saída associadas a esta Conexão de link.</span><span class="sxs-lookup"><span data-stu-id="658a0-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

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

### <span data-ttu-id="658a0-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="658a0-119">-EnableBgp</span></span>
<span data-ttu-id="658a0-120">Habilitar BGP para esta conexão de link</span><span class="sxs-lookup"><span data-stu-id="658a0-120">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="658a0-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="658a0-121">-IngressNatRule</span></span>
<span data-ttu-id="658a0-122">A lista de regras NAT de entrada associadas a esta Conexão de link.</span><span class="sxs-lookup"><span data-stu-id="658a0-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

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

### <span data-ttu-id="658a0-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="658a0-123">-IpSecPolicy</span></span>
<span data-ttu-id="658a0-124">Política IpSec a ser considerada para esta conexão de link.</span><span class="sxs-lookup"><span data-stu-id="658a0-124">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="658a0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="658a0-125">-Name</span></span>
<span data-ttu-id="658a0-126">Nome</span><span class="sxs-lookup"><span data-stu-id="658a0-126">Name</span></span>

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

### <span data-ttu-id="658a0-127">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="658a0-127">-RoutingWeight</span></span>
<span data-ttu-id="658a0-128">Peso do Roteamento</span><span class="sxs-lookup"><span data-stu-id="658a0-128">Routing Weight</span></span>

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

### <span data-ttu-id="658a0-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="658a0-129">-SharedKey</span></span>
<span data-ttu-id="658a0-130">A chave compartilhada necessária para configurar essa conexão de link.</span><span class="sxs-lookup"><span data-stu-id="658a0-130">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="658a0-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="658a0-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="658a0-132">Use o endereço ip local do azure como IP de origem para esta conexão de link.</span><span class="sxs-lookup"><span data-stu-id="658a0-132">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="658a0-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="658a0-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="658a0-134">Use seletores de tráfego baseados em política para esta conexão de link.</span><span class="sxs-lookup"><span data-stu-id="658a0-134">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="658a0-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="658a0-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="658a0-136">Protocolo de conexão do gateway:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="658a0-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="658a0-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="658a0-137">-VpnSiteLink</span></span>
<span data-ttu-id="658a0-138">O objeto de link de site vpn para se conectar.</span><span class="sxs-lookup"><span data-stu-id="658a0-138">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="658a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658a0-139">CommonParameters</span></span>
<span data-ttu-id="658a0-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="658a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658a0-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="658a0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658a0-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="658a0-142">INPUTS</span></span>

### <span data-ttu-id="658a0-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="658a0-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="658a0-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="658a0-144">OUTPUTS</span></span>

### <span data-ttu-id="658a0-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="658a0-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="658a0-146">Notas</span><span class="sxs-lookup"><span data-stu-id="658a0-146">NOTES</span></span>

## <span data-ttu-id="658a0-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="658a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="658a0-148">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="658a0-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)