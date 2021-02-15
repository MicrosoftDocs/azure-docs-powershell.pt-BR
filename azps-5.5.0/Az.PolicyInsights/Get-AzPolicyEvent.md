---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115013"
---
# <span data-ttu-id="afeea-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="afeea-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="afeea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afeea-102">SYNOPSIS</span></span>
<span data-ttu-id="afeea-103">Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="afeea-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="afeea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afeea-104">SYNTAX</span></span>

### <span data-ttu-id="afeea-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="afeea-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="afeea-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="afeea-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="afeea-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="afeea-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="afeea-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="afeea-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-112">Resourcescope</span><span class="sxs-lookup"><span data-stu-id="afeea-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afeea-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="afeea-113">DESCRIPTION</span></span>
<span data-ttu-id="afeea-114">Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="afeea-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="afeea-115">Os registros de eventos de política podem ser consultados em vários escopos com base no intervalo de tempo especificado (padrões para o último dia).</span><span class="sxs-lookup"><span data-stu-id="afeea-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="afeea-116">Os resultados podem ser filtrados, agrupados e agregados de grupo podem ser computados.</span><span class="sxs-lookup"><span data-stu-id="afeea-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="afeea-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="afeea-117">EXAMPLES</span></span>

### <span data-ttu-id="afeea-118">Exemplo 1: Obter eventos de política no escopo da assinatura atual</span><span class="sxs-lookup"><span data-stu-id="afeea-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="afeea-119">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="afeea-120">Exemplo 2: Obter eventos de política no escopo de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="afeea-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="afeea-121">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="afeea-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="afeea-122">Exemplo 3: Obter eventos de política no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="afeea-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="afeea-123">Obtém registros de eventos de política gerados no último dia para todos os recursos do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="afeea-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="afeea-124">Exemplo 4: Obter eventos de política no escopo do grupo de recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="afeea-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="afeea-125">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="afeea-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="afeea-126">Exemplo 5: Obter eventos de política no escopo do grupo de recursos na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="afeea-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="afeea-127">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="afeea-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="afeea-128">Exemplo 6: Obter eventos de política para um recurso</span><span class="sxs-lookup"><span data-stu-id="afeea-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="afeea-129">Obtém registros de eventos de política gerados no último dia para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="afeea-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="afeea-130">Exemplo 7: Obter eventos de política para uma definição de conjunto de políticas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="afeea-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="afeea-131">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) efetivados pela definição de conjunto de política especificado (que existe na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="afeea-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="afeea-132">Exemplo 8: Obter eventos de política para uma definição de conjunto de políticas na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="afeea-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="afeea-133">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="afeea-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="afeea-134">Exemplo 9: Obter eventos de política para uma definição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="afeea-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="afeea-135">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="afeea-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="afeea-136">Exemplo 10: Obter eventos de política para uma definição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="afeea-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="afeea-137">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="afeea-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="afeea-138">Exemplo 11: Obter eventos de política para uma atribuição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="afeea-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="afeea-139">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="afeea-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="afeea-140">Exemplo 12: Obter eventos de política para uma atribuição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="afeea-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="afeea-141">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="afeea-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="afeea-142">Exemplo 13: Obter eventos de política para uma atribuição de política no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="afeea-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="afeea-143">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe no grupo de recursos na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="afeea-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="afeea-144">Exemplo 14: Obter eventos de política no escopo da assinatura atual, com as opções de consulta OrderBy, Top e Select</span><span class="sxs-lookup"><span data-stu-id="afeea-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="afeea-145">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="afeea-146">O comando ordena os resultados por data/hora e propriedades de nome de atribuição de política e leva apenas 5 dos 5 primeiros listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="afeea-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="afeea-147">Ele também seleciona para listar apenas um subconjunto das colunas para cada registro.</span><span class="sxs-lookup"><span data-stu-id="afeea-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="afeea-148">Exemplo 15: Obter eventos de política no escopo da assinatura atual, com opções de consulta De e Para</span><span class="sxs-lookup"><span data-stu-id="afeea-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="afeea-149">Obtém registros de eventos de política gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="afeea-150">Exemplo 16: Obter eventos de política no escopo da assinatura atual, com a opção de consulta Filtro</span><span class="sxs-lookup"><span data-stu-id="afeea-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="afeea-151">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="afeea-152">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do leste).</span><span class="sxs-lookup"><span data-stu-id="afeea-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="afeea-153">Exemplo 17: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando agregação de contagem de linhas</span><span class="sxs-lookup"><span data-stu-id="afeea-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="afeea-154">Obtém o número de registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="afeea-155">O comando retorna a contagem apenas dos registros de eventos de política, que são retornados dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="afeea-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="afeea-156">Exemplo 18: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando o agrupamento com agregação</span><span class="sxs-lookup"><span data-stu-id="afeea-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="afeea-157">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="afeea-158">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas eventos de auditoria e negação).</span><span class="sxs-lookup"><span data-stu-id="afeea-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="afeea-159">Ele agrupa os resultados com base na atribuição de política, definição de política, ação de definição de política e ID de recurso, e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="afeea-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="afeea-160">Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas 5 dos 5 primeiros listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="afeea-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="afeea-161">Exemplo 19: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando o agrupamento sem agregação</span><span class="sxs-lookup"><span data-stu-id="afeea-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="afeea-162">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="afeea-163">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas eventos de auditoria e negação).</span><span class="sxs-lookup"><span data-stu-id="afeea-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="afeea-164">Ele grupos os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que gerou um evento de política para pelo menos uma política de auditoria ou negação.</span><span class="sxs-lookup"><span data-stu-id="afeea-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="afeea-165">Exemplo 20: Obter eventos de política no escopo da assinatura atual, com Aplicar especificando vários grupos</span><span class="sxs-lookup"><span data-stu-id="afeea-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="afeea-166">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="afeea-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="afeea-167">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas negar eventos).</span><span class="sxs-lookup"><span data-stu-id="afeea-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="afeea-168">Ele grupos os resultados primeiro com base na atribuição de política, na definição da política e na ID do recurso. Em seguida, agrupa ainda mais os resultados desse grupo com as mesmas propriedades, exceto a ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="afeea-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="afeea-169">Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas 5 dos 5 primeiros listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="afeea-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="afeea-170">Isso gera as cinco principais políticas de negação com o maior número de recursos negados.</span><span class="sxs-lookup"><span data-stu-id="afeea-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="afeea-171">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afeea-171">PARAMETERS</span></span>

