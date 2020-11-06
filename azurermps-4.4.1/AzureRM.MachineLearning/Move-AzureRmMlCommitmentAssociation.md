---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441028"
---
# <span data-ttu-id="791af-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="791af-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="791af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="791af-102">SYNOPSIS</span></span>
<span data-ttu-id="791af-103">Move uma associação de compromisso de um plano de compromisso para outro.</span><span class="sxs-lookup"><span data-stu-id="791af-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="791af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="791af-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="791af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="791af-105">DESCRIPTION</span></span>
<span data-ttu-id="791af-106">Move um recurso de associação de compromisso de seu plano de compromisso pai para outro plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="791af-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="791af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="791af-107">EXAMPLES</span></span>

### <span data-ttu-id="791af-108">--------------------------Exemplo 1: mover uma associação de compromisso--------------------------</span><span class="sxs-lookup"><span data-stu-id="791af-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="791af-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="791af-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="791af-110">OS</span><span class="sxs-lookup"><span data-stu-id="791af-110">PARAMETERS</span></span>

### <span data-ttu-id="791af-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="791af-111">-CommitmentPlanName</span></span>
<span data-ttu-id="791af-112">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="791af-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="791af-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="791af-113">-DestinationPlanId</span></span>
<span data-ttu-id="791af-114">A ID de recurso do Azure do plano de compromisso do Azure ML de destino.</span><span class="sxs-lookup"><span data-stu-id="791af-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="791af-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="791af-115">-Name</span></span>
<span data-ttu-id="791af-116">O nome da Associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="791af-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="791af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791af-117">-ResourceGroupName</span></span>
<span data-ttu-id="791af-118">O nome do grupo de recursos para a associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="791af-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="791af-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="791af-119">-Confirm</span></span>
<span data-ttu-id="791af-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="791af-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="791af-121">-WhatIf</span></span>
<span data-ttu-id="791af-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="791af-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="791af-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="791af-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791af-124">-DefaultProfile</span></span>
<span data-ttu-id="791af-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="791af-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="791af-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791af-126">CommonParameters</span></span>
<span data-ttu-id="791af-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="791af-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791af-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791af-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791af-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="791af-129">INPUTS</span></span>

## <span data-ttu-id="791af-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="791af-130">OUTPUTS</span></span>

### <span data-ttu-id="791af-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="791af-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="791af-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="791af-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="791af-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="791af-133">NOTES</span></span>
<span data-ttu-id="791af-134">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="791af-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="791af-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="791af-135">RELATED LINKS</span></span>

