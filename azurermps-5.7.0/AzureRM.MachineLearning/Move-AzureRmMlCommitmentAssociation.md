---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441330"
---
# <span data-ttu-id="6e709-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="6e709-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="6e709-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e709-102">SYNOPSIS</span></span>
<span data-ttu-id="6e709-103">Move uma associação de compromisso de um plano de compromisso para outro.</span><span class="sxs-lookup"><span data-stu-id="6e709-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e709-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e709-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e709-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e709-105">DESCRIPTION</span></span>
<span data-ttu-id="6e709-106">Move um recurso de associação de compromisso de seu plano de compromisso pai para outro plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="6e709-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="6e709-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e709-107">EXAMPLES</span></span>

### <span data-ttu-id="6e709-108">--------------------------Exemplo 1: mover uma associação de compromisso--------------------------</span><span class="sxs-lookup"><span data-stu-id="6e709-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="6e709-109">OS</span><span class="sxs-lookup"><span data-stu-id="6e709-109">PARAMETERS</span></span>

### <span data-ttu-id="6e709-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="6e709-110">-CommitmentPlanName</span></span>
<span data-ttu-id="6e709-111">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6e709-111">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e709-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e709-112">-DefaultProfile</span></span>
<span data-ttu-id="6e709-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6e709-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e709-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="6e709-114">-DestinationPlanId</span></span>
<span data-ttu-id="6e709-115">A ID de recurso do Azure do plano de compromisso do Azure ML de destino.</span><span class="sxs-lookup"><span data-stu-id="6e709-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e709-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e709-116">-Name</span></span>
<span data-ttu-id="6e709-117">O nome da Associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6e709-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e709-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e709-118">-ResourceGroupName</span></span>
<span data-ttu-id="6e709-119">O nome do grupo de recursos para a associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6e709-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e709-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e709-120">-Confirm</span></span>
<span data-ttu-id="6e709-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e709-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e709-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e709-122">-WhatIf</span></span>
<span data-ttu-id="6e709-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e709-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e709-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e709-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e709-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e709-125">CommonParameters</span></span>
<span data-ttu-id="6e709-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e709-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e709-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e709-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e709-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e709-128">INPUTS</span></span>

### <span data-ttu-id="6e709-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6e709-129">None</span></span>
<span data-ttu-id="6e709-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6e709-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e709-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e709-131">OUTPUTS</span></span>

### <span data-ttu-id="6e709-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6e709-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="6e709-133">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="6e709-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="6e709-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e709-134">NOTES</span></span>
<span data-ttu-id="6e709-135">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6e709-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6e709-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e709-136">RELATED LINKS</span></span>

