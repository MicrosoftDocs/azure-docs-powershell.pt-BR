---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890431"
---
# <span data-ttu-id="ba6f9-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ba6f9-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="ba6f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6f9-103">Obtém os detalhes de uma assinatura de evento ou obtém uma lista de todas as assinaturas de evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="ba6f9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ba6f9-104">SYNTAX</span></span>

### <span data-ttu-id="ba6f9-105">EventSubscriptionTopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ba6f9-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6f9-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6f9-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6f9-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6f9-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6f9-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6f9-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba6f9-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6f9-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6f9-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6f9-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6f9-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6f9-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6f9-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba6f9-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba6f9-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ba6f9-113">DESCRIPTION</span></span>
<span data-ttu-id="ba6f9-114">O Get-AzEventGridSubscription cmdlet obtém os detalhes de uma assinatura de Grade de Eventos especificada ou uma lista de todas as assinaturas de Grade de Eventos na assinatura atual do Azure ou grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="ba6f9-115">Se o nome da assinatura do evento for fornecido, os detalhes de uma única assinatura de Grade de Eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="ba6f9-116">Se o nome da assinatura do evento não for fornecido, uma lista de todas as assinaturas de evento será retornada.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="ba6f9-117">O número de elementos retornados nesta lista é controlado pelo parâmetro Top.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="ba6f9-118">Se o valor Top não for especificado ou $null, a lista conterá todos os itens de assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="ba6f9-119">Caso contrário, Top indicará o número máximo de elementos a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="ba6f9-120">Se mais assinaturas de eventos ainda estão disponíveis, o valor no NextLink deve ser usado na próxima chamada para obter a próxima página de assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="ba6f9-121">Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="ba6f9-122">A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="ba6f9-123">As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="ba6f9-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba6f9-124">EXAMPLES</span></span>

### <span data-ttu-id="ba6f9-125">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ba6f9-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ba6f9-126">Obtém os detalhes da assinatura do evento EventSubscription1 criado para o tópico Tópico1 no grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ba6f9-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ba6f9-127">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ba6f9-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="ba6f9-128">Obtém os detalhes da assinatura do evento EventSubscription1 criado para o tópico Tópico1 no grupo de recursos \` \` \` \` \` MyResourceGroupName , incluindo \` a URL de ponto de extremidade completa se for uma assinatura de evento baseada em webhook.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="ba6f9-129">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ba6f9-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="ba6f9-130">Obter uma lista de todas as assinaturas de evento criadas para o tópico Tópico1 no grupo de recursos \` \` \` MyResourceGroupName \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="ba6f9-131">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ba6f9-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba6f9-132">Listar as primeiras 10 assinaturas de evento (se alguma) criadas para o tópico Tópico1 no grupo de recursos \` \` \` MyResourceGroupName que atenda à $odataFilter \` de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba6f9-133">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba6f9-134">Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário chame Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba6f9-135">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba6f9-136">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="ba6f9-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ba6f9-137">Obtém os detalhes da assinatura do \` evento EventSubscription1 criado para o \` grupo de recursos \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ba6f9-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ba6f9-138">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="ba6f9-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ba6f9-139">Obtém os detalhes da assinatura do evento EventSubscription1 criado para a assinatura do \` \` Azure selecionada no momento.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="ba6f9-140">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="ba6f9-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ba6f9-141">Obtém a lista de todas as assinaturas de eventos globais criadas no grupo de recursos \` MyResourceGroupName \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="ba6f9-142">Exemplo 8</span><span class="sxs-lookup"><span data-stu-id="ba6f9-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba6f9-143">Listar as primeiras 5 assinaturas de evento (se alguma) criadas no grupo de recursos MyResourceGroupName que satisfaça a $odataFilter \` \` consulta.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba6f9-144">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba6f9-145">Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário chame Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba6f9-146">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba6f9-147">Exemplo 9</span><span class="sxs-lookup"><span data-stu-id="ba6f9-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="ba6f9-148">Obtém a lista de todas as assinaturas de eventos globais criadas na assinatura do Azure atualmente selecionada sem paginação.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="ba6f9-149">Exemplo 10</span><span class="sxs-lookup"><span data-stu-id="ba6f9-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba6f9-150">Listar as primeiras 15 assinaturas de evento global (se alguma) criadas sob a assinatura do Azure selecionada no momento que atenda à $odataFilter consulta.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba6f9-151">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba6f9-152">Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário chame Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba6f9-153">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba6f9-154">Exemplo 11</span><span class="sxs-lookup"><span data-stu-id="ba6f9-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="ba6f9-155">Obtém a lista de todas as assinaturas de eventos regionais criadas no grupo de recursos \` MyResourceGroupName no local \` especificado \` westus2 \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="ba6f9-156">Exemplo 12</span><span class="sxs-lookup"><span data-stu-id="ba6f9-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba6f9-157">Listar as primeiras 15 assinaturas de eventos regionais (se alguma) criadas no grupo de recursos \` MyResourceGroupName no local especificado westus2 que atenda à consulta \` \` \` $odataFilter.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba6f9-158">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba6f9-159">Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário chame Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba6f9-160">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba6f9-161">Exemplo 13</span><span class="sxs-lookup"><span data-stu-id="ba6f9-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="ba6f9-162">Obtém a lista de todas as assinaturas de evento criadas para o namespace EventHub especificado sem paginação.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="ba6f9-163">Exemplo 14</span><span class="sxs-lookup"><span data-stu-id="ba6f9-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba6f9-164">Listar as primeiras 25 assinaturas de evento (se alguma) criadas para o namespace EventHub especificado que atenda ao $odataFilter consulta.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba6f9-165">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba6f9-166">Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário chame Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba6f9-167">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba6f9-168">Exemplo 15</span><span class="sxs-lookup"><span data-stu-id="ba6f9-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="ba6f9-169">Obtém a lista de todas as assinaturas de evento criadas para o tipo de tópico especificado (namespaces EventHub) no local especificado sem paginação.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="ba6f9-170">Exemplo 16</span><span class="sxs-lookup"><span data-stu-id="ba6f9-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba6f9-171">Listar as primeiras 15 assinaturas de evento (se alguma) criadas para o tipo de tópico especificado (namespaces EventHub) no local especificado que satisfaça $odataFilter consulta.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba6f9-172">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba6f9-173">Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário chame Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba6f9-174">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ba6f9-175">Exemplo 17</span><span class="sxs-lookup"><span data-stu-id="ba6f9-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ba6f9-176">Obtém a lista de todas as assinaturas de evento criadas para o grupo de recursos específico sem paginação.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="ba6f9-177">Exemplo 18</span><span class="sxs-lookup"><span data-stu-id="ba6f9-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ba6f9-178">Listar as primeiras 100 assinaturas de evento (se alguma) criadas para o grupo de recursos específico que satisfaça a $odataFilter consulta.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ba6f9-179">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ba6f9-180">Para obter as próximas páginas de assinaturas de eventos, espera-se que o usuário chame Get-AzEventGridSubscription e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ba6f9-181">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="ba6f9-182">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ba6f9-182">PARAMETERS</span></span>

