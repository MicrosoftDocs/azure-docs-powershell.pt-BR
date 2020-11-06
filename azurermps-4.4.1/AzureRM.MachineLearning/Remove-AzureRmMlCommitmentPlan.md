---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 31678552a43951406d18c49ee80ffaa7897fd1d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611101"
---
# <span data-ttu-id="dfb6c-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dfb6c-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="dfb6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb6c-103">Exclui um plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfb6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfb6c-104">SYNTAX</span></span>

### <span data-ttu-id="dfb6c-105">Remover um plano de compromisso do Azure ML especificado por nome e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-105">Remove an Azure ML commitment plan specified by name and resource group.</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfb6c-106">Remover um plano de compromisso do Azure ML especificado como um objeto.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-106">Remove an Azure ML commitment plan specified as an object.</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfb6c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfb6c-107">DESCRIPTION</span></span>
<span data-ttu-id="dfb6c-108">Exclui um plano de compromisso do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="dfb6c-109">Observe que os planos de compromisso que têm associações de compromisso não podem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="dfb6c-110">As associações de compromisso só podem ser excluídas pelo recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="dfb6c-111">Por exemplo, se você excluir um serviço da Web do Azure Machine Learning, a associação de compromisso que associa o serviço Web a um plano de compromisso também será excluída.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="dfb6c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfb6c-112">EXAMPLES</span></span>

### <span data-ttu-id="dfb6c-113">--------------------------Exemplo 1: excluir um plano de compromisso--------------------------</span><span class="sxs-lookup"><span data-stu-id="dfb6c-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
<span data-ttu-id="dfb6c-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dfb6c-114">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="dfb6c-115">OS</span><span class="sxs-lookup"><span data-stu-id="dfb6c-115">PARAMETERS</span></span>

### <span data-ttu-id="dfb6c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dfb6c-116">-Force</span></span>
<span data-ttu-id="dfb6c-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dfb6c-118">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dfb6c-118">-MlCommitmentPlan</span></span>
<span data-ttu-id="dfb6c-119">O objeto de serviço Web do Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-119">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: Remove an Azure ML commitment plan specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfb6c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfb6c-120">-Name</span></span>
<span data-ttu-id="dfb6c-121">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="dfb6c-123">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb6c-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfb6c-124">-Confirm</span></span>
<span data-ttu-id="dfb6c-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb6c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb6c-126">-WhatIf</span></span>
<span data-ttu-id="dfb6c-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfb6c-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb6c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb6c-129">-DefaultProfile</span></span>
<span data-ttu-id="dfb6c-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfb6c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb6c-131">CommonParameters</span></span>
<span data-ttu-id="dfb6c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb6c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb6c-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb6c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb6c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfb6c-134">INPUTS</span></span>

### <span data-ttu-id="dfb6c-135">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dfb6c-135">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="dfb6c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfb6c-136">OUTPUTS</span></span>

### <span data-ttu-id="dfb6c-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dfb6c-137">None</span></span>

## <span data-ttu-id="dfb6c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfb6c-138">NOTES</span></span>
<span data-ttu-id="dfb6c-139">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="dfb6c-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dfb6c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfb6c-140">RELATED LINKS</span></span>

