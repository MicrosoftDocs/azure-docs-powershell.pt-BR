---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126980"
---
# <span data-ttu-id="587eb-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="587eb-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="587eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="587eb-102">SYNOPSIS</span></span>
<span data-ttu-id="587eb-103">Obtém os detalhes de um tópico de domínio da Grade do Evento ou obtém uma lista de todos os tópicos de domínio da Grade do Evento sob domínio específico da Grade do Evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="587eb-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="587eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="587eb-104">SYNTAX</span></span>

### <span data-ttu-id="587eb-105">DomainTopicNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="587eb-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="587eb-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="587eb-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="587eb-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="587eb-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="587eb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="587eb-108">DESCRIPTION</span></span>
<span data-ttu-id="587eb-109">O cmdlet Get-AzEventGridDomainTopic obtém os detalhes de um tópico de domínio de Grade do Evento especificado ou uma lista de todos os tópicos de domínio da Grade do Evento em um domínio específico na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="587eb-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="587eb-110">Se o nome do tópico do domínio for fornecido, os detalhes de um único tópico de domínio da Grade do Evento serão retornados.</span><span class="sxs-lookup"><span data-stu-id="587eb-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="587eb-111">Se o nome do tópico do domínio não for fornecido, uma lista de tópicos de domínio sob o nome de domínio especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="587eb-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="587eb-112">O número de elementos retornados nesta lista é controlado pelo parâmetro Superior.</span><span class="sxs-lookup"><span data-stu-id="587eb-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="587eb-113">Se o valor Superior não for especificado ou $null, a lista conterá todos os itens de tópicos de domínio.</span><span class="sxs-lookup"><span data-stu-id="587eb-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="587eb-114">Caso contrário, a parte superior indicará o número máximo de elementos a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="587eb-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="587eb-115">Se mais tópicos de domínio ainda estão disponíveis, o valor no NextLink deve ser usado na próxima chamada para obter a próxima página de tópicos de domínio.</span><span class="sxs-lookup"><span data-stu-id="587eb-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="587eb-116">Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="587eb-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="587eb-117">A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Nome.</span><span class="sxs-lookup"><span data-stu-id="587eb-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="587eb-118">As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="587eb-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="587eb-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="587eb-119">EXAMPLES</span></span>

### <span data-ttu-id="587eb-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="587eb-120">Example 1</span></span>

<span data-ttu-id="587eb-121">Obtém os detalhes do tópico de domínio da Grade do Evento DomainTopic1 em Domínio do domínio de Grade do Evento1 no grupo de recursos \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="587eb-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="587eb-122">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="587eb-122">Example 2</span></span>

<span data-ttu-id="587eb-123">Obtém os detalhes do tópico de domínio da Grade do Evento DomainTopic1 em Domínio de Domínio da Grade do Evento1 no grupo de recursos \` \` \` \` \` MyResourceGroupName \` usando a opção ResourceId.</span><span class="sxs-lookup"><span data-stu-id="587eb-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="587eb-124">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="587eb-124">Example 3</span></span>

<span data-ttu-id="587eb-125">Liste todos os tópicos de domínio da Grade do Evento em Domínio do domínio da Grade do Evento1 no grupo de recursos \` \` \` MyResourceGroupName sem paginação (todos os resultados são retornados \` em uma única tentativa).</span><span class="sxs-lookup"><span data-stu-id="587eb-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="587eb-126">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="587eb-126">Example 4</span></span>

<span data-ttu-id="587eb-127">Listar todos os tópicos de domínio da Grade do Evento em Domínio do domínio da Grade do Evento1 no grupo de recursos \` \` \` MyResourceGroupName sem paginação (todos os resultados são retornados em uma única foto) usando a opção \` ResourceId</span><span class="sxs-lookup"><span data-stu-id="587eb-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="587eb-128">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="587eb-128">Example 5</span></span>

<span data-ttu-id="587eb-129">Liste os tópicos de domínio da Grade do Evento (se for o caso) em Domínio1 no grupo de recursos \` MyResourceGroupName que satisfaça o \` \` $odataFilter consulta de 10 tópicos de domínio \` por vez.</span><span class="sxs-lookup"><span data-stu-id="587eb-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="587eb-130">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="587eb-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="587eb-131">Para obter as próximas páginas de tópicos de domínio, espera-se que o usuário ligue Get-AzEventGridDomainTopic e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="587eb-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="587eb-132">O chamador deve parar quando o resultado for. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="587eb-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="587eb-133">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="587eb-133">PARAMETERS</span></span>

### <span data-ttu-id="587eb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587eb-134">-DefaultProfile</span></span>
<span data-ttu-id="587eb-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="587eb-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="587eb-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="587eb-136">-DomainName</span></span>
<span data-ttu-id="587eb-137">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="587eb-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587eb-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="587eb-138">-Name</span></span>
<span data-ttu-id="587eb-139">Nome do tópico do domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="587eb-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587eb-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="587eb-140">-NextLink</span></span>
<span data-ttu-id="587eb-141">O link para a próxima página de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="587eb-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="587eb-142">Esse valor é obtido com a primeira chamada Get-AzEventGrid cmdlet quando mais recursos ainda estão disponíveis para consulta.</span><span class="sxs-lookup"><span data-stu-id="587eb-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="587eb-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="587eb-143">-ODataQuery</span></span>
<span data-ttu-id="587eb-144">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="587eb-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="587eb-145">No momento, a filtragem é permitida somente na propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="587eb-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587eb-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587eb-146">-ResourceGroupName</span></span>
<span data-ttu-id="587eb-147">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="587eb-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587eb-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="587eb-148">-ResourceId</span></span>
<span data-ttu-id="587eb-149">Identificador de Recurso representando o Domínio da Grade do Evento ou o Tópico de Domínio da Grade.</span><span class="sxs-lookup"><span data-stu-id="587eb-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587eb-150">-Superior</span><span class="sxs-lookup"><span data-stu-id="587eb-150">-Top</span></span>
<span data-ttu-id="587eb-151">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="587eb-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="587eb-152">No momento, a filtragem é permitida somente na propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="587eb-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587eb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587eb-153">CommonParameters</span></span>
<span data-ttu-id="587eb-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587eb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587eb-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="587eb-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587eb-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="587eb-156">INPUTS</span></span>

### <span data-ttu-id="587eb-157">System.String</span><span class="sxs-lookup"><span data-stu-id="587eb-157">System.String</span></span>

### <span data-ttu-id="587eb-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="587eb-158">System.Int32</span></span>

## <span data-ttu-id="587eb-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="587eb-159">OUTPUTS</span></span>

### <span data-ttu-id="587eb-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="587eb-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="587eb-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="587eb-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="587eb-162">Notas</span><span class="sxs-lookup"><span data-stu-id="587eb-162">NOTES</span></span>

## <span data-ttu-id="587eb-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="587eb-163">RELATED LINKS</span></span>
