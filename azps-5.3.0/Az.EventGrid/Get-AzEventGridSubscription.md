---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271407"
---
# <span data-ttu-id="c9c6a-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c9c6a-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="c9c6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c6a-103">Obtém os detalhes de uma assinatura de evento ou obtém uma lista de todas as assinaturas de evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="c9c6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9c6a-104">SYNTAX</span></span>

### <span data-ttu-id="c9c6a-105">EventSubscriptionTopicNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c9c6a-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9c6a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9c6a-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6a-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9c6a-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6a-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c6a-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6a-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9c6a-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6a-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9c6a-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6a-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9c6a-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6a-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9c6a-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9c6a-113">DESCRIPTION</span></span>
<span data-ttu-id="c9c6a-114">O cmdlet Get-AzEventGridSubscription Obtém os detalhes de uma assinatura de grade de eventos especificada ou uma lista de todas as assinaturas de grade de eventos na assinatura atual do Azure ou no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="c9c6a-115">Se o nome da assinatura do evento for fornecido, os detalhes de uma única assinatura de grade de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="c9c6a-116">Se o nome da assinatura do evento não for fornecido, uma lista de todas as assinaturas de eventos será retornada.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="c9c6a-117">O número de elementos retornados nessa lista é controlado pelo parâmetro Top.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="c9c6a-118">Se o valor superior não for especificado ou $null, a lista conterá todos os itens de assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="c9c6a-119">Caso contrário, o superior indicará o número máximo de elementos a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="c9c6a-120">Se mais assinaturas de evento ainda estiverem disponíveis, o valor em NextLink deve ser usado na próxima chamada para obter a próxima página de assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="c9c6a-121">Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="c9c6a-122">A consulta filtragem segue a sintaxe OData usando somente a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="c9c6a-123">As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="c9c6a-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9c6a-124">EXAMPLES</span></span>

### <span data-ttu-id="c9c6a-125">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9c6a-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c9c6a-126">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o tópico \` tópico1 \` na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c9c6a-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c9c6a-127">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c9c6a-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="c9c6a-128">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para \` o tópico tópico1 \` no grupo de recursos \` MyResourceGroupName \` , incluindo a URL de ponto de extremidade completa se for uma assinatura de evento baseada em webhook.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="c9c6a-129">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c9c6a-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="c9c6a-130">Obtenha uma lista de todas as assinaturas de evento criadas para o tópico \` tópico1 \` no grupo de \` MyResourceGroupName de recursos \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="c9c6a-131">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c9c6a-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="c9c6a-132">Liste as 10 primeiras assinaturas de evento (se houver) criadas para \` o tópico tópico1 \` no grupo de MyResourceGroupName de recursos \` \` que satisfaz a consulta $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c9c6a-133">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c9c6a-134">Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c9c6a-135">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="c9c6a-136">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="c9c6a-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c9c6a-137">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criado para o grupo de MyResourceGroupName de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="c9c6a-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c9c6a-138">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="c9c6a-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c9c6a-139">Obtém os detalhes da assinatura de evento \` EventSubscription1 \` criada para a assinatura do Azure selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="c9c6a-140">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="c9c6a-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c9c6a-141">Obtém a lista de todas as assinaturas de eventos globais criadas sob a MyResourceGroupName do grupo de recursos \` \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="c9c6a-142">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="c9c6a-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="c9c6a-143">Liste as cinco primeiras assinaturas de evento (se houver) criadas em MyResourceGroupName do grupo de recursos \` \` que satisfaçam a consulta $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c9c6a-144">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c9c6a-145">Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c9c6a-146">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="c9c6a-147">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="c9c6a-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="c9c6a-148">Obtém a lista de todas as assinaturas de eventos globais criadas sob a assinatura do Azure selecionada atualmente, sem paginação.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="c9c6a-149">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="c9c6a-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="c9c6a-150">Liste as 15 primeiras assinaturas de evento global (se houver) criadas sob a assinatura atualmente selecionada do Azure que satisfaz a consulta $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c9c6a-151">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c9c6a-152">Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c9c6a-153">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="c9c6a-154">Exemplo 11</span><span class="sxs-lookup"><span data-stu-id="c9c6a-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="c9c6a-155">Obtém a lista de todas as assinaturas de eventos regionais criadas em MyResourceGroupName do grupo de recursos \` \` no local especificado \` westus2 \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="c9c6a-156">Exemplo 12</span><span class="sxs-lookup"><span data-stu-id="c9c6a-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="c9c6a-157">Liste as 15 primeiras assinaturas de evento regional (se houver) criadas em MyResourceGroupName de \` grupo \` de recursos no local especificado \` westus2 \` que satisfaz a consulta $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c9c6a-158">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c9c6a-159">Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c9c6a-160">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="c9c6a-161">Exemplo 13</span><span class="sxs-lookup"><span data-stu-id="c9c6a-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="c9c6a-162">Obtém a lista de todas as assinaturas de evento criadas para o namespace do EventHub especificado sem paginação.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="c9c6a-163">Exemplo 14</span><span class="sxs-lookup"><span data-stu-id="c9c6a-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="c9c6a-164">Liste as 25 primeiras assinaturas de evento (se houver) criadas para o namespace do EventHub especificado que satisfaz o $odataFilter consulta.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c9c6a-165">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c9c6a-166">Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c9c6a-167">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="c9c6a-168">Exemplo 15</span><span class="sxs-lookup"><span data-stu-id="c9c6a-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="c9c6a-169">Obtém a lista de todas as assinaturas de evento criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado sem paginação.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="c9c6a-170">Exemplo 16</span><span class="sxs-lookup"><span data-stu-id="c9c6a-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="c9c6a-171">Liste as 15 primeiras assinaturas de evento (se houver) criadas para o tipo de tópico especificado (namespaces do EventHub) no local especificado que satisfaz a consulta $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c9c6a-172">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c9c6a-173">Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c9c6a-174">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="c9c6a-175">Exemplo 17</span><span class="sxs-lookup"><span data-stu-id="c9c6a-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c9c6a-176">Obtém a lista de todas as assinaturas de evento criadas para o grupo de recursos específico sem paginação.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="c9c6a-177">Exemplo 18</span><span class="sxs-lookup"><span data-stu-id="c9c6a-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="c9c6a-178">Liste as primeiras 100 assinaturas de evento (se houver) criadas para o grupo de recursos específico que satisfaz a consulta $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="c9c6a-179">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c9c6a-180">Para obter próxima página (s) de assinaturas de evento, espera-se que o usuário chame novamente Get-AzEventGridSubscription e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c9c6a-181">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="c9c6a-182">OS</span><span class="sxs-lookup"><span data-stu-id="c9c6a-182">PARAMETERS</span></span>

