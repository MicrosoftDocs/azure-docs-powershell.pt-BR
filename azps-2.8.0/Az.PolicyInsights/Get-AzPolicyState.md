---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 790d22fbf08da8c03b35b7f53559a92924cadd6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772824"
---
# <span data-ttu-id="cd917-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="cd917-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="cd917-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd917-102">SYNOPSIS</span></span>
<span data-ttu-id="cd917-103">Obtém os Estados de conformidade de política para recursos.</span><span class="sxs-lookup"><span data-stu-id="cd917-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="cd917-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd917-104">SYNTAX</span></span>

### <span data-ttu-id="cd917-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="cd917-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd917-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="cd917-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd917-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="cd917-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd917-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="cd917-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd917-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="cd917-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd917-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="cd917-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd917-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="cd917-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd917-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="cd917-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd917-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd917-113">DESCRIPTION</span></span>
<span data-ttu-id="cd917-114">Obtém os Estados de conformidade de política para recursos.</span><span class="sxs-lookup"><span data-stu-id="cd917-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="cd917-115">Os registros de estado da política podem ser consultados em vários escopos.</span><span class="sxs-lookup"><span data-stu-id="cd917-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="cd917-116">Com base no intervalo de tempo especificado (o padrão é o último dia), os Estados da política mais recente ou todas as transições de estado da política podem ser consultadas.</span><span class="sxs-lookup"><span data-stu-id="cd917-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="cd917-117">Os resultados podem ser calculados, agrupados e as agregações de grupo podem ser calculadas.</span><span class="sxs-lookup"><span data-stu-id="cd917-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="cd917-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd917-118">EXAMPLES</span></span>

