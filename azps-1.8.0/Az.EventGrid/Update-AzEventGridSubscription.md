---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600862"
---
# <span data-ttu-id="969ef-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="969ef-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="969ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="969ef-102">SYNOPSIS</span></span>
<span data-ttu-id="969ef-103">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="969ef-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="969ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="969ef-104">SYNTAX</span></span>

### <span data-ttu-id="969ef-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="969ef-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="969ef-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="969ef-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="969ef-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="969ef-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969ef-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="969ef-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969ef-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="969ef-109">DESCRIPTION</span></span>
<span data-ttu-id="969ef-110">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="969ef-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="969ef-111">Isso pode ser usado para atualizar o filtro, o destino ou os rótulos de uma assinatura de evento existente.</span><span class="sxs-lookup"><span data-stu-id="969ef-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="969ef-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="969ef-112">EXAMPLES</span></span>

### <span data-ttu-id="969ef-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="969ef-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="969ef-114">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="969ef-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="969ef-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="969ef-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="969ef-116">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="969ef-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="969ef-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="969ef-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="969ef-118">Atualiza as propriedades da assinatura de evento \` ES1 \` para o namespace do EventHub ContosoNamespace com o novo ponto de extremidade como \` https://requestb.in/1kxxoui1\ "e o novo filtro SubjectEndsWith como \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="969ef-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="969ef-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="969ef-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="969ef-120">Atualiza as propriedades da assinatura do evento \` ES1 \` para o MyResourceGroupName do grupo de recursos \` \` com os novos rótulos $Labels.</span><span class="sxs-lookup"><span data-stu-id="969ef-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="969ef-121">OS</span><span class="sxs-lookup"><span data-stu-id="969ef-121">PARAMETERS</span></span>

### <span data-ttu-id="969ef-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="969ef-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="969ef-123">O ponto de extremidade usado para armazenar eventos não entregues.</span><span class="sxs-lookup"><span data-stu-id="969ef-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="969ef-124">Especifique a ID do recurso do Azure de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="969ef-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="969ef-125">Por exemplo:/subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="969ef-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="969ef-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969ef-126">-DefaultProfile</span></span>
<span data-ttu-id="969ef-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="969ef-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="969ef-128">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="969ef-128">-Endpoint</span></span>
<span data-ttu-id="969ef-129">Ponto de extremidade de assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="969ef-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="969ef-130">Pode ser uma URL do webhook ou a ID do recurso do Azure de um EventHub, fila de armazenamento ou hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="969ef-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="969ef-131">Por exemplo, a ID do recurso para uma conexão híbrida tem o seguinte formato:/subscriptions/[ID da assinatura do Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="969ef-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="969ef-132">Espera-se que o ponto de extremidade de destino seja criado e esteja disponível para uso antes de executar cmdlets de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="969ef-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="969ef-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="969ef-133">-EndpointType</span></span>
<span data-ttu-id="969ef-134">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="969ef-134">Endpoint Type.</span></span>
<span data-ttu-id="969ef-135">Pode ser webhook, eventhub, storagequeue ou hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="969ef-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="969ef-136">O valor padrão é webhook.</span><span class="sxs-lookup"><span data-stu-id="969ef-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ef-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="969ef-137">-EventSubscriptionName</span></span>
<span data-ttu-id="969ef-138">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="969ef-138">The name of the event subscription</span></span>

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

### <span data-ttu-id="969ef-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="969ef-139">-EventTtl</span></span>
<span data-ttu-id="969ef-140">O tempo em minutos para a entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="969ef-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="969ef-141">Esse valor deve estar entre 1 e 1440</span><span class="sxs-lookup"><span data-stu-id="969ef-141">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="969ef-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="969ef-142">-IncludedEventType</span></span>
<span data-ttu-id="969ef-143">Filtro que especifica uma lista de tipos de eventos a serem incluídos. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="969ef-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="969ef-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="969ef-144">-InputObject</span></span>
<span data-ttu-id="969ef-145">Objeto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="969ef-145">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="969ef-146">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="969ef-146">-Label</span></span>
<span data-ttu-id="969ef-147">Etiquetas para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="969ef-147">Labels for the event subscription</span></span>

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

### <span data-ttu-id="969ef-148">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="969ef-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="969ef-149">O número máximo de tentativas de entregar o evento.</span><span class="sxs-lookup"><span data-stu-id="969ef-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="969ef-150">Esse valor deve estar entre 1 e 30</span><span class="sxs-lookup"><span data-stu-id="969ef-150">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="969ef-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969ef-151">-ResourceGroupName</span></span>
<span data-ttu-id="969ef-152">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="969ef-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969ef-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="969ef-153">-ResourceId</span></span>
<span data-ttu-id="969ef-154">O identificador do recurso para o qual a assinatura de evento foi criada.</span><span class="sxs-lookup"><span data-stu-id="969ef-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="969ef-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="969ef-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="969ef-156">Filtro que especifica que somente os eventos que correspondem ao prefixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="969ef-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="969ef-157">Se não for especificado, os eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="969ef-157">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="969ef-158">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="969ef-158">-SubjectEndsWith</span></span>
<span data-ttu-id="969ef-159">Filtro que especifica que somente os eventos que correspondem ao sufixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="969ef-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="969ef-160">Se não for especificado, os eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="969ef-160">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="969ef-161">-Topicname</span><span class="sxs-lookup"><span data-stu-id="969ef-161">-TopicName</span></span>
<span data-ttu-id="969ef-162">O nome do tópico para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="969ef-162">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="969ef-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="969ef-163">-Confirm</span></span>
<span data-ttu-id="969ef-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969ef-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969ef-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969ef-165">-WhatIf</span></span>
<span data-ttu-id="969ef-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="969ef-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969ef-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="969ef-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969ef-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969ef-168">CommonParameters</span></span>
<span data-ttu-id="969ef-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969ef-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969ef-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969ef-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969ef-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="969ef-171">INPUTS</span></span>

### <span data-ttu-id="969ef-172">System. String</span><span class="sxs-lookup"><span data-stu-id="969ef-172">System.String</span></span>

### <span data-ttu-id="969ef-173">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="969ef-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="969ef-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="969ef-174">OUTPUTS</span></span>

### <span data-ttu-id="969ef-175">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="969ef-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="969ef-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="969ef-176">NOTES</span></span>

## <span data-ttu-id="969ef-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="969ef-177">RELATED LINKS</span></span>
