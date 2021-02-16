---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 21529e75ab32cf4dde0434b9e2d4de8951beeb39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118349"
---
# <span data-ttu-id="d78a3-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d78a3-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="d78a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d78a3-102">SYNOPSIS</span></span> 
<span data-ttu-id="d78a3-103">Obter a lista de saúde da conexão do cliente vpn de um gateway de rede virtual do Azure para conexão de cliente vpn</span><span class="sxs-lookup"><span data-stu-id="d78a3-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="d78a3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d78a3-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="d78a3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d78a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d78a3-106">Listar toda a conexões de cliente vpn conectadas.</span><span class="sxs-lookup"><span data-stu-id="d78a3-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="d78a3-107">Isso inclui: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressosBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="d78a3-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="d78a3-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d78a3-108">EXAMPLES</span></span>

### <span data-ttu-id="d78a3-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d78a3-109">Example 1</span></span>
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

<span data-ttu-id="d78a3-110">Para o gateway de rede virtual do Azure chamado gatewayname no resourceGroup do grupo de recursos, recupera a conexão de cliente vpn conectada no momento usando o OpenVpn.</span><span class="sxs-lookup"><span data-stu-id="d78a3-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="d78a3-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d78a3-111">Example 2</span></span>

<span data-ttu-id="d78a3-112">Obter a lista de saúde da conexão do cliente vpn de um gateway de rede virtual do Azure para conexão de cliente vpn.</span><span class="sxs-lookup"><span data-stu-id="d78a3-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="d78a3-113">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="d78a3-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="d78a3-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d78a3-114">PARAMETERS</span></span>

### <span data-ttu-id="d78a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="d78a3-116">Nome do grupo de recursos do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d78a3-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="d78a3-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d78a3-117">-ResourceName</span></span>
<span data-ttu-id="d78a3-118">Nome do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d78a3-118">Virtual network gateway name</span></span>

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
### <span data-ttu-id="d78a3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d78a3-119">-ResourceId</span></span>
<span data-ttu-id="d78a3-120">ID de recurso do gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d78a3-120">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="d78a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d78a3-121">-InputObject</span></span>
<span data-ttu-id="d78a3-122">Objeto de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d78a3-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="d78a3-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d78a3-123">-AsJob</span></span>
<span data-ttu-id="d78a3-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d78a3-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d78a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78a3-125">CommonParameters</span></span>
<span data-ttu-id="d78a3-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78a3-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d78a3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78a3-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="d78a3-128">INPUTS</span></span>

### <span data-ttu-id="d78a3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d78a3-129">System.String</span></span>

## <span data-ttu-id="d78a3-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="d78a3-130">OUTPUTS</span></span>

### <span data-ttu-id="d78a3-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="d78a3-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="d78a3-132">Notas</span><span class="sxs-lookup"><span data-stu-id="d78a3-132">NOTES</span></span>

## <span data-ttu-id="d78a3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d78a3-133">RELATED LINKS</span></span>
