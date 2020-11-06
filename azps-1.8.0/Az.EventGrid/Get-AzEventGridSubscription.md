---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600880"
---
# <span data-ttu-id="a3805-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="a3805-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="a3805-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3805-102">SYNOPSIS</span></span>
<span data-ttu-id="a3805-103">Obtém os detalhes de uma assinatura de evento ou obtém uma lista de todas as assinaturas de evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3805-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="a3805-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3805-104">SYNTAX</span></span>

### <span data-ttu-id="a3805-105">EventSubscriptionTopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3805-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3805-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3805-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3805-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3805-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3805-108">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3805-108">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3805-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3805-109">DESCRIPTION</span></span>
<span data-ttu-id="a3805-110">O cmdlet Get-AzEventGridSubscription Obtém os detalhes de uma assinatura de grade de eventos especificada ou uma lista de todas as assinaturas de grade de eventos na assinatura atual do Azure ou no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3805-110">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="a3805-111">Se o nome da assinatura do evento for fornecido, os detalhes de uma única assinatura de grade de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="a3805-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="a3805-112">Se o nome da assinatura do evento não for fornecido, uma lista de todas as assinaturas de eventos será retornada.</span><span class="sxs-lookup"><span data-stu-id="a3805-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="a3805-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3805-113">EXAMPLES</span></span>

### <span data-ttu-id="a3805-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3805-114">Example 1</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a3805-115">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o tópico \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3805-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3805-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a3805-116">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="a3805-117">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para \` o tópico tópico1 \` no grupo de recursos \` MyResourceGroupName \` , incluindo a URL de ponto de extremidade completa se for uma assinatura de evento baseada em webhook.</span><span class="sxs-lookup"><span data-stu-id="a3805-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="a3805-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a3805-118">Example 3</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="a3805-119">Obtenha uma lista de todas as assinaturas de evento criadas para o tópico \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3805-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3805-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="a3805-120">Example 4</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a3805-121">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o grupo de MyResourceGroupName de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3805-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3805-122">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="a3805-122">Example 5</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="a3805-123">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criada para a assinatura do Azure selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="a3805-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a3805-124">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="a3805-124">Example 6</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a3805-125">Obtém a lista de todas as assinaturas de eventos globais criadas sob a MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a3805-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a3805-126">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="a3805-126">Example 7</span></span>
```
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="a3805-127">Obtém a lista de todas as assinaturas de eventos globais criadas sob a assinatura do Azure selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="a3805-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="a3805-128">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="a3805-128">Example 8</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="a3805-129">Obtém a lista de todas as assinaturas de eventos regionais criadas em MyResourceGroupName do grupo de recursos \` \` no local especificado \` westus2 \` .</span><span class="sxs-lookup"><span data-stu-id="a3805-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="a3805-130">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="a3805-130">Example 9</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="a3805-131">Obtém a lista de todas as assinaturas de evento criadas para o namespace do EventHub especificado.</span><span class="sxs-lookup"><span data-stu-id="a3805-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="a3805-132">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="a3805-132">Example 10</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="a3805-133">Obtém a lista de todas as assinaturas de evento criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado.</span><span class="sxs-lookup"><span data-stu-id="a3805-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="a3805-134">Exemplo 11</span><span class="sxs-lookup"><span data-stu-id="a3805-134">Example 11</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="a3805-135">Obtém a lista de todas as assinaturas de evento criadas para o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="a3805-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="a3805-136">OS</span><span class="sxs-lookup"><span data-stu-id="a3805-136">PARAMETERS</span></span>

### <span data-ttu-id="a3805-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3805-137">-DefaultProfile</span></span>
<span data-ttu-id="a3805-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a3805-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3805-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a3805-139">-EventSubscriptionName</span></span>
<span data-ttu-id="a3805-140">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="a3805-140">The name of the event subscription</span></span>

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

### <span data-ttu-id="a3805-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a3805-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="a3805-142">Inclua a URL completa de ponto de extremidade do destino da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="a3805-142">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="a3805-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3805-143">-InputObject</span></span>
<span data-ttu-id="a3805-144">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a3805-144">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="a3805-145">-Local</span><span class="sxs-lookup"><span data-stu-id="a3805-145">-Location</span></span>
<span data-ttu-id="a3805-146">Ponto</span><span class="sxs-lookup"><span data-stu-id="a3805-146">Location</span></span>

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

### <span data-ttu-id="a3805-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3805-147">-ResourceGroupName</span></span>
<span data-ttu-id="a3805-148">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3805-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="a3805-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3805-149">-ResourceId</span></span>
<span data-ttu-id="a3805-150">Identificador do recurso para o qual as assinaturas de eventos foram criadas.</span><span class="sxs-lookup"><span data-stu-id="a3805-150">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="a3805-151">-Topicname</span><span class="sxs-lookup"><span data-stu-id="a3805-151">-TopicName</span></span>
<span data-ttu-id="a3805-152">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="a3805-152">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="a3805-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="a3805-153">-TopicTypeName</span></span>
<span data-ttu-id="a3805-154">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="a3805-154">TopicType name</span></span>

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

### <span data-ttu-id="a3805-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3805-155">CommonParameters</span></span>
<span data-ttu-id="a3805-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3805-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3805-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3805-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3805-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3805-158">INPUTS</span></span>

### <span data-ttu-id="a3805-159">System. String</span><span class="sxs-lookup"><span data-stu-id="a3805-159">System.String</span></span>

### <span data-ttu-id="a3805-160">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a3805-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a3805-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3805-161">OUTPUTS</span></span>

### <span data-ttu-id="a3805-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="a3805-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="a3805-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3805-163">NOTES</span></span>

## <span data-ttu-id="a3805-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3805-164">RELATED LINKS</span></span>
