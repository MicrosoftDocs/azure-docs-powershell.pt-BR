---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: f5386f3c971159f2a33353efeb380164447ee295
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887976"
---
# <span data-ttu-id="c3f64-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c3f64-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="c3f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3f64-102">SYNOPSIS</span></span>
<span data-ttu-id="c3f64-103">Cria um novo plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="c3f64-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="c3f64-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c3f64-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3f64-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c3f64-105">DESCRIPTION</span></span>
<span data-ttu-id="c3f64-106">Cria um plano de compromisso do Azure Machine Learning em um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="c3f64-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="c3f64-107">Se existir um plano de compromisso com o mesmo nome no grupo de recursos, a chamada atuará como uma operação de atualização e o plano de compromisso existente será substituído.</span><span class="sxs-lookup"><span data-stu-id="c3f64-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="c3f64-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3f64-108">EXAMPLES</span></span>

### <span data-ttu-id="c3f64-109">Exemplo 1: Criar um novo plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="c3f64-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="c3f64-110">Cria um novo plano de compromisso do Azure Machine Learning chamado "MyCommitmentPlanName" no grupo "MyResourceGroup" e região do Centro Sul dos EUA.</span><span class="sxs-lookup"><span data-stu-id="c3f64-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="c3f64-111">Neste exemplo, o SKU DevTest/Standard é usado, ou seja, os recursos fornecidos pelo plano de compromisso serão definidos pelos limites de DevTest/Standard.</span><span class="sxs-lookup"><span data-stu-id="c3f64-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="c3f64-112">A SkuCapacity neste exemplo é 1, o que significa que o custo do plano será 1x o custo de DevTest, e os recursos que o plano contém serão 1x o que o DevTest fornece.</span><span class="sxs-lookup"><span data-stu-id="c3f64-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="c3f64-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c3f64-113">PARAMETERS</span></span>

### <span data-ttu-id="c3f64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3f64-114">-DefaultProfile</span></span>
<span data-ttu-id="c3f64-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c3f64-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3f64-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c3f64-116">-Force</span></span>
<span data-ttu-id="c3f64-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="c3f64-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f64-118">-Location</span><span class="sxs-lookup"><span data-stu-id="c3f64-118">-Location</span></span>
<span data-ttu-id="c3f64-119">O local do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c3f64-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c3f64-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c3f64-120">-Name</span></span>
<span data-ttu-id="c3f64-121">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c3f64-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c3f64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3f64-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3f64-123">O nome do grupo de recursos do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c3f64-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c3f64-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c3f64-124">-SkuCapacity</span></span>
<span data-ttu-id="c3f64-125">A capacidade do SKU a ser usado ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c3f64-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3f64-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c3f64-126">-SkuName</span></span>
<span data-ttu-id="c3f64-127">O nome do SKU a ser usado ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c3f64-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c3f64-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c3f64-128">-SkuTier</span></span>
<span data-ttu-id="c3f64-129">A camada do SKU a ser usada ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="c3f64-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c3f64-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3f64-130">-Confirm</span></span>
<span data-ttu-id="c3f64-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3f64-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3f64-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3f64-132">-WhatIf</span></span>
<span data-ttu-id="c3f64-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3f64-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3f64-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3f64-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3f64-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3f64-135">CommonParameters</span></span>
<span data-ttu-id="c3f64-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3f64-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3f64-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3f64-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3f64-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3f64-138">INPUTS</span></span>

### <span data-ttu-id="c3f64-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c3f64-139">None</span></span>

## <span data-ttu-id="c3f64-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c3f64-140">OUTPUTS</span></span>

### <span data-ttu-id="c3f64-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c3f64-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="c3f64-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="c3f64-142">NOTES</span></span>
<span data-ttu-id="c3f64-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="c3f64-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c3f64-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3f64-144">RELATED LINKS</span></span>