### <span data-ttu-id="afeea-172">-Aplicar</span><span class="sxs-lookup"><span data-stu-id="afeea-172">-Apply</span></span>
<span data-ttu-id="afeea-173">Aplicar expressão para agregação usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="afeea-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="afeea-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afeea-174">-DefaultProfile</span></span>
<span data-ttu-id="afeea-175">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="afeea-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afeea-176">-Filtro</span><span class="sxs-lookup"><span data-stu-id="afeea-176">-Filter</span></span>
<span data-ttu-id="afeea-177">Expressão de filtro usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="afeea-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="afeea-178">-De</span><span class="sxs-lookup"><span data-stu-id="afeea-178">-From</span></span>
<span data-ttu-id="afeea-179">O data/hora formatado iso 8601 especifica a hora de início do intervalo a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="afeea-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="afeea-180">Quando não especificado, o padrão é o valor do parâmetro 'Para' menos 1 dia.</span><span class="sxs-lookup"><span data-stu-id="afeea-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="afeea-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="afeea-181">-ManagementGroupName</span></span>
<span data-ttu-id="afeea-182">Nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="afeea-182">Management group name.</span></span>

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

### <span data-ttu-id="afeea-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="afeea-183">-OrderBy</span></span>
<span data-ttu-id="afeea-184">Expressão de ordenação usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="afeea-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="afeea-185">Um ou mais nomes de coluna separados por vírgulas com um "desc" opcional (o padrão) ou "asc".</span><span class="sxs-lookup"><span data-stu-id="afeea-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="afeea-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="afeea-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="afeea-187">Nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="afeea-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="afeea-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="afeea-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="afeea-189">Nome da definição de política.</span><span class="sxs-lookup"><span data-stu-id="afeea-189">Policy definition name.</span></span>

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

### <span data-ttu-id="afeea-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="afeea-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="afeea-191">Nome de definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="afeea-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="afeea-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afeea-192">-ResourceGroupName</span></span>
<span data-ttu-id="afeea-193">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="afeea-193">Resource group name.</span></span>

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

### <span data-ttu-id="afeea-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afeea-194">-ResourceId</span></span>
<span data-ttu-id="afeea-195">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="afeea-195">Resource ID.</span></span>

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

### <span data-ttu-id="afeea-196">-Selecionar</span><span class="sxs-lookup"><span data-stu-id="afeea-196">-Select</span></span>
<span data-ttu-id="afeea-197">Selecione a expressão usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="afeea-197">Select expression using OData notation.</span></span>
<span data-ttu-id="afeea-198">Um ou mais nomes de coluna separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="afeea-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="afeea-199">Limita as colunas em cada registro apenas às solicitadas.</span><span class="sxs-lookup"><span data-stu-id="afeea-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="afeea-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afeea-200">-SubscriptionId</span></span>
<span data-ttu-id="afeea-201">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="afeea-201">Subscription ID.</span></span>

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

### <span data-ttu-id="afeea-202">-Para</span><span class="sxs-lookup"><span data-stu-id="afeea-202">-To</span></span>
<span data-ttu-id="afeea-203">ÉO 8601 data/hora formatada especificando a hora de término do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="afeea-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="afeea-204">Quando não especificado, o padrão é o horário da solicitação.</span><span class="sxs-lookup"><span data-stu-id="afeea-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="afeea-205">-Superior</span><span class="sxs-lookup"><span data-stu-id="afeea-205">-Top</span></span>
<span data-ttu-id="afeea-206">Número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="afeea-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="afeea-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afeea-207">CommonParameters</span></span>
<span data-ttu-id="afeea-208">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afeea-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afeea-209">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afeea-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afeea-210">Entradas</span><span class="sxs-lookup"><span data-stu-id="afeea-210">INPUTS</span></span>

### <span data-ttu-id="afeea-211">System.String</span><span class="sxs-lookup"><span data-stu-id="afeea-211">System.String</span></span>

## <span data-ttu-id="afeea-212">Saídas</span><span class="sxs-lookup"><span data-stu-id="afeea-212">OUTPUTS</span></span>

### <span data-ttu-id="afeea-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="afeea-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="afeea-214">Notas</span><span class="sxs-lookup"><span data-stu-id="afeea-214">NOTES</span></span>

## <span data-ttu-id="afeea-215">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afeea-215">RELATED LINKS</span></span>
