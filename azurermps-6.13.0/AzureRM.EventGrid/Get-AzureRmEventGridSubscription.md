---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 3117433c677330eba4585d45337c44658225ee0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430944"
---
# <span data-ttu-id="5e68a-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5e68a-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="5e68a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e68a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e68a-103">Obtém os detalhes de uma assinatura de evento ou obtém uma lista de todas as assinaturas de evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e68a-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e68a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e68a-104">SYNTAX</span></span>

### <span data-ttu-id="5e68a-105">EventSubscriptionTopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e68a-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e68a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e68a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e68a-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e68a-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e68a-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e68a-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e68a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e68a-109">DESCRIPTION</span></span>
<span data-ttu-id="5e68a-110">O cmdlet Get-AzureRmEventGridSubscription Obtém os detalhes de uma assinatura de grade de eventos especificada ou uma lista de todas as assinaturas de grade de eventos na assinatura atual do Azure ou no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e68a-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="5e68a-111">Se o nome da assinatura do evento for fornecido, os detalhes de uma única assinatura de grade de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="5e68a-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="5e68a-112">Se o nome da assinatura do evento não for fornecido, uma lista de todas as assinaturas de eventos será retornada.</span><span class="sxs-lookup"><span data-stu-id="5e68a-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="5e68a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e68a-113">EXAMPLES</span></span>

### <span data-ttu-id="5e68a-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e68a-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5e68a-115">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o tópico \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="5e68a-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5e68a-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5e68a-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="5e68a-117">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para \` o tópico tópico1 \` no grupo de recursos \` MyResourceGroupName \` , incluindo a URL de ponto de extremidade completa se for uma assinatura de evento baseada em webhook.</span><span class="sxs-lookup"><span data-stu-id="5e68a-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="5e68a-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5e68a-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="5e68a-119">Obtenha uma lista de todas as assinaturas de evento criadas para o tópico \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="5e68a-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5e68a-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="5e68a-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5e68a-121">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o grupo de MyResourceGroupName de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="5e68a-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5e68a-122">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="5e68a-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="5e68a-123">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criada para a assinatura do Azure selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="5e68a-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="5e68a-124">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="5e68a-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="5e68a-125">Obtém a lista de todas as assinaturas de eventos globais criadas sob a MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="5e68a-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5e68a-126">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="5e68a-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="5e68a-127">Obtém a lista de todas as assinaturas de eventos globais criadas sob a assinatura do Azure selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="5e68a-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="5e68a-128">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="5e68a-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="5e68a-129">Obtém a lista de todas as assinaturas de eventos regionais criadas em MyResourceGroupName do grupo de recursos \` \` no local especificado \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="5e68a-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="5e68a-130">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="5e68a-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="5e68a-131">Obtém a lista de todas as assinaturas de evento criadas para o namespace do EventHub especificado.</span><span class="sxs-lookup"><span data-stu-id="5e68a-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="5e68a-132">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="5e68a-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="5e68a-133">Obtém a lista de todas as assinaturas de evento criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado.</span><span class="sxs-lookup"><span data-stu-id="5e68a-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="5e68a-134">Exemplo 11</span><span class="sxs-lookup"><span data-stu-id="5e68a-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="5e68a-135">Obtém a lista de todas as assinaturas de evento criadas para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="5e68a-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="5e68a-136">OS</span><span class="sxs-lookup"><span data-stu-id="5e68a-136">PARAMETERS</span></span>

### <span data-ttu-id="5e68a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e68a-137">-DefaultProfile</span></span>
<span data-ttu-id="5e68a-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5e68a-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e68a-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5e68a-139">-EventSubscriptionName</span></span>
<span data-ttu-id="5e68a-140">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="5e68a-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e68a-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5e68a-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="5e68a-142">Inclua a URL completa de ponto de extremidade do destino da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="5e68a-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e68a-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e68a-143">-InputObject</span></span>
<span data-ttu-id="5e68a-144">Objeto de assinatura de evento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5e68a-144">EventGrid Event Subscription object.</span></span>

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

### <span data-ttu-id="5e68a-145">-Local</span><span class="sxs-lookup"><span data-stu-id="5e68a-145">-Location</span></span>
<span data-ttu-id="5e68a-146">Ponto</span><span class="sxs-lookup"><span data-stu-id="5e68a-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e68a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e68a-147">-ResourceGroupName</span></span>
<span data-ttu-id="5e68a-148">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5e68a-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e68a-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e68a-149">-ResourceId</span></span>
<span data-ttu-id="5e68a-150">Identificador do recurso para o qual as assinaturas de eventos foram criadas.</span><span class="sxs-lookup"><span data-stu-id="5e68a-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e68a-151">-Topicname</span><span class="sxs-lookup"><span data-stu-id="5e68a-151">-TopicName</span></span>
<span data-ttu-id="5e68a-152">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5e68a-152">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e68a-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="5e68a-153">-TopicTypeName</span></span>
<span data-ttu-id="5e68a-154">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="5e68a-154">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e68a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e68a-155">CommonParameters</span></span>
<span data-ttu-id="5e68a-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e68a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e68a-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e68a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e68a-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e68a-158">INPUTS</span></span>

### <span data-ttu-id="5e68a-159">System. String</span><span class="sxs-lookup"><span data-stu-id="5e68a-159">System.String</span></span>

### <span data-ttu-id="5e68a-160">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5e68a-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="5e68a-161">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5e68a-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5e68a-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e68a-162">OUTPUTS</span></span>

### <span data-ttu-id="5e68a-163">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="5e68a-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="5e68a-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e68a-164">NOTES</span></span>

## <span data-ttu-id="5e68a-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e68a-165">RELATED LINKS</span></span>