### <span data-ttu-id="cd917-119">Exemplo 1: obter os Estados da política mais recentes no escopo da assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cd917-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="cd917-120">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="cd917-121">Exemplo 2: obter os Estados da política mais recentes no escopo de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="cd917-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="cd917-122">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="cd917-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="cd917-123">Exemplo 3: obter todos os Estados de política no escopo de assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cd917-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="cd917-124">Obtém todos os registros de estado do estado da política (incluindo o mais recente) gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="cd917-125">Exemplo 4: obter os Estados da política mais recentes no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="cd917-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="cd917-126">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="cd917-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="cd917-127">Exemplo 5: obter os Estados da política mais recentes no escopo do grupo de recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cd917-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="cd917-128">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="cd917-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="cd917-129">Exemplo 6: obter os Estados da política mais recentes no escopo do grupo de recursos na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="cd917-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="cd917-130">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="cd917-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="cd917-131">Exemplo 7: obter os Estados da política mais recentes para um recurso</span><span class="sxs-lookup"><span data-stu-id="cd917-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="cd917-132">Obtém os registros de estado da política mais recentes gerados no último dia do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="cd917-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="cd917-133">Exemplo 8: obter os Estados da política mais recentes para uma definição de conjunto de políticas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cd917-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="cd917-134">Obtém os últimos registros de estado da política gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="cd917-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="cd917-135">Exemplo 9: obter os Estados da política mais recentes para uma definição de política definida na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="cd917-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="cd917-136">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="cd917-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="cd917-137">Exemplo 10: obter os Estados da política mais recentes para uma definição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cd917-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="cd917-138">Obtém os últimos registros de estado da política gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela definição de política especificada (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="cd917-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="cd917-139">Exemplo 11: obter os Estados da política mais recentes para uma definição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="cd917-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="cd917-140">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="cd917-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="cd917-141">Exemplo 12: obter os Estados da política mais recentes para uma atribuição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cd917-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="cd917-142">Obtém os últimos registros de estado da política gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela atribuição de política especificada (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="cd917-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="cd917-143">Exemplo 13: obter os Estados da política mais recentes para uma atribuição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="cd917-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="cd917-144">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela atribuição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="cd917-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="cd917-145">Exemplo 14: obter os Estados da política mais recentes para uma atribuição de política no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cd917-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="cd917-146">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto da sessão atual) afetados pela atribuição de política especificada (que existe no grupo de recursos na assinatura do contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="cd917-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="cd917-147">Exemplo 15: obter os Estados da política mais recentes em escopo de assinatura atual, com as opções de consulta OrderBy, Top e Select</span><span class="sxs-lookup"><span data-stu-id="cd917-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="cd917-148">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="cd917-149">O comando ordena os resultados por carimbos de data/hora e propriedades de nome da atribuição de política e leva apenas as cinco primeiras das primeiras listadas nesta ordem.</span><span class="sxs-lookup"><span data-stu-id="cd917-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="cd917-150">Ele também seleciona para listar apenas um subconjunto de colunas para cada registro.</span><span class="sxs-lookup"><span data-stu-id="cd917-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="cd917-151">Exemplo 16: obter os Estados da política mais recentes no escopo de assinatura atual, com as opções de consulta de e até</span><span class="sxs-lookup"><span data-stu-id="cd917-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="cd917-152">Obtém os registros de estado da política mais recentes gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="cd917-153">Exemplo 17: obter os Estados da política mais recentes em escopo de assinatura atual, com opção de consulta de filtro</span><span class="sxs-lookup"><span data-stu-id="cd917-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="cd917-154">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="cd917-155">O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui ações de negação ou auditoria), status de conformidade (inclui apenas status não compatível) e local do recurso (exclui a localização do lesteus).</span><span class="sxs-lookup"><span data-stu-id="cd917-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="cd917-156">Exemplo 18: obter os Estados da política mais recentes no escopo atual da assinatura, com aplicar especificando a agregação de contagem de linhas</span><span class="sxs-lookup"><span data-stu-id="cd917-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="cd917-157">Obtém o número de registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="cd917-158">O comando retorna a contagem dos registros de estado da política apenas, que é retornada dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="cd917-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="cd917-159">Exemplo 19: obter os Estados da política mais recentes no escopo de assinatura atual, com aplicar ao agrupamento de agrupamento com agregação</span><span class="sxs-lookup"><span data-stu-id="cd917-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="cd917-160">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="cd917-161">O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas status não compatível).</span><span class="sxs-lookup"><span data-stu-id="cd917-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="cd917-162">Ele agrupa os resultados com base em atribuição de política, definição de conjunto de políticas e definição de política e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="cd917-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="cd917-163">Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="cd917-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="cd917-164">Exemplo 20: obter os Estados da política mais recentes no escopo de assinatura atual, com aplicar ao agrupamento sem agregação</span><span class="sxs-lookup"><span data-stu-id="cd917-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="cd917-165">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="cd917-166">O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas status não compatível).</span><span class="sxs-lookup"><span data-stu-id="cd917-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="cd917-167">Ele agrupa os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que não está em conformidade em pelo menos uma política.</span><span class="sxs-lookup"><span data-stu-id="cd917-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="cd917-168">Exemplo 21: obter os Estados da política mais recentes no escopo de assinatura atual, com aplicar ao mesmo tempo especificando vários agrupamentos</span><span class="sxs-lookup"><span data-stu-id="cd917-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="cd917-169">Exemplo 22: obter Estados de política mais recentes incluindo detalhes de avaliação de política de um recurso</span><span class="sxs-lookup"><span data-stu-id="cd917-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span> 
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="cd917-170">Obtém os registros de estado da política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="cd917-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="cd917-171">O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui apenas status não compatível).</span><span class="sxs-lookup"><span data-stu-id="cd917-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="cd917-172">Ele agrupa os resultados primeiro com base na atribuição da política, definição do conjunto de políticas, definição da política e ID do recurso. Em seguida, ele agrupa ainda mais os resultados desse Agrupamento com as mesmas propriedades, exceto para ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="cd917-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="cd917-173">Ele ordena os resultados pela agregação Count em ordem decrescente e leva apenas 5 principais daqueles listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="cd917-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="cd917-174">Isso gera as cinco principais políticas com a maior quantidade de recursos não compatíveis.</span><span class="sxs-lookup"><span data-stu-id="cd917-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="cd917-175">OS</span><span class="sxs-lookup"><span data-stu-id="cd917-175">PARAMETERS</span></span>

