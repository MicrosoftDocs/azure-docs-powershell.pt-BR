---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886766"
---
# <span data-ttu-id="ee685-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="ee685-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="ee685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee685-102">SYNOPSIS</span></span>
<span data-ttu-id="ee685-103">Atualiza um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="ee685-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="ee685-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ee685-104">SYNTAX</span></span>

### <span data-ttu-id="ee685-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ee685-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ee685-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="ee685-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee685-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ee685-107">DESCRIPTION</span></span>
<span data-ttu-id="ee685-108">Atualiza um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="ee685-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="ee685-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee685-109">EXAMPLES</span></span>

### <span data-ttu-id="ee685-110">Exemplo 1: atualizar um plano de serviço de aplicativo para sku EP2 com vinte funcionários máximos.</span><span class="sxs-lookup"><span data-stu-id="ee685-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="ee685-111">Este comando atualiza um plano de serviço de aplicativo para sku EP2 com vinte funcionários máximos.</span><span class="sxs-lookup"><span data-stu-id="ee685-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="ee685-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ee685-112">PARAMETERS</span></span>

### <span data-ttu-id="ee685-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee685-113">-AsJob</span></span>
<span data-ttu-id="ee685-114">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ee685-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="ee685-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee685-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="ee685-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee685-116">-InputObject</span></span>
<span data-ttu-id="ee685-117">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ee685-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee685-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="ee685-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="ee685-119">O número máximo de funcionários para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="ee685-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="ee685-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="ee685-121">O número mínimo de funcionários para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="ee685-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ee685-122">-Name</span></span>
<span data-ttu-id="ee685-123">Nome do plano serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="ee685-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ee685-124">-NoWait</span></span>
<span data-ttu-id="ee685-125">Execute o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ee685-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ee685-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee685-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee685-127">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="ee685-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="ee685-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="ee685-128">-Sku</span></span>
<span data-ttu-id="ee685-129">O plano sku.</span><span class="sxs-lookup"><span data-stu-id="ee685-129">The plan sku.</span></span>
<span data-ttu-id="ee685-130">As entradas válidas são: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="ee685-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="ee685-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee685-131">-SubscriptionId</span></span>
<span data-ttu-id="ee685-132">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ee685-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="ee685-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee685-133">-Tag</span></span>
<span data-ttu-id="ee685-134">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-134">Resource tags.</span></span>

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

### <span data-ttu-id="ee685-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee685-135">-Confirm</span></span>
<span data-ttu-id="ee685-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee685-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee685-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee685-137">-WhatIf</span></span>
<span data-ttu-id="ee685-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee685-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee685-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee685-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee685-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee685-140">CommonParameters</span></span>
<span data-ttu-id="ee685-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee685-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee685-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee685-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee685-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee685-143">INPUTS</span></span>

### <span data-ttu-id="ee685-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ee685-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="ee685-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ee685-145">OUTPUTS</span></span>

### <span data-ttu-id="ee685-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ee685-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="ee685-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="ee685-147">NOTES</span></span>

<span data-ttu-id="ee685-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ee685-148">ALIASES</span></span>

<span data-ttu-id="ee685-149">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ee685-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee685-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ee685-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee685-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee685-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee685-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="ee685-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="ee685-153">`Location <String>`: Localização do Recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="ee685-154">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="ee685-155">`[Tag <IResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ee685-156">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="ee685-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ee685-157">`[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="ee685-158">`[FreeOfferExpirationTime <DateTime?>]`: O tempo em que a oferta gratuita do farm de servidores expira.</span><span class="sxs-lookup"><span data-stu-id="ee685-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="ee685-159">`[HostingEnvironmentProfileId <String>]`: ID de recurso do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="ee685-160">`[HyperV <Boolean?>]`: Se o plano de serviço de aplicativo de contêiner do Hyper-V <code>true</code> for, <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ee685-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="ee685-161">`[IsSpot <Boolean?>]`: If <code>true</code> , this App Service Plan owns spot instances.</span><span class="sxs-lookup"><span data-stu-id="ee685-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="ee685-162">`[IsXenon <Boolean?>]`: Obsoleto: se o plano de serviço de aplicativo de contêiner do Hyper-V <code>true</code> for , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ee685-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="ee685-163">`[MaximumElasticWorkerCount <Int32?>]`: Número máximo de funcionários permitidos para este Plano de Serviço de Aplicativo ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="ee685-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="ee685-164">`[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo podem ser dimensionados independentemente.</span><span class="sxs-lookup"><span data-stu-id="ee685-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="ee685-165">Se <code>false</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo serão dimensionados para todas as instâncias do plano.</span><span class="sxs-lookup"><span data-stu-id="ee685-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="ee685-166">`[Reserved <Boolean?>]`: Se o plano de serviço do aplicativo <code>true</code> Linux, <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ee685-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="ee685-167">`[SkuCapability <ICapability[]>]`: Os recursos do SKU, por exemplo, estão habilitados para o gerenciador de tráfego?</span><span class="sxs-lookup"><span data-stu-id="ee685-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="ee685-168">`[Name <String>]`: Nome da funcionalidade SKU.</span><span class="sxs-lookup"><span data-stu-id="ee685-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="ee685-169">`[Reason <String>]`: Motivo da funcionalidade SKU.</span><span class="sxs-lookup"><span data-stu-id="ee685-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="ee685-170">`[Value <String>]`: Valor da funcionalidade SKU.</span><span class="sxs-lookup"><span data-stu-id="ee685-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="ee685-171">`[SkuCapacityDefault <Int32?>]`: Número padrão de funcionários para este SKU do plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="ee685-172">`[SkuCapacityMaximum <Int32?>]`: Número máximo de funcionários para este SKU do plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="ee685-173">`[SkuCapacityMinimum <Int32?>]`: Número mínimo de funcionários para este SKU do plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="ee685-174">`[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="ee685-175">`[SkuFamily <String>]`: Código da família do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="ee685-176">`[SkuLocation <String[]>]`: Locais do SKU.</span><span class="sxs-lookup"><span data-stu-id="ee685-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="ee685-177">`[SkuName <String>]`: Nome da SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="ee685-178">`[SkuSize <String>]`: Especificador de tamanho do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="ee685-179">`[SkuTier <String>]`: Camada de serviço do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="ee685-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="ee685-180">`[SpotExpirationTime <DateTime?>]`: A hora em que o farm de servidores expira.</span><span class="sxs-lookup"><span data-stu-id="ee685-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="ee685-181">Válido somente se for um farm de servidores spot.</span><span class="sxs-lookup"><span data-stu-id="ee685-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="ee685-182">`[TargetWorkerCount <Int32?>]`: Escala de contagem de funcionários.</span><span class="sxs-lookup"><span data-stu-id="ee685-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="ee685-183">`[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do tamanho do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ee685-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="ee685-184">`[WorkerTierName <String>]`: Camada de trabalho de destino atribuída ao plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee685-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="ee685-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee685-185">RELATED LINKS</span></span>

