---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: c1aa160d7a0773569255f425f3993de0b47d552a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595953"
---
# <span data-ttu-id="f709c-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f709c-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="f709c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f709c-102">SYNOPSIS</span></span>
<span data-ttu-id="f709c-103">Atualiza as propriedades de um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="f709c-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="f709c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f709c-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f709c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f709c-105">DESCRIPTION</span></span>
<span data-ttu-id="f709c-106">Atualiza um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="f709c-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="f709c-107">Observe que a maioria das propriedades do plano de compromisso é imutável e não pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="f709c-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="f709c-108">As propriedades que podem ser modificadas incluem SKU (permitindo que você migre o plano de compromisso de uma SKU para outra) e marcas.</span><span class="sxs-lookup"><span data-stu-id="f709c-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="f709c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f709c-109">EXAMPLES</span></span>

### <span data-ttu-id="f709c-110">Exemplo 1: atualizar um plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="f709c-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="f709c-111">OS</span><span class="sxs-lookup"><span data-stu-id="f709c-111">PARAMETERS</span></span>

### <span data-ttu-id="f709c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f709c-112">-DefaultProfile</span></span>
<span data-ttu-id="f709c-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f709c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f709c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f709c-114">-Force</span></span>
<span data-ttu-id="f709c-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f709c-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f709c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f709c-116">-Name</span></span>
<span data-ttu-id="f709c-117">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f709c-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f709c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f709c-118">-ResourceGroupName</span></span>
<span data-ttu-id="f709c-119">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f709c-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f709c-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f709c-120">-SkuCapacity</span></span>
<span data-ttu-id="f709c-121">A capacidade da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f709c-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f709c-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f709c-122">-SkuName</span></span>
<span data-ttu-id="f709c-123">O nome da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f709c-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f709c-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f709c-124">-SkuTier</span></span>
<span data-ttu-id="f709c-125">A camada da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f709c-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f709c-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="f709c-126">-Tag</span></span>
<span data-ttu-id="f709c-127">Marcas do recurso de plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="f709c-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="f709c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f709c-128">-Confirm</span></span>
<span data-ttu-id="f709c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f709c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f709c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f709c-130">-WhatIf</span></span>
<span data-ttu-id="f709c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f709c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f709c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f709c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f709c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f709c-133">CommonParameters</span></span>
<span data-ttu-id="f709c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f709c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f709c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f709c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f709c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f709c-136">INPUTS</span></span>

### <span data-ttu-id="f709c-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f709c-137">None</span></span>

## <span data-ttu-id="f709c-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f709c-138">OUTPUTS</span></span>

### <span data-ttu-id="f709c-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f709c-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f709c-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f709c-140">NOTES</span></span>
<span data-ttu-id="f709c-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f709c-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f709c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f709c-142">RELATED LINKS</span></span>
