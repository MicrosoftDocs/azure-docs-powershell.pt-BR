---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: 7a6f7833a2b123a4f0235d331952b1403316df37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429794"
---
# <span data-ttu-id="55f3d-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="55f3d-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="55f3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="55f3d-103">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="55f3d-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55f3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55f3d-104">SYNTAX</span></span>

### <span data-ttu-id="55f3d-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="55f3d-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f3d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f3d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f3d-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55f3d-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f3d-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="55f3d-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f3d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55f3d-109">DESCRIPTION</span></span>
<span data-ttu-id="55f3d-110">Atualizar as propriedades de uma assinatura de evento de grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="55f3d-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="55f3d-111">Isso pode ser usado para atualizar o filtro, o destino ou os rótulos de uma assinatura de evento existente.</span><span class="sxs-lookup"><span data-stu-id="55f3d-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="55f3d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55f3d-112">EXAMPLES</span></span>

### <span data-ttu-id="55f3d-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55f3d-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="55f3d-114">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="55f3d-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="55f3d-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="55f3d-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="55f3d-116">Atualiza o ponto de extremidade da assinatura do evento \` ES1 \` para o tópico \` tópico1 \` no grupo de recursos \` MyResourceGroupName \` para \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="55f3d-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="55f3d-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="55f3d-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="55f3d-118">Atualiza as propriedades da assinatura de evento \` ES1 \` para o namespace do EventHub ContosoNamespace com o novo ponto de extremidade como \` https://requestb.in/1kxxoui1\ "e o novo filtro SubjectEndsWith como \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="55f3d-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="55f3d-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="55f3d-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="55f3d-120">Atualiza as propriedades da assinatura do evento \` ES1 \` para o MyResourceGroupName do grupo de recursos \` \` com os novos rótulos $Labels.</span><span class="sxs-lookup"><span data-stu-id="55f3d-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="55f3d-121">OS</span><span class="sxs-lookup"><span data-stu-id="55f3d-121">PARAMETERS</span></span>

### <span data-ttu-id="55f3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f3d-122">-DefaultProfile</span></span>
<span data-ttu-id="55f3d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55f3d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-124">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="55f3d-124">-Endpoint</span></span>
<span data-ttu-id="55f3d-125">Ponto de extremidade de assinatura de evento.</span><span class="sxs-lookup"><span data-stu-id="55f3d-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="55f3d-126">Pode ser uma URL do webhook ou a ID do recurso do Azure de um EventHub.</span><span class="sxs-lookup"><span data-stu-id="55f3d-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="55f3d-127">-EndpointType</span></span>
<span data-ttu-id="55f3d-128">Tipo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="55f3d-128">Endpoint Type.</span></span>
<span data-ttu-id="55f3d-129">Pode ser webhook ou eventhub</span><span class="sxs-lookup"><span data-stu-id="55f3d-129">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="55f3d-130">-EventSubscriptionName</span></span>
<span data-ttu-id="55f3d-131">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="55f3d-131">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="55f3d-132">-IncludedEventType</span></span>
<span data-ttu-id="55f3d-133">Filtro que especifica uma lista de tipos de eventos a serem incluídos. Se não for especificado, todos os tipos de evento serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="55f3d-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55f3d-134">-InputObject</span></span>
<span data-ttu-id="55f3d-135">Objeto EventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="55f3d-135">EventGridSubscription object.</span></span>

```yaml
Type: PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-136">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="55f3d-136">-Label</span></span>
<span data-ttu-id="55f3d-137">Etiquetas para a assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="55f3d-137">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f3d-138">-ResourceGroupName</span></span>
<span data-ttu-id="55f3d-139">O grupo de recursos do tópico.</span><span class="sxs-lookup"><span data-stu-id="55f3d-139">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55f3d-140">-ResourceId</span></span>
<span data-ttu-id="55f3d-141">O identificador do recurso para o qual a assinatura de evento foi criada.</span><span class="sxs-lookup"><span data-stu-id="55f3d-141">The identifier of the resource to which the event subscription was created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="55f3d-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="55f3d-143">Filtro que especifica que somente os eventos que correspondem ao prefixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="55f3d-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="55f3d-144">Se não for especificado, os eventos com todos os prefixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="55f3d-144">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="55f3d-145">-SubjectEndsWith</span></span>
<span data-ttu-id="55f3d-146">Filtro que especifica que somente os eventos que correspondem ao sufixo do assunto especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="55f3d-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="55f3d-147">Se não for especificado, os eventos com todos os sufixos de assunto serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="55f3d-147">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-148">-Topicname</span><span class="sxs-lookup"><span data-stu-id="55f3d-148">-TopicName</span></span>
<span data-ttu-id="55f3d-149">O nome do tópico para o qual a assinatura do evento deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="55f3d-149">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-150">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55f3d-150">-Confirm</span></span>
<span data-ttu-id="55f3d-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f3d-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f3d-152">-WhatIf</span></span>
<span data-ttu-id="55f3d-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55f3d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f3d-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55f3d-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f3d-155">CommonParameters</span></span>
<span data-ttu-id="55f3d-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f3d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f3d-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f3d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f3d-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55f3d-158">INPUTS</span></span>

### <span data-ttu-id="55f3d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="55f3d-159">System.String</span></span>
<span data-ttu-id="55f3d-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription System. String []</span><span class="sxs-lookup"><span data-stu-id="55f3d-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.String[]</span></span>

## <span data-ttu-id="55f3d-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55f3d-161">OUTPUTS</span></span>

### <span data-ttu-id="55f3d-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="55f3d-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="55f3d-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55f3d-163">NOTES</span></span>

## <span data-ttu-id="55f3d-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55f3d-164">RELATED LINKS</span></span>

