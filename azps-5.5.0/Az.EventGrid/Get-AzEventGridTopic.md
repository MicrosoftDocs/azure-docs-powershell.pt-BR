---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115324"
---
# <span data-ttu-id="8f2b3-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8f2b3-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="8f2b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2b3-103">Obtém os detalhes de um tópico de Grade do Evento ou obtém uma lista de todos os tópicos da Grade do Evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="8f2b3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f2b3-104">SYNTAX</span></span>

### <span data-ttu-id="8f2b3-105">ResourceGroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f2b3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f2b3-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f2b3-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f2b3-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f2b3-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f2b3-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f2b3-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f2b3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f2b3-109">DESCRIPTION</span></span>
<span data-ttu-id="8f2b3-110">O Get-AzEventGridTopic cmdlet obtém os detalhes de um Tópico de Grade de Evento especificado ou uma lista de todos os tópicos da Grade do Evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="8f2b3-111">Se o nome do tópico for fornecido, os detalhes de um único Tópico da Grade do Evento serão retornados.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="8f2b3-112">Se o nome do tópico não for fornecido, uma lista de tópicos será retornada.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="8f2b3-113">O número de elementos retornados nesta lista é controlado pelo parâmetro Superior.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="8f2b3-114">Se o valor Superior não for especificado ou $null, a lista conterá todos os itens de tópicos.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="8f2b3-115">Caso contrário, a parte superior indicará o número máximo de elementos a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="8f2b3-116">Se mais tópicos ainda estão disponíveis, o valor no NextLink deve ser usado na próxima chamada para obter a próxima página de tópicos.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="8f2b3-117">Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="8f2b3-118">A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Nome.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="8f2b3-119">As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="8f2b3-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f2b3-120">EXAMPLES</span></span>

### <span data-ttu-id="8f2b3-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f2b3-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="8f2b3-122">Obtém os detalhes do tópico da Grade do Evento1 no grupo \` \` de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="8f2b3-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8f2b3-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8f2b3-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="8f2b3-124">Obtém os detalhes do tópico da Grade do Evento1 no grupo \` \` de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="8f2b3-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8f2b3-125">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8f2b3-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="8f2b3-126">Liste todos os tópicos da Grade do Evento no grupo de recursos \` MyResourceGroupName \` sem paginação.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="8f2b3-127">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="8f2b3-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="8f2b3-128">Liste os primeiros 10 tópicos da Grade do Evento (se for o caso) no grupo de recursos MyResourceGroupName que satisfaça a $odataFilter \` \` consulta.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8f2b3-129">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8f2b3-130">Para obter as próximas páginas de tópicos, espera-se que o usuário ligue Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8f2b3-131">O chamador deve parar quando o resultado for. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="8f2b3-132">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="8f2b3-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="8f2b3-133">Liste todos os tópicos da Grade do Evento na assinatura sem paginação.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="8f2b3-134">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="8f2b3-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="8f2b3-135">Liste os primeiros 10 tópicos da Grade do Evento (se for o caso) na assinatura que satisfaça a $odataFilter consulta.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="8f2b3-136">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="8f2b3-137">Para obter as próximas páginas de tópicos, espera-se que o usuário ligue Get-AzEventGridTopic e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="8f2b3-138">O chamador deve parar quando o resultado for. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="8f2b3-139">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f2b3-139">PARAMETERS</span></span>

### <span data-ttu-id="8f2b3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2b3-140">-DefaultProfile</span></span>
<span data-ttu-id="8f2b3-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8f2b3-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f2b3-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f2b3-142">-Name</span></span>
<span data-ttu-id="8f2b3-143">Nome do tópico do EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="8f2b3-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="8f2b3-144">-NextLink</span></span>
<span data-ttu-id="8f2b3-145">O link para a próxima página de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="8f2b3-146">Esse valor é obtido com a primeira chamada Get-AzEventGrid cmdlet quando mais recursos ainda estão disponíveis para consulta.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="8f2b3-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8f2b3-147">-ODataQuery</span></span>
<span data-ttu-id="8f2b3-148">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="8f2b3-149">No momento, a filtragem é permitida somente na propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="8f2b3-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2b3-150">-ResourceGroupName</span></span>
<span data-ttu-id="8f2b3-151">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f2b3-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f2b3-152">-ResourceId</span></span>
<span data-ttu-id="8f2b3-153">Identificador de Recurso representando o Tópico da Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="8f2b3-154">-Superior</span><span class="sxs-lookup"><span data-stu-id="8f2b3-154">-Top</span></span>
<span data-ttu-id="8f2b3-155">O número máximo de recursos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="8f2b3-156">O valor válido está entre 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="8f2b3-157">Se o valor superior for especificado e mais resultados ainda estarão disponíveis, o resultado conterá um link para a próxima página a ser consultada no NextLink.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="8f2b3-158">Se o valor Superior não for especificado, a lista completa de recursos será retornada ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="8f2b3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2b3-159">CommonParameters</span></span>
<span data-ttu-id="8f2b3-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2b3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2b3-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f2b3-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2b3-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f2b3-162">INPUTS</span></span>

### <span data-ttu-id="8f2b3-163">System.String</span><span class="sxs-lookup"><span data-stu-id="8f2b3-163">System.String</span></span>

### <span data-ttu-id="8f2b3-164">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8f2b3-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8f2b3-165">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f2b3-165">OUTPUTS</span></span>

### <span data-ttu-id="8f2b3-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="8f2b3-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8f2b3-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="8f2b3-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="8f2b3-168">Notas</span><span class="sxs-lookup"><span data-stu-id="8f2b3-168">NOTES</span></span>

## <span data-ttu-id="8f2b3-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f2b3-169">RELATED LINKS</span></span>
