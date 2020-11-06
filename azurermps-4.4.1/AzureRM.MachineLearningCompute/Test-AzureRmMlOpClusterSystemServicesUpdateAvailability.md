---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603360"
---
# <span data-ttu-id="ce9e4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="ce9e4-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="ce9e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9e4-103">Verifica se há atualizações disponíveis para os serviços do sistema associados a um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce9e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce9e4-104">SYNTAX</span></span>

### <span data-ttu-id="ce9e4-105">Teste para a disponibilidade de atualização dos parâmetros de entrada do cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="ce9e4-106">Teste a disponibilidade de atualização de uma definição de instância OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="ce9e4-107">Testar a disponibilidade da atualização a partir de uma ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="ce9e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce9e4-108">DESCRIPTION</span></span>
<span data-ttu-id="ce9e4-109">Os serviços do sistema recebem atualizações independentemente do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="ce9e4-110">Usar esse cmdlet permitirá que o usuário saiba se Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="ce9e4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce9e4-111">EXAMPLES</span></span>

### <span data-ttu-id="ce9e4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce9e4-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="ce9e4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce9e4-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="ce9e4-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce9e4-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="ce9e4-115">OS</span><span class="sxs-lookup"><span data-stu-id="ce9e4-115">PARAMETERS</span></span>

### <span data-ttu-id="ce9e4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce9e4-116">-InputObject</span></span>
<span data-ttu-id="ce9e4-117">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9e4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce9e4-118">-Name</span></span>
<span data-ttu-id="ce9e4-119">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9e4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9e4-120">-ResourceGroupName</span></span>
<span data-ttu-id="ce9e4-121">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9e4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce9e4-122">-ResourceId</span></span>
<span data-ttu-id="ce9e4-123">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="ce9e4-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="ce9e4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce9e4-124">INPUTS</span></span>

### <span data-ttu-id="ce9e4-125">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="ce9e4-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="ce9e4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ce9e4-126">System.String</span></span>


## <span data-ttu-id="ce9e4-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce9e4-127">OUTPUTS</span></span>

### <span data-ttu-id="ce9e4-128">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="ce9e4-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="ce9e4-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce9e4-129">NOTES</span></span>

## <span data-ttu-id="ce9e4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce9e4-130">RELATED LINKS</span></span>

