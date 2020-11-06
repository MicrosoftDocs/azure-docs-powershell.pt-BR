---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93611150"
---
# <span data-ttu-id="233f4-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="233f4-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="233f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="233f4-102">SYNOPSIS</span></span>
<span data-ttu-id="233f4-103">Remove um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="233f4-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="233f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="233f4-104">SYNTAX</span></span>

### <span data-ttu-id="233f4-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="233f4-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="233f4-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="233f4-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="233f4-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="233f4-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="233f4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="233f4-108">DESCRIPTION</span></span>
<span data-ttu-id="233f4-109">Remove um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="233f4-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="233f4-110">Alguns recursos associados ao cluster podem não ser removidos.</span><span class="sxs-lookup"><span data-stu-id="233f4-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="233f4-111">Por exemplo, o serviço de contêiner do Azure será removido, mas as máquinas virtuais associadas não.</span><span class="sxs-lookup"><span data-stu-id="233f4-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="233f4-112">A conta de armazenamento, o registro de contêiner e o Application insights não são removidos para obter informações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="233f4-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="233f4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="233f4-113">EXAMPLES</span></span>

### <span data-ttu-id="233f4-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="233f4-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="233f4-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="233f4-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="233f4-116">OS</span><span class="sxs-lookup"><span data-stu-id="233f4-116">PARAMETERS</span></span>

### <span data-ttu-id="233f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="233f4-117">-DefaultProfile</span></span>
<span data-ttu-id="233f4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="233f4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="233f4-119">-IncludeAllResources</span></span>
<span data-ttu-id="233f4-120">Remove todos os recursos que foram criados com o cluster.</span><span class="sxs-lookup"><span data-stu-id="233f4-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="233f4-121">-InputObject</span></span>
<span data-ttu-id="233f4-122">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="233f4-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="233f4-123">-Name</span></span>
<span data-ttu-id="233f4-124">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="233f4-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="233f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="233f4-126">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="233f4-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="233f4-127">-ResourceId</span></span>
<span data-ttu-id="233f4-128">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="233f4-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="233f4-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="233f4-129">-Confirm</span></span>
<span data-ttu-id="233f4-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="233f4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="233f4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="233f4-131">-WhatIf</span></span>
<span data-ttu-id="233f4-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="233f4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="233f4-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="233f4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="233f4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="233f4-134">CommonParameters</span></span>
<span data-ttu-id="233f4-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="233f4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="233f4-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="233f4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="233f4-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="233f4-137">INPUTS</span></span>

### <span data-ttu-id="233f4-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="233f4-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="233f4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="233f4-139">System.String</span></span>

## <span data-ttu-id="233f4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="233f4-140">OUTPUTS</span></span>

### <span data-ttu-id="233f4-141">System. void</span><span class="sxs-lookup"><span data-stu-id="233f4-141">System.Void</span></span>

## <span data-ttu-id="233f4-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="233f4-142">NOTES</span></span>

## <span data-ttu-id="233f4-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="233f4-143">RELATED LINKS</span></span>