### <span data-ttu-id="c9c6a-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c6a-183">-DefaultProfile</span></span>
<span data-ttu-id="c9c6a-184">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c9c6a-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9c6a-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="c9c6a-185">-DomainInputObject</span></span>
<span data-ttu-id="c9c6a-186">Objeto de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="c9c6a-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="c9c6a-187">-DomainName</span></span>
<span data-ttu-id="c9c6a-188">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="c9c6a-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="c9c6a-190">Objeto de tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="c9c6a-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="c9c6a-191">-DomainTopicName</span></span>
<span data-ttu-id="c9c6a-192">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c9c6a-193">-EventSubscriptionName</span></span>
<span data-ttu-id="c9c6a-194">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="c9c6a-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="c9c6a-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="c9c6a-196">Inclua a URL completa de ponto de extremidade do destino da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c6a-197">-InputObject</span></span>
<span data-ttu-id="c9c6a-198">Objeto de tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c9c6a-199">-Local</span><span class="sxs-lookup"><span data-stu-id="c9c6a-199">-Location</span></span>
<span data-ttu-id="c9c6a-200">Ponto</span><span class="sxs-lookup"><span data-stu-id="c9c6a-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="c9c6a-201">-NextLink</span></span>
<span data-ttu-id="c9c6a-202">O link para a próxima página de recursos a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="c9c6a-203">Esse valor é obtido com a primeira chamada de cmdlet Get-AzEventGrid quando mais recursos ainda estão disponíveis para consulta.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c9c6a-204">-ODataQuery</span></span>
<span data-ttu-id="c9c6a-205">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="c9c6a-206">Atualmente, a filtragem só é permitida na propriedade Name. As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c6a-207">-ResourceGroupName</span></span>
<span data-ttu-id="c9c6a-208">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c6a-209">-ResourceId</span></span>
<span data-ttu-id="c9c6a-210">Identificador do recurso para o qual as assinaturas de eventos foram criadas.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="c9c6a-211">-Início</span><span class="sxs-lookup"><span data-stu-id="c9c6a-211">-Top</span></span>
<span data-ttu-id="c9c6a-212">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="c9c6a-213">Atualmente, a filtragem só é permitida na propriedade Name. As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-214">-Topicname</span><span class="sxs-lookup"><span data-stu-id="c9c6a-214">-TopicName</span></span>
<span data-ttu-id="c9c6a-215">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="c9c6a-216">-TopicTypeName</span></span>
<span data-ttu-id="c9c6a-217">Nome do tópico</span><span class="sxs-lookup"><span data-stu-id="c9c6a-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c6a-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c6a-218">CommonParameters</span></span>
<span data-ttu-id="c9c6a-219">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c6a-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c6a-220">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9c6a-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c6a-221">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9c6a-221">INPUTS</span></span>

### <span data-ttu-id="c9c6a-222">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c6a-222">System.String</span></span>

### <span data-ttu-id="c9c6a-223">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c9c6a-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="c9c6a-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="c9c6a-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="c9c6a-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="c9c6a-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="c9c6a-226">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c9c6a-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c9c6a-227">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9c6a-227">OUTPUTS</span></span>

### <span data-ttu-id="c9c6a-228">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c9c6a-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c9c6a-229">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9c6a-229">NOTES</span></span>

## <span data-ttu-id="c9c6a-230">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9c6a-230">RELATED LINKS</span></span>
