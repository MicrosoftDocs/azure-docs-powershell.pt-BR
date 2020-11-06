---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d14baa5382d5d9ffeeac8efd863a17cbad279865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433233"
---
# <span data-ttu-id="a7205-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a7205-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="a7205-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7205-102">SYNOPSIS</span></span>
<span data-ttu-id="a7205-103">Exclui um plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="a7205-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7205-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7205-104">SYNTAX</span></span>

### <span data-ttu-id="a7205-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a7205-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7205-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a7205-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7205-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7205-107">DESCRIPTION</span></span>
<span data-ttu-id="a7205-108">Exclui um plano de compromisso do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="a7205-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="a7205-109">Observe que os planos de compromisso que têm associações de compromisso não podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="a7205-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="a7205-110">As associações de compromisso só podem ser excluídas pelo recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="a7205-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="a7205-111">Por exemplo, se você excluir um serviço da Web do Azure Machine Learning, a associação de compromisso que associa o serviço Web a um plano de compromisso também será excluída.</span><span class="sxs-lookup"><span data-stu-id="a7205-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="a7205-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7205-112">EXAMPLES</span></span>

### <span data-ttu-id="a7205-113">Exemplo 1: excluir um plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="a7205-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="a7205-114">OS</span><span class="sxs-lookup"><span data-stu-id="a7205-114">PARAMETERS</span></span>

### <span data-ttu-id="a7205-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7205-115">-DefaultProfile</span></span>
<span data-ttu-id="a7205-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a7205-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7205-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a7205-117">-Force</span></span>
<span data-ttu-id="a7205-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a7205-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a7205-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a7205-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="a7205-120">O objeto de serviço Web do Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="a7205-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="a7205-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7205-121">-Name</span></span>
<span data-ttu-id="a7205-122">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a7205-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a7205-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7205-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7205-124">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a7205-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a7205-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7205-125">-Confirm</span></span>
<span data-ttu-id="a7205-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7205-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7205-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7205-127">-WhatIf</span></span>
<span data-ttu-id="a7205-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7205-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7205-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7205-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7205-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7205-130">CommonParameters</span></span>
<span data-ttu-id="a7205-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7205-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7205-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7205-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7205-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7205-133">INPUTS</span></span>

### <span data-ttu-id="a7205-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a7205-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="a7205-135">Parâmetros: MlCommitmentPlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7205-135">Parameters: MlCommitmentPlan (ByValue)</span></span>

## <span data-ttu-id="a7205-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7205-136">OUTPUTS</span></span>

### <span data-ttu-id="a7205-137">System. void</span><span class="sxs-lookup"><span data-stu-id="a7205-137">System.Void</span></span>

## <span data-ttu-id="a7205-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7205-138">NOTES</span></span>
<span data-ttu-id="a7205-139">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="a7205-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a7205-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7205-140">RELATED LINKS</span></span>
