---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428422"
---
# <span data-ttu-id="9a603-101">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="9a603-101">Get-AzureRmPolicyStateSummary</span></span>

## <span data-ttu-id="9a603-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a603-102">SYNOPSIS</span></span>
<span data-ttu-id="9a603-103">Obtém o resumo dos Estados mais recentes de conformidade com a política para recursos.</span><span class="sxs-lookup"><span data-stu-id="9a603-103">Gets latest policy compliance states summary for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a603-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a603-104">SYNTAX</span></span>

### <span data-ttu-id="9a603-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="9a603-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a603-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="9a603-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a603-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="9a603-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a603-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="9a603-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a603-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="9a603-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a603-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="9a603-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a603-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="9a603-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a603-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="9a603-112">ResourceScope</span></span>
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a603-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a603-113">DESCRIPTION</span></span>
<span data-ttu-id="9a603-114">Obtém um resumo dos números de estado de conformidade da política mais recentes em vários escopos, divididos em atribuições de política e definições de política.</span><span class="sxs-lookup"><span data-stu-id="9a603-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="9a603-115">Ele inclui apenas Estados de política não compatíveis.</span><span class="sxs-lookup"><span data-stu-id="9a603-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="9a603-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a603-116">EXAMPLES</span></span>

### <span data-ttu-id="9a603-117">Exemplo 1: obter o resumo dos Estados mais recentes da política não compatível com o escopo atual da assinatura</span><span class="sxs-lookup"><span data-stu-id="9a603-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

<span data-ttu-id="9a603-118">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="9a603-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="9a603-119">Exemplo 2: obter o resumo de Estados da política sem conformidade mais recente no escopo de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="9a603-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="9a603-120">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="9a603-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="9a603-121">Exemplo 3: obter o resumo dos Estados da política não compatível mais recentes no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="9a603-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="9a603-122">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="9a603-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="9a603-123">Exemplo 4: obter o resumo dos Estados da política não compatível mais recentes no escopo do grupo de recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="9a603-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9a603-124">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="9a603-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="9a603-125">Exemplo 5: obter o resumo dos Estados da política não compatível mais recentes no escopo do grupo de recursos na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="9a603-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="9a603-126">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="9a603-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="9a603-127">Exemplo 6: obter o resumo de Estados da política não compatível mais recente para um recurso</span><span class="sxs-lookup"><span data-stu-id="9a603-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="9a603-128">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia do recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="9a603-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="9a603-129">Exemplo 7: obter o resumo de Estados da política não compatível mais recente para uma definição de conjunto de políticas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="9a603-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9a603-130">Obtém a exibição de resumo dos últimos Estados de conformidade de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="9a603-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9a603-131">Exemplo 8: obter o resumo de Estados da política não compatível mais recente para uma definição de conjunto de políticas na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="9a603-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9a603-132">Obtém a exibição de resumo dos últimos Estados de conformidade de política gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição do conjunto de políticas especificado (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="9a603-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9a603-133">Exemplo 9: obter o resumo de Estados da política não compatível mais recentes para uma definição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="9a603-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9a603-134">Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura do contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="9a603-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9a603-135">Exemplo 10: obter o resumo de Estados da política não compatível mais recente para uma definição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="9a603-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="9a603-136">Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela definição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="9a603-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9a603-137">Exemplo 11: obter o resumo de Estados da política sem conformidade mais recente para uma atribuição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="9a603-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9a603-138">Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="9a603-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="9a603-139">Exemplo 12: obter o resumo de Estados da política não compatível mais recente para uma atribuição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="9a603-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9a603-140">Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="9a603-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="9a603-141">Exemplo 13: obter o resumo de Estados da política sem conformidade mais recente para uma atribuição de política no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="9a603-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="9a603-142">Obtém a exibição de resumo dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) afetados pela atribuição de política especificada (que existe no grupo de recursos na assinatura do contexto de sessão atual).</span><span class="sxs-lookup"><span data-stu-id="9a603-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="9a603-143">Exemplo 14: obter o resumo dos Estados mais recentes da política não compatível com o escopo atual da assinatura, com a opção de consulta superior</span><span class="sxs-lookup"><span data-stu-id="9a603-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

