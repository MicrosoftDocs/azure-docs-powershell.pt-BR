---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115786"
---
# <span data-ttu-id="0c57b-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="0c57b-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="0c57b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c57b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c57b-103">Cria um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="0c57b-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="0c57b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c57b-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c57b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c57b-105">DESCRIPTION</span></span>
<span data-ttu-id="0c57b-106">Cria um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="0c57b-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="0c57b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c57b-107">EXAMPLES</span></span>

### <span data-ttu-id="0c57b-108">Exemplo 1: Crie um plano de aplicativo premium do Windows na Europa Ocidental com capacidade de saída de até 10 instâncias.</span><span class="sxs-lookup"><span data-stu-id="0c57b-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="0c57b-109">Esse comando cria um plano de aplicativo premium do Windows na Europa Ocidental com capacidade de saída de até 10 instâncias.</span><span class="sxs-lookup"><span data-stu-id="0c57b-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="0c57b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c57b-110">PARAMETERS</span></span>

### <span data-ttu-id="0c57b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c57b-111">-AsJob</span></span>
<span data-ttu-id="0c57b-112">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="0c57b-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="0c57b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c57b-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c57b-114">-Local</span><span class="sxs-lookup"><span data-stu-id="0c57b-114">-Location</span></span>
<span data-ttu-id="0c57b-115">O local do plano de consumo.</span><span class="sxs-lookup"><span data-stu-id="0c57b-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="0c57b-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0c57b-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="0c57b-117">O número máximo de trabalhadores para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c57b-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c57b-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0c57b-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="0c57b-119">O número mínimo de trabalhadores para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c57b-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c57b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c57b-120">-Name</span></span>
<span data-ttu-id="0c57b-121">Nome do plano serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c57b-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="0c57b-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0c57b-122">-NoWait</span></span>
<span data-ttu-id="0c57b-123">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0c57b-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0c57b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c57b-124">-ResourceGroupName</span></span>
<span data-ttu-id="0c57b-125">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="0c57b-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="0c57b-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="0c57b-126">-Sku</span></span>
<span data-ttu-id="0c57b-127">A SKU do plano.</span><span class="sxs-lookup"><span data-stu-id="0c57b-127">The plan sku.</span></span>
<span data-ttu-id="0c57b-128">As entradas válidas são: EP1, EP2, TEM3</span><span class="sxs-lookup"><span data-stu-id="0c57b-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="0c57b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c57b-129">-SubscriptionId</span></span>
<span data-ttu-id="0c57b-130">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c57b-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c57b-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c57b-131">-Tag</span></span>
<span data-ttu-id="0c57b-132">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="0c57b-132">Resource tags.</span></span>

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

### <span data-ttu-id="0c57b-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="0c57b-133">-WorkerType</span></span>
<span data-ttu-id="0c57b-134">O tipo de trabalhador do plano.</span><span class="sxs-lookup"><span data-stu-id="0c57b-134">The worker type for the plan.</span></span>
<span data-ttu-id="0c57b-135">As entradas válidas são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="0c57b-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="0c57b-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0c57b-136">-Confirm</span></span>
<span data-ttu-id="0c57b-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c57b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c57b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c57b-138">-WhatIf</span></span>
<span data-ttu-id="0c57b-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0c57b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c57b-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c57b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c57b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c57b-141">CommonParameters</span></span>
<span data-ttu-id="0c57b-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c57b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c57b-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c57b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c57b-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="0c57b-144">INPUTS</span></span>

## <span data-ttu-id="0c57b-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="0c57b-145">OUTPUTS</span></span>

### <span data-ttu-id="0c57b-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0c57b-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="0c57b-147">Notas</span><span class="sxs-lookup"><span data-stu-id="0c57b-147">NOTES</span></span>

<span data-ttu-id="0c57b-148">Aliases</span><span class="sxs-lookup"><span data-stu-id="0c57b-148">ALIASES</span></span>

## <span data-ttu-id="0c57b-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c57b-149">RELATED LINKS</span></span>

