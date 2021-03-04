---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/disconnect-azp2svpngatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzP2SVpnGatewayVpnConnection.md
ms.openlocfilehash: 493927a21b4154065777109341b437d75f934ee3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888686"
---
# <span data-ttu-id="620cc-101">Disconnect-AzP2sVpnGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="620cc-101">Disconnect-AzP2sVpnGatewayVpnConnection</span></span>

## <span data-ttu-id="620cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="620cc-102">SYNOPSIS</span></span>
<span data-ttu-id="620cc-103">Desconectar determinadas conexões de cliente vpn conectadas com um determinado gateway vpn p2s</span><span class="sxs-lookup"><span data-stu-id="620cc-103">Disconnect given connected vpn client connections with a given p2s vpn gateway</span></span>

## <span data-ttu-id="620cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="620cc-104">SYNTAX</span></span>

### <span data-ttu-id="620cc-105">ByP2SVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="620cc-105">ByP2SVpnGatewayName (Default)</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -Name <String> -ResourceGroupName <String>
 -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="620cc-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="620cc-106">ByP2SVpnGatewayObject</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="620cc-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="620cc-107">ByP2SVpnGatewayResourceId</span></span>
```
Disconnect-AzP2sVpnGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="620cc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="620cc-108">DESCRIPTION</span></span>
<span data-ttu-id="620cc-109">O cmdlet **Disconnect-AzP2sVpnGatewayVpnConnection** permite desconectar determinado ponto atual para a conexão de site do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="620cc-109">The **Disconnect-AzP2sVpnGatewayVpnConnection** cmdlet enables you to disconnect given current point to site connection from P2SVpnGateway.</span></span>

## <span data-ttu-id="620cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="620cc-110">EXAMPLES</span></span>

### <span data-ttu-id="620cc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="620cc-111">Example 1</span></span>
```powershell
PS C:\> Disconnect-AzP2sVpnGatewayVpnConnection -ResourceName 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

## <span data-ttu-id="620cc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="620cc-112">PARAMETERS</span></span>

### <span data-ttu-id="620cc-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="620cc-113">-InputObject</span></span>
<span data-ttu-id="620cc-114">O objeto gateway vpn p2s a ser modificado</span><span class="sxs-lookup"><span data-stu-id="620cc-114">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="620cc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="620cc-115">-Name</span></span>
<span data-ttu-id="620cc-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="620cc-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="620cc-117">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="620cc-117">-VpnConnectionId</span></span>
<span data-ttu-id="620cc-118">Vpn Connection Ida</span><span class="sxs-lookup"><span data-stu-id="620cc-118">Vpn Connection Ida</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="620cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="620cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="620cc-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="620cc-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="620cc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="620cc-121">-ResourceId</span></span>
<span data-ttu-id="620cc-122">ID do recurso de gateway de rede virtual P2s</span><span class="sxs-lookup"><span data-stu-id="620cc-122">P2s Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="620cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620cc-123">CommonParameters</span></span>
<span data-ttu-id="620cc-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620cc-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620cc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620cc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="620cc-126">INPUTS</span></span>

### <span data-ttu-id="620cc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="620cc-127">System.String</span></span>

## <span data-ttu-id="620cc-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="620cc-128">OUTPUTS</span></span>

### <span data-ttu-id="620cc-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="620cc-129">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="620cc-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="620cc-130">NOTES</span></span>

## <span data-ttu-id="620cc-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="620cc-131">RELATED LINKS</span></span>
