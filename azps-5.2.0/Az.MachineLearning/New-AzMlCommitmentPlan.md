---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260136"
---
# <span data-ttu-id="76684-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="76684-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="76684-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76684-102">SYNOPSIS</span></span>
<span data-ttu-id="76684-103">Cria um novo plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="76684-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="76684-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76684-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76684-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76684-105">DESCRIPTION</span></span>
<span data-ttu-id="76684-106">Cria um plano de compromisso do Azure Machine Learning em um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="76684-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="76684-107">Se um plano de compromisso com o mesmo nome existir no grupo de recursos, a chamada funcionará como uma operação de atualização e o plano de compromisso existente será substituído.</span><span class="sxs-lookup"><span data-stu-id="76684-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="76684-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76684-108">EXAMPLES</span></span>

### <span data-ttu-id="76684-109">Exemplo 1: criar um novo plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="76684-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="76684-110">Cria um novo plano de compromisso do Azure Machine Learning chamado "MyCommitmentPlanName" no grupo "grupo de recursos" e a região do centro-oeste do Sul.</span><span class="sxs-lookup"><span data-stu-id="76684-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="76684-111">Neste exemplo, o DevTest/padrão de SKU é usado, o que significa que os recursos fornecidos pelo plano de compromisso serão definidos pelos limites de DevTest/padrão.</span><span class="sxs-lookup"><span data-stu-id="76684-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="76684-112">O SkuCapacity neste exemplo é 1, o que significa que o custo do plano vai 1x o custo de DevTest, e os recursos que o plano contém serão de 1x o que o DevTest fornece.</span><span class="sxs-lookup"><span data-stu-id="76684-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="76684-113">OS</span><span class="sxs-lookup"><span data-stu-id="76684-113">PARAMETERS</span></span>

### <span data-ttu-id="76684-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76684-114">-DefaultProfile</span></span>
<span data-ttu-id="76684-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="76684-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76684-116">-Force</span><span class="sxs-lookup"><span data-stu-id="76684-116">-Force</span></span>
<span data-ttu-id="76684-117">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="76684-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="76684-118">-Local</span><span class="sxs-lookup"><span data-stu-id="76684-118">-Location</span></span>
<span data-ttu-id="76684-119">O local do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76684-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="76684-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="76684-120">-Name</span></span>
<span data-ttu-id="76684-121">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76684-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="76684-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76684-122">-ResourceGroupName</span></span>
<span data-ttu-id="76684-123">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76684-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="76684-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="76684-124">-SkuCapacity</span></span>
<span data-ttu-id="76684-125">A capacidade da SKU a ser usada ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76684-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="76684-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="76684-126">-SkuName</span></span>
<span data-ttu-id="76684-127">O nome da SKU a ser usada ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76684-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="76684-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="76684-128">-SkuTier</span></span>
<span data-ttu-id="76684-129">A camada da SKU a ser usada ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76684-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="76684-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76684-130">-Confirm</span></span>
<span data-ttu-id="76684-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76684-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76684-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76684-132">-WhatIf</span></span>
<span data-ttu-id="76684-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76684-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76684-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76684-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76684-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76684-135">CommonParameters</span></span>
<span data-ttu-id="76684-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76684-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76684-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76684-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76684-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76684-138">INPUTS</span></span>

### <span data-ttu-id="76684-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="76684-139">None</span></span>

## <span data-ttu-id="76684-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76684-140">OUTPUTS</span></span>

### <span data-ttu-id="76684-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="76684-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="76684-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76684-142">NOTES</span></span>
<span data-ttu-id="76684-143">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="76684-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="76684-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76684-144">RELATED LINKS</span></span>
