---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 21529e75ab32cf4dde0434b9e2d4de8951beeb39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429585"
---
# <span data-ttu-id="e831b-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e831b-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="e831b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e831b-102">SYNOPSIS</span></span> 
<span data-ttu-id="e831b-103">Obter a lista de integridade da conexão do cliente VPN de um gateway virtual de rede do Azure para conexão por cliente VPN</span><span class="sxs-lookup"><span data-stu-id="e831b-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="e831b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e831b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="e831b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e831b-105">DESCRIPTION</span></span>
<span data-ttu-id="e831b-106">Listar todas as condições de conexão do cliente VPN conectado.</span><span class="sxs-lookup"><span data-stu-id="e831b-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="e831b-107">Isso inclui: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="e831b-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="e831b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e831b-108">EXAMPLES</span></span>

### <span data-ttu-id="e831b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e831b-109">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName gatewayName -ResourceGroupName resourceGroup

VpnConnectionId           : OVPN_0085393D-B345-4846-0426-140616833F4C
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39672
PrivateIpAddress          : 10.1.1.131
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104084
EgressBytesTransferred    : 4059276
IngressPacketsTransferred : 1410
IngressBytesTransferred   : 67680
MaxPacketsPerSecond       : 1

VpnConnectionId           : OVPN_00F692AC-2D6F-DE7B-DCAF-07BE896233A0
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39692
PrivateIpAddress          : 10.1.1.79
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104623
EgressBytesTransferred    : 4080297
IngressPacketsTransferred : 1416
IngressBytesTransferred   : 67968
MaxPacketsPerSecond       : 1
```

<span data-ttu-id="e831b-110">Para o gateway de rede virtual do Azure chamado GATEWAYNAME no grupo de Resource do grupo de recursos, recupere a conexão de cliente VPN atualmente conectada usando OpenVpn.</span><span class="sxs-lookup"><span data-stu-id="e831b-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="e831b-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e831b-111">Example 2</span></span>

<span data-ttu-id="e831b-112">Obter a lista de integridade da conexão do cliente VPN de um gateway virtual de rede do Azure para conexão por cliente VPN.</span><span class="sxs-lookup"><span data-stu-id="e831b-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="e831b-113">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e831b-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="e831b-114">OS</span><span class="sxs-lookup"><span data-stu-id="e831b-114">PARAMETERS</span></span>

### <span data-ttu-id="e831b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e831b-115">-ResourceGroupName</span></span>
<span data-ttu-id="e831b-116">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e831b-116">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e831b-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e831b-117">-ResourceName</span></span>
<span data-ttu-id="e831b-118">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e831b-118">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="e831b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e831b-119">-ResourceId</span></span>
<span data-ttu-id="e831b-120">ID do recurso do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e831b-120">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e831b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e831b-121">-InputObject</span></span>
<span data-ttu-id="e831b-122">Objeto de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e831b-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e831b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e831b-123">-AsJob</span></span>
<span data-ttu-id="e831b-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e831b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e831b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e831b-125">CommonParameters</span></span>
<span data-ttu-id="e831b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e831b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e831b-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e831b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e831b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e831b-128">INPUTS</span></span>

### <span data-ttu-id="e831b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e831b-129">System.String</span></span>

## <span data-ttu-id="e831b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e831b-130">OUTPUTS</span></span>

### <span data-ttu-id="e831b-131">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="e831b-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="e831b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e831b-132">NOTES</span></span>

## <span data-ttu-id="e831b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e831b-133">RELATED LINKS</span></span>
