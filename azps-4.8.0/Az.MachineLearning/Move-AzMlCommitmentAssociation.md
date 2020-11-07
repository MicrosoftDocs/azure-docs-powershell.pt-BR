---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948193"
---
# <span data-ttu-id="7c357-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="7c357-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="7c357-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c357-102">SYNOPSIS</span></span>
<span data-ttu-id="7c357-103">Move uma associação de compromisso de um plano de compromisso para outro.</span><span class="sxs-lookup"><span data-stu-id="7c357-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="7c357-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c357-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c357-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c357-105">DESCRIPTION</span></span>
<span data-ttu-id="7c357-106">Move um recurso de associação de compromisso de seu plano de compromisso pai para outro plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="7c357-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="7c357-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c357-107">EXAMPLES</span></span>

### <span data-ttu-id="7c357-108">Exemplo 1: mover uma associação de compromisso</span><span class="sxs-lookup"><span data-stu-id="7c357-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="7c357-109">OS</span><span class="sxs-lookup"><span data-stu-id="7c357-109">PARAMETERS</span></span>

### <span data-ttu-id="7c357-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="7c357-110">-CommitmentPlanName</span></span>
<span data-ttu-id="7c357-111">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7c357-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7c357-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c357-112">-DefaultProfile</span></span>
<span data-ttu-id="7c357-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7c357-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c357-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="7c357-114">-DestinationPlanId</span></span>
<span data-ttu-id="7c357-115">A ID de recurso do Azure do plano de compromisso do Azure ML de destino.</span><span class="sxs-lookup"><span data-stu-id="7c357-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="7c357-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c357-116">-Name</span></span>
<span data-ttu-id="7c357-117">O nome da Associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7c357-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7c357-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c357-118">-ResourceGroupName</span></span>
<span data-ttu-id="7c357-119">O nome do grupo de recursos para a associação de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="7c357-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="7c357-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c357-120">-Confirm</span></span>
<span data-ttu-id="7c357-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c357-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c357-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c357-122">-WhatIf</span></span>
<span data-ttu-id="7c357-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c357-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c357-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c357-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c357-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c357-125">CommonParameters</span></span>
<span data-ttu-id="7c357-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c357-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c357-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c357-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c357-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c357-128">INPUTS</span></span>

### <span data-ttu-id="7c357-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7c357-129">None</span></span>

## <span data-ttu-id="7c357-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c357-130">OUTPUTS</span></span>

### <span data-ttu-id="7c357-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7c357-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="7c357-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c357-132">NOTES</span></span>
<span data-ttu-id="7c357-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7c357-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7c357-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c357-134">RELATED LINKS</span></span>
