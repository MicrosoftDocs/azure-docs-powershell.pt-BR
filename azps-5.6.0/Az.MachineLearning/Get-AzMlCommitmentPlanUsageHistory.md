---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 8baf0e2af5ebc06e51c0f8b588fe04ff3106f892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892855"
---
# <span data-ttu-id="2dc8d-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="2dc8d-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="2dc8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc8d-103">Recupera informações de histórico de uso para um plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="2dc8d-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="2dc8d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2dc8d-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc8d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2dc8d-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc8d-106">Recupera informações de histórico de uso para um plano de compromisso especificado, incluindo recursos usados e recursos restantes dentro do plano.</span><span class="sxs-lookup"><span data-stu-id="2dc8d-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="2dc8d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dc8d-107">EXAMPLES</span></span>

### <span data-ttu-id="2dc8d-108">Exemplo 1: obter histórico de uso para um plano de compromisso específico</span><span class="sxs-lookup"><span data-stu-id="2dc8d-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="2dc8d-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2dc8d-109">PARAMETERS</span></span>

### <span data-ttu-id="2dc8d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc8d-110">-DefaultProfile</span></span>
<span data-ttu-id="2dc8d-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2dc8d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dc8d-112">-Name</span><span class="sxs-lookup"><span data-stu-id="2dc8d-112">-Name</span></span>
<span data-ttu-id="2dc8d-113">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="2dc8d-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2dc8d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc8d-114">-ResourceGroupName</span></span>
<span data-ttu-id="2dc8d-115">O nome do grupo de recursos do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="2dc8d-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2dc8d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc8d-116">CommonParameters</span></span>
<span data-ttu-id="2dc8d-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc8d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc8d-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc8d-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc8d-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dc8d-119">INPUTS</span></span>

### <span data-ttu-id="2dc8d-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2dc8d-120">None</span></span>

## <span data-ttu-id="2dc8d-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2dc8d-121">OUTPUTS</span></span>

### <span data-ttu-id="2dc8d-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="2dc8d-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="2dc8d-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="2dc8d-123">NOTES</span></span>
<span data-ttu-id="2dc8d-124">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2dc8d-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2dc8d-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dc8d-125">RELATED LINKS</span></span>
