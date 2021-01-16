---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272729"
---
# <span data-ttu-id="28ff7-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="28ff7-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="28ff7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="28ff7-103">Recupera as informações resumidas para uma ou mais associações de compromisso.</span><span class="sxs-lookup"><span data-stu-id="28ff7-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="28ff7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28ff7-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ff7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="28ff7-106">Recupera informações de associação de compromisso.</span><span class="sxs-lookup"><span data-stu-id="28ff7-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="28ff7-107">Dependendo dos parâmetros passados, o cmdlet retorna uma associação de compromisso específica ou uma coleção de associações de compromisso para o plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="28ff7-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="28ff7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28ff7-108">EXAMPLES</span></span>

### <span data-ttu-id="28ff7-109">Exemplo 1: obter uma associação de compromisso específica</span><span class="sxs-lookup"><span data-stu-id="28ff7-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="28ff7-110">Exemplo 2: obter todas as associações de compromisso para o plano de compromisso especificado</span><span class="sxs-lookup"><span data-stu-id="28ff7-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="28ff7-111">OS</span><span class="sxs-lookup"><span data-stu-id="28ff7-111">PARAMETERS</span></span>

### <span data-ttu-id="28ff7-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="28ff7-112">-CommitmentPlanName</span></span>
<span data-ttu-id="28ff7-113">O nome do plano de compromisso do Azure ML que tem uma ou mais associações de compromisso.</span><span class="sxs-lookup"><span data-stu-id="28ff7-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="28ff7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ff7-114">-DefaultProfile</span></span>
<span data-ttu-id="28ff7-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="28ff7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28ff7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="28ff7-116">-Name</span></span>
<span data-ttu-id="28ff7-117">O nome da Associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="28ff7-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="28ff7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ff7-118">-ResourceGroupName</span></span>
<span data-ttu-id="28ff7-119">O nome do grupo de recursos para a associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="28ff7-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="28ff7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ff7-120">CommonParameters</span></span>
<span data-ttu-id="28ff7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ff7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ff7-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ff7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ff7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28ff7-123">INPUTS</span></span>

### <span data-ttu-id="28ff7-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="28ff7-124">None</span></span>

## <span data-ttu-id="28ff7-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28ff7-125">OUTPUTS</span></span>

### <span data-ttu-id="28ff7-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="28ff7-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="28ff7-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28ff7-127">NOTES</span></span>
<span data-ttu-id="28ff7-128">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="28ff7-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="28ff7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28ff7-129">RELATED LINKS</span></span>
