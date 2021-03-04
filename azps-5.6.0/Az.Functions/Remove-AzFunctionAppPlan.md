---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: e930a0848f39ec94cb6eeb4ef290b1842ea6793a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890841"
---
# <span data-ttu-id="fb353-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="fb353-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="fb353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb353-102">SYNOPSIS</span></span>
<span data-ttu-id="fb353-103">Exclui um plano de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="fb353-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="fb353-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fb353-104">SYNTAX</span></span>

### <span data-ttu-id="fb353-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fb353-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fb353-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="fb353-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb353-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fb353-107">DESCRIPTION</span></span>
<span data-ttu-id="fb353-108">Exclui um plano de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="fb353-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="fb353-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb353-109">EXAMPLES</span></span>

### <span data-ttu-id="fb353-110">Exemplo 1: Obter um plano de aplicativo de função pelo nome e excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="fb353-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="fb353-111">Esse comando obtém um plano de aplicativo de função por nome e o exclui.</span><span class="sxs-lookup"><span data-stu-id="fb353-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="fb353-112">Exemplo 2: Excluir um plano de aplicativo de função por nome.</span><span class="sxs-lookup"><span data-stu-id="fb353-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="fb353-113">Este comando exclui um plano de aplicativo de função por nome.</span><span class="sxs-lookup"><span data-stu-id="fb353-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="fb353-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fb353-114">PARAMETERS</span></span>

### <span data-ttu-id="fb353-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb353-115">-DefaultProfile</span></span>
<span data-ttu-id="fb353-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb353-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb353-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fb353-117">-Force</span></span>
<span data-ttu-id="fb353-118">Força o cmdlet a remover o plano do aplicativo de função sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="fb353-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fb353-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb353-119">-InputObject</span></span>
<span data-ttu-id="fb353-120">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fb353-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb353-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fb353-121">-Name</span></span>
<span data-ttu-id="fb353-122">O nome do aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="fb353-122">The name of function app.</span></span>

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

### <span data-ttu-id="fb353-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb353-123">-PassThru</span></span>
<span data-ttu-id="fb353-124">Retorna true quando o comando é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fb353-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="fb353-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb353-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="fb353-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb353-126">-SubscriptionId</span></span>
<span data-ttu-id="fb353-127">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb353-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="fb353-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb353-128">-Confirm</span></span>
<span data-ttu-id="fb353-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb353-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb353-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb353-130">-WhatIf</span></span>
<span data-ttu-id="fb353-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb353-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb353-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb353-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb353-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb353-133">CommonParameters</span></span>
<span data-ttu-id="fb353-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb353-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb353-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb353-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb353-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb353-136">INPUTS</span></span>

### <span data-ttu-id="fb353-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fb353-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="fb353-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fb353-138">OUTPUTS</span></span>

### <span data-ttu-id="fb353-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb353-139">System.Boolean</span></span>

## <span data-ttu-id="fb353-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="fb353-140">NOTES</span></span>

<span data-ttu-id="fb353-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fb353-141">ALIASES</span></span>

<span data-ttu-id="fb353-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="fb353-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb353-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fb353-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb353-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb353-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb353-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="fb353-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="fb353-146">`Location <String>`: Localização do Recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="fb353-147">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="fb353-148">`[Tag <IResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="fb353-149">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="fb353-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fb353-150">`[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="fb353-151">`[FreeOfferExpirationTime <DateTime?>]`: O tempo em que a oferta gratuita do farm de servidores expira.</span><span class="sxs-lookup"><span data-stu-id="fb353-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="fb353-152">`[HostingEnvironmentProfileId <String>]`: ID de recurso do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb353-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="fb353-153">`[HyperV <Boolean?>]`: Se o plano de serviço de aplicativo de contêiner do Hyper-V <code>true</code> for, <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fb353-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="fb353-154">`[IsSpot <Boolean?>]`: If <code>true</code> , this App Service Plan owns spot instances.</span><span class="sxs-lookup"><span data-stu-id="fb353-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="fb353-155">`[IsXenon <Boolean?>]`: Obsoleto: se o plano de serviço de aplicativo de contêiner do Hyper-V <code>true</code> for , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fb353-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="fb353-156">`[MaximumElasticWorkerCount <Int32?>]`: Número máximo de funcionários permitidos para este Plano de Serviço de Aplicativo ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="fb353-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="fb353-157">`[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo podem ser dimensionados independentemente.</span><span class="sxs-lookup"><span data-stu-id="fb353-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="fb353-158">Se <code>false</code> , os aplicativos atribuídos a este plano de Serviço de Aplicativo serão dimensionados para todas as instâncias do plano.</span><span class="sxs-lookup"><span data-stu-id="fb353-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="fb353-159">`[Reserved <Boolean?>]`: Se o plano de serviço do aplicativo <code>true</code> Linux, <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fb353-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="fb353-160">`[SkuCapability <ICapability[]>]`: Os recursos do SKU, por exemplo, estão habilitados para o gerenciador de tráfego?</span><span class="sxs-lookup"><span data-stu-id="fb353-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="fb353-161">`[Name <String>]`: Nome da funcionalidade SKU.</span><span class="sxs-lookup"><span data-stu-id="fb353-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="fb353-162">`[Reason <String>]`: Motivo da funcionalidade SKU.</span><span class="sxs-lookup"><span data-stu-id="fb353-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="fb353-163">`[Value <String>]`: Valor da funcionalidade SKU.</span><span class="sxs-lookup"><span data-stu-id="fb353-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="fb353-164">`[SkuCapacityDefault <Int32?>]`: Número padrão de funcionários para este SKU do plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb353-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="fb353-165">`[SkuCapacityMaximum <Int32?>]`: Número máximo de funcionários para este SKU do plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb353-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="fb353-166">`[SkuCapacityMinimum <Int32?>]`: Número mínimo de funcionários para este SKU do plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb353-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="fb353-167">`[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb353-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="fb353-168">`[SkuFamily <String>]`: Código da família do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="fb353-169">`[SkuLocation <String[]>]`: Locais do SKU.</span><span class="sxs-lookup"><span data-stu-id="fb353-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="fb353-170">`[SkuName <String>]`: Nome da SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="fb353-171">`[SkuSize <String>]`: Especificador de tamanho do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="fb353-172">`[SkuTier <String>]`: Camada de serviço do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="fb353-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="fb353-173">`[SpotExpirationTime <DateTime?>]`: A hora em que o farm de servidores expira.</span><span class="sxs-lookup"><span data-stu-id="fb353-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="fb353-174">Válido somente se for um farm de servidores spot.</span><span class="sxs-lookup"><span data-stu-id="fb353-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="fb353-175">`[TargetWorkerCount <Int32?>]`: Escala de contagem de funcionários.</span><span class="sxs-lookup"><span data-stu-id="fb353-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="fb353-176">`[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do tamanho do trabalho.</span><span class="sxs-lookup"><span data-stu-id="fb353-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="fb353-177">`[WorkerTierName <String>]`: Camada de trabalho de destino atribuída ao plano de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb353-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="fb353-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb353-178">RELATED LINKS</span></span>

