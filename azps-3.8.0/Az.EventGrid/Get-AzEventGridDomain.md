---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: f2f3c3799ff16cdcc5f1091f8a66cb531cf46cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777535"
---
# <span data-ttu-id="36891-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="36891-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="36891-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36891-102">SYNOPSIS</span></span>
<span data-ttu-id="36891-103">Obtém os detalhes de um domínio de grade de eventos ou obtém uma lista de todos os domínios de grade de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="36891-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="36891-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36891-104">SYNTAX</span></span>

### <span data-ttu-id="36891-105">ResourceGroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="36891-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36891-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36891-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36891-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="36891-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36891-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="36891-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36891-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36891-109">DESCRIPTION</span></span>
<span data-ttu-id="36891-110">O cmdlet Get-AzEventGridDomain Obtém os detalhes de um domínio de grade de eventos especificado ou uma lista de todos os domínios de grade de eventos na assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="36891-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="36891-111">Se o nome de domínio for fornecido, os detalhes de um único domínio de grade de eventos serão retornados.</span><span class="sxs-lookup"><span data-stu-id="36891-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="36891-112">Se o nome de domínio não for fornecido, uma lista de domínios será retornada.</span><span class="sxs-lookup"><span data-stu-id="36891-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="36891-113">O número de elementos retornados nessa lista é controlado pelo parâmetro Top.</span><span class="sxs-lookup"><span data-stu-id="36891-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="36891-114">Se o valor superior não for especificado ou $null, a lista conterá todos os itens de domínios retornados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="36891-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="36891-115">Caso contrário, o superior indicará o número máximo de elementos a serem retornados na lista.</span><span class="sxs-lookup"><span data-stu-id="36891-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="36891-116">Se mais domínios ainda estiverem disponíveis, o valor em NextLink deve ser usado na próxima chamada para obter a próxima página de domínios.</span><span class="sxs-lookup"><span data-stu-id="36891-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="36891-117">Por fim, o parâmetro ODataQuery é usado para executar a filtragem dos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="36891-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="36891-118">A consulta filtragem segue a sintaxe OData usando somente a propriedade Name.</span><span class="sxs-lookup"><span data-stu-id="36891-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="36891-119">As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.</span><span class="sxs-lookup"><span data-stu-id="36891-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="36891-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36891-120">EXAMPLES</span></span>

### <span data-ttu-id="36891-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36891-121">Example 1</span></span>

<span data-ttu-id="36891-122">Obtém os detalhes da domain1 de domínio da grade \` \` de eventos na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="36891-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="36891-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="36891-123">Example 2</span></span>

<span data-ttu-id="36891-124">Obtém os detalhes da domain1 de domínio da grade de eventos \` \` na opção MyResourceGroupName grupo de recursos \` usando a \` opção ResourceId.</span><span class="sxs-lookup"><span data-stu-id="36891-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="36891-125">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="36891-125">Example 3</span></span>

<span data-ttu-id="36891-126">Listar todos os domínios da grade de eventos na MyResourceGroupName do grupo de recursos \` \` sem paginação (todos os domínios são retornados em uma única captura)</span><span class="sxs-lookup"><span data-stu-id="36891-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="36891-127">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="36891-127">Example 4</span></span>

<span data-ttu-id="36891-128">Liste os domínios de grade de eventos (se houver) no grupo de MyResourceGroupName de recursos \` \` que satisfaçam o $odataFilter consulta 10 domínios de cada vez.</span><span class="sxs-lookup"><span data-stu-id="36891-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="36891-129">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="36891-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="36891-130">Para obter a (s) próxima (s) página (s) de domínios, espera-se que o usuário chame novamente Get-AzEventGridDomain e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="36891-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="36891-131">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="36891-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="36891-132">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="36891-132">Example 5</span></span>

<span data-ttu-id="36891-133">Listar todos os domínios de grade de eventos na assinatura do Azure sem paginação (todos os domínios são retornados em uma única captura)</span><span class="sxs-lookup"><span data-stu-id="36891-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="36891-134">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="36891-134">Example 6</span></span>

<span data-ttu-id="36891-135">Liste os domínios da grade de eventos (se houver) na assinatura do Azure que satisfaça o $odataFilter Query 20 Domains de cada vez.</span><span class="sxs-lookup"><span data-stu-id="36891-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="36891-136">Se houver mais resultados disponíveis, o $result. NextLink não será $null.</span><span class="sxs-lookup"><span data-stu-id="36891-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="36891-137">Para obter a (s) próxima (s) página (s) de domínios, espera-se que o usuário chame novamente Get-AzEventGridDomain e use o resultado. NextLink obtidos na chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="36891-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="36891-138">O chamador deve parar quando o resultado for. NextLink se torna $null.</span><span class="sxs-lookup"><span data-stu-id="36891-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="36891-139">OS</span><span class="sxs-lookup"><span data-stu-id="36891-139">PARAMETERS</span></span>

### <span data-ttu-id="36891-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36891-140">-DefaultProfile</span></span>
<span data-ttu-id="36891-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36891-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36891-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="36891-142">-Name</span></span>
<span data-ttu-id="36891-143">Nome de domínio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="36891-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36891-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="36891-144">-NextLink</span></span>
<span data-ttu-id="36891-145">O link para a próxima página de recursos a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="36891-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="36891-146">Esse valor é obtido com a primeira chamada de cmdlet Get-AzEventGrid quando mais recursos ainda estão disponíveis para consulta.</span><span class="sxs-lookup"><span data-stu-id="36891-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36891-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="36891-147">-ODataQuery</span></span>
<span data-ttu-id="36891-148">A consulta OData usada para filtrar os resultados da lista.</span><span class="sxs-lookup"><span data-stu-id="36891-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="36891-149">Atualmente, a filtragem só é permitida na propriedade Name. As operações com suporte incluem: CONTAINS, EQ (para igual), ne (para não igual) e, ou e não.</span><span class="sxs-lookup"><span data-stu-id="36891-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36891-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36891-150">-ResourceGroupName</span></span>
<span data-ttu-id="36891-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36891-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36891-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36891-152">-ResourceId</span></span>
<span data-ttu-id="36891-153">Identificador de recurso que representa o domínio da grade de eventos.</span><span class="sxs-lookup"><span data-stu-id="36891-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="36891-154">-Início</span><span class="sxs-lookup"><span data-stu-id="36891-154">-Top</span></span>
<span data-ttu-id="36891-155">O número máximo de recursos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="36891-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="36891-156">O valor válido é entre 1 e 100.</span><span class="sxs-lookup"><span data-stu-id="36891-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="36891-157">Se o valor principal for especificado e mais resultados ainda estiverem disponíveis, o resultado conterá um link para a próxima página a ser consultada no NextLink.</span><span class="sxs-lookup"><span data-stu-id="36891-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="36891-158">Se o valor principal não for especificado, a lista completa de recursos será retornada ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="36891-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36891-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36891-159">CommonParameters</span></span>
<span data-ttu-id="36891-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36891-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36891-161">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36891-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36891-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36891-162">INPUTS</span></span>

### <span data-ttu-id="36891-163">System. String</span><span class="sxs-lookup"><span data-stu-id="36891-163">System.String</span></span>

## <span data-ttu-id="36891-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36891-164">OUTPUTS</span></span>

### <span data-ttu-id="36891-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="36891-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="36891-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="36891-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="36891-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36891-167">NOTES</span></span>

## <span data-ttu-id="36891-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36891-168">RELATED LINKS</span></span>
