---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116787"
---
# <span data-ttu-id="0f3ea-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="0f3ea-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="0f3ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="0f3ea-103">Atualiza um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="0f3ea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f3ea-104">SYNTAX</span></span>

### <span data-ttu-id="0f3ea-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="0f3ea-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0f3ea-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="0f3ea-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f3ea-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f3ea-107">DESCRIPTION</span></span>
<span data-ttu-id="0f3ea-108">Atualiza um plano de serviço de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="0f3ea-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f3ea-109">EXAMPLES</span></span>

### <span data-ttu-id="0f3ea-110">Exemplo 1: Atualize um plano de serviço de aplicativo para a SKU DE ACORDO2 com vinte trabalhadores máximos.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="0f3ea-111">Este comando atualiza um plano de serviço de aplicativo para a SKU DE ACORDO2 com vinte trabalhadores máximos.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="0f3ea-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f3ea-112">PARAMETERS</span></span>

### <span data-ttu-id="0f3ea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f3ea-113">-AsJob</span></span>
<span data-ttu-id="0f3ea-114">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="0f3ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f3ea-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="0f3ea-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f3ea-116">-InputObject</span></span>
<span data-ttu-id="0f3ea-117">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f3ea-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0f3ea-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="0f3ea-119">O número máximo de trabalhadores para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="0f3ea-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0f3ea-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="0f3ea-121">O número mínimo de trabalhadores para o plano de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="0f3ea-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f3ea-122">-Name</span></span>
<span data-ttu-id="0f3ea-123">Nome do plano serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="0f3ea-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0f3ea-124">-NoWait</span></span>
<span data-ttu-id="0f3ea-125">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0f3ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f3ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="0f3ea-127">Nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="0f3ea-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="0f3ea-128">-Sku</span></span>
<span data-ttu-id="0f3ea-129">A SKU do plano.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-129">The plan sku.</span></span>
<span data-ttu-id="0f3ea-130">As entradas válidas são: EP1, EP2, TEM3</span><span class="sxs-lookup"><span data-stu-id="0f3ea-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="0f3ea-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f3ea-131">-SubscriptionId</span></span>
<span data-ttu-id="0f3ea-132">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="0f3ea-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f3ea-133">-Tag</span></span>
<span data-ttu-id="0f3ea-134">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-134">Resource tags.</span></span>

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

### <span data-ttu-id="0f3ea-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0f3ea-135">-Confirm</span></span>
<span data-ttu-id="0f3ea-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f3ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f3ea-137">-WhatIf</span></span>
<span data-ttu-id="0f3ea-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f3ea-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f3ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f3ea-140">CommonParameters</span></span>
<span data-ttu-id="0f3ea-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f3ea-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f3ea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f3ea-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="0f3ea-143">INPUTS</span></span>

### <span data-ttu-id="0f3ea-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0f3ea-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="0f3ea-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="0f3ea-145">OUTPUTS</span></span>

### <span data-ttu-id="0f3ea-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0f3ea-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="0f3ea-147">Notas</span><span class="sxs-lookup"><span data-stu-id="0f3ea-147">NOTES</span></span>

<span data-ttu-id="0f3ea-148">Aliases</span><span class="sxs-lookup"><span data-stu-id="0f3ea-148">ALIASES</span></span>

<span data-ttu-id="0f3ea-149">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="0f3ea-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f3ea-150">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f3ea-151">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f3ea-152">INPUTOBJECT: <IAppServicePlan></span><span class="sxs-lookup"><span data-stu-id="0f3ea-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="0f3ea-153">`Location <String>`: Localização do Recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="0f3ea-154">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="0f3ea-155">`[Tag <IResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0f3ea-156">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0f3ea-157">`[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="0f3ea-158">`[FreeOfferExpirationTime <DateTime?>]`: o tempo em que a oferta gratuita de farm do servidor expira.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="0f3ea-159">`[HostingEnvironmentProfileId <String>]`: ID do recurso do Ambiente de Serviço de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="0f3ea-160">`[HyperV <Boolean?>]`: caso contrário, se o plano de serviço do aplicativo de contêineres Hiper-V <code>true</code> <code>false</code> for.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0f3ea-161">`[IsSpot <Boolean?>]`: Se <code>true</code> , este Plano de Serviço de Aplicativo possui instâncias de local.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="0f3ea-162">`[IsXenon <Boolean?>]`: Obsoleto: se o plano de serviço do aplicativo de contêineres Hiper-V, <code>true</code> <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0f3ea-163">`[MaximumElasticWorkerCount <Int32?>]`: número máximo de trabalhadores totais permitidos para este Plano de Serviço de Aplicativo ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="0f3ea-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="0f3ea-164">`[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativos podem ser dimensionados independentemente.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="0f3ea-165">Se <code>false</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo serão dimensionados para todas as instâncias do plano.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="0f3ea-166">`[Reserved <Boolean?>]`: Se o plano de serviço do aplicativo <code>true</code> Linux, <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0f3ea-167">`[SkuCapability <ICapability[]>]`: Os recursos da SKU, por exemplo, estão habilitados no gerenciador de tráfego?</span><span class="sxs-lookup"><span data-stu-id="0f3ea-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="0f3ea-168">`[Name <String>]`: Nome do recurso SKU.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="0f3ea-169">`[Reason <String>]`: motivo da capacidade da SKU.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="0f3ea-170">`[Value <String>]`: Valor da capacidade de SKU.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="0f3ea-171">`[SkuCapacityDefault <Int32?>]`: Número padrão de trabalhadores para esta SKU do plano serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0f3ea-172">`[SkuCapacityMaximum <Int32?>]`: Número máximo de trabalhadores para esta SKU do plano serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0f3ea-173">`[SkuCapacityMinimum <Int32?>]`: Número mínimo de trabalhadores para esta SKU do plano serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0f3ea-174">`[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="0f3ea-175">`[SkuFamily <String>]`: Código da família da SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="0f3ea-176">`[SkuLocation <String[]>]`: locais da SKU.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="0f3ea-177">`[SkuName <String>]`: Nome da SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="0f3ea-178">`[SkuSize <String>]`: Especificador de tamanho da SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="0f3ea-179">`[SkuTier <String>]`: Nível de serviço da SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="0f3ea-180">`[SpotExpirationTime <DateTime?>]`: o tempo em que o farm do servidor expira.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="0f3ea-181">Válido somente se for um farm de servidor local.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="0f3ea-182">`[TargetWorkerCount <Int32?>]`: Dimensionando a contagem de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="0f3ea-183">`[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do tamanho do trabalhador.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="0f3ea-184">`[WorkerTierName <String>]`: Nível de trabalhador de destino atribuído ao plano serviço de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0f3ea-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="0f3ea-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f3ea-185">RELATED LINKS</span></span>

