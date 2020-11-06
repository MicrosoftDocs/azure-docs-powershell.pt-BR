---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: e7c296c74aad7e733659930aea9487cf2a73aef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603108"
---
# <span data-ttu-id="d8c52-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d8c52-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="d8c52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8c52-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c52-103">Atualiza as propriedades de um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="d8c52-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8c52-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tags <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8c52-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c52-106">Atualiza um recurso de plano de compromisso existente.</span><span class="sxs-lookup"><span data-stu-id="d8c52-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="d8c52-107">Observe que a maioria das propriedades do plano de compromisso é imutável e não pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="d8c52-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="d8c52-108">As propriedades que podem ser modificadas incluem SKU (permitindo que você migre o plano de compromisso de uma SKU para outra) e marcas.</span><span class="sxs-lookup"><span data-stu-id="d8c52-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="d8c52-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8c52-109">EXAMPLES</span></span>

### <span data-ttu-id="d8c52-110">--------------------------Exemplo 1: atualizar um plano de compromisso--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8c52-110">--------------------------  Example 1: Update a commitment plan  --------------------------</span></span>
<span data-ttu-id="d8c52-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d8c52-111">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="d8c52-112">OS</span><span class="sxs-lookup"><span data-stu-id="d8c52-112">PARAMETERS</span></span>

### <span data-ttu-id="d8c52-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d8c52-113">-Force</span></span>
<span data-ttu-id="d8c52-114">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="d8c52-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d8c52-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8c52-115">-Name</span></span>
<span data-ttu-id="d8c52-116">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d8c52-116">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d8c52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c52-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8c52-118">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d8c52-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d8c52-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d8c52-119">-SkuCapacity</span></span>
<span data-ttu-id="d8c52-120">A capacidade da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d8c52-120">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d8c52-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d8c52-121">-SkuName</span></span>
<span data-ttu-id="d8c52-122">O nome da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d8c52-122">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d8c52-123">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d8c52-123">-SkuTier</span></span>
<span data-ttu-id="d8c52-124">A camada da SKU a ser usada ao atualizar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d8c52-124">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d8c52-125">-Marcas</span><span class="sxs-lookup"><span data-stu-id="d8c52-125">-Tags</span></span>
<span data-ttu-id="d8c52-126">Marcas do recurso de plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="d8c52-126">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="d8c52-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8c52-127">-Confirm</span></span>
<span data-ttu-id="d8c52-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8c52-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c52-129">-WhatIf</span></span>
<span data-ttu-id="d8c52-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8c52-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8c52-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8c52-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c52-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c52-132">-DefaultProfile</span></span>
<span data-ttu-id="d8c52-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c52-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8c52-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c52-134">CommonParameters</span></span>
<span data-ttu-id="d8c52-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c52-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c52-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c52-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c52-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8c52-137">INPUTS</span></span>

## <span data-ttu-id="d8c52-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8c52-138">OUTPUTS</span></span>

### <span data-ttu-id="d8c52-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d8c52-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="d8c52-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8c52-140">NOTES</span></span>
<span data-ttu-id="d8c52-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d8c52-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d8c52-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8c52-142">RELATED LINKS</span></span>

