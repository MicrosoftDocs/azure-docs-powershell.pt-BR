---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892983"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Criar um objeto na memória para QueryFilter

## SINTAXE

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## DESCRIPTION
Criar um objeto na memória para QueryFilter

## EXEMPLOS

### Exemplo 1: Criar um objeto filter de consulta para exportação de gerenciamento de custos
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

este comando cria um objeto filter de consulta para exportação de gerenciamento de custos.

## PARÂMETROS

### -And
A expressão lógica "AND".
Deve ter pelo menos 2 itens.
Para construir, consulte a seção NOTES para propriedades AND e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dimensões
Tem expressão de comparação para dimensões.
Para construir, consulte a seção NOTES para propriedades DIMENSIONS e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Not
A expressão lógica "NOT".
Para construir, consulte a seção NOTES para propriedades NOT e crie uma tabela de hash.

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

### -Or
A expressão "OR" lógica.
Deve ter pelo menos 2 itens.
Para construir, consulte a seção NOTES para propriedades OR e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Tem expressão de comparação para uma marca.
Para construir, consulte a seção NOTES para propriedades TAG e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: a expressão lógica "AND". Deve ter pelo menos 2 itens.
  - `[And <IQueryFilter[]>]`: a expressão lógica "AND". Deve ter pelo menos 2 itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão
    - `Name <String>`: o nome da coluna a ser usada em comparação.
    - `Value <String[]>`: Matriz de valores a ser usado para comparação
  - `[Not <IQueryFilter>]`: a expressão lógica "NOT".
  - `[Or <IQueryFilter[]>]`: A expressão "OR" lógica. Deve ter pelo menos 2 itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca

DIMENSÕES <IQueryComparisonExpression> : tem expressão de comparação para uma dimensão.
  - `Name <String>`: o nome da coluna a ser usada em comparação.
  - `Value <String[]>`: Matriz de valores a ser usado para comparação

NÃO <IQueryFilter> : a expressão lógica "NOT".
  - `[And <IQueryFilter[]>]`: a expressão lógica "AND". Deve ter pelo menos 2 itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão
    - `Name <String>`: o nome da coluna a ser usada em comparação.
    - `Value <String[]>`: Matriz de valores a ser usado para comparação
  - `[Not <IQueryFilter>]`: a expressão lógica "NOT".
  - `[Or <IQueryFilter[]>]`: A expressão "OR" lógica. Deve ter pelo menos 2 itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca

OU <IQueryFilter[]>: a expressão lógica "OR". Deve ter pelo menos 2 itens.
  - `[And <IQueryFilter[]>]`: a expressão lógica "AND". Deve ter pelo menos 2 itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão
    - `Name <String>`: o nome da coluna a ser usada em comparação.
    - `Value <String[]>`: Matriz de valores a ser usado para comparação
  - `[Not <IQueryFilter>]`: a expressão lógica "NOT".
  - `[Or <IQueryFilter[]>]`: A expressão "OR" lógica. Deve ter pelo menos 2 itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca

TAG <IQueryComparisonExpression> : tem expressão de comparação para uma marca.
  - `Name <String>`: o nome da coluna a ser usada em comparação.
  - `Value <String[]>`: Matriz de valores a ser usado para comparação

## LINKS RELACIONADOS

