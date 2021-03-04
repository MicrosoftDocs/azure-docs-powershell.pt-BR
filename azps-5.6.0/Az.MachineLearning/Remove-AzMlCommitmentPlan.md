---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 287db082c5cbe842b0a92b124870effb77068912
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886455"
---
# <span data-ttu-id="ab5f2-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab5f2-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="ab5f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ab5f2-103">Exclui um plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="ab5f2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ab5f2-104">SYNTAX</span></span>

### <span data-ttu-id="ab5f2-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab5f2-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab5f2-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ab5f2-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab5f2-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ab5f2-107">DESCRIPTION</span></span>
<span data-ttu-id="ab5f2-108">Exclui um plano de compromisso do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="ab5f2-109">Observe que os planos de compromisso que têm associações de compromisso não podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="ab5f2-110">Associações de compromisso só podem ser excluídas pelo recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="ab5f2-111">Por exemplo, se você excluir um serviço Web do Azure Machine Learning, a associação de compromisso que associa o serviço Web a um plano de compromisso também será excluída.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="ab5f2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab5f2-112">EXAMPLES</span></span>

### <span data-ttu-id="ab5f2-113">Exemplo 1: Excluir um plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="ab5f2-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="ab5f2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ab5f2-114">PARAMETERS</span></span>

### <span data-ttu-id="ab5f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab5f2-115">-DefaultProfile</span></span>
<span data-ttu-id="ab5f2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ab5f2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab5f2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ab5f2-117">-Force</span></span>
<span data-ttu-id="ab5f2-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ab5f2-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab5f2-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="ab5f2-120">O objeto de serviço Web de aprendizado de máquina.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab5f2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ab5f2-121">-Name</span></span>
<span data-ttu-id="ab5f2-122">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ab5f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab5f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab5f2-124">O nome do grupo de recursos do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ab5f2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab5f2-125">-Confirm</span></span>
<span data-ttu-id="ab5f2-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab5f2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab5f2-127">-WhatIf</span></span>
<span data-ttu-id="ab5f2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab5f2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab5f2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab5f2-130">CommonParameters</span></span>
<span data-ttu-id="ab5f2-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab5f2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab5f2-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab5f2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab5f2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab5f2-133">INPUTS</span></span>

### <span data-ttu-id="ab5f2-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab5f2-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ab5f2-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ab5f2-135">OUTPUTS</span></span>

### <span data-ttu-id="ab5f2-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="ab5f2-136">System.Void</span></span>

## <span data-ttu-id="ab5f2-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="ab5f2-137">NOTES</span></span>
<span data-ttu-id="ab5f2-138">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ab5f2-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ab5f2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab5f2-139">RELATED LINKS</span></span>
