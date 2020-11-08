---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125683"
---
# <span data-ttu-id="18f0b-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="18f0b-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="18f0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="18f0b-103">Criar uma fonte de eventos no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18f0b-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="18f0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18f0b-104">SYNTAX</span></span>

### <span data-ttu-id="18f0b-105">eventhub (padrão)</span><span class="sxs-lookup"><span data-stu-id="18f0b-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18f0b-106">iothub</span><span class="sxs-lookup"><span data-stu-id="18f0b-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18f0b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18f0b-107">DESCRIPTION</span></span>
<span data-ttu-id="18f0b-108">Criar uma fonte de eventos no ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18f0b-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="18f0b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18f0b-109">EXAMPLES</span></span>

### <span data-ttu-id="18f0b-110">Exemplo 1: criar uma fonte de evento do eventhub no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="18f0b-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="18f0b-111">Esse comando cria uma fonte de evento do eventhub sob o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18f0b-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="18f0b-112">Exemplo 2: criar uma fonte de eventos iothub no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="18f0b-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="18f0b-113">Esse comando cria uma fonte de eventos iothub sob o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="18f0b-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="18f0b-114">OS</span><span class="sxs-lookup"><span data-stu-id="18f0b-114">PARAMETERS</span></span>

### <span data-ttu-id="18f0b-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="18f0b-115">-ConsumerGroupName</span></span>
<span data-ttu-id="18f0b-116">O nome do grupo de consumidores do evento/Hub IOT que mantém as partições dos quais os eventos serão lidos.</span><span class="sxs-lookup"><span data-stu-id="18f0b-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="18f0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f0b-117">-DefaultProfile</span></span>
<span data-ttu-id="18f0b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18f0b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18f0b-119">-Environmentname</span><span class="sxs-lookup"><span data-stu-id="18f0b-119">-EnvironmentName</span></span>
<span data-ttu-id="18f0b-120">O nome do ambiente do insights de série temporal associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="18f0b-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="18f0b-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="18f0b-121">-EventHubName</span></span>
<span data-ttu-id="18f0b-122">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="18f0b-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="18f0b-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="18f0b-123">-EventSourceResourceId</span></span>
<span data-ttu-id="18f0b-124">A ID do recurso da fonte do evento no Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="18f0b-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="18f0b-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="18f0b-125">-IoTHubName</span></span>
<span data-ttu-id="18f0b-126">O nome do Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="18f0b-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="18f0b-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="18f0b-127">-KeyName</span></span>
<span data-ttu-id="18f0b-128">O nome da chave SAS que concede o acesso do serviço insights de série de tempo ao Hub Event/IOT.</span><span class="sxs-lookup"><span data-stu-id="18f0b-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="18f0b-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="18f0b-129">-Kind</span></span>
<span data-ttu-id="18f0b-130">O tipo da fonte do evento.</span><span class="sxs-lookup"><span data-stu-id="18f0b-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="18f0b-131">-Local</span><span class="sxs-lookup"><span data-stu-id="18f0b-131">-Location</span></span>
<span data-ttu-id="18f0b-132">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="18f0b-132">The location of the resource.</span></span>

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

### <span data-ttu-id="18f0b-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="18f0b-133">-Name</span></span>
<span data-ttu-id="18f0b-134">Nome da fonte do evento.</span><span class="sxs-lookup"><span data-stu-id="18f0b-134">Name of the event source.</span></span>

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

### <span data-ttu-id="18f0b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18f0b-135">-ResourceGroupName</span></span>
<span data-ttu-id="18f0b-136">Nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="18f0b-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="18f0b-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="18f0b-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="18f0b-138">O nome do barramento do serviço que contém o Hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="18f0b-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="18f0b-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="18f0b-139">-SharedAccessKey</span></span>
<span data-ttu-id="18f0b-140">O valor da chave de acesso compartilhada que concede acesso de leitura ao serviço de insights série tempo ao Hub evento/IOT.</span><span class="sxs-lookup"><span data-stu-id="18f0b-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="18f0b-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18f0b-141">-SubscriptionId</span></span>
<span data-ttu-id="18f0b-142">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="18f0b-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="18f0b-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="18f0b-143">-Tag</span></span>
<span data-ttu-id="18f0b-144">Pares de valores chave de propriedades adicionais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="18f0b-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="18f0b-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="18f0b-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="18f0b-146">A propriedade de evento que será usada como carimbo de data/hora da fonte do evento.</span><span class="sxs-lookup"><span data-stu-id="18f0b-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="18f0b-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18f0b-147">-Confirm</span></span>
<span data-ttu-id="18f0b-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18f0b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18f0b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18f0b-149">-WhatIf</span></span>
<span data-ttu-id="18f0b-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18f0b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18f0b-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18f0b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18f0b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f0b-152">CommonParameters</span></span>
<span data-ttu-id="18f0b-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18f0b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f0b-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18f0b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f0b-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18f0b-155">INPUTS</span></span>

## <span data-ttu-id="18f0b-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18f0b-156">OUTPUTS</span></span>

### <span data-ttu-id="18f0b-157">Microsoft. Azure. PowerShell. cmdlets. TimeSeriesInsights. Models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="18f0b-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="18f0b-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18f0b-158">NOTES</span></span>

<span data-ttu-id="18f0b-159">ALIASES</span><span class="sxs-lookup"><span data-stu-id="18f0b-159">ALIASES</span></span>

## <span data-ttu-id="18f0b-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18f0b-160">RELATED LINKS</span></span>

