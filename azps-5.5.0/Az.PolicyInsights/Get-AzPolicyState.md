---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118202"
---
# <span data-ttu-id="23541-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="23541-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="23541-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23541-102">SYNOPSIS</span></span>
<span data-ttu-id="23541-103">Obtém estados de conformidade de política para recursos.</span><span class="sxs-lookup"><span data-stu-id="23541-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="23541-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23541-104">SYNTAX</span></span>

### <span data-ttu-id="23541-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23541-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23541-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="23541-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23541-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="23541-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23541-108">Resourcescope</span><span class="sxs-lookup"><span data-stu-id="23541-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23541-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="23541-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23541-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="23541-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23541-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="23541-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23541-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="23541-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23541-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="23541-113">DESCRIPTION</span></span>
<span data-ttu-id="23541-114">Obtém estados de conformidade de política para recursos.</span><span class="sxs-lookup"><span data-stu-id="23541-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="23541-115">Os registros de estado de política podem ser consultados em vários escopos.</span><span class="sxs-lookup"><span data-stu-id="23541-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="23541-116">Com base no intervalo de tempo especificado (padrões para o último dia), os estados de política mais recentes ou todas as transições de estado de política podem ser consultadas.</span><span class="sxs-lookup"><span data-stu-id="23541-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="23541-117">Os resultados podem ser filtrados, agrupados e agregados de grupo podem ser computados.</span><span class="sxs-lookup"><span data-stu-id="23541-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="23541-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23541-118">EXAMPLES</span></span>

