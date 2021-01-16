---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272298"
---
# <span data-ttu-id="a461f-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="a461f-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="a461f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a461f-102">SYNOPSIS</span></span>
<span data-ttu-id="a461f-103">Atualiza o ambiente com o nome especificado na assinatura especificada e no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a461f-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a461f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a461f-104">SYNTAX</span></span>

### <span data-ttu-id="a461f-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="a461f-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a461f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a461f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a461f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a461f-107">DESCRIPTION</span></span>
<span data-ttu-id="a461f-108">Atualiza o ambiente com o nome especificado na assinatura especificada e no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a461f-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a461f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a461f-109">EXAMPLES</span></span>

### <span data-ttu-id="a461f-110">Exemplo 1: atualizar um ambiente do insights série tempo do Gen1</span><span class="sxs-lookup"><span data-stu-id="a461f-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="a461f-111">Esse comando atualiza um ambiente do insights série de tempo do Gen1.</span><span class="sxs-lookup"><span data-stu-id="a461f-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="a461f-112">Exemplo 2: atualizar um ambiente do insights série tempo do Gen1</span><span class="sxs-lookup"><span data-stu-id="a461f-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="a461f-113">Esse comando atualiza um ambiente do insights série de tempo do Gen1.</span><span class="sxs-lookup"><span data-stu-id="a461f-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="a461f-114">OS</span><span class="sxs-lookup"><span data-stu-id="a461f-114">PARAMETERS</span></span>

### <span data-ttu-id="a461f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a461f-115">-AsJob</span></span>
<span data-ttu-id="a461f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a461f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a461f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a461f-117">-DefaultProfile</span></span>
<span data-ttu-id="a461f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a461f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a461f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a461f-119">-InputObject</span></span>
<span data-ttu-id="a461f-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a461f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a461f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a461f-121">-Name</span></span>
<span data-ttu-id="a461f-122">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="a461f-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a461f-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a461f-123">-NoWait</span></span>
<span data-ttu-id="a461f-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a461f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a461f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a461f-125">-ResourceGroupName</span></span>
<span data-ttu-id="a461f-126">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a461f-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a461f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a461f-127">-SubscriptionId</span></span>
<span data-ttu-id="a461f-128">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a461f-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a461f-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="a461f-129">-Tag</span></span>
<span data-ttu-id="a461f-130">Pares de valores chave de propriedades adicionais para o ambiente.</span><span class="sxs-lookup"><span data-stu-id="a461f-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="a461f-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a461f-131">-Confirm</span></span>
<span data-ttu-id="a461f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a461f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a461f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a461f-133">-WhatIf</span></span>
<span data-ttu-id="a461f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a461f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a461f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a461f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a461f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a461f-136">CommonParameters</span></span>
<span data-ttu-id="a461f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a461f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a461f-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a461f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a461f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a461f-139">INPUTS</span></span>

### <span data-ttu-id="a461f-140">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a461f-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a461f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a461f-141">OUTPUTS</span></span>

### <span data-ttu-id="a461f-142">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="a461f-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="a461f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a461f-143">NOTES</span></span>

<span data-ttu-id="a461f-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a461f-144">ALIASES</span></span>

<span data-ttu-id="a461f-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a461f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a461f-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a461f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a461f-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a461f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a461f-148">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a461f-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a461f-149">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="a461f-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a461f-150">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="a461f-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a461f-151">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="a461f-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a461f-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a461f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a461f-153">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="a461f-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a461f-154">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a461f-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a461f-155">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a461f-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a461f-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a461f-156">RELATED LINKS</span></span>

