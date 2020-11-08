---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112225"
---
# <span data-ttu-id="27948-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="27948-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="27948-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27948-102">SYNOPSIS</span></span>
<span data-ttu-id="27948-103">Cria uma função de plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27948-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="27948-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27948-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27948-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27948-105">DESCRIPTION</span></span>
<span data-ttu-id="27948-106">Cria uma função de plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27948-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="27948-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27948-107">EXAMPLES</span></span>

### <span data-ttu-id="27948-108">Exemplo 1: criar um plano de aplicativo do Windows Premium na Europa Ocidental com capacidade de intermitência out de até 10 instâncias.</span><span class="sxs-lookup"><span data-stu-id="27948-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="27948-109">Esse comando cria um plano de aplicativo do Windows Premium na Europa Ocidental com capacidade de intermitência de saída de até 10 instâncias.</span><span class="sxs-lookup"><span data-stu-id="27948-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="27948-110">OS</span><span class="sxs-lookup"><span data-stu-id="27948-110">PARAMETERS</span></span>

### <span data-ttu-id="27948-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27948-111">-AsJob</span></span>
<span data-ttu-id="27948-112">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="27948-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="27948-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27948-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="27948-114">-Local</span><span class="sxs-lookup"><span data-stu-id="27948-114">-Location</span></span>
<span data-ttu-id="27948-115">O local para o plano de consumo.</span><span class="sxs-lookup"><span data-stu-id="27948-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="27948-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="27948-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="27948-117">O número máximo de trabalhadores para o plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27948-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="27948-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="27948-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="27948-119">O número mínimo de trabalhadores para o plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27948-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="27948-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="27948-120">-Name</span></span>
<span data-ttu-id="27948-121">Nome do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27948-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="27948-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="27948-122">-NoWait</span></span>
<span data-ttu-id="27948-123">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="27948-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="27948-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27948-124">-ResourceGroupName</span></span>
<span data-ttu-id="27948-125">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="27948-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="27948-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="27948-126">-Sku</span></span>
<span data-ttu-id="27948-127">A SKU do plano.</span><span class="sxs-lookup"><span data-stu-id="27948-127">The plan sku.</span></span>
<span data-ttu-id="27948-128">As entradas válidas são: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="27948-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="27948-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27948-129">-SubscriptionId</span></span>
<span data-ttu-id="27948-130">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="27948-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="27948-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="27948-131">-Tag</span></span>
<span data-ttu-id="27948-132">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="27948-132">Resource tags.</span></span>

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

### <span data-ttu-id="27948-133">-Workertype</span><span class="sxs-lookup"><span data-stu-id="27948-133">-WorkerType</span></span>
<span data-ttu-id="27948-134">O tipo de trabalhador para o plano.</span><span class="sxs-lookup"><span data-stu-id="27948-134">The worker type for the plan.</span></span>
<span data-ttu-id="27948-135">As entradas válidas são: Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="27948-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="27948-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27948-136">-Confirm</span></span>
<span data-ttu-id="27948-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27948-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27948-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27948-138">-WhatIf</span></span>
<span data-ttu-id="27948-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27948-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27948-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27948-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27948-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27948-141">CommonParameters</span></span>
<span data-ttu-id="27948-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27948-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27948-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27948-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27948-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27948-144">INPUTS</span></span>

## <span data-ttu-id="27948-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27948-145">OUTPUTS</span></span>

### <span data-ttu-id="27948-146">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="27948-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="27948-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27948-147">NOTES</span></span>

<span data-ttu-id="27948-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="27948-148">ALIASES</span></span>

## <span data-ttu-id="27948-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27948-149">RELATED LINKS</span></span>

