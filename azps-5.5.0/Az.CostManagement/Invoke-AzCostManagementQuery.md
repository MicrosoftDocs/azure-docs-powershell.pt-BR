---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 37f4d4b5650060b490e8c6bb691d938b78fa1166
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112014"
---
# <span data-ttu-id="49fc2-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="49fc2-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="49fc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="49fc2-103">Consultar os dados de uso para escopo definidos.</span><span class="sxs-lookup"><span data-stu-id="49fc2-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="49fc2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49fc2-104">SYNTAX</span></span>

### <span data-ttu-id="49fc2-105">UsageExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="49fc2-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49fc2-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="49fc2-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49fc2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="49fc2-107">DESCRIPTION</span></span>
<span data-ttu-id="49fc2-108">Consultar os dados de uso para escopo definidos.</span><span class="sxs-lookup"><span data-stu-id="49fc2-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="49fc2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49fc2-109">EXAMPLES</span></span>

### <span data-ttu-id="49fc2-110">Exemplo 1: Invoke AzCostManagementQuery por Escopo</span><span class="sxs-lookup"><span data-stu-id="49fc2-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="49fc2-111">Invoke AzCostManagementQuery by Scope</span><span class="sxs-lookup"><span data-stu-id="49fc2-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="49fc2-112">Exemplo 2: Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="49fc2-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="49fc2-113">Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="49fc2-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="49fc2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49fc2-114">PARAMETERS</span></span>

### <span data-ttu-id="49fc2-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="49fc2-115">-ConfigurationColumn</span></span>
<span data-ttu-id="49fc2-116">Matriz de nomes de coluna a serem incluídos na consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-116">Array of column names to be included in the query.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="49fc2-117">-DatasetAggregation</span></span>
<span data-ttu-id="49fc2-118">Dicionário de expressão de agregação a ser usado na consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-118">Dictionary of aggregation expression to use in the query.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="49fc2-119">-DatasetFilter</span></span>
<span data-ttu-id="49fc2-120">Tem expressão de filtro para usar na consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="49fc2-121">Para construir, consulte a seção ANOTAÇÕES para propriedades DATASETFILTER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="49fc2-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-122">-DatasetArularity</span><span class="sxs-lookup"><span data-stu-id="49fc2-122">-DatasetGranularity</span></span>
<span data-ttu-id="49fc2-123">A granularidade das linhas na consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-123">The granularity of rows in the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="49fc2-124">-DatasetGrouping</span></span>
<span data-ttu-id="49fc2-125">Matriz de grupo por expressão a ser usada na consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="49fc2-126">Para construir, confira a seção ANOTAÇÕES para propriedades DATASETGROUPING e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="49fc2-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fc2-127">-DefaultProfile</span></span>
<span data-ttu-id="49fc2-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49fc2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="49fc2-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="49fc2-130">Pode ser '{externalSubscriptionId}' para conta vinculada ou '{externalBillingAccountId}' para contas consolidadas usadas com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="49fc2-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="49fc2-132">O tipo de provedor de nuvem externo associado às operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-133">-Escopo</span><span class="sxs-lookup"><span data-stu-id="49fc2-133">-Scope</span></span>
<span data-ttu-id="49fc2-134">Isso inclui 'assinaturas/{subscriptionId}/' para escopo de assinatura, 'assinaturas/{subscriptionId}/resourceGroups/{resourceGroupName}' para escopo resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' para escopo de Conta de Cobrança e 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' para escopo do Departamento, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'provedores/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' para escopo billingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}//billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' para escopo invoiceSection e 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' específicos para parceiros.</span><span class="sxs-lookup"><span data-stu-id="49fc2-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-135">-Prazo</span><span class="sxs-lookup"><span data-stu-id="49fc2-135">-Timeframe</span></span>
<span data-ttu-id="49fc2-136">O período de tempo para a coleta de dados para a consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="49fc2-137">-TimePeriodFrom</span></span>
<span data-ttu-id="49fc2-138">A data de início da onde os dados serão coletados.</span><span class="sxs-lookup"><span data-stu-id="49fc2-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="49fc2-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="49fc2-139">-TimePeriodTo</span></span>
<span data-ttu-id="49fc2-140">A data de término para a coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="49fc2-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="49fc2-141">-Tipo</span><span class="sxs-lookup"><span data-stu-id="49fc2-141">-Type</span></span>
<span data-ttu-id="49fc2-142">O tipo da consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="49fc2-143">-Confirm</span></span>
<span data-ttu-id="49fc2-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49fc2-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49fc2-145">-WhatIf</span></span>
<span data-ttu-id="49fc2-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="49fc2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49fc2-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="49fc2-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49fc2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fc2-148">CommonParameters</span></span>
<span data-ttu-id="49fc2-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49fc2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fc2-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49fc2-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fc2-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="49fc2-151">INPUTS</span></span>

## <span data-ttu-id="49fc2-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="49fc2-152">OUTPUTS</span></span>

### <span data-ttu-id="49fc2-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="49fc2-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="49fc2-154">Notas</span><span class="sxs-lookup"><span data-stu-id="49fc2-154">NOTES</span></span>

<span data-ttu-id="49fc2-155">Aliases</span><span class="sxs-lookup"><span data-stu-id="49fc2-155">ALIASES</span></span>

<span data-ttu-id="49fc2-156">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="49fc2-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49fc2-157">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="49fc2-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49fc2-158">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49fc2-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49fc2-159">DATASETFILTER: <IQueryFilter> tem expressão de filtro para usar na consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="49fc2-160">`[And <IQueryFilter[]>]`: a expressão lógica "E".</span><span class="sxs-lookup"><span data-stu-id="49fc2-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="49fc2-161">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="49fc2-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="49fc2-162">`[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="49fc2-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="49fc2-163">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="49fc2-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="49fc2-164">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="49fc2-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="49fc2-165">`[Not <IQueryFilter>]`: a expressão lógica "NÃO".</span><span class="sxs-lookup"><span data-stu-id="49fc2-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="49fc2-166">`[Or <IQueryFilter[]>]`: a expressão lógica "OU".</span><span class="sxs-lookup"><span data-stu-id="49fc2-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="49fc2-167">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="49fc2-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="49fc2-168">`[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="49fc2-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="49fc2-169">DATASETGROUPING <IQueryGrouping[]>: Matriz de grupo por expressão a ser usada na consulta.</span><span class="sxs-lookup"><span data-stu-id="49fc2-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="49fc2-170">`Name <String>`: o nome da coluna a ser agrupada.</span><span class="sxs-lookup"><span data-stu-id="49fc2-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="49fc2-171">`Type <QueryColumnType>`: Tem o tipo da coluna a ser agrupada.</span><span class="sxs-lookup"><span data-stu-id="49fc2-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="49fc2-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49fc2-172">RELATED LINKS</span></span>

