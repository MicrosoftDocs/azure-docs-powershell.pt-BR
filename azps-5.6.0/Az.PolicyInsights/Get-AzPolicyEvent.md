---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890118"
---
# <span data-ttu-id="a6275-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a6275-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="a6275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6275-102">SYNOPSIS</span></span>
<span data-ttu-id="a6275-103">Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="a6275-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="a6275-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6275-104">SYNTAX</span></span>

### <span data-ttu-id="a6275-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6275-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6275-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a6275-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6275-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a6275-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6275-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="a6275-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6275-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="a6275-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6275-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="a6275-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6275-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="a6275-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6275-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="a6275-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6275-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6275-113">DESCRIPTION</span></span>
<span data-ttu-id="a6275-114">Obtém eventos de avaliação de política gerados à medida que os recursos são criados ou atualizados.</span><span class="sxs-lookup"><span data-stu-id="a6275-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="a6275-115">Os registros de eventos de política podem ser consultados em vários escopos com base no intervalo de tempo especificado (padrões para o último dia).</span><span class="sxs-lookup"><span data-stu-id="a6275-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="a6275-116">Os resultados podem ser filtrados, agrupados e agregaçãos de grupo podem ser computados.</span><span class="sxs-lookup"><span data-stu-id="a6275-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="a6275-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6275-117">EXAMPLES</span></span>

### <span data-ttu-id="a6275-118">Exemplo 1: Obter eventos de política no escopo de assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a6275-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="a6275-119">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="a6275-120">Exemplo 2: Obter eventos de política no escopo de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="a6275-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="a6275-121">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="a6275-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="a6275-122">Exemplo 3: Obter eventos de política no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a6275-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="a6275-123">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="a6275-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="a6275-124">Exemplo 4: Obter eventos de política no escopo do grupo de recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a6275-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="a6275-125">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="a6275-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="a6275-126">Exemplo 5: Obter eventos de política no escopo do grupo de recursos na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="a6275-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="a6275-127">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="a6275-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="a6275-128">Exemplo 6: Obter eventos de política para um recurso</span><span class="sxs-lookup"><span data-stu-id="a6275-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="a6275-129">Obtém registros de eventos de política gerados no último dia para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="a6275-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="a6275-130">Exemplo 7: Obter eventos de política para uma definição de conjunto de políticas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a6275-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a6275-131">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de políticas especificado (que existe na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="a6275-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="a6275-132">Exemplo 8: Obter eventos de política para uma definição de conjunto de políticas na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="a6275-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a6275-133">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de políticas especificado (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="a6275-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="a6275-134">Exemplo 9: Obter eventos de política para uma definição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a6275-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a6275-135">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto atual da sessão) e efetivados pela definição de política especificada (que existe na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="a6275-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="a6275-136">Exemplo 10: Obter eventos de política para uma definição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="a6275-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a6275-137">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="a6275-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="a6275-138">Exemplo 11: Obter eventos de política para uma atribuição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a6275-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="a6275-139">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="a6275-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="a6275-140">Exemplo 12: Obter eventos de política para uma atribuição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="a6275-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="a6275-141">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="a6275-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="a6275-142">Exemplo 13: Obter eventos de política para uma atribuição de política no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="a6275-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="a6275-143">Obtém registros de eventos de política gerados no último dia para todos os recursos (dentro do locatário no contexto atual da sessão) e efetivados pela atribuição de política especificada (que existe no grupo de recursos na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="a6275-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="a6275-144">Exemplo 14: Obter eventos de política no escopo de assinatura atual, com opções de consulta OrderBy, Top e Select</span><span class="sxs-lookup"><span data-stu-id="a6275-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="a6275-145">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="a6275-146">O comando ordena os resultados por propriedades de nome de atribuição de data e hora e assume apenas o top 5 daqueles listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="a6275-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="a6275-147">Ele também seleciona listar apenas um subconjunto das colunas para cada registro.</span><span class="sxs-lookup"><span data-stu-id="a6275-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="a6275-148">Exemplo 15: Obter eventos de política no escopo de assinatura atual, com opções de consulta De e Para</span><span class="sxs-lookup"><span data-stu-id="a6275-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="a6275-149">Obtém registros de eventos de política gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="a6275-150">Exemplo 16: Obter eventos de política no escopo de assinatura atual, com a opção De consulta filter</span><span class="sxs-lookup"><span data-stu-id="a6275-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="a6275-151">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="a6275-152">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do eastus).</span><span class="sxs-lookup"><span data-stu-id="a6275-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="a6275-153">Exemplo 17: Obter eventos de política no escopo de assinatura atual, com Aplicar especificando agregação de contagem de linhas</span><span class="sxs-lookup"><span data-stu-id="a6275-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="a6275-154">Obtém o número de registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="a6275-155">O comando retorna a contagem apenas dos registros de eventos de política, que é retornada dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="a6275-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="a6275-156">Exemplo 18: Obter eventos de política no escopo de assinatura atual, com Aplicar especificando agrupação com agregação</span><span class="sxs-lookup"><span data-stu-id="a6275-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="a6275-157">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="a6275-158">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas eventos de auditoria e negação).</span><span class="sxs-lookup"><span data-stu-id="a6275-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="a6275-159">Ele agrupa os resultados com base na atribuição de política, definição de política, ação de definição de política e id de recurso e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="a6275-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="a6275-160">Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas o top 5 dos listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="a6275-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="a6275-161">Exemplo 19: Obter eventos de política no escopo de assinatura atual, com Aplicar especificando agrupação sem agregação</span><span class="sxs-lookup"><span data-stu-id="a6275-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="a6275-162">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="a6275-163">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas eventos de auditoria e negação).</span><span class="sxs-lookup"><span data-stu-id="a6275-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="a6275-164">Ele grupos os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que gerou um evento de política para pelo menos uma política de auditoria ou negação.</span><span class="sxs-lookup"><span data-stu-id="a6275-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="a6275-165">Exemplo 20: Obter eventos de política no escopo de assinatura atual, com Aplicar especificando vários agrupamentos</span><span class="sxs-lookup"><span data-stu-id="a6275-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="a6275-166">Obtém registros de eventos de política gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6275-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="a6275-167">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui apenas eventos de negação).</span><span class="sxs-lookup"><span data-stu-id="a6275-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="a6275-168">Ele grupos os resultados primeiro com base na atribuição de política, definição de política e id de recurso. Em seguida, ele agrupa ainda mais os resultados desse grupo com as mesmas propriedades, exceto a ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="a6275-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="a6275-169">Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas o top 5 dos listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="a6275-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="a6275-170">Isso gera as 5 principais políticas de negação com o maior número de recursos negados.</span><span class="sxs-lookup"><span data-stu-id="a6275-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="a6275-171">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6275-171">PARAMETERS</span></span>

