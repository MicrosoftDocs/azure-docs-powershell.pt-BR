---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 13db3232c7d3f2245c6a99ac9a5d38054d885a0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890416"
---
# <span data-ttu-id="a5fbd-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a5fbd-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="a5fbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fbd-103">Cria uma nova Assinatura de Evento de Grade de Eventos do Azure para um tópico, recurso do Azure, assinatura do Azure ou Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="a5fbd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a5fbd-104">SYNTAX</span></span>

### <span data-ttu-id="a5fbd-105">ResourceGroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a5fbd-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fbd-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fbd-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fbd-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fbd-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fbd-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fbd-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fbd-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fbd-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fbd-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fbd-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fbd-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fbd-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5fbd-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5fbd-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5fbd-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a5fbd-113">DESCRIPTION</span></span>
<span data-ttu-id="a5fbd-114">Crie uma nova assinatura de evento para um tópico grade de eventos do Azure, um recurso do Azure com suporte, uma assinatura do Azure ou Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="a5fbd-115">Para criar uma assinatura de evento para a assinatura do Azure selecionada no momento, especifique o nome da assinatura do evento e o ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="a5fbd-116">Para criar uma assinatura de evento para um grupo de recursos, especifique o nome do grupo de recursos, além do nome da assinatura do evento e do ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="a5fbd-117">Para criar uma assinatura de evento para um tópico grade de eventos do Azure, especifique o nome do tópico também.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="a5fbd-118">Para criar uma assinatura de evento para um recurso do Azure com suporte, especifique a ID de recurso completa do recurso.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="a5fbd-119">Para exibir a lista de tipos com suporte, execute o cmdlet Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="a5fbd-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5fbd-120">EXAMPLES</span></span>

### <span data-ttu-id="a5fbd-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5fbd-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a5fbd-122">Cria uma nova assinatura de evento EventSubscription1 para um tópico de Grade de Eventos do Azure1 no grupo de recursos \` \` \` \` \` MyResourceGroupName \` com o ponto de extremidade de destino do `https://requestb.in/19qlscd1` webhook.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="a5fbd-123">Essa assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a5fbd-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a5fbd-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a5fbd-125">Cria uma nova assinatura de evento EventSubscription1 para um grupo de recursos \` \` \` MyResourceGroupName com o ponto de extremidade \` de destino do `https://requestb.in/19qlscd1` webhook.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="a5fbd-126">Essa assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a5fbd-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a5fbd-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a5fbd-128">Cria uma nova assinatura de evento EventSubscription1 para a assinatura do Azure atualmente selecionada com o ponto de extremidade \` \` de destino do `https://requestb.in/19qlscd1` webhook.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="a5fbd-129">Essa assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a5fbd-130">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="a5fbd-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="a5fbd-131">Cria uma nova assinatura de evento EventSubscription1 para a assinatura do Azure atualmente selecionada com o ponto de extremidade \` \` de destino do `https://requestb.in/19qlscd1` webhook.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="a5fbd-132">Essa assinatura de evento especifica os filtros adicionais para tipos de eventos e assunto, e somente os eventos correspondentes a esses filtros serão entregues ao ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="a5fbd-133">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="a5fbd-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="a5fbd-134">Cria uma nova assinatura de evento EventSubscription1 para a assinatura do Azure atualmente selecionada com o hub de eventos especificado como o \` \` destino dos eventos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="a5fbd-135">Essa assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="a5fbd-136">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="a5fbd-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a5fbd-137">Cria uma nova assinatura de evento \` EventSubscription1 para um namespace EventHub com o ponto de extremidade de destino de \` webhook `https://requestb.in/19qlscd1` especificado.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="a5fbd-138">Essa assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="a5fbd-139">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a5fbd-139">PARAMETERS</span></span>

