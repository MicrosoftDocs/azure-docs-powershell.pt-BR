---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118865"
---
# <span data-ttu-id="5882d-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="5882d-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="5882d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5882d-102">SYNOPSIS</span></span>
<span data-ttu-id="5882d-103">Crie uma fonte de eventos sob o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="5882d-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="5882d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5882d-104">SYNTAX</span></span>

### <span data-ttu-id="5882d-105">eventhub (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5882d-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5882d-106">iothub</span><span class="sxs-lookup"><span data-stu-id="5882d-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5882d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5882d-107">DESCRIPTION</span></span>
<span data-ttu-id="5882d-108">Crie uma fonte de eventos sob o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="5882d-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="5882d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5882d-109">EXAMPLES</span></span>

### <span data-ttu-id="5882d-110">Exemplo 1: Criar uma fonte de eventos do eventhub sob o ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="5882d-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="5882d-111">Esse comando cria uma fonte de eventos eventhub sob o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="5882d-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="5882d-112">Exemplo 2: Criar uma fonte de eventos do iothub no ambiente especificado</span><span class="sxs-lookup"><span data-stu-id="5882d-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="5882d-113">Esse comando cria uma fonte de eventos do iothub sob o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="5882d-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="5882d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5882d-114">PARAMETERS</span></span>

### <span data-ttu-id="5882d-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5882d-115">-ConsumerGroupName</span></span>
<span data-ttu-id="5882d-116">O nome do grupo de consumidor do hub de eventos/iot que retém as partições das quais os eventos serão lidos.</span><span class="sxs-lookup"><span data-stu-id="5882d-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="5882d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5882d-117">-DefaultProfile</span></span>
<span data-ttu-id="5882d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5882d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5882d-119">-Nome do Ambiente</span><span class="sxs-lookup"><span data-stu-id="5882d-119">-EnvironmentName</span></span>
<span data-ttu-id="5882d-120">O nome do ambiente insights de série de tempo associado ao grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="5882d-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="5882d-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="5882d-121">-EventHubName</span></span>
<span data-ttu-id="5882d-122">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="5882d-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="5882d-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="5882d-123">-EventSourceResourceId</span></span>
<span data-ttu-id="5882d-124">A ID do recurso da fonte de eventos no Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5882d-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="5882d-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="5882d-125">-IoTHubName</span></span>
<span data-ttu-id="5882d-126">O nome do hub iot.</span><span class="sxs-lookup"><span data-stu-id="5882d-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="5882d-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5882d-127">-KeyName</span></span>
<span data-ttu-id="5882d-128">O nome da chave SAS que concede ao serviço Insights de Série de Tempo acesso ao hub de eventos/iot.</span><span class="sxs-lookup"><span data-stu-id="5882d-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="5882d-129">-Tipo</span><span class="sxs-lookup"><span data-stu-id="5882d-129">-Kind</span></span>
<span data-ttu-id="5882d-130">O tipo de fonte de evento.</span><span class="sxs-lookup"><span data-stu-id="5882d-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="5882d-131">-Local</span><span class="sxs-lookup"><span data-stu-id="5882d-131">-Location</span></span>
<span data-ttu-id="5882d-132">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="5882d-132">The location of the resource.</span></span>

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

### <span data-ttu-id="5882d-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="5882d-133">-Name</span></span>
<span data-ttu-id="5882d-134">Nome da fonte do evento.</span><span class="sxs-lookup"><span data-stu-id="5882d-134">Name of the event source.</span></span>

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

### <span data-ttu-id="5882d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5882d-135">-ResourceGroupName</span></span>
<span data-ttu-id="5882d-136">Nome de um grupo de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5882d-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="5882d-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="5882d-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="5882d-138">O nome do barramento de serviço que contém o hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="5882d-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="5882d-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="5882d-139">-SharedAccessKey</span></span>
<span data-ttu-id="5882d-140">O valor da chave de acesso compartilhado que concede ao serviço Insights de Série de Tempo acesso de leitura ao hub de eventos/iot.</span><span class="sxs-lookup"><span data-stu-id="5882d-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="5882d-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5882d-141">-SubscriptionId</span></span>
<span data-ttu-id="5882d-142">ID de Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5882d-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5882d-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="5882d-143">-Tag</span></span>
<span data-ttu-id="5882d-144">Pares de valor-chave de propriedades adicionais para o recurso.</span><span class="sxs-lookup"><span data-stu-id="5882d-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="5882d-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="5882d-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="5882d-146">A propriedade do evento que será usada como data/hora da fonte do evento.</span><span class="sxs-lookup"><span data-stu-id="5882d-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="5882d-147">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5882d-147">-Confirm</span></span>
<span data-ttu-id="5882d-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5882d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5882d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5882d-149">-WhatIf</span></span>
<span data-ttu-id="5882d-150">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5882d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5882d-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5882d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5882d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5882d-152">CommonParameters</span></span>
<span data-ttu-id="5882d-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5882d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5882d-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5882d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5882d-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="5882d-155">INPUTS</span></span>

## <span data-ttu-id="5882d-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="5882d-156">OUTPUTS</span></span>

### <span data-ttu-id="5882d-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="5882d-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="5882d-158">Notas</span><span class="sxs-lookup"><span data-stu-id="5882d-158">NOTES</span></span>

<span data-ttu-id="5882d-159">Aliases</span><span class="sxs-lookup"><span data-stu-id="5882d-159">ALIASES</span></span>

## <span data-ttu-id="5882d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5882d-160">RELATED LINKS</span></span>

