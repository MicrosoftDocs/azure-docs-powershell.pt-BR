---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115417"
---
# <span data-ttu-id="012af-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="012af-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="012af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="012af-102">SYNOPSIS</span></span>
<span data-ttu-id="012af-103">Exclui um plano de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="012af-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="012af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="012af-104">SYNTAX</span></span>

### <span data-ttu-id="012af-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="012af-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="012af-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="012af-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="012af-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="012af-107">DESCRIPTION</span></span>
<span data-ttu-id="012af-108">Exclui um plano de aplicativo de função.</span><span class="sxs-lookup"><span data-stu-id="012af-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="012af-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="012af-109">EXAMPLES</span></span>

### <span data-ttu-id="012af-110">Exemplo 1: obter uma função plano do aplicativo por nome e excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="012af-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="012af-111">Esse comando obtém uma função plano do aplicativo por nome e a exclui.</span><span class="sxs-lookup"><span data-stu-id="012af-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="012af-112">Exemplo 2: excluir uma função de plano do aplicativo por nome.</span><span class="sxs-lookup"><span data-stu-id="012af-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="012af-113">Esse comando exclui um plano de aplicativo de função por nome.</span><span class="sxs-lookup"><span data-stu-id="012af-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="012af-114">OS</span><span class="sxs-lookup"><span data-stu-id="012af-114">PARAMETERS</span></span>

### <span data-ttu-id="012af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="012af-115">-DefaultProfile</span></span>
<span data-ttu-id="012af-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="012af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="012af-117">-Force</span><span class="sxs-lookup"><span data-stu-id="012af-117">-Force</span></span>
<span data-ttu-id="012af-118">Força o cmdlet a remover o plano de aplicativo da função sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="012af-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="012af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="012af-119">-InputObject</span></span>
<span data-ttu-id="012af-120">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="012af-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="012af-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="012af-121">-Name</span></span>
<span data-ttu-id="012af-122">O nome da função do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="012af-122">The name of function app.</span></span>

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

### <span data-ttu-id="012af-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="012af-123">-PassThru</span></span>
<span data-ttu-id="012af-124">Retorna true quando o comando é bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="012af-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="012af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="012af-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="012af-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="012af-126">-SubscriptionId</span></span>
<span data-ttu-id="012af-127">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="012af-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="012af-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="012af-128">-Confirm</span></span>
<span data-ttu-id="012af-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="012af-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="012af-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="012af-130">-WhatIf</span></span>
<span data-ttu-id="012af-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="012af-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="012af-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="012af-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="012af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012af-133">CommonParameters</span></span>
<span data-ttu-id="012af-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="012af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012af-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="012af-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012af-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="012af-136">INPUTS</span></span>

### <span data-ttu-id="012af-137">Microsoft. Azure. PowerShell. cmdlets. Functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="012af-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="012af-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="012af-138">OUTPUTS</span></span>

### <span data-ttu-id="012af-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="012af-139">System.Boolean</span></span>

## <span data-ttu-id="012af-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="012af-140">NOTES</span></span>

<span data-ttu-id="012af-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="012af-141">ALIASES</span></span>

<span data-ttu-id="012af-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="012af-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="012af-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="012af-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="012af-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="012af-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="012af-145">INPUTobject <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="012af-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="012af-146">`Location <String>`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="012af-147">`[Kind <String>]`: Tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="012af-148">`[Tag <IResourceTags>]`: Marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="012af-149">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="012af-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="012af-150">`[Capacity <Int32?>]`: Número atual de instâncias atribuídas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="012af-151">`[FreeOfferExpirationTime <DateTime?>]`: O tempo em que a oferta gratuita do farm de servidores vence.</span><span class="sxs-lookup"><span data-stu-id="012af-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="012af-152">`[HostingEnvironmentProfileId <String>]`: ID do recurso do ambiente do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="012af-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="012af-153">`[HyperV <Boolean?>]`: Se o plano do serviço de aplicativo contêiner Hyper-V <code>true</code> , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="012af-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="012af-154">`[IsSpot <Boolean?>]`: Se <code>true</code> , esse plano do serviço de aplicativo possui instâncias especiais.</span><span class="sxs-lookup"><span data-stu-id="012af-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="012af-155">`[IsXenon <Boolean?>]`: Obsoleto: se o plano do serviço de aplicativo contêiner do Hyper-V <code>true</code> , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="012af-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="012af-156">`[MaximumElasticWorkerCount <Int32?>]`: Número máximo do total de trabalhadores permitidos para este plano do serviço de aplicativo ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="012af-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="012af-157">`[PerSiteScaling <Boolean?>]`: Se <code>true</code> , os aplicativos atribuídos a esse plano do serviço de aplicativo poderão ser dimensionados independentemente.</span><span class="sxs-lookup"><span data-stu-id="012af-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="012af-158">Se <code>false</code> , os aplicativos atribuídos a esse plano do serviço de aplicativo serão dimensionados para todas as instâncias do plano.</span><span class="sxs-lookup"><span data-stu-id="012af-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="012af-159">`[Reserved <Boolean?>]`: Se for o plano do serviço de aplicativo Linux <code>true</code> , <code>false</code> caso contrário.</span><span class="sxs-lookup"><span data-stu-id="012af-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="012af-160">`[SkuCapability <ICapability[]>]`: Recursos do SKU, por exemplo, o Gerenciador de tráfego está habilitado?</span><span class="sxs-lookup"><span data-stu-id="012af-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="012af-161">`[Name <String>]`: Nome do recurso de SKU.</span><span class="sxs-lookup"><span data-stu-id="012af-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="012af-162">`[Reason <String>]`: Motivo da funcionalidade de SKU.</span><span class="sxs-lookup"><span data-stu-id="012af-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="012af-163">`[Value <String>]`: Valor da funcionalidade de SKU.</span><span class="sxs-lookup"><span data-stu-id="012af-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="012af-164">`[SkuCapacityDefault <Int32?>]`: Número padrão de trabalhadores para esta SKU do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="012af-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="012af-165">`[SkuCapacityMaximum <Int32?>]`: Número máximo de trabalhadores para esta SKU do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="012af-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="012af-166">`[SkuCapacityMinimum <Int32?>]`: Número mínimo de trabalhadores para esta SKU do plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="012af-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="012af-167">`[SkuCapacityScaleType <String>]`: Configurações de escala disponíveis para um plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="012af-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="012af-168">`[SkuFamily <String>]`: Código da família do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="012af-169">`[SkuLocation <String[]>]`: Locais da SKU.</span><span class="sxs-lookup"><span data-stu-id="012af-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="012af-170">`[SkuName <String>]`: Nome do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="012af-171">`[SkuSize <String>]`: Especificador de tamanho do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="012af-172">`[SkuTier <String>]`: Camada de serviço do SKU do recurso.</span><span class="sxs-lookup"><span data-stu-id="012af-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="012af-173">`[SpotExpirationTime <DateTime?>]`: O tempo em que o farm de servidores vence.</span><span class="sxs-lookup"><span data-stu-id="012af-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="012af-174">Válido somente se for um farm de servidores Spot.</span><span class="sxs-lookup"><span data-stu-id="012af-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="012af-175">`[TargetWorkerCount <Int32?>]`: Dimensionando a contagem de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="012af-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="012af-176">`[TargetWorkerSizeId <Int32?>]`: Dimensionando a ID do valor do trabalhador.</span><span class="sxs-lookup"><span data-stu-id="012af-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="012af-177">`[WorkerTierName <String>]`: Camada de trabalho de destino atribuída ao plano do serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="012af-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="012af-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="012af-178">RELATED LINKS</span></span>

