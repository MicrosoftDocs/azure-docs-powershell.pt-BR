---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: c28d33e4da860a68227228564c55a151a3068329
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888588"
---
# <span data-ttu-id="18aa3-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="18aa3-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="18aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="18aa3-103">Obtém a origem do evento com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18aa3-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="18aa3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="18aa3-104">SYNTAX</span></span>

### <span data-ttu-id="18aa3-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18aa3-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18aa3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="18aa3-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18aa3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18aa3-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="18aa3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="18aa3-108">DESCRIPTION</span></span>
<span data-ttu-id="18aa3-109">Obtém a origem do evento com o nome especificado no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18aa3-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="18aa3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18aa3-110">EXAMPLES</span></span>

### <span data-ttu-id="18aa3-111">Exemplo 1: listar todas as fontes de eventos no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="18aa3-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="18aa3-112">Este comando lista todas as fontes de eventos nos ambientes especificados.</span><span class="sxs-lookup"><span data-stu-id="18aa3-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="18aa3-113">Exemplo 2: Obter uma fonte de eventos especificada pelo nome</span><span class="sxs-lookup"><span data-stu-id="18aa3-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="18aa3-114">Este comando obtém uma fonte de evento específica.</span><span class="sxs-lookup"><span data-stu-id="18aa3-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="18aa3-115">Exemplo 3: Obter uma fonte de evento especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="18aa3-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="18aa3-116">Este comando obtém uma fonte de evento específica.</span><span class="sxs-lookup"><span data-stu-id="18aa3-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="18aa3-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="18aa3-117">PARAMETERS</span></span>

### <span data-ttu-id="18aa3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18aa3-118">-DefaultProfile</span></span>
<span data-ttu-id="18aa3-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18aa3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18aa3-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="18aa3-120">-EnvironmentName</span></span>
<span data-ttu-id="18aa3-121">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="18aa3-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="18aa3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18aa3-122">-InputObject</span></span>
<span data-ttu-id="18aa3-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="18aa3-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18aa3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="18aa3-124">-Name</span></span>
<span data-ttu-id="18aa3-125">O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18aa3-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18aa3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18aa3-126">-ResourceGroupName</span></span>
<span data-ttu-id="18aa3-127">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="18aa3-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="18aa3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18aa3-128">-SubscriptionId</span></span>
<span data-ttu-id="18aa3-129">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="18aa3-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18aa3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18aa3-130">CommonParameters</span></span>
<span data-ttu-id="18aa3-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18aa3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18aa3-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18aa3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18aa3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18aa3-133">INPUTS</span></span>

### <span data-ttu-id="18aa3-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="18aa3-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="18aa3-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="18aa3-135">OUTPUTS</span></span>

### <span data-ttu-id="18aa3-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="18aa3-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="18aa3-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="18aa3-137">NOTES</span></span>

<span data-ttu-id="18aa3-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="18aa3-138">ALIASES</span></span>

<span data-ttu-id="18aa3-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="18aa3-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18aa3-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="18aa3-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18aa3-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18aa3-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18aa3-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="18aa3-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18aa3-143">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="18aa3-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="18aa3-144">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="18aa3-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="18aa3-145">`[EventSourceName <String>]`: O nome da fonte de eventos Insights da Série de Tempo associada ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18aa3-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="18aa3-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="18aa3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18aa3-147">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="18aa3-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="18aa3-148">`[ResourceGroupName <String>]`: Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="18aa3-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="18aa3-149">`[SubscriptionId <String>]`: ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="18aa3-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="18aa3-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18aa3-150">RELATED LINKS</span></span>

