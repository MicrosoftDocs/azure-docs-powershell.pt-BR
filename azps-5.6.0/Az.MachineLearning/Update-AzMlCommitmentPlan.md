---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 6bd60ced20e9c5b8ce9c3be01d419af55281aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885901"
---
# <span data-ttu-id="5984f-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5984f-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="5984f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5984f-102">SYNOPSIS</span></span>
<span data-ttu-id="5984f-103">Atualiza as propriedades de um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="5984f-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="5984f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5984f-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5984f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5984f-105">DESCRIPTION</span></span>
<span data-ttu-id="5984f-106">Atualiza um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="5984f-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="5984f-107">Observe que a maioria das propriedades do plano de compromisso é imutável e não pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="5984f-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="5984f-108">As propriedades que podem ser modificadas incluem Sku (permitindo que você migre o plano de compromisso de um SKU para outro) e Tags.</span><span class="sxs-lookup"><span data-stu-id="5984f-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="5984f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5984f-109">EXAMPLES</span></span>

### <span data-ttu-id="5984f-110">Exemplo 1: atualizar um plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="5984f-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="5984f-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5984f-111">PARAMETERS</span></span>

### <span data-ttu-id="5984f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5984f-112">-DefaultProfile</span></span>
<span data-ttu-id="5984f-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5984f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5984f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5984f-114">-Force</span></span>
<span data-ttu-id="5984f-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="5984f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5984f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5984f-116">-Name</span></span>
<span data-ttu-id="5984f-117">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5984f-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5984f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5984f-118">-ResourceGroupName</span></span>
<span data-ttu-id="5984f-119">O nome do grupo de recursos do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5984f-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5984f-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5984f-120">-SkuCapacity</span></span>
<span data-ttu-id="5984f-121">A capacidade do SKU a ser usado ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5984f-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5984f-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5984f-122">-SkuName</span></span>
<span data-ttu-id="5984f-123">O nome do SKU a ser usado ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5984f-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5984f-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5984f-124">-SkuTier</span></span>
<span data-ttu-id="5984f-125">A camada do SKU a ser usado ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5984f-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5984f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="5984f-126">-Tag</span></span>
<span data-ttu-id="5984f-127">Marcas para o recurso de plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="5984f-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="5984f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5984f-128">-Confirm</span></span>
<span data-ttu-id="5984f-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5984f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5984f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5984f-130">-WhatIf</span></span>
<span data-ttu-id="5984f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5984f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5984f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5984f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5984f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5984f-133">CommonParameters</span></span>
<span data-ttu-id="5984f-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5984f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5984f-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5984f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5984f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5984f-136">INPUTS</span></span>

### <span data-ttu-id="5984f-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5984f-137">None</span></span>

## <span data-ttu-id="5984f-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5984f-138">OUTPUTS</span></span>

### <span data-ttu-id="5984f-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5984f-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="5984f-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="5984f-140">NOTES</span></span>
<span data-ttu-id="5984f-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5984f-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5984f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5984f-142">RELATED LINKS</span></span>
