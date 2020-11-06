---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: f61f411f3d4f23ddfd35e2b5dcbfea07b9b85cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600871"
---
# <span data-ttu-id="866a9-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="866a9-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="866a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="866a9-102">SYNOPSIS</span></span>
<span data-ttu-id="866a9-103">Cria uma nova assinatura de evento de grade de eventos do Azure para um tópico, recurso do Azure, assinatura do Azure ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="866a9-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="866a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="866a9-104">SYNTAX</span></span>

### <span data-ttu-id="866a9-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="866a9-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866a9-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="866a9-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866a9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="866a9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866a9-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="866a9-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="866a9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="866a9-109">DESCRIPTION</span></span>
<span data-ttu-id="866a9-110">Crie uma nova assinatura de evento para um tópico de grade de eventos do Azure, um recurso do Azure compatível, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="866a9-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="866a9-111">Para criar uma assinatura de evento para a assinatura do Azure selecionada atualmente, especifique o nome da assinatura do evento e o ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="866a9-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="866a9-112">Para criar uma assinatura de evento para um grupo de recursos, especifique o nome do grupo de recursos, além do nome da assinatura do evento e do ponto de extremidade do destino.</span><span class="sxs-lookup"><span data-stu-id="866a9-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="866a9-113">Para criar uma assinatura de evento para um tópico da grade do evento do Azure, especifique também o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="866a9-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="866a9-114">Para criar uma assinatura de evento para um recurso do Azure compatível, especifique a ID do recurso completo do recurso.</span><span class="sxs-lookup"><span data-stu-id="866a9-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="866a9-115">Para exibir a lista de tipos com suporte, execute o cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="866a9-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="866a9-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="866a9-116">EXAMPLES</span></span>

### <span data-ttu-id="866a9-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="866a9-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="866a9-118">Cria uma nova assinatura de evento \` EventSubscription1 \` para um tópico de Tópico1 de grade de eventos do Azure \` \` no grupo de recursos \` MyResourceGroupName \` com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="866a9-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="866a9-119">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="866a9-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="866a9-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="866a9-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="866a9-121">Cria uma nova assinatura de evento \` EventSubscription1 \` a um grupo de recursos \` MyResourceGroupName \` com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="866a9-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="866a9-122">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="866a9-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="866a9-123">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="866a9-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="866a9-124">Cria uma nova assinatura de evento \` EventSubscription1 \` para a assinatura do Azure selecionada no momento com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="866a9-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="866a9-125">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="866a9-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="866a9-126">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="866a9-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="866a9-127">Cria uma nova assinatura de evento \` EventSubscription1 \` para a assinatura do Azure selecionada no momento com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="866a9-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="866a9-128">Essa assinatura de evento especifica os filtros adicionais para tipos de evento e assunto, e somente os eventos que correspondem a esses filtros serão entregues ao ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="866a9-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="866a9-129">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="866a9-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="866a9-130">Cria uma nova assinatura de evento \` EventSubscription1 a \` assinatura do Azure selecionada atualmente com o Hub de eventos especificado como o destino de eventos.</span><span class="sxs-lookup"><span data-stu-id="866a9-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="866a9-131">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="866a9-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="866a9-132">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="866a9-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="866a9-133">Cria uma nova assinatura de evento \` EventSubscription1 \` para um namespace do EventHub com o ponto de extremidade de destino do webhhok especificado https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="866a9-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="866a9-134">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="866a9-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="866a9-135">OS</span><span class="sxs-lookup"><span data-stu-id="866a9-135">PARAMETERS</span></span>

