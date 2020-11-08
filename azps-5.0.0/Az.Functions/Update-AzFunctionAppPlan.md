---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115404"
---
# <span data-ttu-id="c7854-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="c7854-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="c7854-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7854-102">SYNOPSIS</span></span>
<span data-ttu-id="c7854-103">Atualiza um plano do serviço de aplicativo função.</span><span class="sxs-lookup"><span data-stu-id="c7854-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="c7854-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7854-104">SYNTAX</span></span>

### <span data-ttu-id="c7854-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7854-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7854-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="c7854-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7854-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7854-107">DESCRIPTION</span></span>
<span data-ttu-id="c7854-108">Atualiza um plano do serviço de aplicativo função.</span><span class="sxs-lookup"><span data-stu-id="c7854-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="c7854-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7854-109">EXAMPLES</span></span>

### <span data-ttu-id="c7854-110">Exemplo 1: atualizar um plano de serviço de aplicativo para EP2 SKU com vinte funcionários máximos.</span><span class="sxs-lookup"><span data-stu-id="c7854-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="c7854-111">Esse comando atualiza um plano do serviço de aplicativo para EP2 SKU com vinte trabalhadores máximos.</span><span class="sxs-lookup"><span data-stu-id="c7854-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="c7854-112">OS</span><span class="sxs-lookup"><span data-stu-id="c7854-112">PARAMETERS</span></span>

### <span data-ttu-id="c7854-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7854-113">-AsJob</span></span>
<span data-ttu-id="c7854-114">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="c7854-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="c7854-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7854-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="c7854-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7854-116">-InputObject</span></span>
<span data-ttu-id="c7854-117">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c7854-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c7854-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="c7854-119">O número máximo de trabalhadores para o plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="c7854-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="c7854-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="c7854-121">O número mínimo de trabalhadores para o plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="c7854-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7854-122">-Name</span></span>
<span data-ttu-id="c7854-123">Nome do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c7854-124">-NoWait</span></span>
<span data-ttu-id="c7854-125">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c7854-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c7854-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7854-126">-ResourceGroupName</span></span>
<span data-ttu-id="c7854-127">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="c7854-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="c7854-128">-Sku</span></span>
<span data-ttu-id="c7854-129">A SKU do plano.</span><span class="sxs-lookup"><span data-stu-id="c7854-129">The plan sku.</span></span>
<span data-ttu-id="c7854-130">As entradas válidas são: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="c7854-130">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7854-131">-SubscriptionId</span></span>
<span data-ttu-id="c7854-132">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c7854-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="c7854-133">-Tag</span></span>
<span data-ttu-id="c7854-134">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-134">Resource tags.</span></span>

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

### <span data-ttu-id="c7854-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7854-135">-Confirm</span></span>
<span data-ttu-id="c7854-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7854-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7854-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7854-137">-WhatIf</span></span>
<span data-ttu-id="c7854-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7854-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7854-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7854-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7854-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7854-140">CommonParameters</span></span>
<span data-ttu-id="c7854-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7854-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7854-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7854-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7854-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7854-143">INPUTS</span></span>

### <span data-ttu-id="c7854-144">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7854-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="c7854-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7854-145">OUTPUTS</span></span>

### <span data-ttu-id="c7854-146">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7854-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="c7854-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7854-147">NOTES</span></span>

<span data-ttu-id="c7854-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c7854-148">ALIASES</span></span>

<span data-ttu-id="c7854-149">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c7854-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7854-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c7854-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7854-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7854-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7854-152">INPUTobject <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="c7854-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="c7854-153">`Location <String>`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="c7854-154">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="c7854-155">`[Tag <IResourceTags>]`: Marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="c7854-156">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c7854-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c7854-157">`[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="c7854-158">`[FreeOfferExpirationTime <DateTime?>]`: O tempo em que a oferta gratuita do farm de servidores vence.</span><span class="sxs-lookup"><span data-stu-id="c7854-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="c7854-159">`[HostingEnvironmentProfileId <String>]`: ID do recurso do ambiente do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="c7854-160">`[HyperV <Boolean?>]`: Se o plano do serviço de aplicativo contêiner Hyper-V <code>true</code> , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c7854-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="c7854-161">`[IsSpot <Boolean?>]`: Se <code>true</code> , esse plano do serviço de aplicativo possui instâncias especiais.</span><span class="sxs-lookup"><span data-stu-id="c7854-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="c7854-162">`[IsXenon <Boolean?>]`: Obsoleto: se o plano do serviço de aplicativo contêiner do Hyper-V <code>true</code> , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c7854-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="c7854-163">`[MaximumElasticWorkerCount <Int32?>]`: Número máximo do total de trabalhadores permitidos para este plano do serviço de aplicativo ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="c7854-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="c7854-164">`[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a esse plano do serviço de aplicativo poderão ser dimensionados independentemente.</span><span class="sxs-lookup"><span data-stu-id="c7854-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="c7854-165">Se <code>false</code> , os aplicativos atribuídos a esse plano do serviço de aplicativo serão dimensionados para todas as instâncias do plano.</span><span class="sxs-lookup"><span data-stu-id="c7854-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="c7854-166">`[Reserved <Boolean?>]`: Se for o plano do serviço de aplicativo Linux <code>true</code> , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c7854-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="c7854-167">`[SkuCapability <ICapability[]>]`: Recursos do SKU, por exemplo, o Gerenciador de tráfego está habilitado?</span><span class="sxs-lookup"><span data-stu-id="c7854-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="c7854-168">`[Name <String>]`: Nome do recurso de SKU.</span><span class="sxs-lookup"><span data-stu-id="c7854-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="c7854-169">`[Reason <String>]`: Motivo da funcionalidade de SKU.</span><span class="sxs-lookup"><span data-stu-id="c7854-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="c7854-170">`[Value <String>]`: Valor da funcionalidade de SKU.</span><span class="sxs-lookup"><span data-stu-id="c7854-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="c7854-171">`[SkuCapacityDefault <Int32?>]`: Número padrão de trabalhadores para esta SKU do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="c7854-172">`[SkuCapacityMaximum <Int32?>]`: Número máximo de trabalhadores para esta SKU do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="c7854-173">`[SkuCapacityMinimum <Int32?>]`: Número mínimo de trabalhadores para esta SKU do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="c7854-174">`[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="c7854-175">`[SkuFamily <String>]`: Código da família do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="c7854-176">`[SkuLocation <String[]>]`: Locais da SKU.</span><span class="sxs-lookup"><span data-stu-id="c7854-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="c7854-177">`[SkuName <String>]`: Nome do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="c7854-178">`[SkuSize <String>]`: Especificador de tamanho do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="c7854-179">`[SkuTier <String>]`: Camada de serviço do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="c7854-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="c7854-180">`[SpotExpirationTime <DateTime?>]`: O tempo em que o farm de servidores vence.</span><span class="sxs-lookup"><span data-stu-id="c7854-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="c7854-181">Válido somente se for um farm de servidores Spot.</span><span class="sxs-lookup"><span data-stu-id="c7854-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="c7854-182">`[TargetWorkerCount <Int32?>]`: Dimensionando a contagem de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="c7854-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="c7854-183">`[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do valor do trabalhador.</span><span class="sxs-lookup"><span data-stu-id="c7854-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="c7854-184">`[WorkerTierName <String>]`: Camada de trabalho de destino atribuída ao plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="c7854-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7854-185">RELATED LINKS</span></span>

