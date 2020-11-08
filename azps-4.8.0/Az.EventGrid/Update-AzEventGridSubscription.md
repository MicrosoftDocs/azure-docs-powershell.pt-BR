---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114977"
---
# <span data-ttu-id="767f8-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="767f8-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="767f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="767f8-102">SYNOPSIS</span></span>
<span data-ttu-id="767f8-103">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="767f8-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="767f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="767f8-104">SYNTAX</span></span>

### <span data-ttu-id="767f8-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="767f8-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="767f8-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="767f8-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="767f8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="767f8-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="767f8-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="767f8-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="767f8-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="767f8-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="767f8-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="767f8-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="767f8-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="767f8-111">DESCRIPTION</span></span>
<span data-ttu-id="767f8-112">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="767f8-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="767f8-113">Isso pode ser usado para atualizar o filtro, o destino ou os rótulos de uma assinatura de evento existente.</span><span class="sxs-lookup"><span data-stu-id="767f8-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="767f8-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="767f8-114">EXAMPLES</span></span>

### <span data-ttu-id="767f8-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="767f8-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="767f8-116">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="767f8-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="767f8-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="767f8-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="767f8-118">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="767f8-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="767f8-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="767f8-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="767f8-120">Atualiza as propriedades da assinatura de evento \` ES1 \` para o namespace do EventHub ContosoNamespace com o novo ponto de extremidade como \` https://requestb.in/1kxxoui1\ "e o novo filtro SubjectEndsWith como \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="767f8-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="767f8-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="767f8-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="767f8-122">Atualiza as propriedades da assinatura do evento \` ES1 \` para o MyResourceGroupName do grupo de recursos \` \` com os novos rótulos $Labels.</span><span class="sxs-lookup"><span data-stu-id="767f8-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="767f8-123">OS</span><span class="sxs-lookup"><span data-stu-id="767f8-123">PARAMETERS</span></span>

