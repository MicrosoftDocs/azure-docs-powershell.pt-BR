---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 1eec241ab9fba3f9e8daa3218b65140d644d56ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429988"
---
# <span data-ttu-id="b7e16-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="b7e16-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="b7e16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7e16-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e16-103">Consulta os dados de uso para o escopo definido.</span><span class="sxs-lookup"><span data-stu-id="b7e16-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="b7e16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7e16-104">SYNTAX</span></span>

### <span data-ttu-id="b7e16-105">UsageExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="b7e16-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7e16-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="b7e16-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7e16-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7e16-107">DESCRIPTION</span></span>
<span data-ttu-id="b7e16-108">Consulta os dados de uso para o escopo definido.</span><span class="sxs-lookup"><span data-stu-id="b7e16-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="b7e16-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7e16-109">EXAMPLES</span></span>

### <span data-ttu-id="b7e16-110">Exemplo 1: invocar AzCostManagementQuery por escopo</span><span class="sxs-lookup"><span data-stu-id="b7e16-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="b7e16-111">Invocar AzCostManagementQuery por escopo</span><span class="sxs-lookup"><span data-stu-id="b7e16-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="b7e16-112">Exemplo 2: invocar AzCostManagementQuery por escopo com dimensões</span><span class="sxs-lookup"><span data-stu-id="b7e16-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Operator 'In' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="b7e16-113">Invocar AzCostManagementQuery pelo escopo com dimensões</span><span class="sxs-lookup"><span data-stu-id="b7e16-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="b7e16-114">OS</span><span class="sxs-lookup"><span data-stu-id="b7e16-114">PARAMETERS</span></span>

### <span data-ttu-id="b7e16-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="b7e16-115">-ConfigurationColumn</span></span>
<span data-ttu-id="b7e16-116">Matriz de nomes de coluna a serem incluídos na consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="b7e16-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="b7e16-117">-DatasetAggregation</span></span>
<span data-ttu-id="b7e16-118">Dicionário de expressão de agregação a ser usado na consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-118">Dictionary of aggregation expression to use in the query.</span></span>

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

### <span data-ttu-id="b7e16-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="b7e16-119">-DatasetFilter</span></span>
<span data-ttu-id="b7e16-120">Tem uma expressão de filtro para usar na consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="b7e16-121">Para construir, consulte a seção notas para propriedades DATASETFILTER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b7e16-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7e16-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="b7e16-122">-DatasetGranularity</span></span>
<span data-ttu-id="b7e16-123">A granularidade das linhas na consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="b7e16-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="b7e16-124">-DatasetGrouping</span></span>
<span data-ttu-id="b7e16-125">Matriz de expressão Group by para usar na consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="b7e16-126">Para construir, consulte a seção notas para propriedades DATASETGROUPING e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b7e16-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7e16-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e16-127">-DefaultProfile</span></span>
<span data-ttu-id="b7e16-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e16-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7e16-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="b7e16-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="b7e16-130">Pode ser "{externalSubscriptionId}" da conta vinculada ou "{externalBillingAccountId}" para a conta consolidada usada com operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

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

### <span data-ttu-id="b7e16-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="b7e16-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="b7e16-132">O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-132">The external cloud provider type associated with dimension/query operations.</span></span>

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

### <span data-ttu-id="b7e16-133">-Escopo</span><span class="sxs-lookup"><span data-stu-id="b7e16-133">-Scope</span></span>
<span data-ttu-id="b7e16-134">Isso inclui ' assinaturas/{SubscriptionId}/' para o escopo da assinatura, ' assinaturas/{SubscriptionId}/resourceGroups/{resourceGroupName} ' para o escopo do subsource, ' Providers/Microsoft. billing/billingAccounts/{billingAccountId} ' para o escopo da conta de cobrança e ' provedores/Microsoft. billing/billingAccounts/{billingAccountId}/departamentos/{DepartmentID} ' para escopo do departamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} ' para escopo EnrollmentAccount, ' provedores/Microsoft. Management/managementGroups/{managementGroupId} para escopo do grupo de gerenciamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' para billingProfile Scope, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId} ' para invoiceSection escopo e ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/clientes/{customerId} ' específico para parceiros.</span><span class="sxs-lookup"><span data-stu-id="b7e16-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

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

