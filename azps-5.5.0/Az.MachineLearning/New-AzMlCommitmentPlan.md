---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118452"
---
# <span data-ttu-id="a5249-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a5249-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="a5249-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5249-102">SYNOPSIS</span></span>
<span data-ttu-id="a5249-103">Cria um novo plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="a5249-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="a5249-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5249-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5249-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a5249-105">DESCRIPTION</span></span>
<span data-ttu-id="a5249-106">Cria um plano de compromisso do Azure Machine Learning em um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="a5249-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="a5249-107">Se houver um plano de compromisso com o mesmo nome no grupo de recursos, a chamada atuará como uma operação de atualização e o plano de compromisso existente será substituído.</span><span class="sxs-lookup"><span data-stu-id="a5249-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="a5249-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5249-108">EXAMPLES</span></span>

### <span data-ttu-id="a5249-109">Exemplo 1: Criar um novo plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="a5249-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="a5249-110">Cria um novo plano de compromisso do Azure Machine Learning chamado "MyCommitmentPlanName" no grupo "MyResourceGroup" e região do Centro Sul dos EUA.</span><span class="sxs-lookup"><span data-stu-id="a5249-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="a5249-111">Neste exemplo, o Teste/Padrão de Desenvolvimento da SKU é usado, o que significa que os recursos fornecidos pelo plano de compromisso serão definidos pelos limites de Teste de Desenvolvimento/Padrão.</span><span class="sxs-lookup"><span data-stu-id="a5249-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="a5249-112">A SkuCapacity neste exemplo é 1, o que significa que o custo do plano será 1x o custo do DevTest, e os recursos que o plano contém serão 1x o que o DevTest fornece.</span><span class="sxs-lookup"><span data-stu-id="a5249-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="a5249-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5249-113">PARAMETERS</span></span>

### <span data-ttu-id="a5249-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5249-114">-DefaultProfile</span></span>
<span data-ttu-id="a5249-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a5249-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5249-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a5249-116">-Force</span></span>
<span data-ttu-id="a5249-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="a5249-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a5249-118">-Local</span><span class="sxs-lookup"><span data-stu-id="a5249-118">-Location</span></span>
<span data-ttu-id="a5249-119">A localização do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5249-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a5249-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5249-120">-Name</span></span>
<span data-ttu-id="a5249-121">O nome do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5249-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a5249-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5249-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5249-123">O nome do grupo de recursos do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5249-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a5249-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a5249-124">-SkuCapacity</span></span>
<span data-ttu-id="a5249-125">A capacidade da SKU de usar ao provisionar o plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5249-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a5249-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a5249-126">-SkuName</span></span>
<span data-ttu-id="a5249-127">O nome da SKU a ser usada ao provisionar o plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5249-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a5249-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a5249-128">-SkuTier</span></span>
<span data-ttu-id="a5249-129">O nível da SKU a ser usado ao provisionar o plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="a5249-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="a5249-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a5249-130">-Confirm</span></span>
<span data-ttu-id="a5249-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5249-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5249-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5249-132">-WhatIf</span></span>
<span data-ttu-id="a5249-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a5249-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5249-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5249-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5249-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5249-135">CommonParameters</span></span>
<span data-ttu-id="a5249-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5249-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5249-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5249-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5249-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a5249-138">INPUTS</span></span>

### <span data-ttu-id="a5249-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a5249-139">None</span></span>

## <span data-ttu-id="a5249-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="a5249-140">OUTPUTS</span></span>

### <span data-ttu-id="a5249-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a5249-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="a5249-142">Notas</span><span class="sxs-lookup"><span data-stu-id="a5249-142">NOTES</span></span>
<span data-ttu-id="a5249-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="a5249-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a5249-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5249-144">RELATED LINKS</span></span>
