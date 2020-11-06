---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 5619b9ca4e7f5593a20baf04951d0d5594b31215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428098"
---
# <span data-ttu-id="0971b-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0971b-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="0971b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0971b-102">SYNOPSIS</span></span>
<span data-ttu-id="0971b-103">Remove um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="0971b-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0971b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0971b-104">SYNTAX</span></span>

### <span data-ttu-id="0971b-105">RemoveByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="0971b-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0971b-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0971b-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0971b-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="0971b-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0971b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0971b-108">DESCRIPTION</span></span>
<span data-ttu-id="0971b-109">Remove um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="0971b-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="0971b-110">Alguns recursos associados ao cluster podem não ser removidos.</span><span class="sxs-lookup"><span data-stu-id="0971b-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="0971b-111">Por exemplo, o serviço de contêiner do Azure será removido, mas as máquinas virtuais associadas não.</span><span class="sxs-lookup"><span data-stu-id="0971b-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="0971b-112">A conta de armazenamento, o registro de contêiner e o Application insights não são removidos para obter informações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0971b-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="0971b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0971b-113">EXAMPLES</span></span>

### <span data-ttu-id="0971b-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0971b-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="0971b-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0971b-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="0971b-116">OS</span><span class="sxs-lookup"><span data-stu-id="0971b-116">PARAMETERS</span></span>

### <span data-ttu-id="0971b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0971b-117">-DefaultProfile</span></span>
<span data-ttu-id="0971b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0971b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="0971b-119">-IncludeAllResources</span></span>
<span data-ttu-id="0971b-120">Remove todos os recursos que foram criados com o cluster.</span><span class="sxs-lookup"><span data-stu-id="0971b-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0971b-121">-InputObject</span></span>
<span data-ttu-id="0971b-122">O objeto de cluster operacional.</span><span class="sxs-lookup"><span data-stu-id="0971b-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0971b-123">-Name</span></span>
<span data-ttu-id="0971b-124">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="0971b-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0971b-125">-ResourceGroupName</span></span>
<span data-ttu-id="0971b-126">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="0971b-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0971b-127">-ResourceId</span></span>
<span data-ttu-id="0971b-128">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="0971b-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0971b-129">-Confirm</span></span>
<span data-ttu-id="0971b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0971b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0971b-131">-WhatIf</span></span>
<span data-ttu-id="0971b-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0971b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0971b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0971b-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0971b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0971b-134">CommonParameters</span></span>
<span data-ttu-id="0971b-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0971b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0971b-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0971b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0971b-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0971b-137">INPUTS</span></span>

### <span data-ttu-id="0971b-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="0971b-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="0971b-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0971b-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0971b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0971b-140">System.String</span></span>

## <span data-ttu-id="0971b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0971b-141">OUTPUTS</span></span>

### <span data-ttu-id="0971b-142">System. void</span><span class="sxs-lookup"><span data-stu-id="0971b-142">System.Void</span></span>

## <span data-ttu-id="0971b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0971b-143">NOTES</span></span>

## <span data-ttu-id="0971b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0971b-144">RELATED LINKS</span></span>
