---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603107"
---
# <span data-ttu-id="51fee-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="51fee-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="51fee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51fee-102">SYNOPSIS</span></span>
<span data-ttu-id="51fee-103">Remove um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="51fee-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51fee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51fee-104">SYNTAX</span></span>

### <span data-ttu-id="51fee-105">Remova um cluster de operação de funcionamento dos parâmetros de entrada de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51fee-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51fee-106">Remova um cluster de operação de funcionamento de uma definição de instância OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="51fee-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51fee-107">Remova um cluster de operação de operação de uma ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="51fee-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="51fee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51fee-108">DESCRIPTION</span></span>
<span data-ttu-id="51fee-109">Remove um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="51fee-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="51fee-110">Alguns recursos associados ao cluster podem não ser removidos.</span><span class="sxs-lookup"><span data-stu-id="51fee-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="51fee-111">Por exemplo, o serviço de contêiner do Azure será removido, mas as máquinas virtuais associadas não.</span><span class="sxs-lookup"><span data-stu-id="51fee-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="51fee-112">A conta de armazenamento, o registro de contêiner e o Application insights não são removidos para obter informações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="51fee-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="51fee-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51fee-113">EXAMPLES</span></span>

### <span data-ttu-id="51fee-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51fee-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="51fee-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="51fee-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="51fee-116">OS</span><span class="sxs-lookup"><span data-stu-id="51fee-116">PARAMETERS</span></span>

### <span data-ttu-id="51fee-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51fee-117">-InputObject</span></span>
<span data-ttu-id="51fee-118">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="51fee-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51fee-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51fee-119">-Confirm</span></span>
<span data-ttu-id="51fee-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51fee-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fee-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="51fee-121">-Name</span></span>
<span data-ttu-id="51fee-122">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="51fee-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fee-123">-ResourceGroupName</span></span>
<span data-ttu-id="51fee-124">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="51fee-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51fee-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51fee-125">-ResourceId</span></span>
<span data-ttu-id="51fee-126">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="51fee-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51fee-127">-WhatIf</span></span>
<span data-ttu-id="51fee-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51fee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51fee-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51fee-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="51fee-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51fee-130">INPUTS</span></span>

### <span data-ttu-id="51fee-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="51fee-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="51fee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="51fee-132">System.String</span></span>


## <span data-ttu-id="51fee-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51fee-133">OUTPUTS</span></span>

### <span data-ttu-id="51fee-134">System. void</span><span class="sxs-lookup"><span data-stu-id="51fee-134">System.Void</span></span>


## <span data-ttu-id="51fee-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51fee-135">NOTES</span></span>

## <span data-ttu-id="51fee-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51fee-136">RELATED LINKS</span></span>

