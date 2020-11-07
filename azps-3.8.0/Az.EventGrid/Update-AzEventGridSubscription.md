---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: d4967dd45cc420035a4be60736389729d019fd45
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940930"
---
# <span data-ttu-id="2b3f5-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2b3f5-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="2b3f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3f5-103">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="2b3f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b3f5-104">SYNTAX</span></span>

### <span data-ttu-id="2b3f5-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b3f5-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3f5-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b3f5-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b3f5-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b3f5-111">DESCRIPTION</span></span>
<span data-ttu-id="2b3f5-112">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="2b3f5-113">Isso pode ser usado para atualizar o filtro, o destino ou os rótulos de uma assinatura de evento existente.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="2b3f5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b3f5-114">EXAMPLES</span></span>

### <span data-ttu-id="2b3f5-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2b3f5-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="2b3f5-116">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="2b3f5-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="2b3f5-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2b3f5-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="2b3f5-118">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="2b3f5-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="2b3f5-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2b3f5-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="2b3f5-120">Atualiza as propriedades da assinatura de evento \` ES1 \` para o namespace do EventHub ContosoNamespace com o novo ponto de extremidade como \` https://requestb.in/1kxxoui1\ "e o novo filtro SubjectEndsWith como \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="2b3f5-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="2b3f5-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="2b3f5-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="2b3f5-122">Atualiza as propriedades da assinatura do evento \` ES1 \` para o MyResourceGroupName do grupo de recursos \` \` com os novos rótulos $Labels.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="2b3f5-123">OS</span><span class="sxs-lookup"><span data-stu-id="2b3f5-123">PARAMETERS</span></span>

### <span data-ttu-id="2b3f5-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="2b3f5-124">-AdvancedFilter</span></span>
<span data-ttu-id="2b3f5-125">Filtro avançado que especifica uma matriz de vários valores de Hashtable usados para a filtragem baseada em atributo.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="2b3f5-126">Cada valor de Hashtable tem as seguintes informações de valor-chave: operação, chave e valor ou valores.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="2b3f5-127">Operator pode ser um dos seguintes valores: Numberie, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, Stringem, StringNotIn, StringBeginsWith, StringEndsWith ou StringContains.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="2b3f5-128">Chave representa a Propriedade Payload na qual as políticas de filtragem avançada são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="2b3f5-129">Por fim, valor ou valores representam o valor ou o conjunto de valores a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="2b3f5-130">Pode ser um valor único do tipo correspondente ou uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="2b3f5-131">Como um exemplo dos parâmetros de filtro avançado: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) onde $AdvFilter 1 = @ {Operator = "Numberem"; Key = "Data. key1"; Valores = @ (1, 2)} e $AdvFilter 2 = @ {Operator = "StringBringsWith"; Key = "Subject"; Valores = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="2b3f5-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b3f5-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="2b3f5-133">O ponto de extremidade usado para armazenar eventos não entregues.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="2b3f5-134">Especifique a ID do recurso do Azure de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="2b3f5-135">Por exemplo:/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="2b3f5-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="2b3f5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3f5-136">-DefaultProfile</span></span>
<span data-ttu-id="2b3f5-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b3f5-138">-DomainName</span><span class="sxs-lookup"><span data-stu-id="2b3f5-138">-DomainName</span></span>
<span data-ttu-id="2b3f5-139">O nome do domínio para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="2b3f5-140">-DomainTopicName</span></span>
<span data-ttu-id="2b3f5-141">O nome do tópico de domínio para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-142">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="2b3f5-142">-Endpoint</span></span>
<span data-ttu-id="2b3f5-143">Ponto de extremidade de assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="2b3f5-144">Pode ser uma URL do webhook ou a ID do recurso do Azure de um EventHub, fila de armazenamento, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="2b3f5-145">Por exemplo, a ID do recurso para uma conexão híbrida tem o seguinte formato:/subscriptions/[ID da assinatura do Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="2b3f5-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="2b3f5-146">Espera-se que o ponto de extremidade de destino seja criado e esteja disponível para uso antes de executar cmdlets de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="2b3f5-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="2b3f5-147">-EndpointType</span></span>
<span data-ttu-id="2b3f5-148">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-148">Endpoint Type.</span></span>
<span data-ttu-id="2b3f5-149">Pode ser webhook, eventhub, storagequeue, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="2b3f5-150">O valor padrão é webhook.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2b3f5-151">-EventSubscriptionName</span></span>
<span data-ttu-id="2b3f5-152">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="2b3f5-152">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="2b3f5-153">-EventTtl</span></span>
<span data-ttu-id="2b3f5-154">O tempo em minutos para a entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="2b3f5-155">Esse valor deve estar entre 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="2b3f5-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-156">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="2b3f5-156">-ExpirationDate</span></span>
<span data-ttu-id="2b3f5-157">Determina a data de expiração para a assinatura do evento após a qual a assinatura do evento será desativada.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="2b3f5-158">-IncludedEventType</span></span>
<span data-ttu-id="2b3f5-159">Filtro que especifica uma lista de tipos de eventos a serem incluídos. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b3f5-160">-InputObject</span></span>
<span data-ttu-id="2b3f5-161">Objeto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-161">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-162">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="2b3f5-162">-Label</span></span>
<span data-ttu-id="2b3f5-163">Etiquetas para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="2b3f5-163">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-164">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="2b3f5-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="2b3f5-165">O número máximo de tentativas de entregar o evento.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="2b3f5-166">Esse valor deve estar entre 1 e 30</span><span class="sxs-lookup"><span data-stu-id="2b3f5-166">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3f5-167">-ResourceGroupName</span></span>
<span data-ttu-id="2b3f5-168">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-168">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b3f5-169">-ResourceId</span></span>
<span data-ttu-id="2b3f5-170">O identificador do recurso para o qual a assinatura de evento foi criada.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="2b3f5-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="2b3f5-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="2b3f5-172">Filtro que especifica que somente os eventos que correspondem ao prefixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="2b3f5-173">Se não for especificado, os eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-173">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="2b3f5-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="2b3f5-174">-SubjectEndsWith</span></span>
<span data-ttu-id="2b3f5-175">Filtro que especifica que somente os eventos que correspondem ao sufixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="2b3f5-176">Se não for especificado, os eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-176">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="2b3f5-177">-Topicname</span><span class="sxs-lookup"><span data-stu-id="2b3f5-177">-TopicName</span></span>
<span data-ttu-id="2b3f5-178">O nome do tópico para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-178">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f5-179">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2b3f5-179">-Confirm</span></span>
<span data-ttu-id="2b3f5-180">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b3f5-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3f5-181">-WhatIf</span></span>
<span data-ttu-id="2b3f5-182">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b3f5-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b3f5-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3f5-184">CommonParameters</span></span>
<span data-ttu-id="2b3f5-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3f5-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3f5-186">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3f5-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3f5-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b3f5-187">INPUTS</span></span>

### <span data-ttu-id="2b3f5-188">System. String</span><span class="sxs-lookup"><span data-stu-id="2b3f5-188">System.String</span></span>

### <span data-ttu-id="2b3f5-189">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="2b3f5-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="2b3f5-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b3f5-190">OUTPUTS</span></span>

### <span data-ttu-id="2b3f5-191">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="2b3f5-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="2b3f5-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b3f5-192">NOTES</span></span>

## <span data-ttu-id="2b3f5-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b3f5-193">RELATED LINKS</span></span>
