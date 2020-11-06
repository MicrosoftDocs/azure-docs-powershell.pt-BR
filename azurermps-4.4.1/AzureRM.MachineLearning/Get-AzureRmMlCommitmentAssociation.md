---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 63c0184b9104b939073c4d58313777e8940d0f93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432205"
---
# <span data-ttu-id="7cdc8-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="7cdc8-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="7cdc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7cdc8-103">Recupera as informações resumidas para uma ou mais associações de compromisso.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cdc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7cdc8-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cdc8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7cdc8-105">DESCRIPTION</span></span>
<span data-ttu-id="7cdc8-106">Recupera informações de associação de compromisso.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="7cdc8-107">Dependendo dos cmdlets passados, o cmdlet retorna uma associação de compromisso específica ou uma coleção de associações de compromisso para o plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="7cdc8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cdc8-108">EXAMPLES</span></span>

### <span data-ttu-id="7cdc8-109">--------------------------Exemplo 1: obter uma associação de compromisso específica--------------------------</span><span class="sxs-lookup"><span data-stu-id="7cdc8-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
<span data-ttu-id="7cdc8-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7cdc8-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="7cdc8-111">--------------------------Exemplo 2: obter todas as associações de compromisso para o plano de compromisso especificado--------------------------</span><span class="sxs-lookup"><span data-stu-id="7cdc8-111">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
<span data-ttu-id="7cdc8-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7cdc8-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="7cdc8-113">OS</span><span class="sxs-lookup"><span data-stu-id="7cdc8-113">PARAMETERS</span></span>

### <span data-ttu-id="7cdc8-114">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="7cdc8-114">-CommitmentPlanName</span></span>
<span data-ttu-id="7cdc8-115">O nome do plano de compromisso do Azure ML que tem uma ou mais associações de compromisso.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-115">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="7cdc8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cdc8-116">-Name</span></span>
<span data-ttu-id="7cdc8-117">O nome da Associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7cdc8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cdc8-118">-ResourceGroupName</span></span>
<span data-ttu-id="7cdc8-119">O nome do grupo de recursos para a associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7cdc8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cdc8-120">-DefaultProfile</span></span>
<span data-ttu-id="7cdc8-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cdc8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdc8-122">CommonParameters</span></span>
<span data-ttu-id="7cdc8-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cdc8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cdc8-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cdc8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdc8-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7cdc8-125">INPUTS</span></span>

## <span data-ttu-id="7cdc8-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7cdc8-126">OUTPUTS</span></span>

### <span data-ttu-id="7cdc8-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7cdc8-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="7cdc8-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="7cdc8-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="7cdc8-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7cdc8-129">NOTES</span></span>
<span data-ttu-id="7cdc8-130">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7cdc8-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7cdc8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cdc8-131">RELATED LINKS</span></span>

