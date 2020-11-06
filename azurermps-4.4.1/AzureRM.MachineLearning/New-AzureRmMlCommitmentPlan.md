---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 984e1f9d75a7c5a56e6a9bda71a07b193df5be15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610763"
---
# <span data-ttu-id="3d8d6-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3d8d6-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="3d8d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8d6-103">Cria um novo plano de compromisso.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d8d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d8d6-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d8d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="3d8d6-106">Cria um plano de compromisso do Azure Machine Learning em um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="3d8d6-107">Se um plano de compromisso com o mesmo nome existir no grupo de recursos, a chamada funcionará como uma operação de atualização e o plano de compromisso existente será substituído.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="3d8d6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d8d6-108">EXAMPLES</span></span>

### <span data-ttu-id="3d8d6-109">--------------------------Exemplo 1: criar um novo plano de compromisso--------------------------</span><span class="sxs-lookup"><span data-stu-id="3d8d6-109">--------------------------  Example 1: Create a new commitment plan  --------------------------</span></span>
<span data-ttu-id="3d8d6-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3d8d6-110">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="3d8d6-111">Cria um novo plano de compromisso do Azure Machine Learning chamado "MyCommitmentPlanName" no grupo "grupo de recursos" e a região do centro-oeste do Sul.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-111">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="3d8d6-112">Neste exemplo, o DevTest/padrão de SKU é usado, o que significa que os recursos fornecidos pelo plano de compromisso serão definidos pelos limites de DevTest/padrão.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-112">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="3d8d6-113">O SkuCapacity neste exemplo é 1, o que significa que o custo do plano vai 1x o custo de DevTest, e os recursos que o plano contém serão de 1x o que o DevTest fornece.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-113">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="3d8d6-114">OS</span><span class="sxs-lookup"><span data-stu-id="3d8d6-114">PARAMETERS</span></span>

### <span data-ttu-id="3d8d6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3d8d6-115">-Force</span></span>
<span data-ttu-id="3d8d6-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3d8d6-117">-Local</span><span class="sxs-lookup"><span data-stu-id="3d8d6-117">-Location</span></span>
<span data-ttu-id="3d8d6-118">O local do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-118">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d8d6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d8d6-119">-Name</span></span>
<span data-ttu-id="3d8d6-120">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-120">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d8d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d8d6-122">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-122">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d8d6-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3d8d6-123">-SkuCapacity</span></span>
<span data-ttu-id="3d8d6-124">A capacidade da SKU a ser usada ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-124">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d8d6-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3d8d6-125">-SkuName</span></span>
<span data-ttu-id="3d8d6-126">O nome da SKU a ser usada ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-126">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d8d6-127">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="3d8d6-127">-SkuTier</span></span>
<span data-ttu-id="3d8d6-128">A camada da SKU a ser usada ao provisionar o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-128">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d8d6-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d8d6-129">-Confirm</span></span>
<span data-ttu-id="3d8d6-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8d6-131">-WhatIf</span></span>
<span data-ttu-id="3d8d6-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8d6-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8d6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8d6-134">-DefaultProfile</span></span>
<span data-ttu-id="3d8d6-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d8d6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8d6-136">CommonParameters</span></span>
<span data-ttu-id="3d8d6-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d8d6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8d6-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d8d6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8d6-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d8d6-139">INPUTS</span></span>

## <span data-ttu-id="3d8d6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d8d6-140">OUTPUTS</span></span>

### <span data-ttu-id="3d8d6-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3d8d6-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3d8d6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d8d6-142">NOTES</span></span>
<span data-ttu-id="3d8d6-143">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3d8d6-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3d8d6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d8d6-144">RELATED LINKS</span></span>

