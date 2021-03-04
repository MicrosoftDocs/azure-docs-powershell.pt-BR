---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 8b2e8902257566256ed41c38c90c31cb430d12d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885656"
---
# <span data-ttu-id="8b7a6-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b7a6-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="8b7a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7a6-103">Obtém serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="8b7a6-103">Gets private link service</span></span>

## <span data-ttu-id="8b7a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8b7a6-104">SYNTAX</span></span>

### <span data-ttu-id="8b7a6-105">NoExpand (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8b7a6-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b7a6-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="8b7a6-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b7a6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8b7a6-107">DESCRIPTION</span></span>
<span data-ttu-id="8b7a6-108">O cmdlet **Get-AzPrivateLinkService** obtém um ou mais serviços de link privado.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="8b7a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b7a6-109">EXAMPLES</span></span>

### <span data-ttu-id="8b7a6-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8b7a6-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="8b7a6-111">Esse commandlet obtém um serviço de link privado no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="8b7a6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8b7a6-112">PARAMETERS</span></span>

### <span data-ttu-id="8b7a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7a6-113">-DefaultProfile</span></span>
<span data-ttu-id="8b7a6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b7a6-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8b7a6-115">-ExpandResource</span></span>
<span data-ttu-id="8b7a6-116">A referência de recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7a6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8b7a6-117">-Name</span></span>
<span data-ttu-id="8b7a6-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b7a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b7a6-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7a6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7a6-121">CommonParameters</span></span>
<span data-ttu-id="8b7a6-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b7a6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7a6-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b7a6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7a6-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b7a6-124">INPUTS</span></span>

### <span data-ttu-id="8b7a6-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8b7a6-125">System.String</span></span>

## <span data-ttu-id="8b7a6-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8b7a6-126">OUTPUTS</span></span>

### <span data-ttu-id="8b7a6-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8b7a6-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="8b7a6-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="8b7a6-128">NOTES</span></span>

## <span data-ttu-id="8b7a6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b7a6-129">RELATED LINKS</span></span>
