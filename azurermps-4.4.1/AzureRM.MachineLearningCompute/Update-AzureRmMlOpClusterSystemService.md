---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441026"
---
# <span data-ttu-id="dc766-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="dc766-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="dc766-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc766-102">SYNOPSIS</span></span>
<span data-ttu-id="dc766-103">Inicia uma atualização nos serviços do sistema do cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="dc766-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc766-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc766-104">SYNTAX</span></span>

### <span data-ttu-id="dc766-105">Iniciar uma atualização de serviços do sistema a partir de parâmetros de entrada de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc766-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="dc766-106">Iniciar uma atualização de serviços do sistema a partir de uma definição de instância PSOperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="dc766-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="dc766-107">Iniciar uma atualização de serviços do sistema a partir de uma ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc766-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="dc766-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc766-108">DESCRIPTION</span></span>
<span data-ttu-id="dc766-109">Os serviços do sistema podem ser atualizados independentemente do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="dc766-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="dc766-110">Para iniciar uma atualização nos serviços do sistema, use este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc766-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="dc766-111">Se nenhuma atualização estiver disponível, uma atualização ainda será iniciada e retornará com êxito.</span><span class="sxs-lookup"><span data-stu-id="dc766-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="dc766-112">Depois que a atualização terminar, ele relata quando começou, terminou e se foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dc766-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="dc766-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc766-113">EXAMPLES</span></span>

### <span data-ttu-id="dc766-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc766-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="dc766-115">Inicia uma atualização dos serviços do sistema no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="dc766-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="dc766-116">OS</span><span class="sxs-lookup"><span data-stu-id="dc766-116">PARAMETERS</span></span>

### <span data-ttu-id="dc766-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc766-117">-InputObject</span></span>
<span data-ttu-id="dc766-118">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="dc766-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc766-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc766-119">-Confirm</span></span>
<span data-ttu-id="dc766-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc766-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc766-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc766-121">-Name</span></span>
<span data-ttu-id="dc766-122">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="dc766-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc766-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc766-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc766-124">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="dc766-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc766-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc766-125">-ResourceId</span></span>
<span data-ttu-id="dc766-126">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="dc766-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc766-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc766-127">-WhatIf</span></span>
<span data-ttu-id="dc766-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc766-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc766-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc766-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="dc766-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc766-130">INPUTS</span></span>

### <span data-ttu-id="dc766-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="dc766-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="dc766-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dc766-132">System.String</span></span>


## <span data-ttu-id="dc766-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc766-133">OUTPUTS</span></span>

### <span data-ttu-id="dc766-134">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="dc766-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="dc766-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc766-135">NOTES</span></span>

## <span data-ttu-id="dc766-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc766-136">RELATED LINKS</span></span>

