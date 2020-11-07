---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGateway.md
ms.openlocfilehash: 05881e5248ecad95222d5e3e7148edbc8c1a1dea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940372"
---
# <span data-ttu-id="44ccd-101">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="44ccd-101">Get-AzP2sVpnGateway</span></span>

## <span data-ttu-id="44ccd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="44ccd-103">Obtém um P2SVpnGateway existente em VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="44ccd-103">Gets an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="44ccd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44ccd-104">SYNTAX</span></span>

### <span data-ttu-id="44ccd-105">ListBySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="44ccd-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzP2sVpnGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44ccd-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ccd-106">ListByResourceGroupName</span></span>
```
Get-AzP2sVpnGateway [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44ccd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44ccd-107">DESCRIPTION</span></span>
<span data-ttu-id="44ccd-108">O cmdlet **Get-AzP2sVpnGateway** permite que você obtenha um P2SVpnGateway existente em VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="44ccd-108">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="44ccd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44ccd-109">EXAMPLES</span></span>

### <span data-ttu-id="44ccd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44ccd-110">Example 1</span></span>
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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="44ccd-111">O cmdlet **Get-AzP2sVpnGateway** permite que você obtenha um P2SVpnGateway existente em VirtualHub que é usado para apontar para a conectividade do site.</span><span class="sxs-lookup"><span data-stu-id="44ccd-111">The **Get-AzP2sVpnGateway** cmdlet enables you to get an existing P2SVpnGateway under VirtualHub that is used for Point to site connectivity.</span></span>

## <span data-ttu-id="44ccd-112">OS</span><span class="sxs-lookup"><span data-stu-id="44ccd-112">PARAMETERS</span></span>

### <span data-ttu-id="44ccd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ccd-113">-DefaultProfile</span></span>
<span data-ttu-id="44ccd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44ccd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ccd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="44ccd-115">-Name</span></span>
<span data-ttu-id="44ccd-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="44ccd-116">The resource name.</span></span>

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

### <span data-ttu-id="44ccd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ccd-117">-ResourceGroupName</span></span>
<span data-ttu-id="44ccd-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44ccd-118">The resource group name.</span></span>

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

### <span data-ttu-id="44ccd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ccd-119">CommonParameters</span></span>
<span data-ttu-id="44ccd-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ccd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ccd-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ccd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ccd-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44ccd-122">INPUTS</span></span>

### <span data-ttu-id="44ccd-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44ccd-123">None</span></span>

## <span data-ttu-id="44ccd-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44ccd-124">OUTPUTS</span></span>

### <span data-ttu-id="44ccd-125">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="44ccd-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="44ccd-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44ccd-126">NOTES</span></span>

## <span data-ttu-id="44ccd-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44ccd-127">RELATED LINKS</span></span>
