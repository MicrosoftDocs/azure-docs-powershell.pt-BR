---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113602"
---
# <span data-ttu-id="6a8fb-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="6a8fb-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="6a8fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8fb-103">Recupera informações do histórico de uso para um plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="6a8fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a8fb-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8fb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a8fb-105">DESCRIPTION</span></span>
<span data-ttu-id="6a8fb-106">Recupera informações do histórico de uso para um plano de compromisso especificado, incluindo os recursos usados e os recursos restantes dentro do plano.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="6a8fb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a8fb-107">EXAMPLES</span></span>

### <span data-ttu-id="6a8fb-108">Exemplo 1: Obter histórico de uso para um plano de compromisso específico</span><span class="sxs-lookup"><span data-stu-id="6a8fb-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="6a8fb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a8fb-109">PARAMETERS</span></span>

### <span data-ttu-id="6a8fb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8fb-110">-DefaultProfile</span></span>
<span data-ttu-id="6a8fb-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6a8fb-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a8fb-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a8fb-112">-Name</span></span>
<span data-ttu-id="6a8fb-113">O nome do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6a8fb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8fb-114">-ResourceGroupName</span></span>
<span data-ttu-id="6a8fb-115">O nome do grupo de recursos do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6a8fb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8fb-116">CommonParameters</span></span>
<span data-ttu-id="6a8fb-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8fb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8fb-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a8fb-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8fb-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="6a8fb-119">INPUTS</span></span>

### <span data-ttu-id="6a8fb-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6a8fb-120">None</span></span>

## <span data-ttu-id="6a8fb-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="6a8fb-121">OUTPUTS</span></span>

### <span data-ttu-id="6a8fb-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="6a8fb-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="6a8fb-123">Notas</span><span class="sxs-lookup"><span data-stu-id="6a8fb-123">NOTES</span></span>
<span data-ttu-id="6a8fb-124">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6a8fb-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6a8fb-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a8fb-125">RELATED LINKS</span></span>
