---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: b3ea89f2470052a0d5858da199ee5285b3d5ea18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887114"
---
# <span data-ttu-id="12b47-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="12b47-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="12b47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12b47-102">SYNOPSIS</span></span>
<span data-ttu-id="12b47-103">Recupera as informações resumidas de um ou mais planos de compromisso.</span><span class="sxs-lookup"><span data-stu-id="12b47-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="12b47-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12b47-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12b47-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12b47-105">DESCRIPTION</span></span>
<span data-ttu-id="12b47-106">Recupera informações do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="12b47-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="12b47-107">Dependendo dos parâmetros passados, o cmdlet retorna o plano de compromisso específico, uma coleção de planos de compromisso para um grupo de recursos especificado dentro da assinatura atual ou uma coleção de planos de compromisso dentro da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="12b47-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="12b47-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12b47-108">EXAMPLES</span></span>

### <span data-ttu-id="12b47-109">Exemplo 1: Obter um plano de compromisso específico</span><span class="sxs-lookup"><span data-stu-id="12b47-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="12b47-110">Exemplo 2: Obter todos os recursos do plano de compromisso na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="12b47-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="12b47-111">Exemplo 3: Obter todos os planos de compromisso na assinatura atual e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="12b47-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="12b47-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12b47-112">PARAMETERS</span></span>

### <span data-ttu-id="12b47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b47-113">-DefaultProfile</span></span>
<span data-ttu-id="12b47-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="12b47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12b47-115">-Name</span><span class="sxs-lookup"><span data-stu-id="12b47-115">-Name</span></span>
<span data-ttu-id="12b47-116">O nome do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="12b47-116">The name of the commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12b47-117">-ResourceGroupName</span></span>
<span data-ttu-id="12b47-118">O nome do grupo de recursos do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="12b47-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b47-119">CommonParameters</span></span>
<span data-ttu-id="12b47-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b47-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b47-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b47-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12b47-122">INPUTS</span></span>

### <span data-ttu-id="12b47-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="12b47-123">None</span></span>

## <span data-ttu-id="12b47-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12b47-124">OUTPUTS</span></span>

### <span data-ttu-id="12b47-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="12b47-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="12b47-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="12b47-126">NOTES</span></span>
<span data-ttu-id="12b47-127">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="12b47-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="12b47-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12b47-128">RELATED LINKS</span></span>