### <span data-ttu-id="23541-119">Exemplo 1: Obter os estados de política mais recentes no escopo da assinatura atual</span><span class="sxs-lookup"><span data-stu-id="23541-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="23541-120">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="23541-121">Exemplo 2: Obter os estados de política mais recentes no escopo de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="23541-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="23541-122">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="23541-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="23541-123">Exemplo 3: Obter todos os estados de política no escopo da assinatura atual</span><span class="sxs-lookup"><span data-stu-id="23541-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="23541-124">Obtém todos os registros de estado de política histórico (incluindo os mais recentes) gerados no último dia para todos os recursos dentro da assinatura no contexto da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="23541-125">Exemplo 4: Obter os estados de política mais recentes no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="23541-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="23541-126">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="23541-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="23541-127">Exemplo 5: Obter os estados de política mais recentes no escopo do grupo de recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="23541-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="23541-128">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="23541-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="23541-129">Exemplo 6: Obter os estados de política mais recentes no escopo do grupo de recursos na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="23541-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="23541-130">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="23541-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="23541-131">Exemplo 7: Obter os estados de política mais recentes para um recurso</span><span class="sxs-lookup"><span data-stu-id="23541-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="23541-132">Obtém registros de estado de política mais recentes gerados no último dia para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="23541-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="23541-133">Exemplo 8: Obter os estados de política mais recentes para uma definição de conjunto de políticas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="23541-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="23541-134">Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de política especificado (que existe na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="23541-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="23541-135">Exemplo 9: Obter os estados de política mais recentes para uma definição de conjunto de políticas na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="23541-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="23541-136">Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de conjunto de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="23541-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="23541-137">Exemplo 10: Obter os estados de política mais recentes para uma definição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="23541-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="23541-138">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) efetivados pela definição de política especificada (que existe na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="23541-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="23541-139">Exemplo 11: Obter os estados de política mais recentes para uma definição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="23541-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="23541-140">Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="23541-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="23541-141">Exemplo 12: Obter os estados de política mais recentes para uma atribuição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="23541-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="23541-142">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="23541-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="23541-143">Exemplo 13: Obter os estados de política mais recentes para uma atribuição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="23541-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="23541-144">Obtém os registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="23541-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="23541-145">Exemplo 14: Obter os estados de política mais recentes para uma atribuição de política no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="23541-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="23541-146">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe no grupo de recursos na assinatura no contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="23541-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="23541-147">Exemplo 15: Obter os estados de política mais recentes no escopo da assinatura atual, com as opções de consulta OrderBy, Top e Select</span><span class="sxs-lookup"><span data-stu-id="23541-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="23541-148">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="23541-149">O comando ordena os resultados por data/hora e propriedades de nome de atribuição de política e leva apenas 5 dos 5 primeiros listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="23541-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="23541-150">Ele também seleciona para listar apenas um subconjunto das colunas para cada registro.</span><span class="sxs-lookup"><span data-stu-id="23541-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="23541-151">Exemplo 16: Obter os estados de política mais recentes no escopo da assinatura atual, com opções de consulta De e Para</span><span class="sxs-lookup"><span data-stu-id="23541-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="23541-152">Obtém registros de estado de política mais recentes gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="23541-153">Exemplo 17: Obter os estados de política mais recentes no escopo da assinatura atual, com a opção de consulta Filtro</span><span class="sxs-lookup"><span data-stu-id="23541-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="23541-154">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="23541-155">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui ações de negação ou auditoria), status de conformidade (inclui somente status não compatível) e localização de recursos (exclui o local do leste).</span><span class="sxs-lookup"><span data-stu-id="23541-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="23541-156">Exemplo 18: Obter os estados de política mais recentes no escopo da assinatura atual, com Aplicar especificando agregação de contagem de linhas</span><span class="sxs-lookup"><span data-stu-id="23541-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="23541-157">Obtém o número de registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="23541-158">O comando retorna apenas a contagem dos registros de estado de política, que é retornada dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="23541-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="23541-159">Exemplo 19: Obter os estados de política mais recentes no escopo da assinatura atual, com Aplicar especificando o agrupamento com agregação</span><span class="sxs-lookup"><span data-stu-id="23541-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="23541-160">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="23541-161">O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui somente status não compatível).</span><span class="sxs-lookup"><span data-stu-id="23541-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="23541-162">Ele agrupa os resultados com base na atribuição de política, definição de conjunto de políticas e definição de política e calcula o número de registros em cada grupo, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="23541-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="23541-163">Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas 5 dos 5 primeiros listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="23541-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="23541-164">Exemplo 20: Obter os estados de política mais recentes no escopo da assinatura atual, com Aplicar especificando o agrupamento sem agregação</span><span class="sxs-lookup"><span data-stu-id="23541-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="23541-165">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="23541-166">O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui somente status não compatível).</span><span class="sxs-lookup"><span data-stu-id="23541-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="23541-167">Ele grupos os resultados com base na ID do recurso. Isso gera a lista de todos os recursos dentro da assinatura que não são compatíveis com pelo menos uma política.</span><span class="sxs-lookup"><span data-stu-id="23541-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="23541-168">Exemplo 21: Obter os estados de política mais recentes no escopo da assinatura atual, com Aplicar especificando vários grupos</span><span class="sxs-lookup"><span data-stu-id="23541-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="23541-169">Exemplo 22: Obter os estados de política mais recentes, incluindo detalhes da avaliação da política de um recurso</span><span class="sxs-lookup"><span data-stu-id="23541-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="23541-170">Obtém registros de estado de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="23541-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="23541-171">O comando limita os resultados retornados pela filtragem com base no status de conformidade (inclui somente status não compatível).</span><span class="sxs-lookup"><span data-stu-id="23541-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="23541-172">Ele grupos os resultados primeiro com base na atribuição de política, definição de conjunto de políticas, definição de política e ID do recurso. Em seguida, agrupa ainda mais os resultados desse grupo com as mesmas propriedades, exceto a ID do recurso, e calcula o número de registros em cada um desses grupos, que é retornado dentro da propriedade AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="23541-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="23541-173">Ele ordena os resultados pela agregação de contagem em ordem decrescente e leva apenas 5 dos 5 primeiros listados nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="23541-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="23541-174">Isso gera as cinco principais políticas com o maior número de recursos não compatíveis.</span><span class="sxs-lookup"><span data-stu-id="23541-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="23541-175">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23541-175">PARAMETERS</span></span>

### <span data-ttu-id="23541-176">-Tudo</span><span class="sxs-lookup"><span data-stu-id="23541-176">-All</span></span>
<span data-ttu-id="23541-177">Dentro do intervalo de tempo especificado, obter todos os estados de política em vez de somente o mais recente.</span><span class="sxs-lookup"><span data-stu-id="23541-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="23541-178">-Aplicar</span><span class="sxs-lookup"><span data-stu-id="23541-178">-Apply</span></span>
<span data-ttu-id="23541-179">Aplicar expressão para agregação usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="23541-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="23541-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23541-180">-DefaultProfile</span></span>
<span data-ttu-id="23541-181">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23541-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23541-182">-Expandir</span><span class="sxs-lookup"><span data-stu-id="23541-182">-Expand</span></span>
<span data-ttu-id="23541-183">Expanda a expressão usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="23541-183">Expand expression using OData notation.</span></span>

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

