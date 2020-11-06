---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433088"
---
# <span data-ttu-id="8e442-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="8e442-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="8e442-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e442-102">SYNOPSIS</span></span>
<span data-ttu-id="8e442-103">Obtém as teclas de acesso associadas a um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="8e442-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e442-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e442-104">SYNTAX</span></span>

### <span data-ttu-id="8e442-105">Obter chaves do cluster de operação de parâmetros de entrada de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e442-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="8e442-106">Obter as chaves do cluster de operação de uma definição de instância do OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="8e442-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="8e442-107">Obter chaves do cluster de operação de um ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e442-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="8e442-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e442-108">DESCRIPTION</span></span>
<span data-ttu-id="8e442-109">As chaves para a conta de armazenamento, o registro de contêiner e outros serviços associados ao cluster de operação de funcionamento não são retornadas ao obter as propriedades do cluster.</span><span class="sxs-lookup"><span data-stu-id="8e442-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="8e442-110">Uma chamada específica para recuperar as chaves deve ser feita, já que elas são informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="8e442-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="8e442-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e442-111">EXAMPLES</span></span>

### <span data-ttu-id="8e442-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e442-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="8e442-113">Retorna as chaves secretas dos serviços associados ao cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="8e442-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="8e442-114">OS</span><span class="sxs-lookup"><span data-stu-id="8e442-114">PARAMETERS</span></span>

### <span data-ttu-id="8e442-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e442-115">-InputObject</span></span>
<span data-ttu-id="8e442-116">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="8e442-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e442-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e442-117">-Name</span></span>
<span data-ttu-id="8e442-118">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="8e442-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e442-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e442-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e442-120">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="8e442-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e442-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e442-121">-ResourceId</span></span>
<span data-ttu-id="8e442-122">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="8e442-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="8e442-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e442-123">INPUTS</span></span>

### <span data-ttu-id="8e442-124">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="8e442-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="8e442-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8e442-125">System.String</span></span>


## <span data-ttu-id="8e442-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e442-126">OUTPUTS</span></span>

### <span data-ttu-id="8e442-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="8e442-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="8e442-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e442-128">NOTES</span></span>

## <span data-ttu-id="8e442-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e442-129">RELATED LINKS</span></span>

