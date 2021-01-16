---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260326"
---
# <span data-ttu-id="f7ea6-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="f7ea6-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="f7ea6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ea6-103">Atualiza a origem do evento com o nome especificado na assinatura especificada, grupo de recursos e no ambiente.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="f7ea6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7ea6-104">SYNTAX</span></span>

### <span data-ttu-id="f7ea6-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="f7ea6-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f7ea6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f7ea6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7ea6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="f7ea6-108">Atualiza a origem do evento com o nome especificado na assinatura especificada, grupo de recursos e no ambiente.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="f7ea6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7ea6-109">EXAMPLES</span></span>

### <span data-ttu-id="f7ea6-110">Exemplo 1: atualizar uma fonte de evento especificada por nome</span><span class="sxs-lookup"><span data-stu-id="f7ea6-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="f7ea6-111">Esse comando atualiza uma fonte de eventos específica.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="f7ea6-112">Exemplo 3: atualizar uma fonte de evento especificada por objeto</span><span class="sxs-lookup"><span data-stu-id="f7ea6-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="f7ea6-113">Esse comando atualiza uma fonte de eventos específica.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="f7ea6-114">OS</span><span class="sxs-lookup"><span data-stu-id="f7ea6-114">PARAMETERS</span></span>

### <span data-ttu-id="f7ea6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ea6-115">-DefaultProfile</span></span>
<span data-ttu-id="f7ea6-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ea6-117">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="f7ea6-117">-EnvironmentName</span></span>
<span data-ttu-id="f7ea6-118">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f7ea6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7ea6-119">-InputObject</span></span>
<span data-ttu-id="f7ea6-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f7ea6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7ea6-121">-Name</span></span>
<span data-ttu-id="f7ea6-122">O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7ea6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ea6-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7ea6-124">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f7ea6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7ea6-125">-SubscriptionId</span></span>
<span data-ttu-id="f7ea6-126">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f7ea6-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="f7ea6-127">-Tag</span></span>
<span data-ttu-id="f7ea6-128">Pares de valores chave de propriedades adicionais para a fonte do evento.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="f7ea6-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f7ea6-129">-Confirm</span></span>
<span data-ttu-id="f7ea6-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7ea6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7ea6-131">-WhatIf</span></span>
<span data-ttu-id="f7ea6-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7ea6-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7ea6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ea6-134">CommonParameters</span></span>
<span data-ttu-id="f7ea6-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ea6-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7ea6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ea6-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7ea6-137">INPUTS</span></span>

### <span data-ttu-id="f7ea6-138">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="f7ea6-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f7ea6-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7ea6-139">OUTPUTS</span></span>

### <span data-ttu-id="f7ea6-140">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="f7ea6-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="f7ea6-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7ea6-141">NOTES</span></span>

<span data-ttu-id="f7ea6-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f7ea6-142">ALIASES</span></span>

<span data-ttu-id="f7ea6-143">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f7ea6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7ea6-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7ea6-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7ea6-146">INPUTobject <ITimeSeriesInsightsIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f7ea6-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7ea6-147">`[AccessPolicyName <String>]`: Nome da política de acesso.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f7ea6-148">`[EnvironmentName <String>]`: Nome do ambiente</span><span class="sxs-lookup"><span data-stu-id="f7ea6-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f7ea6-149">`[EventSourceName <String>]`: O nome da fonte de evento de insights série temporal associado ao ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f7ea6-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f7ea6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7ea6-151">`[ReferenceDataSetName <String>]`: Nome do conjunto de dados de referência.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f7ea6-152">`[ResourceGroupName <String>]`: Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f7ea6-153">`[SubscriptionId <String>]`: ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ea6-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f7ea6-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7ea6-154">RELATED LINKS</span></span>

