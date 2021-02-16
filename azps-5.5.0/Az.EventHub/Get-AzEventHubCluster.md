---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113206"
---
# <span data-ttu-id="9bda2-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="9bda2-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="9bda2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bda2-102">SYNOPSIS</span></span>
<span data-ttu-id="9bda2-103">Obtém os detalhes de um único Cluster do Hub de Eventos ou obtém uma lista de Clusters do Hub de Eventos.</span><span class="sxs-lookup"><span data-stu-id="9bda2-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="9bda2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bda2-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bda2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bda2-105">DESCRIPTION</span></span>
<span data-ttu-id="9bda2-106">O Get-AzEventHubCluster cmdlet retorna os detalhes de um Cluster do Hub de Eventos ou uma lista de todos os Clusters do Hub de Eventos em determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9bda2-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="9bda2-107">Se o nome do cluster for fornecido, os detalhes de um único cluster serão retornados.</span><span class="sxs-lookup"><span data-stu-id="9bda2-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="9bda2-108">Se um nome de cluster não for fornecido, uma lista de todos os clusters no grupo de recursos especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="9bda2-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="9bda2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bda2-109">EXAMPLES</span></span>

### <span data-ttu-id="9bda2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9bda2-110">Example 1</span></span>
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

<span data-ttu-id="9bda2-111">Retorna as decivações de cluster 'Eventhub-Cluster-5557' do grupo de recursos 'RSG-Cluster27651'</span><span class="sxs-lookup"><span data-stu-id="9bda2-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="9bda2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bda2-112">PARAMETERS</span></span>

### <span data-ttu-id="9bda2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bda2-113">-DefaultProfile</span></span>
<span data-ttu-id="9bda2-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bda2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bda2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bda2-115">-Name</span></span>
<span data-ttu-id="9bda2-116">Nome do Cluster</span><span class="sxs-lookup"><span data-stu-id="9bda2-116">Cluster Name</span></span>

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

### <span data-ttu-id="9bda2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bda2-117">-ResourceGroupName</span></span>
<span data-ttu-id="9bda2-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="9bda2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9bda2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bda2-119">CommonParameters</span></span>
<span data-ttu-id="9bda2-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bda2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bda2-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9bda2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bda2-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="9bda2-122">INPUTS</span></span>

### <span data-ttu-id="9bda2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9bda2-123">System.String</span></span>

## <span data-ttu-id="9bda2-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="9bda2-124">OUTPUTS</span></span>

### <span data-ttu-id="9bda2-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="9bda2-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="9bda2-126">Notas</span><span class="sxs-lookup"><span data-stu-id="9bda2-126">NOTES</span></span>

## <span data-ttu-id="9bda2-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bda2-127">RELATED LINKS</span></span>