### <span data-ttu-id="767f8-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="767f8-124">-AdvancedFilter</span></span>
<span data-ttu-id="767f8-125">Filtro avançado que especifica uma matriz de vários valores de Hashtable usados para a filtragem baseada em atributo.</span><span class="sxs-lookup"><span data-stu-id="767f8-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="767f8-126">Cada valor de Hashtable tem as seguintes informações de valor-chave: operação, chave e valor ou valores.</span><span class="sxs-lookup"><span data-stu-id="767f8-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="767f8-127">Operator pode ser um dos seguintes valores: Numberie, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, Stringem, StringNotIn, StringBeginsWith, StringEndsWith ou StringContains.</span><span class="sxs-lookup"><span data-stu-id="767f8-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="767f8-128">Chave representa a Propriedade Payload na qual as políticas de filtragem avançada são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="767f8-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="767f8-129">Por fim, valor ou valores representam o valor ou o conjunto de valores a ser correspondido.</span><span class="sxs-lookup"><span data-stu-id="767f8-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="767f8-130">Pode ser um valor único do tipo correspondente ou uma matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="767f8-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="767f8-131">Como um exemplo dos parâmetros de filtro avançado: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2) onde $AdvFilter 1 = @ {Operator = "Numberem"; Key = "Data. key1"; Valores = @ (1, 2)} e $AdvFilter 2 = @ {Operator = "StringBeginsWith"; Key = "Subject"; Valores = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="767f8-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="767f8-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="767f8-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="767f8-133">A ID de aplicativo (AAD) do Azure Active Directory (AAD) ou URI para obter o token de acesso que será incluído como o token de portador nas solicitações de entrega. Aplicável somente para webhook como destino.</span><span class="sxs-lookup"><span data-stu-id="767f8-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767f8-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="767f8-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="767f8-135">A ID de locatário do Azure Active Directory (AAD) para obter o token de acesso que será incluído como o token de portador nas solicitações de entrega. Aplicável somente para webhook como destino.</span><span class="sxs-lookup"><span data-stu-id="767f8-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767f8-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="767f8-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="767f8-137">O ponto de extremidade usado para armazenar eventos não entregues.</span><span class="sxs-lookup"><span data-stu-id="767f8-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="767f8-138">Especifique a ID do recurso do Azure de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="767f8-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="767f8-139">Por exemplo:/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="767f8-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="767f8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="767f8-140">-DefaultProfile</span></span>
<span data-ttu-id="767f8-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="767f8-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="767f8-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="767f8-142">-DomainName</span></span>
<span data-ttu-id="767f8-143">O nome do domínio para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="767f8-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="767f8-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="767f8-144">-DomainTopicName</span></span>
<span data-ttu-id="767f8-145">O nome do tópico de domínio para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="767f8-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="767f8-146">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="767f8-146">-Endpoint</span></span>
<span data-ttu-id="767f8-147">Ponto de extremidade de assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="767f8-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="767f8-148">Pode ser uma URL do webhook ou a ID do recurso do Azure de um EventHub, fila de armazenamento, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="767f8-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="767f8-149">Por exemplo, a ID do recurso para uma conexão híbrida tem o seguinte formato:/subscriptions/[ID da assinatura do Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="767f8-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="767f8-150">Espera-se que o ponto de extremidade de destino seja criado e esteja disponível para uso antes de executar cmdlets de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="767f8-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="767f8-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="767f8-151">-EndpointType</span></span>
<span data-ttu-id="767f8-152">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="767f8-152">Endpoint Type.</span></span>
<span data-ttu-id="767f8-153">Pode ser webhook, eventhub, storagequeue, hybridconnection ou servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="767f8-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="767f8-154">O valor padrão é webhook.</span><span class="sxs-lookup"><span data-stu-id="767f8-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767f8-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="767f8-155">-EventSubscriptionName</span></span>
<span data-ttu-id="767f8-156">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="767f8-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="767f8-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="767f8-157">-EventTtl</span></span>
<span data-ttu-id="767f8-158">O tempo em minutos para a entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="767f8-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="767f8-159">Esse valor deve estar entre 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="767f8-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="767f8-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="767f8-160">-ExpirationDate</span></span>
<span data-ttu-id="767f8-161">Determina a data de expiração para a assinatura do evento após a qual a assinatura do evento será desativada.</span><span class="sxs-lookup"><span data-stu-id="767f8-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="767f8-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="767f8-162">-IncludedEventType</span></span>
<span data-ttu-id="767f8-163">Filtro que especifica uma lista de tipos de eventos a serem incluídos. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="767f8-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="767f8-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="767f8-164">-InputObject</span></span>
<span data-ttu-id="767f8-165">Objeto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="767f8-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="767f8-166">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="767f8-166">-Label</span></span>
<span data-ttu-id="767f8-167">Etiquetas para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="767f8-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="767f8-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="767f8-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="767f8-169">O número máximo de tentativas de entregar o evento.</span><span class="sxs-lookup"><span data-stu-id="767f8-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="767f8-170">Esse valor deve estar entre 1 e 30</span><span class="sxs-lookup"><span data-stu-id="767f8-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="767f8-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="767f8-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="767f8-172">O número máximo de eventos em um lote.</span><span class="sxs-lookup"><span data-stu-id="767f8-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="767f8-173">Esse valor deve estar entre 1 e 5000.</span><span class="sxs-lookup"><span data-stu-id="767f8-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="767f8-174">Esse parâmetro é válido quando o tipo Endpint é webhook apenas.</span><span class="sxs-lookup"><span data-stu-id="767f8-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="767f8-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="767f8-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="767f8-176">O tamanho do lote preferido em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="767f8-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="767f8-177">Esse valor deve estar entre 1 e 1024.</span><span class="sxs-lookup"><span data-stu-id="767f8-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="767f8-178">Esse parâmetro é válido quando o tipo Endpint é webhook apenas.</span><span class="sxs-lookup"><span data-stu-id="767f8-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="767f8-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="767f8-179">-ResourceGroupName</span></span>
<span data-ttu-id="767f8-180">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="767f8-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="767f8-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="767f8-181">-ResourceId</span></span>
<span data-ttu-id="767f8-182">O identificador do recurso para o qual a assinatura de evento foi criada.</span><span class="sxs-lookup"><span data-stu-id="767f8-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="767f8-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="767f8-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="767f8-184">Filtro que especifica que somente os eventos que correspondem ao prefixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="767f8-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="767f8-185">Se não for especificado, os eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="767f8-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="767f8-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="767f8-186">-SubjectEndsWith</span></span>
<span data-ttu-id="767f8-187">Filtro que especifica que somente os eventos que correspondem ao sufixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="767f8-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="767f8-188">Se não for especificado, os eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="767f8-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="767f8-189">-Topicname</span><span class="sxs-lookup"><span data-stu-id="767f8-189">-TopicName</span></span>
<span data-ttu-id="767f8-190">O nome do tópico para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="767f8-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="767f8-191">-Confirme</span><span class="sxs-lookup"><span data-stu-id="767f8-191">-Confirm</span></span>
<span data-ttu-id="767f8-192">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="767f8-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="767f8-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="767f8-193">-WhatIf</span></span>
<span data-ttu-id="767f8-194">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="767f8-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="767f8-195">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="767f8-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="767f8-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="767f8-196">CommonParameters</span></span>
<span data-ttu-id="767f8-197">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="767f8-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="767f8-198">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="767f8-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="767f8-199">SENSORES</span><span class="sxs-lookup"><span data-stu-id="767f8-199">INPUTS</span></span>

### <span data-ttu-id="767f8-200">System. String</span><span class="sxs-lookup"><span data-stu-id="767f8-200">System.String</span></span>

### <span data-ttu-id="767f8-201">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="767f8-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="767f8-202">EXIBE</span><span class="sxs-lookup"><span data-stu-id="767f8-202">OUTPUTS</span></span>

### <span data-ttu-id="767f8-203">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="767f8-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="767f8-204">INFORMA</span><span class="sxs-lookup"><span data-stu-id="767f8-204">NOTES</span></span>

## <span data-ttu-id="767f8-205">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="767f8-205">RELATED LINKS</span></span>
