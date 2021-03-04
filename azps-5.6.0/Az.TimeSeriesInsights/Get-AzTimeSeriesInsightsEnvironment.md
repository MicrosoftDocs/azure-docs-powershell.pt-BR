---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 151b8a431183727dbfaec242705421ba775b0b99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893046"
---
# <span data-ttu-id="263d5-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="263d5-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="263d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="263d5-102">SYNOPSIS</span></span>
<span data-ttu-id="263d5-103">Obtém o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="263d5-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="263d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="263d5-104">SYNTAX</span></span>

### <span data-ttu-id="263d5-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="263d5-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="263d5-106">Obter</span><span class="sxs-lookup"><span data-stu-id="263d5-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="263d5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="263d5-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="263d5-108">Listar</span><span class="sxs-lookup"><span data-stu-id="263d5-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="263d5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="263d5-109">DESCRIPTION</span></span>
<span data-ttu-id="263d5-110">Obtém o ambiente com o nome especificado no grupo de recursos e assinatura especificado.</span><span class="sxs-lookup"><span data-stu-id="263d5-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="263d5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="263d5-111">EXAMPLES</span></span>

### <span data-ttu-id="263d5-112">Exemplo 1: Obter um ambiente de insights de séries de tempo</span><span class="sxs-lookup"><span data-stu-id="263d5-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="263d5-113">Este comando obtém um ambiente de insights de séries de tempo.</span><span class="sxs-lookup"><span data-stu-id="263d5-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="263d5-114">Exemplo 2: listar todos os ambientes de insights de séries de tempo</span><span class="sxs-lookup"><span data-stu-id="263d5-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="263d5-115">Este comando lista todos os ambientes de insights de séries de tempo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="263d5-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="263d5-116">Exemplo 3: Obter um ambiente de insights de série de tempo por objeto</span><span class="sxs-lookup"><span data-stu-id="263d5-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="263d5-117">Este comando obtém ambientes de insights de séries de tempo.</span><span class="sxs-lookup"><span data-stu-id="263d5-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="263d5-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="263d5-118">PARAMETERS</span></span>

### <span data-ttu-id="263d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263d5-119">-DefaultProfile</span></span>
<span data-ttu-id="263d5-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="263d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="263d5-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="263d5-121">-Expand</span></span>
<span data-ttu-id="263d5-122">A configuração $expand=status incluirá o status dos serviços internos do ambiente no serviço Insights da Série de Tempo.</span><span class="sxs-lookup"><span data-stu-id="263d5-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="263d5-123">-InputObject</span></span>
<span data-ttu-id="263d5-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="263d5-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="263d5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="263d5-125">-Name</span></span>
<span data-ttu-id="263d5-126">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="263d5-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="263d5-128">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="263d5-128">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263d5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="263d5-129">-SubscriptionId</span></span>
<span data-ttu-id="263d5-130">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="263d5-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263d5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263d5-131">CommonParameters</span></span>
<span data-ttu-id="263d5-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263d5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263d5-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="263d5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263d5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="263d5-134">INPUTS</span></span>

### <span data-ttu-id="263d5-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="263d5-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="263d5-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="263d5-136">OUTPUTS</span></span>

### <span data-ttu-id="263d5-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="263d5-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="263d5-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="263d5-138">NOTES</span></span>

<span data-ttu-id="263d5-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="263d5-139">ALIASES</span></span>

<span data-ttu-id="263d5-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="263d5-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="263d5-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="263d5-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="263d5-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="263d5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="263d5-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="263d5-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="263d5-144">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="263d5-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="263d5-145">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="263d5-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="263d5-146">`[EventSourceName <String>]`: O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="263d5-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="263d5-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="263d5-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="263d5-148">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="263d5-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="263d5-149">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="263d5-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="263d5-150">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="263d5-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="263d5-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="263d5-151">RELATED LINKS</span></span>

