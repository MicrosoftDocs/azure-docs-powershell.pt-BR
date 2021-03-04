---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 09fce075ae0f6d8c55f5ef18d070a72daafa2cac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890106"
---
# <span data-ttu-id="d6e0b-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="d6e0b-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="d6e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e0b-103">Obtém o resumo dos estados de conformidade de política mais recentes para os recursos.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="d6e0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d6e0b-104">SYNTAX</span></span>

### <span data-ttu-id="d6e0b-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d6e0b-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6e0b-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="d6e0b-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6e0b-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="d6e0b-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6e0b-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="d6e0b-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6e0b-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="d6e0b-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6e0b-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="d6e0b-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6e0b-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="d6e0b-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6e0b-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="d6e0b-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6e0b-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d6e0b-113">DESCRIPTION</span></span>
<span data-ttu-id="d6e0b-114">Obtém uma exibição resumida dos números de estado de conformidade de política mais recentes em vários escopos, divididos em atribuições de política e definições de política.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="d6e0b-115">Ele inclui apenas estados de política não compatíveis.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="d6e0b-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6e0b-116">EXAMPLES</span></span>

### <span data-ttu-id="d6e0b-117">Exemplo 1: obter o resumo mais recente dos estados de política não compatíveis no escopo de assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d6e0b-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="d6e0b-118">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="d6e0b-119">Exemplo 2: Obter o resumo mais recente dos estados de política não compatíveis no escopo de assinatura especificado</span><span class="sxs-lookup"><span data-stu-id="d6e0b-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="d6e0b-120">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="d6e0b-121">Exemplo 3: Obter o resumo mais recente dos estados de política não compatíveis no escopo do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d6e0b-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="d6e0b-122">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="d6e0b-123">Exemplo 4: obter o resumo mais recente dos estados de política não compatíveis no escopo do grupo de recursos na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d6e0b-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d6e0b-124">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="d6e0b-125">Exemplo 5: obter o resumo mais recente dos estados de política não compatíveis no escopo do grupo de recursos na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="d6e0b-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="d6e0b-126">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro do grupo de recursos especificado (na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="d6e0b-127">Exemplo 6: Obter o resumo mais recente de estados de política não compatíveis para um recurso</span><span class="sxs-lookup"><span data-stu-id="d6e0b-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="d6e0b-128">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para o recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="d6e0b-129">Exemplo 7: obter o resumo mais recente dos estados de política não compatíveis para uma definição de conjunto de políticas na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d6e0b-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d6e0b-130">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição do conjunto de políticas especificado (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d6e0b-131">Exemplo 8: obter o resumo mais recente dos estados de política não compatíveis para uma definição de conjunto de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="d6e0b-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d6e0b-132">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição do conjunto de políticas especificado (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d6e0b-133">Exemplo 9: obter o resumo mais recente dos estados de política não compatíveis para uma definição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d6e0b-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d6e0b-134">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d6e0b-135">Exemplo 10: obter o resumo mais recente dos estados de política não compatíveis para uma definição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="d6e0b-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="d6e0b-136">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela definição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d6e0b-137">Exemplo 11: Obter o resumo mais recente dos estados de política não compatíveis para uma atribuição de política na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d6e0b-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d6e0b-138">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura no contexto atual da sessão).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="d6e0b-139">Exemplo 12: Obter o resumo mais recente dos estados de política não compatíveis para uma atribuição de política na assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="d6e0b-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d6e0b-140">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe na assinatura especificada).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="d6e0b-141">Exemplo 13: Obter o resumo mais recente dos estados de política não compatíveis para uma atribuição de política no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d6e0b-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="d6e0b-142">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos (dentro do locatário no contexto de sessão atual) e efetivados pela atribuição de política especificada (que existe no grupo de recursos na assinatura no contexto da sessão atual).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="d6e0b-143">Exemplo 14: Obter o resumo mais recente dos estados de política não compatíveis no escopo de assinatura atual, com a opção Top query</span><span class="sxs-lookup"><span data-stu-id="d6e0b-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="d6e0b-144">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="d6e0b-145">O comando ordena os resumos de atribuição de política nos resultados por contagens de recursos não compatíveis em ordem decrescente e leva apenas o top 5 desses resumos de atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="d6e0b-146">Exemplo 15: Obter o resumo mais recente de estados de política não compatíveis no escopo de assinatura atual, com opções de consulta De e Para</span><span class="sxs-lookup"><span data-stu-id="d6e0b-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="d6e0b-147">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados dentro do intervalo de datas especificado para todos os recursos dentro da assinatura no contexto de sessão atual.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="d6e0b-148">Exemplo 16: Obter o resumo mais recente dos estados de política não compatíveis no escopo de assinatura atual, com a opção De consulta filter</span><span class="sxs-lookup"><span data-stu-id="d6e0b-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="d6e0b-149">Obtém a exibição resumida dos estados de conformidade de política mais recentes gerados no último dia para todos os recursos dentro da assinatura no contexto atual da sessão.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="d6e0b-150">O comando limita os resultados retornados pela filtragem com base na ação de definição de política (inclui ações de negação ou auditoria) e local do recurso (exclui o local do eastus).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="d6e0b-151">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d6e0b-151">PARAMETERS</span></span>

