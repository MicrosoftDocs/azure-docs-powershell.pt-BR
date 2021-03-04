---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 22bbbb79f8662f1e1e70785489187e68e5b38813
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889277"
---
# <span data-ttu-id="4426f-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="4426f-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="4426f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4426f-102">SYNOPSIS</span></span>
<span data-ttu-id="4426f-103">Obtém os detalhes de um único Cluster de Hub de Eventos ou obtém uma lista de Clusters de Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="4426f-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="4426f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4426f-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4426f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4426f-105">DESCRIPTION</span></span>
<span data-ttu-id="4426f-106">O Get-AzEventHubCluster cmdlet retorna os detalhes de um Cluster de Hub de Eventos ou uma lista de todos os Clusters de Hub de Eventos em determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4426f-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="4426f-107">Se o nome do cluster for fornecido, os detalhes de um único cluster serão retornados.</span><span class="sxs-lookup"><span data-stu-id="4426f-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="4426f-108">Se um nome de cluster não for fornecido, uma lista de todos os clusters no grupo de recursos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="4426f-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="4426f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4426f-109">EXAMPLES</span></span>

### <span data-ttu-id="4426f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4426f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="4426f-111">Retorna as detiais do cluster 'Eventhub-Cluster-5557' do grupo de recursos 'RSG-Cluster27651'</span><span class="sxs-lookup"><span data-stu-id="4426f-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="4426f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4426f-112">PARAMETERS</span></span>

### <span data-ttu-id="4426f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4426f-113">-DefaultProfile</span></span>
<span data-ttu-id="4426f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4426f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4426f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4426f-115">-Name</span></span>
<span data-ttu-id="4426f-116">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="4426f-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4426f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4426f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4426f-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4426f-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4426f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4426f-119">CommonParameters</span></span>
<span data-ttu-id="4426f-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4426f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4426f-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4426f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4426f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4426f-122">INPUTS</span></span>

### <span data-ttu-id="4426f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4426f-123">System.String</span></span>

## <span data-ttu-id="4426f-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4426f-124">OUTPUTS</span></span>

### <span data-ttu-id="4426f-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4426f-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="4426f-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="4426f-126">NOTES</span></span>

## <span data-ttu-id="4426f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4426f-127">RELATED LINKS</span></span>
