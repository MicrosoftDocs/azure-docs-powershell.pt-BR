---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111802"
---
# <span data-ttu-id="0a33f-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0a33f-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="0a33f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a33f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a33f-103">Recupera as informações de resumo de um ou mais planos de compromisso.</span><span class="sxs-lookup"><span data-stu-id="0a33f-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="0a33f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a33f-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a33f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a33f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a33f-106">Recupera informações do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="0a33f-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="0a33f-107">Dependendo dos parâmetros passados, o cmdlet retorna um plano de compromisso específico, um conjunto de planos de compromisso para um grupo de recursos especificado dentro da assinatura atual ou um conjunto de planos de compromisso dentro da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0a33f-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="0a33f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a33f-108">EXAMPLES</span></span>

### <span data-ttu-id="0a33f-109">Exemplo 1: Obter um plano de compromisso específico</span><span class="sxs-lookup"><span data-stu-id="0a33f-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="0a33f-110">Exemplo 2: Obter todos os recursos do plano de compromisso na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="0a33f-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="0a33f-111">Exemplo 3: Obter todos os planos de compromisso na assinatura atual e determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0a33f-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="0a33f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a33f-112">PARAMETERS</span></span>

### <span data-ttu-id="0a33f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a33f-113">-DefaultProfile</span></span>
<span data-ttu-id="0a33f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0a33f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a33f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a33f-115">-Name</span></span>
<span data-ttu-id="0a33f-116">O nome do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="0a33f-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="0a33f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a33f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a33f-118">O nome do grupo de recursos do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="0a33f-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="0a33f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a33f-119">CommonParameters</span></span>
<span data-ttu-id="0a33f-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a33f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a33f-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a33f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a33f-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="0a33f-122">INPUTS</span></span>

### <span data-ttu-id="0a33f-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0a33f-123">None</span></span>

## <span data-ttu-id="0a33f-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="0a33f-124">OUTPUTS</span></span>

### <span data-ttu-id="0a33f-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="0a33f-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="0a33f-126">Notas</span><span class="sxs-lookup"><span data-stu-id="0a33f-126">NOTES</span></span>
<span data-ttu-id="0a33f-127">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0a33f-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0a33f-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a33f-128">RELATED LINKS</span></span>
