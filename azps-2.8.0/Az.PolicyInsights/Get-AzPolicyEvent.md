---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 1a0b2a4c66dba962518b9bb5ebca565f4bcd41bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772826"
---
# <span data-ttu-id="6619e-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6619e-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="6619e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6619e-102">SYNOPSIS</span></span>
<span data-ttu-id="6619e-103">Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="6619e-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="6619e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6619e-104">SYNTAX</span></span>

### <span data-ttu-id="6619e-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="6619e-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6619e-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="6619e-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6619e-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="6619e-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6619e-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="6619e-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6619e-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="6619e-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6619e-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="6619e-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6619e-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="6619e-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6619e-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="6619e-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6619e-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6619e-113">DESCRIPTION</span></span>
<span data-ttu-id="6619e-114">Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="6619e-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="6619e-115">Registros de eventos de política podem ser consultados em vários escopos com base no intervalo de tempo especificado (o padrão é o último dia).</span><span class="sxs-lookup"><span data-stu-id="6619e-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="6619e-116">Os resultados podem ser calculados, agrupados e as agregações de grupo podem ser calculadas.</span><span class="sxs-lookup"><span data-stu-id="6619e-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="6619e-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6619e-117">EXAMPLES</span></span>

### <span data-ttu-id="6619e-118">Exemplo 1: obter eventos de política no escopo de assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6619e-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="6619e-119">Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="6619e-120">Exemplo 2: obter eventos de política no escopo de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="6619e-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="6619e-121">Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="6619e-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="6619e-122">Exemplo 3: obter eventos de política no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="6619e-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="6619e-123">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="6619e-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="6619e-124">Exemplo 4: obter eventos de política no escopo do grupo de recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6619e-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="6619e-125">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="6619e-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="6619e-126">Exemplo 5: obter eventos de política no escopo do grupo de recursos na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="6619e-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="6619e-127">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="6619e-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="6619e-128">Exemplo 6: obter eventos de política para um recurso</span><span class="sxs-lookup"><span data-stu-id="6619e-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="6619e-129">Obtém os registros de eventos de política gerados no último dia do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="6619e-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="6619e-130">Exemplo 7: obter eventos de política para uma definição de conjunto de políticas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6619e-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6619e-131">Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="6619e-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6619e-132">Exemplo 8: obter eventos de política para uma definição de política definida na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="6619e-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6619e-133">Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="6619e-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6619e-134">Exemplo 9: obter eventos de política para uma definição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6619e-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6619e-135">Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="6619e-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6619e-136">Exemplo 10: obter eventos de política para uma definição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="6619e-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6619e-137">Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="6619e-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6619e-138">Exemplo 11: obter eventos de política para uma atribuição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6619e-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6619e-139">Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="6619e-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6619e-140">Exemplo 12: obter eventos de política para uma atribuição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="6619e-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6619e-141">Obtém os registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="6619e-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6619e-142">Exemplo 13: obter eventos de política para uma atribuição de política no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6619e-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6619e-143">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe no grupo de recursos na assinatura do contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="6619e-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="6619e-144">Exemplo 14: obter eventos de política em escopo de assinatura atual, com as opções de consulta OrderBy, Top e Select</span><span class="sxs-lookup"><span data-stu-id="6619e-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="6619e-145">Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6619e-146">O comando ordena os resultados por carimbos de data/hora e propriedades de nome da atribuição de política e leva apenas as cinco primeiras das primeiras listadas nesta ordem.</span><span class="sxs-lookup"><span data-stu-id="6619e-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="6619e-147">Ele também seleciona para listar apenas um subconjunto de colunas para cada registro.</span><span class="sxs-lookup"><span data-stu-id="6619e-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="6619e-148">Exemplo 15: obter eventos de política no escopo de assinatura atual, com as opções de consulta de e até</span><span class="sxs-lookup"><span data-stu-id="6619e-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="6619e-149">Obtém registros de eventos de política gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="6619e-150">Exemplo 16: obter eventos de política em escopo de assinatura atual, com opção de consulta de filtro</span><span class="sxs-lookup"><span data-stu-id="6619e-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="6619e-151">Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="6619e-152">O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do lesteus).</span><span class="sxs-lookup"><span data-stu-id="6619e-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="6619e-153">Exemplo 17: obter eventos de política no escopo atual da assinatura, com aplicar especificando a agregação de contagem de linhas</span><span class="sxs-lookup"><span data-stu-id="6619e-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="6619e-154">Obtém o número de registros de eventos de política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="6619e-155">O comando retorna a contagem dos registros de eventos de política apenas, que é retornada dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="6619e-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="6619e-156">Exemplo 18: obter eventos de política no escopo de assinatura atual, com aplicar ao agrupamento de agrupamento com agregação</span><span class="sxs-lookup"><span data-stu-id="6619e-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="6619e-157">Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6619e-158">O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui apenas eventos Audit e Deny).</span><span class="sxs-lookup"><span data-stu-id="6619e-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="6619e-159">Ele agrupa os resultados com base em atribuição de política, definição de política, ação de definição de política e ID do recurso e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="6619e-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="6619e-160">Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="6619e-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="6619e-161">Exemplo 19: obter eventos de política no escopo de assinatura atual, com aplicar ao agrupamento sem agregação</span><span class="sxs-lookup"><span data-stu-id="6619e-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="6619e-162">Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6619e-163">O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui apenas eventos Audit e Deny).</span><span class="sxs-lookup"><span data-stu-id="6619e-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="6619e-164">Ele agrupa os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que gerou um evento de política para pelo menos uma política de auditoria ou negação.</span><span class="sxs-lookup"><span data-stu-id="6619e-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="6619e-165">Exemplo 20: obter eventos de política no escopo atual da assinatura, com aplicar vários agrupamentos</span><span class="sxs-lookup"><span data-stu-id="6619e-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="6619e-166">Obtém os registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="6619e-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6619e-167">O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui apenas eventos Deny).</span><span class="sxs-lookup"><span data-stu-id="6619e-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="6619e-168">Ele agrupa os resultados primeiro com base na atribuição da política, na definição da política e na ID do recurso. Em seguida, ele agrupa ainda mais os resultados desse Agrupamento com as mesmas propriedades, exceto para ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="6619e-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="6619e-169">Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="6619e-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="6619e-170">Isso gera as cinco principais políticas de negação com o maior número de recursos negados.</span><span class="sxs-lookup"><span data-stu-id="6619e-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="6619e-171">OS</span><span class="sxs-lookup"><span data-stu-id="6619e-171">PARAMETERS</span></span>