### <span data-ttu-id="a5fbd-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="a5fbd-140">-AdvancedFilter</span></span>
<span data-ttu-id="a5fbd-141">Filtro avançado que especifica uma matriz de vários valores Hashtable usados para a filtragem baseada em atributo.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="a5fbd-142">Cada valor Hashtable tem as seguintes informações de valor de tecla: Operação, Chave e Valor ou Valores.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="a5fbd-143">O operador pode ser um dos seguintes valores: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith ou StringContains.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="a5fbd-144">A chave representa a propriedade de carga onde as políticas de filtragem avançadas são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="a5fbd-145">Por fim, Valor ou Valores representam o valor ou conjunto de valores a serem matched.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="a5fbd-146">Pode ser um único valor do tipo correspondente ou uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="a5fbd-147">Como exemplo dos parâmetros de filtro avançados: $AdvancedFilters=@($AdvFilter 1, $AdvFilter 2) onde $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} e $AdvFilter 2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="a5fbd-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="a5fbd-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="a5fbd-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="a5fbd-149">O Azure Active Directory (AAD) Application Id ou Uri para obter o token de acesso que será incluído como o token de portador em solicitações de entrega. Aplicável somente para webhook como destino.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fbd-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="a5fbd-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="a5fbd-151">A ID de locatário do Azure Active Directory (AAD) para obter o token de acesso que será incluído como o token de portador em solicitações de entrega. Aplicável somente para webhook como destino.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fbd-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5fbd-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="a5fbd-153">O ponto de extremidade usado para armazenar eventos não entregues.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="a5fbd-154">Especifique a ID de recurso do Azure de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="a5fbd-155">Por exemplo: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="a5fbd-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="a5fbd-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fbd-156">-DefaultProfile</span></span>
<span data-ttu-id="a5fbd-157">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a5fbd-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5fbd-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="a5fbd-158">-DeliverySchema</span></span>
<span data-ttu-id="a5fbd-159">O esquema a ser usado ao fornecer eventos para o destino.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="a5fbd-160">Os valores possíveis são: eventgridschema, CustomInputSchema ou cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="a5fbd-161">O valor padrão é CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

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
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fbd-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="a5fbd-162">-DomainInputObject</span></span>
<span data-ttu-id="a5fbd-163">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="a5fbd-164">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a5fbd-164">-DomainName</span></span>
<span data-ttu-id="a5fbd-165">O nome do domínio da Grade de Eventos para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="a5fbd-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="a5fbd-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="a5fbd-167">Objeto EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="a5fbd-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="a5fbd-168">-DomainTopicName</span></span>
<span data-ttu-id="a5fbd-169">O nome do tópico de domínio para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="a5fbd-170">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="a5fbd-170">-Endpoint</span></span>
<span data-ttu-id="a5fbd-171">Ponto de extremidade de destino da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="a5fbd-172">Pode ser uma URL de webhook ou a ID de recurso do Azure de um EventHub, fila de armazenamento, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="a5fbd-173">Por exemplo, a ID de recurso de uma conexão híbrida tem o seguinte formulário: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="a5fbd-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="a5fbd-174">É esperado que o ponto de extremidade de destino seja criado e disponível para uso antes de executar qualquer cmdlets de Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="a5fbd-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a5fbd-175">-EndpointType</span></span>
<span data-ttu-id="a5fbd-176">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-176">Endpoint Type.</span></span>
<span data-ttu-id="a5fbd-177">Isso pode ser webhook, eventhub, storagequeue, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="a5fbd-178">O valor padrão é webhook.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

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
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fbd-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a5fbd-179">-EventSubscriptionName</span></span>
<span data-ttu-id="a5fbd-180">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="a5fbd-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="a5fbd-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="a5fbd-181">-EventTtl</span></span>
<span data-ttu-id="a5fbd-182">O tempo em minutos para a entrega do evento.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="a5fbd-183">Esse valor deve estar entre 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="a5fbd-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="a5fbd-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="a5fbd-184">-ExpirationDate</span></span>
<span data-ttu-id="a5fbd-185">Determina o DateTime de expiração para a assinatura do evento após o qual a assinatura do evento será desaposente.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="a5fbd-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="a5fbd-186">-IncludedEventType</span></span>
<span data-ttu-id="a5fbd-187">Filtro que especifica uma lista de tipos de evento a incluir. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fbd-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5fbd-188">-InputObject</span></span>
<span data-ttu-id="a5fbd-189">Objeto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a5fbd-190">-Label</span><span class="sxs-lookup"><span data-stu-id="a5fbd-190">-Label</span></span>
<span data-ttu-id="a5fbd-191">Rótulos para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="a5fbd-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fbd-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="a5fbd-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="a5fbd-193">O número máximo de tentativas para entregar o evento.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="a5fbd-194">Esse valor deve estar entre 1 e 30</span><span class="sxs-lookup"><span data-stu-id="a5fbd-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="a5fbd-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="a5fbd-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="a5fbd-196">O número máximo de eventos em um lote.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="a5fbd-197">Esse valor deve estar entre 1 e 5000.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="a5fbd-198">Esse parâmetro é válido quando Endpint Type é apenas webhook.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="a5fbd-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="a5fbd-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="a5fbd-200">O tamanho do lote preferencial em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="a5fbd-201">Esse valor deve estar entre 1 e 1024.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="a5fbd-202">Esse parâmetro é válido quando Endpint Type é apenas webhook.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="a5fbd-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5fbd-203">-ResourceGroupName</span></span>
<span data-ttu-id="a5fbd-204">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="a5fbd-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5fbd-205">-ResourceId</span></span>
<span data-ttu-id="a5fbd-206">O identificador do recurso ao qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="a5fbd-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="a5fbd-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="a5fbd-208">Filtro que especifica que somente os eventos correspondentes ao prefixo de assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="a5fbd-209">Se não for especificado, eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="a5fbd-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="a5fbd-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="a5fbd-211">Filtro que especifica que o campo de assunto deve ser comparado de forma sensível a casos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="a5fbd-212">Se não for especificado, o assunto será comparado de maneira insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="a5fbd-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="a5fbd-213">-SubjectEndsWith</span></span>
<span data-ttu-id="a5fbd-214">Filtro que especifica que somente os eventos correspondentes ao sufixo de assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="a5fbd-215">Se não for especificado, eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="a5fbd-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a5fbd-216">-TopicName</span></span>
<span data-ttu-id="a5fbd-217">O nome do tópico ao qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="a5fbd-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5fbd-218">-Confirm</span></span>
<span data-ttu-id="a5fbd-219">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5fbd-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5fbd-220">-WhatIf</span></span>
<span data-ttu-id="a5fbd-221">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5fbd-222">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5fbd-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fbd-223">CommonParameters</span></span>
<span data-ttu-id="a5fbd-224">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5fbd-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fbd-225">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5fbd-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fbd-226">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5fbd-226">INPUTS</span></span>

### <span data-ttu-id="a5fbd-227">System.String</span><span class="sxs-lookup"><span data-stu-id="a5fbd-227">System.String</span></span>

### <span data-ttu-id="a5fbd-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="a5fbd-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="a5fbd-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a5fbd-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="a5fbd-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="a5fbd-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="a5fbd-231">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a5fbd-231">System.String[]</span></span>

### <span data-ttu-id="a5fbd-232">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a5fbd-232">System.Int32</span></span>

## <span data-ttu-id="a5fbd-233">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a5fbd-233">OUTPUTS</span></span>

### <span data-ttu-id="a5fbd-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a5fbd-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a5fbd-235">NOTES</span><span class="sxs-lookup"><span data-stu-id="a5fbd-235">NOTES</span></span>

## <span data-ttu-id="a5fbd-236">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5fbd-236">RELATED LINKS</span></span>