### <span data-ttu-id="cd917-176">-Tudo</span><span class="sxs-lookup"><span data-stu-id="cd917-176">-All</span></span>
<span data-ttu-id="cd917-177">Dentro do intervalo de tempo especificado, obtenha todos os Estados da política em vez do mais recente.</span><span class="sxs-lookup"><span data-stu-id="cd917-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd917-178">-Aplicar</span><span class="sxs-lookup"><span data-stu-id="cd917-178">-Apply</span></span>
<span data-ttu-id="cd917-179">Aplicar expressão para agregações usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="cd917-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="cd917-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd917-180">-DefaultProfile</span></span>
<span data-ttu-id="cd917-181">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd917-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd917-182">-Expandir</span><span class="sxs-lookup"><span data-stu-id="cd917-182">-Expand</span></span>
<span data-ttu-id="cd917-183">Expanda a expressão usando a notação do OData.</span><span class="sxs-lookup"><span data-stu-id="cd917-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd917-184">-Filtro</span><span class="sxs-lookup"><span data-stu-id="cd917-184">-Filter</span></span>
<span data-ttu-id="cd917-185">Expressão de filtro usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="cd917-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="cd917-186">-De</span><span class="sxs-lookup"><span data-stu-id="cd917-186">-From</span></span>
<span data-ttu-id="cd917-187">Marca de data/hora formatada ISO 8601 especificando a hora de início do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="cd917-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="cd917-188">Quando não especificado, o padrão é o valor do parâmetro ' para ' menos 1 dia.</span><span class="sxs-lookup"><span data-stu-id="cd917-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="cd917-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="cd917-189">-ManagementGroupName</span></span>
<span data-ttu-id="cd917-190">Nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="cd917-190">Management group name.</span></span>

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

### <span data-ttu-id="cd917-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="cd917-191">-OrderBy</span></span>
<span data-ttu-id="cd917-192">Expressão de ordenação usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="cd917-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="cd917-193">Um ou mais nomes de coluna separados por vírgula com um ' DESC ' opcional (o padrão) ou ' ASC '.</span><span class="sxs-lookup"><span data-stu-id="cd917-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="cd917-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="cd917-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="cd917-195">Nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="cd917-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="cd917-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="cd917-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="cd917-197">Nome da definição da política.</span><span class="sxs-lookup"><span data-stu-id="cd917-197">Policy definition name.</span></span>

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

### <span data-ttu-id="cd917-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="cd917-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="cd917-199">Nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="cd917-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="cd917-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd917-200">-ResourceGroupName</span></span>
<span data-ttu-id="cd917-201">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd917-201">Resource group name.</span></span>

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

### <span data-ttu-id="cd917-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd917-202">-ResourceId</span></span>
<span data-ttu-id="cd917-203">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd917-203">Resource ID.</span></span>

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

### <span data-ttu-id="cd917-204">-Selecione</span><span class="sxs-lookup"><span data-stu-id="cd917-204">-Select</span></span>
<span data-ttu-id="cd917-205">Selecione a expressão usando a notação do OData.</span><span class="sxs-lookup"><span data-stu-id="cd917-205">Select expression using OData notation.</span></span>
<span data-ttu-id="cd917-206">Um ou mais nomes de coluna separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="cd917-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="cd917-207">Limita as colunas em cada registro a apenas aquelas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="cd917-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="cd917-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd917-208">-SubscriptionId</span></span>
<span data-ttu-id="cd917-209">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="cd917-209">Subscription ID.</span></span>

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

### <span data-ttu-id="cd917-210">-To</span><span class="sxs-lookup"><span data-stu-id="cd917-210">-To</span></span>
<span data-ttu-id="cd917-211">Marca de data/hora formatada ISO 8601 especificando a hora de término do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="cd917-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="cd917-212">Quando não especificado, o padrão é a hora da solicitação.</span><span class="sxs-lookup"><span data-stu-id="cd917-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="cd917-213">-Início</span><span class="sxs-lookup"><span data-stu-id="cd917-213">-Top</span></span>
<span data-ttu-id="cd917-214">Número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="cd917-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="cd917-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd917-215">CommonParameters</span></span>
<span data-ttu-id="cd917-216">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd917-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd917-217">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd917-217">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd917-218">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd917-218">INPUTS</span></span>

### <span data-ttu-id="cd917-219">System. String</span><span class="sxs-lookup"><span data-stu-id="cd917-219">System.String</span></span>

## <span data-ttu-id="cd917-220">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd917-220">OUTPUTS</span></span>

### <span data-ttu-id="cd917-221">Microsoft. Azure. Commands. PolicyInsights. Models. Policystate</span><span class="sxs-lookup"><span data-stu-id="cd917-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="cd917-222">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd917-222">NOTES</span></span>

## <span data-ttu-id="cd917-223">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd917-223">RELATED LINKS</span></span>

[<span data-ttu-id="cd917-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="cd917-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