### <span data-ttu-id="866a9-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="866a9-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="866a9-137">O ponto de extremidade usado para armazenar eventos não entregues.</span><span class="sxs-lookup"><span data-stu-id="866a9-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="866a9-138">Especifique a ID do recurso do Azure de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="866a9-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="866a9-139">Por exemplo:/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="866a9-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866a9-140">-DefaultProfile</span></span>
<span data-ttu-id="866a9-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="866a9-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-142">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="866a9-142">-Endpoint</span></span>
<span data-ttu-id="866a9-143">Ponto de extremidade de assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="866a9-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="866a9-144">Pode ser uma URL do webhook ou a ID do recurso do Azure de um EventHub, fila de armazenamento ou hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="866a9-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="866a9-145">Por exemplo, a ID do recurso para uma conexão híbrida tem o seguinte formato:/subscriptions/[ID da assinatura do Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="866a9-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="866a9-146">Espera-se que o ponto de extremidade de destino seja criado e esteja disponível para uso antes de executar cmdlets de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="866a9-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="866a9-147">-EndpointType</span></span>
<span data-ttu-id="866a9-148">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="866a9-148">Endpoint Type.</span></span>
<span data-ttu-id="866a9-149">Pode ser webhook, eventhub, storagequeue ou hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="866a9-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="866a9-150">O valor padrão é webhook.</span><span class="sxs-lookup"><span data-stu-id="866a9-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="866a9-151">-EventSubscriptionName</span></span>
<span data-ttu-id="866a9-152">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="866a9-152">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="866a9-153">-EventTtl</span></span>
<span data-ttu-id="866a9-154">O tempo em minutos para a entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="866a9-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="866a9-155">Esse valor deve estar entre 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="866a9-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="866a9-156">-IncludedEventType</span></span>
<span data-ttu-id="866a9-157">Filtro que especifica uma lista de tipos de eventos a serem incluídos. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="866a9-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="866a9-158">-InputObject</span></span>
<span data-ttu-id="866a9-159">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="866a9-159">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-160">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="866a9-160">-Label</span></span>
<span data-ttu-id="866a9-161">Etiquetas para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="866a9-161">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="866a9-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="866a9-163">O número máximo de tentativas de entregar o evento.</span><span class="sxs-lookup"><span data-stu-id="866a9-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="866a9-164">Esse valor deve estar entre 1 e 30</span><span class="sxs-lookup"><span data-stu-id="866a9-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866a9-165">-ResourceGroupName</span></span>
<span data-ttu-id="866a9-166">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="866a9-166">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="866a9-167">-ResourceId</span></span>
<span data-ttu-id="866a9-168">O identificador do recurso para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="866a9-168">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="866a9-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="866a9-170">Filtro que especifica que somente os eventos que correspondem ao prefixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="866a9-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="866a9-171">Se não for especificado, os eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="866a9-171">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="866a9-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="866a9-173">Filtro que especifica que o campo assunto deve ser comparado em uma maneira sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="866a9-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="866a9-174">Se não for especificado, o assunto será comparado em uma maneira não sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="866a9-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="866a9-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="866a9-175">-SubjectEndsWith</span></span>
<span data-ttu-id="866a9-176">Filtro que especifica que somente os eventos que correspondem ao sufixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="866a9-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="866a9-177">Se não for especificado, os eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="866a9-177">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-178">-Topicname</span><span class="sxs-lookup"><span data-stu-id="866a9-178">-TopicName</span></span>
<span data-ttu-id="866a9-179">O nome do tópico para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="866a9-179">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866a9-180">-Confirme</span><span class="sxs-lookup"><span data-stu-id="866a9-180">-Confirm</span></span>
<span data-ttu-id="866a9-181">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866a9-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866a9-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866a9-182">-WhatIf</span></span>
<span data-ttu-id="866a9-183">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="866a9-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="866a9-184">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="866a9-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866a9-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866a9-185">CommonParameters</span></span>
<span data-ttu-id="866a9-186">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866a9-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866a9-187">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866a9-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866a9-188">SENSORES</span><span class="sxs-lookup"><span data-stu-id="866a9-188">INPUTS</span></span>

### <span data-ttu-id="866a9-189">System. String</span><span class="sxs-lookup"><span data-stu-id="866a9-189">System.String</span></span>

### <span data-ttu-id="866a9-190">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="866a9-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="866a9-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="866a9-191">System.String[]</span></span>

## <span data-ttu-id="866a9-192">EXIBE</span><span class="sxs-lookup"><span data-stu-id="866a9-192">OUTPUTS</span></span>

### <span data-ttu-id="866a9-193">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="866a9-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="866a9-194">INFORMA</span><span class="sxs-lookup"><span data-stu-id="866a9-194">NOTES</span></span>

## <span data-ttu-id="866a9-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="866a9-195">RELATED LINKS</span></span>