### <span data-ttu-id="d6e0b-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e0b-152">-DefaultProfile</span></span>
<span data-ttu-id="d6e0b-153">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6e0b-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="d6e0b-154">-Filter</span></span>
<span data-ttu-id="d6e0b-155">Expressão de filtro usando notação OData.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="d6e0b-156">-From</span><span class="sxs-lookup"><span data-stu-id="d6e0b-156">-From</span></span>
<span data-ttu-id="d6e0b-157">Data/hora formatada da ISO 8601 especificando a hora de início do intervalo a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="d6e0b-158">Quando não especificado, o valor do parâmetro 'To' é padrão menos 1 dia.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="d6e0b-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e0b-159">-ManagementGroupName</span></span>
<span data-ttu-id="d6e0b-160">Nome do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-160">Management group name.</span></span>

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

### <span data-ttu-id="d6e0b-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d6e0b-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="d6e0b-162">Nome da atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="d6e0b-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d6e0b-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="d6e0b-164">Nome da definição de política.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-164">Policy definition name.</span></span>

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

### <span data-ttu-id="d6e0b-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d6e0b-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="d6e0b-166">Nome da definição do conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="d6e0b-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e0b-167">-ResourceGroupName</span></span>
<span data-ttu-id="d6e0b-168">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-168">Resource group name.</span></span>

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

### <span data-ttu-id="d6e0b-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e0b-169">-ResourceId</span></span>
<span data-ttu-id="d6e0b-170">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-170">Resource ID.</span></span>

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

### <span data-ttu-id="d6e0b-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6e0b-171">-SubscriptionId</span></span>
<span data-ttu-id="d6e0b-172">ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-172">Subscription ID.</span></span>

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

### <span data-ttu-id="d6e0b-173">-To</span><span class="sxs-lookup"><span data-stu-id="d6e0b-173">-To</span></span>
<span data-ttu-id="d6e0b-174">Data/hora formatada da ISO 8601 especificando a hora de término do intervalo a ser consultado.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="d6e0b-175">Quando não especificado, o padrão é a hora da solicitação.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="d6e0b-176">-Top</span><span class="sxs-lookup"><span data-stu-id="d6e0b-176">-Top</span></span>
<span data-ttu-id="d6e0b-177">Número máximo de registros a retornar.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="d6e0b-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e0b-178">CommonParameters</span></span>
<span data-ttu-id="d6e0b-179">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e0b-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e0b-180">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6e0b-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e0b-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6e0b-181">INPUTS</span></span>

### <span data-ttu-id="d6e0b-182">System.String</span><span class="sxs-lookup"><span data-stu-id="d6e0b-182">System.String</span></span>

## <span data-ttu-id="d6e0b-183">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d6e0b-183">OUTPUTS</span></span>

### <span data-ttu-id="d6e0b-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="d6e0b-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="d6e0b-185">NOTES</span><span class="sxs-lookup"><span data-stu-id="d6e0b-185">NOTES</span></span>

## <span data-ttu-id="d6e0b-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6e0b-186">RELATED LINKS</span></span>

[<span data-ttu-id="d6e0b-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="d6e0b-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
