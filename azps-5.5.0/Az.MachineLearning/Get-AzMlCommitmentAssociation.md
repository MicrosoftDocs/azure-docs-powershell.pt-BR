---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115259"
---
# <span data-ttu-id="be91f-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="be91f-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="be91f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be91f-102">SYNOPSIS</span></span>
<span data-ttu-id="be91f-103">Recupera as informações de resumo de uma ou mais associações de compromisso.</span><span class="sxs-lookup"><span data-stu-id="be91f-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="be91f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be91f-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be91f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="be91f-105">DESCRIPTION</span></span>
<span data-ttu-id="be91f-106">Recupera informações de associação de compromisso.</span><span class="sxs-lookup"><span data-stu-id="be91f-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="be91f-107">Dependendo dos parâmetros passados, o cmdlet retorna uma associação de compromisso específica ou um conjunto de associações de compromisso para o plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="be91f-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="be91f-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be91f-108">EXAMPLES</span></span>

### <span data-ttu-id="be91f-109">Exemplo 1: Obter uma associação de compromisso específica</span><span class="sxs-lookup"><span data-stu-id="be91f-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="be91f-110">Exemplo 2: Obter todas as associações de compromisso para o plano de compromisso especificado</span><span class="sxs-lookup"><span data-stu-id="be91f-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="be91f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be91f-111">PARAMETERS</span></span>

### <span data-ttu-id="be91f-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="be91f-112">-CommitmentPlanName</span></span>
<span data-ttu-id="be91f-113">O nome do plano de compromisso ML do Azure, que tem uma ou mais associações de compromisso.</span><span class="sxs-lookup"><span data-stu-id="be91f-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="be91f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be91f-114">-DefaultProfile</span></span>
<span data-ttu-id="be91f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="be91f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be91f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="be91f-116">-Name</span></span>
<span data-ttu-id="be91f-117">O nome da associação de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="be91f-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="be91f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be91f-118">-ResourceGroupName</span></span>
<span data-ttu-id="be91f-119">O nome do grupo de recursos da associação de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="be91f-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="be91f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be91f-120">CommonParameters</span></span>
<span data-ttu-id="be91f-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be91f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be91f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be91f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be91f-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="be91f-123">INPUTS</span></span>

### <span data-ttu-id="be91f-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="be91f-124">None</span></span>

## <span data-ttu-id="be91f-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="be91f-125">OUTPUTS</span></span>

### <span data-ttu-id="be91f-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="be91f-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="be91f-127">Notas</span><span class="sxs-lookup"><span data-stu-id="be91f-127">NOTES</span></span>
<span data-ttu-id="be91f-128">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="be91f-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="be91f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be91f-129">RELATED LINKS</span></span>
