---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 4d78d6e6a1b0ae5ea9f8815d537bca1496e24bbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770440"
---
# <span data-ttu-id="b5dab-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b5dab-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="b5dab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5dab-102">SYNOPSIS</span></span>
<span data-ttu-id="b5dab-103">Recupera as informações do histórico de uso para um plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="b5dab-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="b5dab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5dab-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5dab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5dab-105">DESCRIPTION</span></span>
<span data-ttu-id="b5dab-106">Recupera as informações do histórico de uso para um plano de compromisso especificado, incluindo recursos usados e recursos restantes no plano.</span><span class="sxs-lookup"><span data-stu-id="b5dab-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="b5dab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5dab-107">EXAMPLES</span></span>

### <span data-ttu-id="b5dab-108">Exemplo 1: obter histórico de uso para um plano de compromisso específico</span><span class="sxs-lookup"><span data-stu-id="b5dab-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="b5dab-109">OS</span><span class="sxs-lookup"><span data-stu-id="b5dab-109">PARAMETERS</span></span>

### <span data-ttu-id="b5dab-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5dab-110">-DefaultProfile</span></span>
<span data-ttu-id="b5dab-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b5dab-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5dab-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5dab-112">-Name</span></span>
<span data-ttu-id="b5dab-113">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b5dab-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dab-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5dab-114">-ResourceGroupName</span></span>
<span data-ttu-id="b5dab-115">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b5dab-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dab-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5dab-116">CommonParameters</span></span>
<span data-ttu-id="b5dab-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5dab-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5dab-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5dab-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5dab-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5dab-119">INPUTS</span></span>

### <span data-ttu-id="b5dab-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b5dab-120">None</span></span>

## <span data-ttu-id="b5dab-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5dab-121">OUTPUTS</span></span>

### <span data-ttu-id="b5dab-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b5dab-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="b5dab-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5dab-123">NOTES</span></span>
<span data-ttu-id="b5dab-124">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b5dab-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b5dab-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5dab-125">RELATED LINKS</span></span>