### <span data-ttu-id="ba6f9-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6f9-183">-DefaultProfile</span></span>
<span data-ttu-id="ba6f9-184">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ba6f9-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba6f9-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="ba6f9-185">-DomainInputObject</span></span>
<span data-ttu-id="ba6f9-186">Objeto EventGrid Domain.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="ba6f9-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ba6f9-187">-DomainName</span></span>
<span data-ttu-id="ba6f9-188">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ba6f9-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="ba6f9-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="ba6f9-190">Objeto EventGrid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="ba6f9-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="ba6f9-191">-DomainTopicName</span></span>
<span data-ttu-id="ba6f9-192">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ba6f9-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ba6f9-193">-EventSubscriptionName</span></span>
<span data-ttu-id="ba6f9-194">O nome da assinatura do evento</span><span class="sxs-lookup"><span data-stu-id="ba6f9-194">The name of the event subscription</span></span>

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

### <span data-ttu-id="ba6f9-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ba6f9-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="ba6f9-196">Inclua a URL de ponto de extremidade completa do destino da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="ba6f9-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba6f9-197">-InputObject</span></span>
<span data-ttu-id="ba6f9-198">Objeto EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ba6f9-199">-Location</span><span class="sxs-lookup"><span data-stu-id="ba6f9-199">-Location</span></span>
<span data-ttu-id="ba6f9-200">Local</span><span class="sxs-lookup"><span data-stu-id="ba6f9-200">Location</span></span>

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

### <span data-ttu-id="ba6f9-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ba6f9-201">-NextLink</span></span>
<span data-ttu-id="ba6f9-202">O link para a próxima página de recursos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="ba6f9-203">Esse valor é obtido com a primeira chamada Get-AzEventGrid cmdlet quando mais recursos ainda estão disponíveis para consulta.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="ba6f9-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ba6f9-204">-ODataQuery</span></span>
<span data-ttu-id="ba6f9-205">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ba6f9-206">Atualmente, a filtragem é permitida somente na propriedade Name. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ba6f9-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6f9-207">-ResourceGroupName</span></span>
<span data-ttu-id="ba6f9-208">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-208">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba6f9-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba6f9-209">-ResourceId</span></span>
<span data-ttu-id="ba6f9-210">Identificador do recurso ao qual as assinaturas de evento foram criadas.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="ba6f9-211">-Top</span><span class="sxs-lookup"><span data-stu-id="ba6f9-211">-Top</span></span>
<span data-ttu-id="ba6f9-212">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ba6f9-213">Atualmente, a filtragem é permitida somente na propriedade Name. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="ba6f9-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ba6f9-214">-TopicName</span></span>
<span data-ttu-id="ba6f9-215">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-215">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="ba6f9-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="ba6f9-216">-TopicTypeName</span></span>
<span data-ttu-id="ba6f9-217">Nome TopicType</span><span class="sxs-lookup"><span data-stu-id="ba6f9-217">TopicType name</span></span>

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

### <span data-ttu-id="ba6f9-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6f9-218">CommonParameters</span></span>
<span data-ttu-id="ba6f9-219">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6f9-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6f9-220">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba6f9-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6f9-221">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba6f9-221">INPUTS</span></span>

### <span data-ttu-id="ba6f9-222">System.String</span><span class="sxs-lookup"><span data-stu-id="ba6f9-222">System.String</span></span>

### <span data-ttu-id="ba6f9-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="ba6f9-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="ba6f9-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ba6f9-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="ba6f9-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ba6f9-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="ba6f9-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ba6f9-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ba6f9-227">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ba6f9-227">OUTPUTS</span></span>

### <span data-ttu-id="ba6f9-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ba6f9-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ba6f9-229">NOTES</span><span class="sxs-lookup"><span data-stu-id="ba6f9-229">NOTES</span></span>

## <span data-ttu-id="ba6f9-230">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba6f9-230">RELATED LINKS</span></span>
