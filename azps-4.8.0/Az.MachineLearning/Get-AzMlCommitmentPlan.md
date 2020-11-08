---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111671"
---
# <span data-ttu-id="abd41-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="abd41-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="abd41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abd41-102">SYNOPSIS</span></span>
<span data-ttu-id="abd41-103">Recupera as informações resumidas para um ou mais planos de compromisso.</span><span class="sxs-lookup"><span data-stu-id="abd41-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="abd41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abd41-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abd41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abd41-105">DESCRIPTION</span></span>
<span data-ttu-id="abd41-106">Recupera informações do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="abd41-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="abd41-107">Dependendo dos parâmetros passados, o cmdlet retorna um plano de compromisso específico, uma coleção de planos de compromisso para um grupo de recursos especificado dentro da assinatura atual ou um conjunto de planos de compromisso dentro da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="abd41-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="abd41-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abd41-108">EXAMPLES</span></span>

### <span data-ttu-id="abd41-109">Exemplo 1: obter um plano de compromisso específico</span><span class="sxs-lookup"><span data-stu-id="abd41-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="abd41-110">Exemplo 2: obter todos os recursos de plano de compromisso na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="abd41-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="abd41-111">Exemplo 3: obter todos os planos de compromisso na assinatura atual e o grupo de recursos fornecido</span><span class="sxs-lookup"><span data-stu-id="abd41-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="abd41-112">OS</span><span class="sxs-lookup"><span data-stu-id="abd41-112">PARAMETERS</span></span>

### <span data-ttu-id="abd41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd41-113">-DefaultProfile</span></span>
<span data-ttu-id="abd41-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="abd41-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abd41-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="abd41-115">-Name</span></span>
<span data-ttu-id="abd41-116">O nome do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="abd41-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="abd41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd41-117">-ResourceGroupName</span></span>
<span data-ttu-id="abd41-118">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="abd41-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="abd41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd41-119">CommonParameters</span></span>
<span data-ttu-id="abd41-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd41-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd41-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd41-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abd41-122">INPUTS</span></span>

### <span data-ttu-id="abd41-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="abd41-123">None</span></span>

## <span data-ttu-id="abd41-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abd41-124">OUTPUTS</span></span>

### <span data-ttu-id="abd41-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="abd41-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="abd41-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abd41-126">NOTES</span></span>
<span data-ttu-id="abd41-127">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="abd41-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="abd41-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abd41-128">RELATED LINKS</span></span>