<span data-ttu-id="9a603-144">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="9a603-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="9a603-145">O comando ordena os resumos da atribuição de política nos resultados por conta de recurso não compatível em ordem decrescente, e usa apenas 5 principais dos resumos da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="9a603-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="9a603-146">Exemplo 15: obter o resumo de Estados da política sem conformidade mais recente no escopo atual da assinatura, com opções de consulta de e até</span><span class="sxs-lookup"><span data-stu-id="9a603-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="9a603-147">Obtém a exibição de resumo dos últimos Estados de conformidade de política gerado dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="9a603-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="9a603-148">Exemplo 16: obter o resumo dos Estados mais recentes da política não compatível com o escopo atual da assinatura, com a opção filtrar consulta</span><span class="sxs-lookup"><span data-stu-id="9a603-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="9a603-149">Obtém a exibição resumida dos últimos Estados de conformidade com a política gerado no último dia para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="9a603-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="9a603-150">O comando limita os resultados retornados pela filtragem com base na ação de definição da política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do lesteus).</span><span class="sxs-lookup"><span data-stu-id="9a603-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="9a603-151">OS</span><span class="sxs-lookup"><span data-stu-id="9a603-151">PARAMETERS</span></span>

### <span data-ttu-id="9a603-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a603-152">-DefaultProfile</span></span>
<span data-ttu-id="9a603-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a603-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a603-154">-Filtro</span><span class="sxs-lookup"><span data-stu-id="9a603-154">-Filter</span></span>
<span data-ttu-id="9a603-155">Expressão de filtro usando a notação OData.</span><span class="sxs-lookup"><span data-stu-id="9a603-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="9a603-156">-De</span><span class="sxs-lookup"><span data-stu-id="9a603-156">-From</span></span>
<span data-ttu-id="9a603-157">Marca de data/hora formatada ISO 8601 especificando a hora de início do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="9a603-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="9a603-158">Quando não especificado, o padrão é o valor do parâmetro ' para ' menos 1 dia.</span><span class="sxs-lookup"><span data-stu-id="9a603-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="9a603-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9a603-159">-ManagementGroupName</span></span>
<span data-ttu-id="9a603-160">Nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="9a603-160">Management group name.</span></span>

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

### <span data-ttu-id="9a603-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="9a603-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="9a603-162">Nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="9a603-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="9a603-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9a603-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="9a603-164">Nome da definição da política.</span><span class="sxs-lookup"><span data-stu-id="9a603-164">Policy definition name.</span></span>

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

### <span data-ttu-id="9a603-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9a603-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="9a603-166">Nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="9a603-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="9a603-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a603-167">-ResourceGroupName</span></span>
<span data-ttu-id="9a603-168">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a603-168">Resource group name.</span></span>

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

### <span data-ttu-id="9a603-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a603-169">-ResourceId</span></span>
<span data-ttu-id="9a603-170">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9a603-170">Resource ID.</span></span>

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

### <span data-ttu-id="9a603-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a603-171">-SubscriptionId</span></span>
<span data-ttu-id="9a603-172">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9a603-172">Subscription ID.</span></span>

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

### <span data-ttu-id="9a603-173">-To</span><span class="sxs-lookup"><span data-stu-id="9a603-173">-To</span></span>
<span data-ttu-id="9a603-174">Marca de data/hora formatada ISO 8601 especificando a hora de término do intervalo para consulta.</span><span class="sxs-lookup"><span data-stu-id="9a603-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="9a603-175">Quando não especificado, o padrão é a hora da solicitação.</span><span class="sxs-lookup"><span data-stu-id="9a603-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="9a603-176">-Início</span><span class="sxs-lookup"><span data-stu-id="9a603-176">-Top</span></span>
<span data-ttu-id="9a603-177">Número máximo de registros a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="9a603-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="9a603-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a603-178">CommonParameters</span></span>
<span data-ttu-id="9a603-179">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a603-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a603-180">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a603-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a603-181">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a603-181">INPUTS</span></span>

### <span data-ttu-id="9a603-182">System. String</span><span class="sxs-lookup"><span data-stu-id="9a603-182">System.String</span></span>

## <span data-ttu-id="9a603-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a603-183">OUTPUTS</span></span>

### <span data-ttu-id="9a603-184">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="9a603-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="9a603-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a603-185">NOTES</span></span>

## <span data-ttu-id="9a603-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a603-186">RELATED LINKS</span></span>

[<span data-ttu-id="9a603-187">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="9a603-187">Get-AzureRmPolicyState</span></span>](./Get-AzureRmPolicyState.md)
