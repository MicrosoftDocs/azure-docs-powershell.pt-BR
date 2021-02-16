---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113207"
---
# <span data-ttu-id="c63aa-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="c63aa-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="c63aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c63aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c63aa-103">Obtém os detalhes de um domínio de Grade do Evento ou obtém uma lista de todos os domínios da Grade do Evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c63aa-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="c63aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c63aa-104">SYNTAX</span></span>

### <span data-ttu-id="c63aa-105">ResourceGroupNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c63aa-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c63aa-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c63aa-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c63aa-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c63aa-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c63aa-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="c63aa-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c63aa-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c63aa-109">DESCRIPTION</span></span>
<span data-ttu-id="c63aa-110">O Get-AzEventGridDomain cmdlet obtém os detalhes de um domínio especificado da Grade do Evento ou uma lista de todos os domínios da Grade do Evento na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="c63aa-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="c63aa-111">Se o nome de domínio for fornecido, os detalhes de um único domínio da Grade do Evento serão retornados.</span><span class="sxs-lookup"><span data-stu-id="c63aa-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="c63aa-112">Se o nome de domínio não for fornecido, uma lista de domínios será retornada.</span><span class="sxs-lookup"><span data-stu-id="c63aa-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="c63aa-113">O número de elementos retornados nesta lista é controlado pelo parâmetro Superior.</span><span class="sxs-lookup"><span data-stu-id="c63aa-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="c63aa-114">Se o valor Superior não for especificado ou $null, a lista conterá todos os itens de domínio retornados de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="c63aa-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="c63aa-115">Caso contrário, a parte superior indicará o número máximo de elementos a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="c63aa-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="c63aa-116">Se mais domínios ainda estão disponíveis, o valor no NextLink deve ser usado na próxima chamada para obter a próxima página de domínios.</span><span class="sxs-lookup"><span data-stu-id="c63aa-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="c63aa-117">Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c63aa-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="c63aa-118">A consulta de filtragem segue a sintaxe OData usando apenas a propriedade Nome.</span><span class="sxs-lookup"><span data-stu-id="c63aa-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="c63aa-119">As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="c63aa-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="c63aa-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c63aa-120">EXAMPLES</span></span>

### <span data-ttu-id="c63aa-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c63aa-121">Example 1</span></span>

<span data-ttu-id="c63aa-122">Obtém os detalhes do domínio de Grade \` do Evento1 \` no grupo de recursos \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="c63aa-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="c63aa-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c63aa-123">Example 2</span></span>

<span data-ttu-id="c63aa-124">Obtém os detalhes do domínio de Grade do Evento1 no grupo \` de recursos \` \` MyResourceGroupName \` usando a opção ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c63aa-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="c63aa-125">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c63aa-125">Example 3</span></span>

<span data-ttu-id="c63aa-126">Listar todos os domínios da Grade do Evento no grupo de recursos \` MyResourceGroupName sem \` paginação (todos os domínios são retornados em uma única foto)</span><span class="sxs-lookup"><span data-stu-id="c63aa-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="c63aa-127">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c63aa-127">Example 4</span></span>

<span data-ttu-id="c63aa-128">Liste os domínios da Grade do Evento (se for o caso) no grupo de recursos MyResourceGroupName que satisfaz $odataFilter consulta \` \` 10 domínios por vez.</span><span class="sxs-lookup"><span data-stu-id="c63aa-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="c63aa-129">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c63aa-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c63aa-130">Para obter as próximas páginas de domínios, espera-se que o usuário ligue Get-AzEventGridDomain e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c63aa-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c63aa-131">O chamador deve parar quando o resultado for. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c63aa-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="c63aa-132">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="c63aa-132">Example 5</span></span>

<span data-ttu-id="c63aa-133">Listar todos os domínios da Grade do Evento na Assinatura do Azure sem paginação (todos os domínios são retornados em uma única foto)</span><span class="sxs-lookup"><span data-stu-id="c63aa-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="c63aa-134">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="c63aa-134">Example 6</span></span>

<span data-ttu-id="c63aa-135">Liste os domínios da Grade do Evento (se for o caso) na Assinatura do Azure que satisfaça a consulta $odataFilter 20 domínios de cada vez.</span><span class="sxs-lookup"><span data-stu-id="c63aa-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="c63aa-136">Se mais resultados estão disponíveis, a $result. O NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="c63aa-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="c63aa-137">Para obter as próximas páginas de domínios, espera-se que o usuário ligue Get-AzEventGridDomain e use o resultado. NextLink obtido da chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="c63aa-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="c63aa-138">O chamador deve parar quando o resultado for. O NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="c63aa-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="c63aa-139">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c63aa-139">PARAMETERS</span></span>

### <span data-ttu-id="c63aa-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63aa-140">-DefaultProfile</span></span>
<span data-ttu-id="c63aa-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c63aa-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63aa-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="c63aa-142">-Name</span></span>
<span data-ttu-id="c63aa-143">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c63aa-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c63aa-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="c63aa-144">-NextLink</span></span>
<span data-ttu-id="c63aa-145">O link para a próxima página de recursos a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="c63aa-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="c63aa-146">Esse valor é obtido com a primeira chamada Get-AzEventGrid cmdlet quando mais recursos ainda estão disponíveis para consulta.</span><span class="sxs-lookup"><span data-stu-id="c63aa-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="c63aa-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c63aa-147">-ODataQuery</span></span>
<span data-ttu-id="c63aa-148">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="c63aa-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="c63aa-149">No momento, a filtragem é permitida somente na propriedade Nome. As operações com suporte incluem: CONTAINS, eq (para igual), ne (para não igual), AND, OR e NOT.</span><span class="sxs-lookup"><span data-stu-id="c63aa-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c63aa-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63aa-150">-ResourceGroupName</span></span>
<span data-ttu-id="c63aa-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c63aa-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c63aa-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c63aa-152">-ResourceId</span></span>
<span data-ttu-id="c63aa-153">Identificador de Recurso representando o Domínio da Grade do Evento.</span><span class="sxs-lookup"><span data-stu-id="c63aa-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="c63aa-154">-Superior</span><span class="sxs-lookup"><span data-stu-id="c63aa-154">-Top</span></span>
<span data-ttu-id="c63aa-155">O número máximo de recursos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="c63aa-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="c63aa-156">O valor válido está entre 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="c63aa-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="c63aa-157">Se o valor superior for especificado e mais resultados ainda estarão disponíveis, o resultado conterá um link para a próxima página a ser consultada no NextLink.</span><span class="sxs-lookup"><span data-stu-id="c63aa-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="c63aa-158">Se o valor Superior não for especificado, a lista completa de recursos será retornada ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c63aa-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c63aa-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63aa-159">CommonParameters</span></span>
<span data-ttu-id="c63aa-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63aa-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63aa-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c63aa-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63aa-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="c63aa-162">INPUTS</span></span>

### <span data-ttu-id="c63aa-163">System.String</span><span class="sxs-lookup"><span data-stu-id="c63aa-163">System.String</span></span>

## <span data-ttu-id="c63aa-164">Saídas</span><span class="sxs-lookup"><span data-stu-id="c63aa-164">OUTPUTS</span></span>

### <span data-ttu-id="c63aa-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="c63aa-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="c63aa-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="c63aa-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="c63aa-167">Notas</span><span class="sxs-lookup"><span data-stu-id="c63aa-167">NOTES</span></span>

## <span data-ttu-id="c63aa-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c63aa-168">RELATED LINKS</span></span>
