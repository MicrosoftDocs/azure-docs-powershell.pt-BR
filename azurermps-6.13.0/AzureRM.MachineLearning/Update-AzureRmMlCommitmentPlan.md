---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 38228cd8f7618d3dfeec1836621d2eeffc5ecb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430883"
---
# <span data-ttu-id="3c3bf-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3c3bf-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="3c3bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="3c3bf-103">Atualiza as propriedades de um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c3bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c3bf-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c3bf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c3bf-105">DESCRIPTION</span></span>
<span data-ttu-id="3c3bf-106">Atualiza um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="3c3bf-107">Observe que a maioria das propriedades do plano de compromisso é imutável e não pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="3c3bf-108">As propriedades que podem ser modificadas incluem SKU (permitindo que você migre o plano de compromisso de uma SKU para outra) e marcas.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="3c3bf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c3bf-109">EXAMPLES</span></span>

### <span data-ttu-id="3c3bf-110">Exemplo 1: atualizar um plano de compromisso</span><span class="sxs-lookup"><span data-stu-id="3c3bf-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="3c3bf-111">OS</span><span class="sxs-lookup"><span data-stu-id="3c3bf-111">PARAMETERS</span></span>

### <span data-ttu-id="3c3bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c3bf-112">-DefaultProfile</span></span>
<span data-ttu-id="3c3bf-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3c3bf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c3bf-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3c3bf-114">-Force</span></span>
<span data-ttu-id="3c3bf-115">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3c3bf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c3bf-116">-Name</span></span>
<span data-ttu-id="3c3bf-117">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3c3bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c3bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="3c3bf-119">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3c3bf-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3c3bf-120">-SkuCapacity</span></span>
<span data-ttu-id="3c3bf-121">A capacidade da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3c3bf-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3c3bf-122">-SkuName</span></span>
<span data-ttu-id="3c3bf-123">O nome da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3c3bf-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3c3bf-124">-SkuTier</span></span>
<span data-ttu-id="3c3bf-125">A camada da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3c3bf-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="3c3bf-126">-Tag</span></span>
<span data-ttu-id="3c3bf-127">Marcas do recurso de plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="3c3bf-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c3bf-128">-Confirm</span></span>
<span data-ttu-id="3c3bf-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c3bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c3bf-130">-WhatIf</span></span>
<span data-ttu-id="3c3bf-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c3bf-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c3bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c3bf-133">CommonParameters</span></span>
<span data-ttu-id="3c3bf-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c3bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c3bf-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c3bf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c3bf-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c3bf-136">INPUTS</span></span>

### <span data-ttu-id="3c3bf-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3c3bf-137">None</span></span>

## <span data-ttu-id="3c3bf-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c3bf-138">OUTPUTS</span></span>

### <span data-ttu-id="3c3bf-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3c3bf-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3c3bf-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c3bf-140">NOTES</span></span>
<span data-ttu-id="3c3bf-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3c3bf-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3c3bf-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c3bf-142">RELATED LINKS</span></span>
