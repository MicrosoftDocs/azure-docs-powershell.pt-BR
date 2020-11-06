---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: ed2855571ccd3ce10a8a41fd72f5e14fde7bba16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441113"
---
# <span data-ttu-id="00e86-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="00e86-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="00e86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00e86-102">SYNOPSIS</span></span>
<span data-ttu-id="00e86-103">Cria uma nova assinatura de evento de grade de eventos do Azure para um tópico, recurso do Azure, assinatura do Azure ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00e86-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00e86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00e86-104">SYNTAX</span></span>

### <span data-ttu-id="00e86-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="00e86-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e86-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="00e86-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e86-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="00e86-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00e86-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="00e86-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00e86-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00e86-109">DESCRIPTION</span></span>
<span data-ttu-id="00e86-110">Crie uma nova assinatura de evento para um tópico de grade de eventos do Azure, um recurso do Azure compatível, uma assinatura do Azure ou um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00e86-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="00e86-111">Para criar uma assinatura de evento para a assinatura do Azure selecionada atualmente, especifique o nome da assinatura do evento e o ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="00e86-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="00e86-112">Para criar uma assinatura de evento para um grupo de recursos, especifique o nome do grupo de recursos, além do nome da assinatura do evento e do ponto de extremidade do destino.</span><span class="sxs-lookup"><span data-stu-id="00e86-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="00e86-113">Para criar uma assinatura de evento para um tópico da grade do evento do Azure, especifique também o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="00e86-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="00e86-114">Para criar uma assinatura de evento para um recurso do Azure compatível, especifique a ID do recurso completo do recurso.</span><span class="sxs-lookup"><span data-stu-id="00e86-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="00e86-115">Para exibir a lista de tipos com suporte, execute o cmdlet Get-AzureRmEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="00e86-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="00e86-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00e86-116">EXAMPLES</span></span>

### <span data-ttu-id="00e86-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00e86-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="00e86-118">Cria uma nova assinatura de evento \` EventSubscription1 \` para um tópico de Tópico1 de grade de eventos do Azure \` \` no grupo de recursos \` MyResourceGroupName \` com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="00e86-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="00e86-119">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="00e86-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="00e86-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="00e86-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="00e86-121">Cria uma nova assinatura de evento \` EventSubscription1 \` a um grupo de recursos \` MyResourceGroupName \` com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="00e86-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="00e86-122">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="00e86-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="00e86-123">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="00e86-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="00e86-124">Cria uma nova assinatura de evento \` EventSubscription1 \` para a assinatura do Azure selecionada no momento com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="00e86-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="00e86-125">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="00e86-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="00e86-126">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="00e86-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="00e86-127">Cria uma nova assinatura de evento \` EventSubscription1 \` para a assinatura do Azure selecionada no momento com o ponto de extremidade de destino do webhook https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="00e86-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="00e86-128">Essa assinatura de evento especifica os filtros adicionais para tipos de evento e assunto, e somente os eventos que correspondem a esses filtros serão entregues ao ponto de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="00e86-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="00e86-129">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="00e86-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="00e86-130">Cria uma nova assinatura de evento \` EventSubscription1 a \` assinatura do Azure selecionada atualmente com o Hub de eventos especificado como o destino de eventos.</span><span class="sxs-lookup"><span data-stu-id="00e86-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="00e86-131">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="00e86-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="00e86-132">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="00e86-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="00e86-133">Cria uma nova assinatura de evento \` EventSubscription1 \` para um namespace do EventHub com o ponto de extremidade de destino do webhhok especificado https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="00e86-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="00e86-134">Esta assinatura de evento usa filtros padrão.</span><span class="sxs-lookup"><span data-stu-id="00e86-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="00e86-135">OS</span><span class="sxs-lookup"><span data-stu-id="00e86-135">PARAMETERS</span></span>

### <span data-ttu-id="00e86-136">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="00e86-136">-Endpoint</span></span>
<span data-ttu-id="00e86-137">Ponto de extremidade de assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="00e86-137">Event subscription destination endpoint.</span></span>
<span data-ttu-id="00e86-138">Pode ser uma URL do webhook ou a ID do recurso do Azure de um EventHub.</span><span class="sxs-lookup"><span data-stu-id="00e86-138">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-139">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="00e86-139">-EndpointType</span></span>
<span data-ttu-id="00e86-140">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="00e86-140">Endpoint Type.</span></span>
<span data-ttu-id="00e86-141">Pode ser webhook ou eventhub</span><span class="sxs-lookup"><span data-stu-id="00e86-141">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-142">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="00e86-142">-EventSubscriptionName</span></span>
<span data-ttu-id="00e86-143">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="00e86-143">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-144">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="00e86-144">-IncludedEventType</span></span>
<span data-ttu-id="00e86-145">Filtro que especifica uma lista de tipos de eventos a serem incluídos. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="00e86-145">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00e86-146">-InputObject</span></span>
<span data-ttu-id="00e86-147">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="00e86-147">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-148">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="00e86-148">-Label</span></span>
<span data-ttu-id="00e86-149">Etiquetas para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="00e86-149">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e86-150">-ResourceGroupName</span></span>
<span data-ttu-id="00e86-151">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="00e86-151">The resource group of the topic.</span></span>

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

### <span data-ttu-id="00e86-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00e86-152">-ResourceId</span></span>
<span data-ttu-id="00e86-153">O identificador do recurso para o qual a assinatura de evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="00e86-153">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="00e86-154">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="00e86-154">-SubjectBeginsWith</span></span>
<span data-ttu-id="00e86-155">Filtro que especifica que somente os eventos que correspondem ao prefixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="00e86-155">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="00e86-156">Se não for especificado, os eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="00e86-156">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-157">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="00e86-157">-SubjectCaseSensitive</span></span>
<span data-ttu-id="00e86-158">Filtro que especifica que o campo assunto deve ser comparado em uma maneira sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="00e86-158">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="00e86-159">Se não for especificado, o assunto será comparado em uma maneira não sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="00e86-159">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="00e86-160">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="00e86-160">-SubjectEndsWith</span></span>
<span data-ttu-id="00e86-161">Filtro que especifica que somente os eventos que correspondem ao sufixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="00e86-161">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="00e86-162">Se não for especificado, os eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="00e86-162">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-163">-Topicname</span><span class="sxs-lookup"><span data-stu-id="00e86-163">-TopicName</span></span>
<span data-ttu-id="00e86-164">O nome do tópico para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="00e86-164">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="00e86-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00e86-165">-Confirm</span></span>
<span data-ttu-id="00e86-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00e86-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00e86-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00e86-167">-WhatIf</span></span>
<span data-ttu-id="00e86-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00e86-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00e86-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00e86-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00e86-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e86-170">-DefaultProfile</span></span>
<span data-ttu-id="00e86-171">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00e86-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e86-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e86-172">CommonParameters</span></span>
<span data-ttu-id="00e86-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e86-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e86-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e86-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e86-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00e86-175">INPUTS</span></span>

### <span data-ttu-id="00e86-176">System. String</span><span class="sxs-lookup"><span data-stu-id="00e86-176">System.String</span></span>
<span data-ttu-id="00e86-177">Microsoft. Azure. Commands. EventGrid. Models. PSTopic System. Management. Automation. SwitchParameter System. String []</span><span class="sxs-lookup"><span data-stu-id="00e86-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="00e86-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00e86-178">OUTPUTS</span></span>

### <span data-ttu-id="00e86-179">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="00e86-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="00e86-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00e86-180">NOTES</span></span>

## <span data-ttu-id="00e86-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00e86-181">RELATED LINKS</span></span>

