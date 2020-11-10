---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1e2ac4d8763376da6854b3c5d1551e4213f25f60
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395298"
---
# <span data-ttu-id="d6dc9-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d6dc9-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="d6dc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dc9-103">Cria uma nova assinatura de evento de grade de eventos do Azure para um tópico, recurso do Azure, assinatura do Azure ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="d6dc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6dc9-104">SYNTAX</span></span>

### <span data-ttu-id="d6dc9-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6dc9-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dc9-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc9-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dc9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dc9-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc9-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dc9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dc9-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc9-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dc9-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc9-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6dc9-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6dc9-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6dc9-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6dc9-113">DESCRIPTION</span></span>
<span data-ttu-id="d6dc9-114">Crie uma nova assinatura de evento para um tópico de grade de eventos do Azure, um recurso do Azure compatível, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="d6dc9-115">Para criar uma assinatura de evento para a assinatura do Azure selecionada atualmente, especifique o nome da assinatura do evento e o ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="d6dc9-116">Para criar uma assinatura de evento para um grupo de recursos, especifique o nome do grupo de recursos, além do nome da assinatura do evento e do ponto de extremidade do destino.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="d6dc9-117">Para criar uma assinatura de evento para um tópico da grade do evento do Azure, especifique também o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="d6dc9-118">Para criar uma assinatura de evento para um recurso do Azure compatível, especifique a ID do recurso completo do recurso.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="d6dc9-119">Para exibir a lista de tipos com suporte, execute o cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="d6dc9-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6dc9-120">EXAMPLES</span></span>

### <span data-ttu-id="d6dc9-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6dc9-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d6dc9-122">Cria uma nova assinatura de evento \` EventSubscription1 \` para um tópico de Tópico1 de grade de eventos do Azure \` \` no grupo de recursos \` MyResourceGroupName \` com o ponto de extremidade de destino do webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d6dc9-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d6dc9-123">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d6dc9-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d6dc9-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d6dc9-125">Cria uma nova assinatura de evento \` EventSubscription1 \` a um grupo de recursos \` MyResourceGroupName \` com o ponto de extremidade de destino do webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d6dc9-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d6dc9-126">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d6dc9-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d6dc9-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d6dc9-128">Cria uma nova assinatura de evento \` EventSubscription1 \` para a assinatura do Azure selecionada no momento com o ponto de extremidade de destino do webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d6dc9-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d6dc9-129">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d6dc9-130">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="d6dc9-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="d6dc9-131">Cria uma nova assinatura de evento \` EventSubscription1 \` para a assinatura do Azure selecionada no momento com o ponto de extremidade de destino do webhook `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d6dc9-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d6dc9-132">Essa assinatura de evento especifica os filtros adicionais para tipos de evento e assunto, e somente os eventos que correspondem a esses filtros serão entregues ao ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="d6dc9-133">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="d6dc9-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="d6dc9-134">Cria uma nova assinatura de evento \` EventSubscription1 a \` assinatura do Azure selecionada atualmente com o Hub de eventos especificado como o destino de eventos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="d6dc9-135">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="d6dc9-136">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="d6dc9-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="d6dc9-137">Cria uma nova assinatura de evento \` EventSubscription1 \` para um namespace do EventHub com o ponto de extremidade de destino do webhook especificado `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="d6dc9-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="d6dc9-138">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="d6dc9-139">OS</span><span class="sxs-lookup"><span data-stu-id="d6dc9-139">PARAMETERS</span></span>

