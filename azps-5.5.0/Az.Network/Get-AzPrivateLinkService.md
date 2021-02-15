---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: fdbb023c6796a780bfe9e6474191185a58489c91
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112895"
---
# <span data-ttu-id="94eae-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94eae-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="94eae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94eae-102">SYNOPSIS</span></span>
<span data-ttu-id="94eae-103">Obtém o serviço de link particular</span><span class="sxs-lookup"><span data-stu-id="94eae-103">Gets private link service</span></span>

## <span data-ttu-id="94eae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94eae-104">SYNTAX</span></span>

### <span data-ttu-id="94eae-105">NoExpand (Padrão)</span><span class="sxs-lookup"><span data-stu-id="94eae-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94eae-106">Expandir</span><span class="sxs-lookup"><span data-stu-id="94eae-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94eae-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="94eae-107">DESCRIPTION</span></span>
<span data-ttu-id="94eae-108">O cmdlet **Get-AzPrivateLinkService** recebe um ou mais serviços de link particular.</span><span class="sxs-lookup"><span data-stu-id="94eae-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="94eae-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94eae-109">EXAMPLES</span></span>

### <span data-ttu-id="94eae-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="94eae-110">Example</span></span>
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

<span data-ttu-id="94eae-111">Esse commandlet obtém um serviço de vinculação particular no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94eae-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="94eae-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94eae-112">PARAMETERS</span></span>

### <span data-ttu-id="94eae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94eae-113">-DefaultProfile</span></span>
<span data-ttu-id="94eae-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94eae-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94eae-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="94eae-115">-ExpandResource</span></span>
<span data-ttu-id="94eae-116">A referência de recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="94eae-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="94eae-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="94eae-117">-Name</span></span>
<span data-ttu-id="94eae-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="94eae-118">The resource name.</span></span>

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

### <span data-ttu-id="94eae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94eae-119">-ResourceGroupName</span></span>
<span data-ttu-id="94eae-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94eae-120">The resource group name.</span></span>

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

### <span data-ttu-id="94eae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94eae-121">CommonParameters</span></span>
<span data-ttu-id="94eae-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94eae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94eae-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94eae-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94eae-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="94eae-124">INPUTS</span></span>

### <span data-ttu-id="94eae-125">System.String</span><span class="sxs-lookup"><span data-stu-id="94eae-125">System.String</span></span>

## <span data-ttu-id="94eae-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="94eae-126">OUTPUTS</span></span>

### <span data-ttu-id="94eae-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94eae-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="94eae-128">Notas</span><span class="sxs-lookup"><span data-stu-id="94eae-128">NOTES</span></span>

## <span data-ttu-id="94eae-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94eae-129">RELATED LINKS</span></span>