### <span data-ttu-id="a6275-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="a6275-172">-Apply</span></span>
<span data-ttu-id="a6275-173">Aplicar expressão para agregação usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="a6275-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="a6275-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6275-174">-DefaultProfile</span></span>
<span data-ttu-id="a6275-175">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6275-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6275-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="a6275-176">-Filter</span></span>
<span data-ttu-id="a6275-177">Expressão de filtro usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="a6275-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="a6275-178">-From</span><span class="sxs-lookup"><span data-stu-id="a6275-178">-From</span></span>
<span data-ttu-id="a6275-179">Data/hora formatada da ISO 8601 especificando a hora de início do intervalo a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="a6275-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="a6275-180">Quando não especificado, o valor do parâmetro 'To' é padrão menos 1 dia.</span><span class="sxs-lookup"><span data-stu-id="a6275-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="a6275-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a6275-181">-ManagementGroupName</span></span>
<span data-ttu-id="a6275-182">Nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="a6275-182">Management group name.</span></span>

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

### <span data-ttu-id="a6275-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="a6275-183">-OrderBy</span></span>
<span data-ttu-id="a6275-184">Expressão de ordenação usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="a6275-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="a6275-185">Um ou mais nomes de coluna separados por vírgulas com um "desc" opcional (o padrão) ou "asc".</span><span class="sxs-lookup"><span data-stu-id="a6275-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="a6275-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a6275-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="a6275-187">Nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="a6275-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="a6275-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a6275-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="a6275-189">Nome da definição de política.</span><span class="sxs-lookup"><span data-stu-id="a6275-189">Policy definition name.</span></span>

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

### <span data-ttu-id="a6275-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a6275-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="a6275-191">Nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="a6275-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="a6275-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6275-192">-ResourceGroupName</span></span>
<span data-ttu-id="a6275-193">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6275-193">Resource group name.</span></span>

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

### <span data-ttu-id="a6275-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6275-194">-ResourceId</span></span>
<span data-ttu-id="a6275-195">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a6275-195">Resource ID.</span></span>

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

### <span data-ttu-id="a6275-196">-Select</span><span class="sxs-lookup"><span data-stu-id="a6275-196">-Select</span></span>
<span data-ttu-id="a6275-197">Selecione expressão usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="a6275-197">Select expression using OData notation.</span></span>
<span data-ttu-id="a6275-198">Um ou mais nomes de coluna separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="a6275-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="a6275-199">Limita as colunas em cada registro apenas às solicitadas.</span><span class="sxs-lookup"><span data-stu-id="a6275-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="a6275-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6275-200">-SubscriptionId</span></span>
<span data-ttu-id="a6275-201">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a6275-201">Subscription ID.</span></span>

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

### <span data-ttu-id="a6275-202">-To</span><span class="sxs-lookup"><span data-stu-id="a6275-202">-To</span></span>
<span data-ttu-id="a6275-203">Data/hora formatada da ISO 8601 especificando a hora de término do intervalo a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="a6275-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="a6275-204">Quando não especificado, o padrão é a hora da solicitação.</span><span class="sxs-lookup"><span data-stu-id="a6275-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="a6275-205">-Top</span><span class="sxs-lookup"><span data-stu-id="a6275-205">-Top</span></span>
<span data-ttu-id="a6275-206">Número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="a6275-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="a6275-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6275-207">CommonParameters</span></span>
<span data-ttu-id="a6275-208">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6275-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6275-209">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6275-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6275-210">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6275-210">INPUTS</span></span>

### <span data-ttu-id="a6275-211">System.String</span><span class="sxs-lookup"><span data-stu-id="a6275-211">System.String</span></span>

## <span data-ttu-id="a6275-212">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6275-212">OUTPUTS</span></span>

### <span data-ttu-id="a6275-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a6275-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="a6275-214">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6275-214">NOTES</span></span>

## <span data-ttu-id="a6275-215">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6275-215">RELATED LINKS</span></span>