### <span data-ttu-id="d6dc9-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="d6dc9-140">-AdvancedFilter</span></span>
<span data-ttu-id="d6dc9-141">Filtro avançado que especifica uma matriz de vários valores de Hashtable usados para a filtragem baseada em atributo.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="d6dc9-142">Cada valor de Hashtable tem as seguintes informações de valor-chave: operação, chave e valor ou valores.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="d6dc9-143">Operator pode ser um dos seguintes valores: Numberie, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, Stringem, StringNotIn, StringBeginsWith, StringEndsWith ou StringContains.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="d6dc9-144">Chave representa a Propriedade Payload na qual as políticas de filtragem avançada são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="d6dc9-145">Por fim, valor ou valores representam o valor ou o conjunto de valores a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="d6dc9-146">Pode ser um valor único do tipo correspondente ou uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="d6dc9-147">Como um exemplo dos parâmetros de filtro avançado: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) onde $AdvFilter 1 = @ {Operator = "Numberem"; Key = "Data. key1"; Valores = @ (1, 2)} e $AdvFilter 2 = @ {Operator = "StringBringsWith"; Key = "Subject"; Valores = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="d6dc9-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="d6dc9-148">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6dc9-148">-DeadLetterEndpoint</span></span>
<span data-ttu-id="d6dc9-149">O ponto de extremidade usado para armazenar eventos não entregues.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-149">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="d6dc9-150">Especifique a ID do recurso do Azure de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-150">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="d6dc9-151">Por exemplo:/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="d6dc9-151">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dc9-152">-DefaultProfile</span></span>
<span data-ttu-id="d6dc9-153">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d6dc9-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6dc9-154">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="d6dc9-154">-DomainInputObject</span></span>
<span data-ttu-id="d6dc9-155">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-155">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-156">-DomainName</span><span class="sxs-lookup"><span data-stu-id="d6dc9-156">-DomainName</span></span>
<span data-ttu-id="d6dc9-157">O nome do domínio da grade de eventos para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-157">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-158">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="d6dc9-158">-DomainTopicInputObject</span></span>
<span data-ttu-id="d6dc9-159">Objeto de tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-159">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-160">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="d6dc9-160">-DomainTopicName</span></span>
<span data-ttu-id="d6dc9-161">O nome do tópico de domínio para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-161">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-162">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="d6dc9-162">-Endpoint</span></span>
<span data-ttu-id="d6dc9-163">Ponto de extremidade de assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-163">Event subscription destination endpoint.</span></span>
<span data-ttu-id="d6dc9-164">Pode ser uma URL do webhook ou a ID do recurso do Azure de um EventHub, fila de armazenamento, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-164">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="d6dc9-165">Por exemplo, a ID do recurso para uma conexão híbrida tem o seguinte formato:/subscriptions/[ID da assinatura do Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="d6dc9-165">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="d6dc9-166">Espera-se que o ponto de extremidade de destino seja criado e esteja disponível para uso antes de executar cmdlets de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-166">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-167">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="d6dc9-167">-EndpointType</span></span>
<span data-ttu-id="d6dc9-168">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-168">Endpoint Type.</span></span>
<span data-ttu-id="d6dc9-169">Pode ser webhook, eventhub, storagequeue, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-169">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="d6dc9-170">O valor padrão é webhook.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-170">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-171">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d6dc9-171">-EventSubscriptionName</span></span>
<span data-ttu-id="d6dc9-172">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="d6dc9-172">The name of the event subscription</span></span>

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

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-173">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="d6dc9-173">-EventTtl</span></span>
<span data-ttu-id="d6dc9-174">O tempo em minutos para a entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-174">The time in minutes for the event delivery.</span></span> <span data-ttu-id="d6dc9-175">Esse valor deve estar entre 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="d6dc9-175">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-176">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="d6dc9-176">-ExpirationDate</span></span>
<span data-ttu-id="d6dc9-177">Determina a data de expiração para a assinatura do evento após a qual a assinatura do evento será desativada.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-177">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="d6dc9-178">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="d6dc9-178">-IncludedEventType</span></span>
<span data-ttu-id="d6dc9-179">Filtro que especifica uma lista de tipos de eventos a serem incluídos. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-179">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6dc9-180">-InputObject</span></span>
<span data-ttu-id="d6dc9-181">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-181">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d6dc9-182">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="d6dc9-182">-Label</span></span>
<span data-ttu-id="d6dc9-183">Etiquetas para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="d6dc9-183">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-184">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="d6dc9-184">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="d6dc9-185">O número máximo de tentativas de entregar o evento.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-185">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="d6dc9-186">Esse valor deve estar entre 1 e 30</span><span class="sxs-lookup"><span data-stu-id="d6dc9-186">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-187">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6dc9-187">-ResourceGroupName</span></span>
<span data-ttu-id="d6dc9-188">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-188">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-189">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6dc9-189">-ResourceId</span></span>
<span data-ttu-id="d6dc9-190">O identificador do recurso para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-190">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d6dc9-191">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="d6dc9-191">-SubjectBeginsWith</span></span>
<span data-ttu-id="d6dc9-192">Filtro que especifica que somente os eventos que correspondem ao prefixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-192">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="d6dc9-193">Se não for especificado, os eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-193">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-194">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="d6dc9-194">-SubjectCaseSensitive</span></span>
<span data-ttu-id="d6dc9-195">Filtro que especifica que o campo assunto deve ser comparado em uma maneira sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-195">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="d6dc9-196">Se não for especificado, o assunto será comparado em uma maneira não sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-196">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="d6dc9-197">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="d6dc9-197">-SubjectEndsWith</span></span>
<span data-ttu-id="d6dc9-198">Filtro que especifica que somente os eventos que correspondem ao sufixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-198">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="d6dc9-199">Se não for especificado, os eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-199">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6dc9-200">-Topicname</span><span class="sxs-lookup"><span data-stu-id="d6dc9-200">-TopicName</span></span>
<span data-ttu-id="d6dc9-201">O nome do tópico para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-201">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="d6dc9-202">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6dc9-202">-Confirm</span></span>
<span data-ttu-id="d6dc9-203">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6dc9-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6dc9-204">-WhatIf</span></span>
<span data-ttu-id="d6dc9-205">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-205">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6dc9-206">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6dc9-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dc9-207">CommonParameters</span></span>
<span data-ttu-id="d6dc9-208">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6dc9-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dc9-209">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6dc9-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dc9-210">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6dc9-210">INPUTS</span></span>

### <span data-ttu-id="d6dc9-211">System. String</span><span class="sxs-lookup"><span data-stu-id="d6dc9-211">System.String</span></span>

### <span data-ttu-id="d6dc9-212">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="d6dc9-212">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="d6dc9-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="d6dc9-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="d6dc9-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d6dc9-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="d6dc9-215">System. String []</span><span class="sxs-lookup"><span data-stu-id="d6dc9-215">System.String[]</span></span>

### <span data-ttu-id="d6dc9-216">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d6dc9-216">System.Int32</span></span>

## <span data-ttu-id="d6dc9-217">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6dc9-217">OUTPUTS</span></span>

### <span data-ttu-id="d6dc9-218">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="d6dc9-218">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="d6dc9-219">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6dc9-219">NOTES</span></span>

## <span data-ttu-id="d6dc9-220">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6dc9-220">RELATED LINKS</span></span>
