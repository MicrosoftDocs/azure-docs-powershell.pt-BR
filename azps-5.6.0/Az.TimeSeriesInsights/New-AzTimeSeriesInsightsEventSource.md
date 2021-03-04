---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: fa2573a774df86ee96563e90b617db43aed0b1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891071"
---
# <span data-ttu-id="cccdc-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="cccdc-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="cccdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cccdc-102">SYNOPSIS</span></span>
<span data-ttu-id="cccdc-103">Crie uma fonte de eventos no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="cccdc-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="cccdc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cccdc-104">SYNTAX</span></span>

### <span data-ttu-id="cccdc-105">eventhub (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cccdc-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cccdc-106">iothub</span><span class="sxs-lookup"><span data-stu-id="cccdc-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cccdc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cccdc-107">DESCRIPTION</span></span>
<span data-ttu-id="cccdc-108">Crie uma fonte de eventos no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="cccdc-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="cccdc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cccdc-109">EXAMPLES</span></span>

### <span data-ttu-id="cccdc-110">Exemplo 1: Criar uma fonte de eventos eventhub no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="cccdc-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="cccdc-111">Esse comando cria uma fonte de eventos eventhub no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="cccdc-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="cccdc-112">Exemplo 2: Criar uma fonte de eventos iothub no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="cccdc-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="cccdc-113">Este comando cria uma fonte de eventos iothub no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="cccdc-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="cccdc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cccdc-114">PARAMETERS</span></span>

### <span data-ttu-id="cccdc-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="cccdc-115">-ConsumerGroupName</span></span>
<span data-ttu-id="cccdc-116">O nome do grupo de consumidores do hub de eventos/iot que contém as partições das quais os eventos serão lidos.</span><span class="sxs-lookup"><span data-stu-id="cccdc-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="cccdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccdc-117">-DefaultProfile</span></span>
<span data-ttu-id="cccdc-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cccdc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccdc-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="cccdc-119">-EnvironmentName</span></span>
<span data-ttu-id="cccdc-120">O nome do ambiente Insights da Série de Tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="cccdc-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="cccdc-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="cccdc-121">-EventHubName</span></span>
<span data-ttu-id="cccdc-122">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="cccdc-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccdc-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="cccdc-123">-EventSourceResourceId</span></span>
<span data-ttu-id="cccdc-124">A id de recurso da fonte de eventos no Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="cccdc-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="cccdc-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="cccdc-125">-IoTHubName</span></span>
<span data-ttu-id="cccdc-126">O nome do hub de iot.</span><span class="sxs-lookup"><span data-stu-id="cccdc-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccdc-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="cccdc-127">-KeyName</span></span>
<span data-ttu-id="cccdc-128">O nome da chave SAS que concede ao serviço Insights de Série de Tempo acesso ao hub de eventos/iot.</span><span class="sxs-lookup"><span data-stu-id="cccdc-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="cccdc-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="cccdc-129">-Kind</span></span>
<span data-ttu-id="cccdc-130">O tipo da fonte de eventos.</span><span class="sxs-lookup"><span data-stu-id="cccdc-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccdc-131">-Location</span><span class="sxs-lookup"><span data-stu-id="cccdc-131">-Location</span></span>
<span data-ttu-id="cccdc-132">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="cccdc-132">The location of the resource.</span></span>

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

### <span data-ttu-id="cccdc-133">-Name</span><span class="sxs-lookup"><span data-stu-id="cccdc-133">-Name</span></span>
<span data-ttu-id="cccdc-134">Nome da origem do evento.</span><span class="sxs-lookup"><span data-stu-id="cccdc-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccdc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cccdc-135">-ResourceGroupName</span></span>
<span data-ttu-id="cccdc-136">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="cccdc-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="cccdc-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="cccdc-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="cccdc-138">O nome do barramento de serviço que contém o hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="cccdc-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccdc-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="cccdc-139">-SharedAccessKey</span></span>
<span data-ttu-id="cccdc-140">O valor da chave de acesso compartilhado que concede ao serviço insights de série de tempo acesso de leitura ao hub de eventos/iot.</span><span class="sxs-lookup"><span data-stu-id="cccdc-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccdc-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cccdc-141">-SubscriptionId</span></span>
<span data-ttu-id="cccdc-142">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="cccdc-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="cccdc-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="cccdc-143">-Tag</span></span>
<span data-ttu-id="cccdc-144">Pares de valores-chave de propriedades adicionais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="cccdc-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="cccdc-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="cccdc-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="cccdc-146">A propriedade event que será usada como o timestamp da fonte de eventos.</span><span class="sxs-lookup"><span data-stu-id="cccdc-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="cccdc-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cccdc-147">-Confirm</span></span>
<span data-ttu-id="cccdc-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cccdc-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cccdc-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cccdc-149">-WhatIf</span></span>
<span data-ttu-id="cccdc-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cccdc-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cccdc-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cccdc-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cccdc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccdc-152">CommonParameters</span></span>
<span data-ttu-id="cccdc-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccdc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccdc-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cccdc-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccdc-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cccdc-155">INPUTS</span></span>

## <span data-ttu-id="cccdc-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cccdc-156">OUTPUTS</span></span>

### <span data-ttu-id="cccdc-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="cccdc-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="cccdc-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="cccdc-158">NOTES</span></span>

<span data-ttu-id="cccdc-159">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cccdc-159">ALIASES</span></span>

## <span data-ttu-id="cccdc-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cccdc-160">RELATED LINKS</span></span>

