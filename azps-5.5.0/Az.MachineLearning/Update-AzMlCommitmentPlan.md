---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114784"
---
# <span data-ttu-id="dc0ac-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dc0ac-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="dc0ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0ac-103">Atualiza as propriedades de um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="dc0ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc0ac-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc0ac-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc0ac-105">DESCRIPTION</span></span>
<span data-ttu-id="dc0ac-106">Atualiza um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="dc0ac-107">Observe que a maioria das propriedades do plano de compromisso é imutável e não pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="dc0ac-108">As propriedades que podem ser modificadas incluem SKU (permitindo que você migre o plano de compromisso de uma SKU para outra) e Marcas.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="dc0ac-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc0ac-109">EXAMPLES</span></span>

### <span data-ttu-id="dc0ac-110">Exemplo 1: Atualizar um plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="dc0ac-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="dc0ac-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc0ac-111">PARAMETERS</span></span>

### <span data-ttu-id="dc0ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0ac-112">-DefaultProfile</span></span>
<span data-ttu-id="dc0ac-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dc0ac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc0ac-114">-Forçar</span><span class="sxs-lookup"><span data-stu-id="dc0ac-114">-Force</span></span>
<span data-ttu-id="dc0ac-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dc0ac-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc0ac-116">-Name</span></span>
<span data-ttu-id="dc0ac-117">O nome do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dc0ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc0ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="dc0ac-119">O nome do grupo de recursos do plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dc0ac-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="dc0ac-120">-SkuCapacity</span></span>
<span data-ttu-id="dc0ac-121">A capacidade da SKU de usar ao atualizar o plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dc0ac-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dc0ac-122">-SkuName</span></span>
<span data-ttu-id="dc0ac-123">O nome da SKU a ser usada ao atualizar o plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dc0ac-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="dc0ac-124">-SkuTier</span></span>
<span data-ttu-id="dc0ac-125">O nível da SKU a ser usada ao atualizar o plano de compromisso ML do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dc0ac-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc0ac-126">-Tag</span></span>
<span data-ttu-id="dc0ac-127">Marcas para o recurso de plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc0ac-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="dc0ac-128">-Confirm</span></span>
<span data-ttu-id="dc0ac-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc0ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc0ac-130">-WhatIf</span></span>
<span data-ttu-id="dc0ac-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc0ac-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc0ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0ac-133">CommonParameters</span></span>
<span data-ttu-id="dc0ac-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0ac-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc0ac-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0ac-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="dc0ac-136">INPUTS</span></span>

### <span data-ttu-id="dc0ac-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dc0ac-137">None</span></span>

## <span data-ttu-id="dc0ac-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="dc0ac-138">OUTPUTS</span></span>

### <span data-ttu-id="dc0ac-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dc0ac-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="dc0ac-140">Notas</span><span class="sxs-lookup"><span data-stu-id="dc0ac-140">NOTES</span></span>
<span data-ttu-id="dc0ac-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="dc0ac-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dc0ac-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc0ac-142">RELATED LINKS</span></span>
