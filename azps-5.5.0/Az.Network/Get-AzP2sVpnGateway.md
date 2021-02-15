---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 541115347cfca85e0259e425912e83c4649e0952
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115163"
---
# <span data-ttu-id="c6a2f-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c6a2f-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="c6a2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a2f-103">Obtém um P2SVpnGateway existente no VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c6a2f-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="c6a2f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6a2f-104">SYNTAX</span></span>

### <span data-ttu-id="c6a2f-105">ListBySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c6a2f-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6a2f-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a2f-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a2f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6a2f-107">DESCRIPTION</span></span>
<span data-ttu-id="c6a2f-108">O cmdlet **Get-AzP2sVpnGateway** permite que você receba um P2SVpnGateway existente no VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c6a2f-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="c6a2f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6a2f-109">EXAMPLES</span></span>

### <span data-ttu-id="c6a2f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6a2f-110">Example 1</span></span>
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

<span data-ttu-id="c6a2f-111">O cmdlet **Get-AzP2sVpnGateway** permite que você receba um P2SVpnGateway existente no VirtualHub que é usado para a conectividade do ponto para o site.</span><span class="sxs-lookup"><span data-stu-id="c6a2f-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="c6a2f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6a2f-112">PARAMETERS</span></span>

### <span data-ttu-id="c6a2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a2f-113">-DefaultProfile</span></span>
<span data-ttu-id="c6a2f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6a2f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a2f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6a2f-115">-Name</span></span>
<span data-ttu-id="c6a2f-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c6a2f-116">The resource name.</span></span>

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

### <span data-ttu-id="c6a2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c6a2f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6a2f-118">The resource group name.</span></span>

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

### <span data-ttu-id="c6a2f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a2f-119">CommonParameters</span></span>
<span data-ttu-id="c6a2f-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a2f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a2f-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a2f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a2f-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="c6a2f-122">INPUTS</span></span>

### <span data-ttu-id="c6a2f-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c6a2f-123">None</span></span>

## <span data-ttu-id="c6a2f-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="c6a2f-124">OUTPUTS</span></span>

### <span data-ttu-id="c6a2f-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c6a2f-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="c6a2f-126">Notas</span><span class="sxs-lookup"><span data-stu-id="c6a2f-126">NOTES</span></span>

## <span data-ttu-id="c6a2f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6a2f-127">RELATED LINKS</span></span>
