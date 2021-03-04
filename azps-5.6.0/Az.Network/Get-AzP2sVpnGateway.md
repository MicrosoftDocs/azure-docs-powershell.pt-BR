---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: d20e2098a797d2e90363f54d79759dc682413803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885668"
---
# <span data-ttu-id="87ed0-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87ed0-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="87ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="87ed0-103">Obtém um P2SVpnGateway existente em VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="87ed0-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="87ed0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="87ed0-104">SYNTAX</span></span>

### <span data-ttu-id="87ed0-105">ListBySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="87ed0-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87ed0-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ed0-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87ed0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="87ed0-107">DESCRIPTION</span></span>
<span data-ttu-id="87ed0-108">O cmdlet **Get-AzP2sVpnGateway** permite que você receba um P2SVpnGateway existente em VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="87ed0-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="87ed0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87ed0-109">EXAMPLES</span></span>

### <span data-ttu-id="87ed0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="87ed0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

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
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="87ed0-111">O cmdlet **Get-AzP2sVpnGateway** permite que você receba um P2SVpnGateway existente em VirtualHub usado para conectividade ponto a site.</span><span class="sxs-lookup"><span data-stu-id="87ed0-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="87ed0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="87ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="87ed0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ed0-113">-DefaultProfile</span></span>
<span data-ttu-id="87ed0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87ed0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="87ed0-115">-Name</span></span>
<span data-ttu-id="87ed0-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="87ed0-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, P2SVpnGatewayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ed0-117">-ResourceGroupName</span></span>
<span data-ttu-id="87ed0-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87ed0-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ed0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ed0-119">CommonParameters</span></span>
<span data-ttu-id="87ed0-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ed0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ed0-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ed0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ed0-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87ed0-122">INPUTS</span></span>

### <span data-ttu-id="87ed0-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="87ed0-123">None</span></span>

## <span data-ttu-id="87ed0-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="87ed0-124">OUTPUTS</span></span>

### <span data-ttu-id="87ed0-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="87ed0-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="87ed0-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="87ed0-126">NOTES</span></span>

## <span data-ttu-id="87ed0-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87ed0-127">RELATED LINKS</span></span>
