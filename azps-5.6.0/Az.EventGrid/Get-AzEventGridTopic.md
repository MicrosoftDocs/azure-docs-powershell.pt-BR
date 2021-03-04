---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2af8125f91618cd929a9389d9327532376e92af1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890427"
---
# <span data-ttu-id="b3f06-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="b3f06-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="b3f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3f06-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f06-103">Obtém os detalhes de um tópico de Grade de Eventos ou obtém uma lista de todos os tópicos da Grade de Eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f06-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="b3f06-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b3f06-104">SYNTAX</span></span>

### <span data-ttu-id="b3f06-105">ResourceGroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b3f06-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f06-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3f06-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f06-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3f06-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3f06-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3f06-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3f06-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b3f06-109">DESCRIPTION</span></span>
<span data-ttu-id="b3f06-110">O Get-AzEventGridTopic cmdlet obtém os detalhes de um Tópico de Grade de Eventos especificado ou uma lista de todos os tópicos da Grade de Eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f06-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="b3f06-111">Se o nome do tópico for fornecido, os detalhes de um único Tópico de Grade de Eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="b3f06-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="b3f06-112">Se o nome do tópico não for fornecido, uma lista de tópicos será retornada.</span><span class="sxs-lookup"><span data-stu-id="b3f06-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="b3f06-113">O número de elementos retornados nesta lista é controlado pelo parâmetro Top.</span><span class="sxs-lookup"><span data-stu-id="b3f06-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="b3f06-114">Se o valor Top não for especificado ou $null, a lista conterá todos os itens de tópicos.</span><span class="sxs-lookup"><span data-stu-id="b3f06-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="b3f06-115">Caso contrário, Top indicará o número máximo de elementos a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="b3f06-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="b3f06-116">Se mais tópicos ainda estão disponíveis, o valor em NextLink deve ser usado na próxima chamada para obter a próxima página de tópicos.</span><span class="sxs-lookup"><span data-stu-id="b3f06-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="b3f06-117">Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b3f06-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="b3f06-118">A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="b3f06-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="b3f06-119">As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="b3f06-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="b3f06-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3f06-120">EXAMPLES</span></span>

### <span data-ttu-id="b3f06-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b3f06-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="b3f06-122">Obtém os detalhes do tópico de Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b3f06-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b3f06-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b3f06-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="b3f06-124">Obtém os detalhes do tópico de Grade de Eventos1 no grupo de recursos \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b3f06-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b3f06-125">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b3f06-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="b3f06-126">Listar todos os tópicos da Grade de Eventos no grupo de recursos \` MyResourceGroupName \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="b3f06-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="b3f06-127">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="b3f06-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="b3f06-128">Listar os primeiros 10 tópicos da Grade de Eventos (se for o caso) no grupo de recursos MyResourceGroupName que atenda ao $odataFilter \` \` consulta.</span><span class="sxs-lookup"><span data-stu-id="b3f06-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="b3f06-129">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="b3f06-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="b3f06-130">Para obter as próximas páginas de tópicos, espera-se que o usuário chame Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="b3f06-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="b3f06-131">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="b3f06-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="b3f06-132">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="b3f06-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="b3f06-133">Listar todos os tópicos da Grade de Eventos na assinatura sem paginação.</span><span class="sxs-lookup"><span data-stu-id="b3f06-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="b3f06-134">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="b3f06-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="b3f06-135">Listar os primeiros 10 tópicos da Grade de Eventos (se algum) na assinatura que atenda ao $odataFilter consulta.</span><span class="sxs-lookup"><span data-stu-id="b3f06-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="b3f06-136">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="b3f06-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="b3f06-137">Para obter as próximas páginas de tópicos, espera-se que o usuário chame Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="b3f06-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="b3f06-138">O chamador deve parar quando o resultado. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="b3f06-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="b3f06-139">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b3f06-139">PARAMETERS</span></span>

### <span data-ttu-id="b3f06-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f06-140">-DefaultProfile</span></span>
<span data-ttu-id="b3f06-141">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b3f06-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3f06-142">-Name</span><span class="sxs-lookup"><span data-stu-id="b3f06-142">-Name</span></span>
<span data-ttu-id="b3f06-143">Nome do tópico EventGrid.</span><span class="sxs-lookup"><span data-stu-id="b3f06-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f06-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="b3f06-144">-NextLink</span></span>
<span data-ttu-id="b3f06-145">O link para a próxima página de recursos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="b3f06-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="b3f06-146">Esse valor é obtido com a primeira chamada Get-AzEventGrid cmdlet quando mais recursos ainda estão disponíveis para consulta.</span><span class="sxs-lookup"><span data-stu-id="b3f06-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="b3f06-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b3f06-147">-ODataQuery</span></span>
<span data-ttu-id="b3f06-148">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="b3f06-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="b3f06-149">Atualmente, a filtragem é permitida somente na propriedade Name. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="b3f06-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f06-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f06-150">-ResourceGroupName</span></span>
<span data-ttu-id="b3f06-151">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b3f06-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f06-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3f06-152">-ResourceId</span></span>
<span data-ttu-id="b3f06-153">Identificador de Recurso que representa o Tópico da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="b3f06-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="b3f06-154">-Top</span><span class="sxs-lookup"><span data-stu-id="b3f06-154">-Top</span></span>
<span data-ttu-id="b3f06-155">O número máximo de recursos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="b3f06-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="b3f06-156">O valor válido está entre 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="b3f06-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="b3f06-157">Se o valor superior for especificado e mais resultados ainda estão disponíveis, o resultado conterá um link para a próxima página a ser consultada no NextLink.</span><span class="sxs-lookup"><span data-stu-id="b3f06-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="b3f06-158">Se o valor Top não for especificado, a lista completa de recursos será retornada de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="b3f06-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f06-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f06-159">CommonParameters</span></span>
<span data-ttu-id="b3f06-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f06-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f06-161">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3f06-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f06-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3f06-162">INPUTS</span></span>

### <span data-ttu-id="b3f06-163">System.String</span><span class="sxs-lookup"><span data-stu-id="b3f06-163">System.String</span></span>

### <span data-ttu-id="b3f06-164">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b3f06-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b3f06-165">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b3f06-165">OUTPUTS</span></span>

### <span data-ttu-id="b3f06-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="b3f06-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="b3f06-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="b3f06-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="b3f06-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="b3f06-168">NOTES</span></span>

## <span data-ttu-id="b3f06-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3f06-169">RELATED LINKS</span></span>