### <span data-ttu-id="23541-184">-Filtro</span><span class="sxs-lookup"><span data-stu-id="23541-184">-Filter</span></span>
<span data-ttu-id="23541-185">Expressão de filtro usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="23541-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="23541-186">-De</span><span class="sxs-lookup"><span data-stu-id="23541-186">-From</span></span>
<span data-ttu-id="23541-187">ISO 8601 data/hora formatada especificando a hora de início do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="23541-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="23541-188">Quando não especificado, o padrão é o valor do parâmetro 'Para' menos 1 dia.</span><span class="sxs-lookup"><span data-stu-id="23541-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="23541-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="23541-189">-ManagementGroupName</span></span>
<span data-ttu-id="23541-190">Nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="23541-190">Management group name.</span></span>

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

### <span data-ttu-id="23541-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="23541-191">-OrderBy</span></span>
<span data-ttu-id="23541-192">Expressão de ordenação usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="23541-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="23541-193">Um ou mais nomes de coluna separados por vírgula com um "desc" opcional (o padrão) ou "asc".</span><span class="sxs-lookup"><span data-stu-id="23541-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="23541-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="23541-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="23541-195">Nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="23541-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="23541-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="23541-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="23541-197">Nome da definição de política.</span><span class="sxs-lookup"><span data-stu-id="23541-197">Policy definition name.</span></span>

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

### <span data-ttu-id="23541-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="23541-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="23541-199">Nome de definição de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="23541-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="23541-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23541-200">-ResourceGroupName</span></span>
<span data-ttu-id="23541-201">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23541-201">Resource group name.</span></span>

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

### <span data-ttu-id="23541-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23541-202">-ResourceId</span></span>
<span data-ttu-id="23541-203">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="23541-203">Resource ID.</span></span>

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

### <span data-ttu-id="23541-204">-Selecionar</span><span class="sxs-lookup"><span data-stu-id="23541-204">-Select</span></span>
<span data-ttu-id="23541-205">Selecione a expressão usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="23541-205">Select expression using OData notation.</span></span>
<span data-ttu-id="23541-206">Um ou mais nomes de coluna separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="23541-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="23541-207">Limita as colunas em cada registro apenas às solicitadas.</span><span class="sxs-lookup"><span data-stu-id="23541-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="23541-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23541-208">-SubscriptionId</span></span>
<span data-ttu-id="23541-209">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="23541-209">Subscription ID.</span></span>

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

### <span data-ttu-id="23541-210">-Para</span><span class="sxs-lookup"><span data-stu-id="23541-210">-To</span></span>
<span data-ttu-id="23541-211">ISO 8601 data/hora formatada especificando a hora de término do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="23541-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="23541-212">Quando não especificado, o padrão é o horário da solicitação.</span><span class="sxs-lookup"><span data-stu-id="23541-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="23541-213">-Superior</span><span class="sxs-lookup"><span data-stu-id="23541-213">-Top</span></span>
<span data-ttu-id="23541-214">Número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="23541-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="23541-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23541-215">CommonParameters</span></span>
<span data-ttu-id="23541-216">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23541-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23541-217">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23541-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23541-218">Entradas</span><span class="sxs-lookup"><span data-stu-id="23541-218">INPUTS</span></span>

### <span data-ttu-id="23541-219">System.String</span><span class="sxs-lookup"><span data-stu-id="23541-219">System.String</span></span>

## <span data-ttu-id="23541-220">Saídas</span><span class="sxs-lookup"><span data-stu-id="23541-220">OUTPUTS</span></span>

### <span data-ttu-id="23541-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="23541-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="23541-222">Notas</span><span class="sxs-lookup"><span data-stu-id="23541-222">NOTES</span></span>

## <span data-ttu-id="23541-223">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23541-223">RELATED LINKS</span></span>

[<span data-ttu-id="23541-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="23541-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
