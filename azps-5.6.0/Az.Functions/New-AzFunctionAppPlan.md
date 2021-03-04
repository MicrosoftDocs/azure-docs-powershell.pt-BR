---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 465c4b366990bb69d437fbdbe51fe2c5f4316758
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887514"
---
# <span data-ttu-id="bfc85-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="bfc85-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="bfc85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc85-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc85-103">Cria um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="bfc85-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="bfc85-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bfc85-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bfc85-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bfc85-105">DESCRIPTION</span></span>
<span data-ttu-id="bfc85-106">Cria um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="bfc85-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="bfc85-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfc85-107">EXAMPLES</span></span>

### <span data-ttu-id="bfc85-108">Exemplo 1: Criar um plano de aplicativo premium do Windows na Europa Ocidental com capacidade de saída de até 10 instâncias.</span><span class="sxs-lookup"><span data-stu-id="bfc85-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="bfc85-109">Este comando cria um plano de aplicativo premium do Windows na Europa Ocidental com capacidade de saída de até 10 instâncias.</span><span class="sxs-lookup"><span data-stu-id="bfc85-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="bfc85-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bfc85-110">PARAMETERS</span></span>

### <span data-ttu-id="bfc85-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfc85-111">-AsJob</span></span>
<span data-ttu-id="bfc85-112">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="bfc85-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="bfc85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc85-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="bfc85-114">-Location</span><span class="sxs-lookup"><span data-stu-id="bfc85-114">-Location</span></span>
<span data-ttu-id="bfc85-115">O local do plano de consumo.</span><span class="sxs-lookup"><span data-stu-id="bfc85-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="bfc85-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="bfc85-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="bfc85-117">O número máximo de funcionários para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfc85-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="bfc85-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="bfc85-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="bfc85-119">O número mínimo de funcionários para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfc85-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="bfc85-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bfc85-120">-Name</span></span>
<span data-ttu-id="bfc85-121">Nome do plano serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfc85-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="bfc85-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bfc85-122">-NoWait</span></span>
<span data-ttu-id="bfc85-123">Execute o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bfc85-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="bfc85-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc85-124">-ResourceGroupName</span></span>
<span data-ttu-id="bfc85-125">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="bfc85-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="bfc85-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="bfc85-126">-Sku</span></span>
<span data-ttu-id="bfc85-127">O plano sku.</span><span class="sxs-lookup"><span data-stu-id="bfc85-127">The plan sku.</span></span>
<span data-ttu-id="bfc85-128">As entradas válidas são: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="bfc85-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="bfc85-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfc85-129">-SubscriptionId</span></span>
<span data-ttu-id="bfc85-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc85-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="bfc85-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="bfc85-131">-Tag</span></span>
<span data-ttu-id="bfc85-132">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="bfc85-132">Resource tags.</span></span>

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

### <span data-ttu-id="bfc85-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="bfc85-133">-WorkerType</span></span>
<span data-ttu-id="bfc85-134">O tipo de trabalho do plano.</span><span class="sxs-lookup"><span data-stu-id="bfc85-134">The worker type for the plan.</span></span>
<span data-ttu-id="bfc85-135">As entradas válidas são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="bfc85-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="bfc85-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfc85-136">-Confirm</span></span>
<span data-ttu-id="bfc85-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc85-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc85-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc85-138">-WhatIf</span></span>
<span data-ttu-id="bfc85-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfc85-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc85-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfc85-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc85-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc85-141">CommonParameters</span></span>
<span data-ttu-id="bfc85-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc85-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc85-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfc85-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc85-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfc85-144">INPUTS</span></span>

## <span data-ttu-id="bfc85-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bfc85-145">OUTPUTS</span></span>

### <span data-ttu-id="bfc85-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bfc85-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="bfc85-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="bfc85-147">NOTES</span></span>

<span data-ttu-id="bfc85-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bfc85-148">ALIASES</span></span>

## <span data-ttu-id="bfc85-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfc85-149">RELATED LINKS</span></span>

