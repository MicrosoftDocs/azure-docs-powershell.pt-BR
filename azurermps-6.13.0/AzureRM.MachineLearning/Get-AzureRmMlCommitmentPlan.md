---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: f0b081911d1bcd2a2b195d3185eb3b36505060c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602716"
---
# <span data-ttu-id="7b636-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7b636-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="7b636-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b636-102">SYNOPSIS</span></span>
<span data-ttu-id="7b636-103">Recupera as informações resumidas para um ou mais planos de compromisso.</span><span class="sxs-lookup"><span data-stu-id="7b636-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b636-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b636-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b636-105">DESCRIPTION</span></span>
<span data-ttu-id="7b636-106">Recupera informações do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="7b636-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="7b636-107">Dependendo dos canceladores passados, o cmdlet retorna um plano de compromisso específico, uma coleção de planos de compromisso para um grupo de recursos especificado na assinatura atual ou um conjunto de planos de compromisso dentro da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="7b636-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="7b636-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b636-108">EXAMPLES</span></span>

### <span data-ttu-id="7b636-109">Exemplo 1: obter um plano de compromisso específico</span><span class="sxs-lookup"><span data-stu-id="7b636-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="7b636-110">Exemplo 2: obter todos os recursos de plano de compromisso na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="7b636-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="7b636-111">Exemplo 3: obter todos os planos de compromisso na assinatura atual e o grupo de recursos fornecido</span><span class="sxs-lookup"><span data-stu-id="7b636-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="7b636-112">OS</span><span class="sxs-lookup"><span data-stu-id="7b636-112">PARAMETERS</span></span>

### <span data-ttu-id="7b636-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b636-113">-DefaultProfile</span></span>
<span data-ttu-id="7b636-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7b636-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b636-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b636-115">-Name</span></span>
<span data-ttu-id="7b636-116">O nome do plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="7b636-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="7b636-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b636-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b636-118">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7b636-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7b636-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b636-119">CommonParameters</span></span>
<span data-ttu-id="7b636-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b636-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b636-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b636-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b636-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b636-122">INPUTS</span></span>

### <span data-ttu-id="7b636-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7b636-123">None</span></span>

## <span data-ttu-id="7b636-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b636-124">OUTPUTS</span></span>

### <span data-ttu-id="7b636-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7b636-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="7b636-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b636-126">NOTES</span></span>
<span data-ttu-id="7b636-127">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7b636-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7b636-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b636-128">RELATED LINKS</span></span>