### <span data-ttu-id="b7e16-135">-Quadro de tempo</span><span class="sxs-lookup"><span data-stu-id="b7e16-135">-Timeframe</span></span>
<span data-ttu-id="b7e16-136">O intervalo de tempo para a recepção de dados da consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-136">The time frame for pulling data for the query.</span></span>

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

### <span data-ttu-id="b7e16-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="b7e16-137">-TimePeriodFrom</span></span>
<span data-ttu-id="b7e16-138">A data de início da qual os dados são extraídos.</span><span class="sxs-lookup"><span data-stu-id="b7e16-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="b7e16-139">-Timeperiodto</span><span class="sxs-lookup"><span data-stu-id="b7e16-139">-TimePeriodTo</span></span>
<span data-ttu-id="b7e16-140">A data de término para a qual os dados são extraídos.</span><span class="sxs-lookup"><span data-stu-id="b7e16-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="b7e16-141">-Digite</span><span class="sxs-lookup"><span data-stu-id="b7e16-141">-Type</span></span>
<span data-ttu-id="b7e16-142">O tipo da consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-142">The type of the query.</span></span>

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

### <span data-ttu-id="b7e16-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7e16-143">-Confirm</span></span>
<span data-ttu-id="b7e16-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7e16-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e16-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e16-145">-WhatIf</span></span>
<span data-ttu-id="b7e16-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7e16-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e16-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7e16-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e16-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e16-148">CommonParameters</span></span>
<span data-ttu-id="b7e16-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7e16-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e16-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7e16-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e16-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7e16-151">INPUTS</span></span>

## <span data-ttu-id="b7e16-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7e16-152">OUTPUTS</span></span>

### <span data-ttu-id="b7e16-153">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. IQueryResult</span><span class="sxs-lookup"><span data-stu-id="b7e16-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="b7e16-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7e16-154">NOTES</span></span>

<span data-ttu-id="b7e16-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b7e16-155">ALIASES</span></span>

<span data-ttu-id="b7e16-156">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b7e16-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7e16-157">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b7e16-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7e16-158">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7e16-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7e16-159">DATASETFILTER <IQueryFilter> : tem uma expressão de filtro para usar na consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="b7e16-160">`[And <IQueryFilter[]>]`: A expressão lógica "e".</span><span class="sxs-lookup"><span data-stu-id="b7e16-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="b7e16-161">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="b7e16-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b7e16-162">`[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="b7e16-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="b7e16-163">`Name <String>`: O nome da coluna a ser usada na comparação.</span><span class="sxs-lookup"><span data-stu-id="b7e16-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="b7e16-164">`Operator <OperatorType>`: O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="b7e16-164">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="b7e16-165">`Value <String[]>`: Matriz de valores a serem usados para comparação</span><span class="sxs-lookup"><span data-stu-id="b7e16-165">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="b7e16-166">`[Not <IQueryFilter>]`: A expressão lógica "não".</span><span class="sxs-lookup"><span data-stu-id="b7e16-166">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="b7e16-167">`[Or <IQueryFilter[]>]`: A expressão lógica "ou".</span><span class="sxs-lookup"><span data-stu-id="b7e16-167">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="b7e16-168">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="b7e16-168">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b7e16-169">`[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="b7e16-169">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="b7e16-170">DATASETGROUPING <IQueryGrouping [] >: matriz da expressão Group by para usar na consulta.</span><span class="sxs-lookup"><span data-stu-id="b7e16-170">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="b7e16-171">`Name <String>`: O nome da coluna a ser agrupada.</span><span class="sxs-lookup"><span data-stu-id="b7e16-171">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="b7e16-172">`Type <QueryColumnType>`: Tem um tipo de coluna a ser agrupada.</span><span class="sxs-lookup"><span data-stu-id="b7e16-172">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="b7e16-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7e16-173">RELATED LINKS</span></span>

