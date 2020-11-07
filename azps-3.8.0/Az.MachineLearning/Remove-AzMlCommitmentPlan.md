---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944231"
---
# <span data-ttu-id="48157-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="48157-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="48157-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48157-102">SYNOPSIS</span></span>
<span data-ttu-id="48157-103">Exclui um plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="48157-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="48157-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48157-104">SYNTAX</span></span>

### <span data-ttu-id="48157-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="48157-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48157-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="48157-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48157-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48157-107">DESCRIPTION</span></span>
<span data-ttu-id="48157-108">Exclui um plano de compromisso do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="48157-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="48157-109">Observe que os planos de compromisso que têm associações de compromisso não podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="48157-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="48157-110">As associações de compromisso só podem ser excluídas pelo recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="48157-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="48157-111">Por exemplo, se você excluir um serviço da Web do Azure Machine Learning, a associação de compromisso que associa o serviço Web a um plano de compromisso também será excluída.</span><span class="sxs-lookup"><span data-stu-id="48157-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="48157-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48157-112">EXAMPLES</span></span>

### <span data-ttu-id="48157-113">Exemplo 1: excluir um plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="48157-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="48157-114">OS</span><span class="sxs-lookup"><span data-stu-id="48157-114">PARAMETERS</span></span>

### <span data-ttu-id="48157-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48157-115">-DefaultProfile</span></span>
<span data-ttu-id="48157-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="48157-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48157-117">-Force</span><span class="sxs-lookup"><span data-stu-id="48157-117">-Force</span></span>
<span data-ttu-id="48157-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="48157-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="48157-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="48157-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="48157-120">O objeto de serviço Web do Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="48157-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="48157-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="48157-121">-Name</span></span>
<span data-ttu-id="48157-122">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="48157-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="48157-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48157-123">-ResourceGroupName</span></span>
<span data-ttu-id="48157-124">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="48157-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="48157-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48157-125">-Confirm</span></span>
<span data-ttu-id="48157-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48157-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48157-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48157-127">-WhatIf</span></span>
<span data-ttu-id="48157-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48157-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48157-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48157-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48157-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48157-130">CommonParameters</span></span>
<span data-ttu-id="48157-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48157-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48157-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48157-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48157-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48157-133">INPUTS</span></span>

### <span data-ttu-id="48157-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="48157-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="48157-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48157-135">OUTPUTS</span></span>

### <span data-ttu-id="48157-136">System. void</span><span class="sxs-lookup"><span data-stu-id="48157-136">System.Void</span></span>

## <span data-ttu-id="48157-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48157-137">NOTES</span></span>
<span data-ttu-id="48157-138">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="48157-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="48157-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48157-139">RELATED LINKS</span></span>
