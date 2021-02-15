---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114786"
---
# <span data-ttu-id="91c3d-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="91c3d-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="91c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="91c3d-103">Move uma associação de compromisso de um plano de compromisso para outro.</span><span class="sxs-lookup"><span data-stu-id="91c3d-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="91c3d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91c3d-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91c3d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="91c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="91c3d-106">Move um recurso de associação de compromisso de seu plano de compromisso pai para outro plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="91c3d-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="91c3d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="91c3d-108">Exemplo 1: Mover uma associação de compromisso</span><span class="sxs-lookup"><span data-stu-id="91c3d-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="91c3d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91c3d-109">PARAMETERS</span></span>

### <span data-ttu-id="91c3d-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="91c3d-110">-CommitmentPlanName</span></span>
<span data-ttu-id="91c3d-111">O nome do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="91c3d-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="91c3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c3d-112">-DefaultProfile</span></span>
<span data-ttu-id="91c3d-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="91c3d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91c3d-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="91c3d-114">-DestinationPlanId</span></span>
<span data-ttu-id="91c3d-115">A ID de recurso do Azure do plano de compromisso Azure ML de destino.</span><span class="sxs-lookup"><span data-stu-id="91c3d-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="91c3d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="91c3d-116">-Name</span></span>
<span data-ttu-id="91c3d-117">O nome da associação de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="91c3d-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="91c3d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c3d-118">-ResourceGroupName</span></span>
<span data-ttu-id="91c3d-119">O nome do grupo de recursos da associação de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="91c3d-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="91c3d-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="91c3d-120">-Confirm</span></span>
<span data-ttu-id="91c3d-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c3d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c3d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c3d-122">-WhatIf</span></span>
<span data-ttu-id="91c3d-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="91c3d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91c3d-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91c3d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c3d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c3d-125">CommonParameters</span></span>
<span data-ttu-id="91c3d-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c3d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c3d-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c3d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c3d-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="91c3d-128">INPUTS</span></span>

### <span data-ttu-id="91c3d-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="91c3d-129">None</span></span>

## <span data-ttu-id="91c3d-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="91c3d-130">OUTPUTS</span></span>

### <span data-ttu-id="91c3d-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="91c3d-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="91c3d-132">Notas</span><span class="sxs-lookup"><span data-stu-id="91c3d-132">NOTES</span></span>
<span data-ttu-id="91c3d-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="91c3d-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="91c3d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91c3d-134">RELATED LINKS</span></span>
