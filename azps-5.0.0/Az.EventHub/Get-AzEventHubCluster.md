---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124640"
---
# <span data-ttu-id="6eb63-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="6eb63-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="6eb63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eb63-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb63-103">Obtém os detalhes de um único cluster de Hub de evento ou obtém uma lista de clusters de Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="6eb63-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="6eb63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eb63-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6eb63-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6eb63-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb63-106">O cmdlet Get-AzEventHubCluster retorna os detalhes de um cluster de Hub de eventos ou uma lista de todos os clusters de Hub de eventos em um determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6eb63-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="6eb63-107">Se o nome do cluster for fornecido, os detalhes de um único cluster serão retornados.</span><span class="sxs-lookup"><span data-stu-id="6eb63-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="6eb63-108">Se um nome de cluster não for fornecido, uma lista de todos os clusters no grupo de recursos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="6eb63-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="6eb63-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6eb63-109">EXAMPLES</span></span>

### <span data-ttu-id="6eb63-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6eb63-110">Example 1</span></span>
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

<span data-ttu-id="6eb63-111">Retorna o detials do cluster ' Eventhub-cluster-5557 ' do grupo de recursos ' RSG-Cluster27651 '</span><span class="sxs-lookup"><span data-stu-id="6eb63-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="6eb63-112">OS</span><span class="sxs-lookup"><span data-stu-id="6eb63-112">PARAMETERS</span></span>

### <span data-ttu-id="6eb63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb63-113">-DefaultProfile</span></span>
<span data-ttu-id="6eb63-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6eb63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb63-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eb63-115">-Name</span></span>
<span data-ttu-id="6eb63-116">Nome do cluster</span><span class="sxs-lookup"><span data-stu-id="6eb63-116">Cluster Name</span></span>

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

### <span data-ttu-id="6eb63-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb63-117">-ResourceGroupName</span></span>
<span data-ttu-id="6eb63-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6eb63-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6eb63-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb63-119">CommonParameters</span></span>
<span data-ttu-id="6eb63-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb63-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb63-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6eb63-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb63-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6eb63-122">INPUTS</span></span>

### <span data-ttu-id="6eb63-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6eb63-123">System.String</span></span>

## <span data-ttu-id="6eb63-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6eb63-124">OUTPUTS</span></span>

### <span data-ttu-id="6eb63-125">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="6eb63-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="6eb63-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6eb63-126">NOTES</span></span>

## <span data-ttu-id="6eb63-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eb63-127">RELATED LINKS</span></span>
