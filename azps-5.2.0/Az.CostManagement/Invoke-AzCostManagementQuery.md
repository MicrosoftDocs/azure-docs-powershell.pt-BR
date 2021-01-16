---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 1eec241ab9fba3f9e8daa3218b65140d644d56ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258486"
---
# Invoke-AzCostManagementQuery

## Sinopse
Consulta os dados de uso para o escopo definido.

## SYNTAX

### UsageExpanded (padrão)
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UsageExpanded1
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRITIVO
Consulta os dados de uso para o escopo definido.

## EXEMPLOS

### Exemplo 1: invocar AzCostManagementQuery por escopo
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

Invocar AzCostManagementQuery por escopo

### Exemplo 2: invocar AzCostManagementQuery por escopo com dimensões
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Operator 'In' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

Invocar AzCostManagementQuery pelo escopo com dimensões

## OS

### -ConfigurationColumn
Matriz de nomes de coluna a serem incluídos na consulta.

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

### -DatasetAggregation
Dicionário de expressão de agregação a ser usado na consulta.

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

### -DatasetFilter
Tem uma expressão de filtro para usar na consulta.
Para construir, consulte a seção notas para propriedades DATASETFILTER e crie uma tabela de hash.

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

### -DatasetGranularity
A granularidade das linhas na consulta.

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

### -DatasetGrouping
Matriz de expressão Group by para usar na consulta.
Para construir, consulte a seção notas para propriedades DATASETGROUPING e crie uma tabela de hash.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -ExternalCloudProviderId
Pode ser "{externalSubscriptionId}" da conta vinculada ou "{externalBillingAccountId}" para a conta consolidada usada com operações de dimensão/consulta.

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

### -ExternalCloudProviderType
O tipo de provedor de nuvem externo associado a operações de dimensão/consulta.

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

### -Escopo
Isso inclui ' assinaturas/{SubscriptionId}/' para o escopo da assinatura, ' assinaturas/{SubscriptionId}/resourceGroups/{resourceGroupName} ' para o escopo do subsource, ' Providers/Microsoft. billing/billingAccounts/{billingAccountId} ' para o escopo da conta de cobrança e ' provedores/Microsoft. billing/billingAccounts/{billingAccountId}/departamentos/{DepartmentID} ' para escopo do departamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} ' para escopo EnrollmentAccount, ' provedores/Microsoft. Management/managementGroups/{managementGroupId} para escopo do grupo de gerenciamento, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' para billingProfile Scope, ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId} ' para invoiceSection escopo e ' Providers/Microsoft. Rebilling/billingAccounts/{billingAccountId}/clientes/{customerId} ' específico para parceiros.

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

### -Quadro de tempo
O intervalo de tempo para a recepção de dados da consulta.

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

### -TimePeriodFrom
A data de início da qual os dados são extraídos.

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

### -Timeperiodto
A data de término para a qual os dados são extraídos.

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

### -Digite
O tipo da consulta.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. IQueryResult

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


DATASETFILTER <IQueryFilter> : tem uma expressão de filtro para usar na consulta.
  - `[And <IQueryFilter[]>]`: A expressão lógica "e". Deve ter pelo menos 2 itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão
    - `Name <String>`: O nome da coluna a ser usada na comparação.
    - `Operator <OperatorType>`: O operador a ser usado para comparação.
    - `Value <String[]>`: Matriz de valores a serem usados para comparação
  - `[Not <IQueryFilter>]`: A expressão lógica "não".
  - `[Or <IQueryFilter[]>]`: A expressão lógica "ou". Deve ter pelo menos 2 itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca

DATASETGROUPING <IQueryGrouping [] >: matriz da expressão Group by para usar na consulta.
  - `Name <String>`: O nome da coluna a ser agrupada.
  - `Type <QueryColumnType>`: Tem um tipo de coluna a ser agrupada.

## LINKS RELACIONADOS