### <span data-ttu-id="6619e-172">-Aplicar</span><span class="sxs-lookup"><span data-stu-id="6619e-172">-Apply</span></span>
<span data-ttu-id="6619e-173">Aplicar expressão para agregações usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="6619e-173">Apply expression for aggregations using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6619e-174">-DefaultProfile</span></span>
<span data-ttu-id="6619e-175">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6619e-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6619e-176">-Filtro</span><span class="sxs-lookup"><span data-stu-id="6619e-176">-Filter</span></span>
<span data-ttu-id="6619e-177">Expressão de filtro usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="6619e-177">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-178">-De</span><span class="sxs-lookup"><span data-stu-id="6619e-178">-From</span></span>
<span data-ttu-id="6619e-179">Marca de data/hora formatada ISO 8601 especificando a hora de início do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="6619e-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="6619e-180">Quando não especificado, o padrão é o valor do parâmetro ' para ' menos 1 dia.</span><span class="sxs-lookup"><span data-stu-id="6619e-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6619e-181">-ManagementGroupName</span></span>
<span data-ttu-id="6619e-182">Nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="6619e-182">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="6619e-183">-OrderBy</span></span>
<span data-ttu-id="6619e-184">Expressão de ordenação usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="6619e-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="6619e-185">Um ou mais nomes de coluna separados por vírgula com um ' DESC ' opcional (o padrão) ou ' ASC '.</span><span class="sxs-lookup"><span data-stu-id="6619e-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6619e-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="6619e-187">Nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="6619e-187">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6619e-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="6619e-189">Nome da definição da política.</span><span class="sxs-lookup"><span data-stu-id="6619e-189">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6619e-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="6619e-191">Nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="6619e-191">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6619e-192">-ResourceGroupName</span></span>
<span data-ttu-id="6619e-193">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6619e-193">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6619e-194">-ResourceId</span></span>
<span data-ttu-id="6619e-195">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="6619e-195">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-196">-Selecione</span><span class="sxs-lookup"><span data-stu-id="6619e-196">-Select</span></span>
<span data-ttu-id="6619e-197">Selecione a expressão usando a notação do OData.</span><span class="sxs-lookup"><span data-stu-id="6619e-197">Select expression using OData notation.</span></span>
<span data-ttu-id="6619e-198">Um ou mais nomes de coluna separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="6619e-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="6619e-199">Limita as colunas em cada registro a apenas aquelas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="6619e-199">Limits the columns on each record to just those requested.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6619e-200">-SubscriptionId</span></span>
<span data-ttu-id="6619e-201">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6619e-201">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-202">-To</span><span class="sxs-lookup"><span data-stu-id="6619e-202">-To</span></span>
<span data-ttu-id="6619e-203">Marca de data/hora formatada ISO 8601 especificando a hora de término do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="6619e-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="6619e-204">Quando não especificado, o padrão é a hora da solicitação.</span><span class="sxs-lookup"><span data-stu-id="6619e-204">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-205">-Início</span><span class="sxs-lookup"><span data-stu-id="6619e-205">-Top</span></span>
<span data-ttu-id="6619e-206">Número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="6619e-206">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6619e-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6619e-207">CommonParameters</span></span>
<span data-ttu-id="6619e-208">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6619e-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6619e-209">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6619e-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6619e-210">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6619e-210">INPUTS</span></span>

### <span data-ttu-id="6619e-211">System. String</span><span class="sxs-lookup"><span data-stu-id="6619e-211">System.String</span></span>

## <span data-ttu-id="6619e-212">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6619e-212">OUTPUTS</span></span>

### <span data-ttu-id="6619e-213">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6619e-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="6619e-214">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6619e-214">NOTES</span></span>

## <span data-ttu-id="6619e-215">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6619e-215">RELATED LINKS</span></span>