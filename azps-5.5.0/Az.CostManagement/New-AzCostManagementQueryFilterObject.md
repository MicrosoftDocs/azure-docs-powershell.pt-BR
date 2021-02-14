---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115886"
---
# New-AzCostManagementQueryFilterObject

## Sinopse
Criar um objeto na memória para o QueryFilter

## Sintaxe

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## Descrição
Criar um objeto na memória para o QueryFilter

## Exemplos

### Exemplo 1: Criar um objeto de filtro de consulta para exportação de gerenciamento de custos
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

esse comando cria um objeto de filtro de consulta para exportação de gerenciamento de custos.

## Parâmetros

### - E
A expressão lógica "E".
Deve ter pelo menos dois itens.
Para construir, consulte a seção ANOTAÇÕES das propriedades E e crie uma tabela hash.

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
Tem expressão de comparação para uma dimensão.
Para construir, consulte a seção ANOTAÇÕES para propriedades DIMENSIONS e crie uma tabela hash.

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

### -Não
A expressão lógica "NÃO".
Para construir, consulte a seção ANOTAÇÕES para propriedades NÃO e crie uma tabela hash.

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

### -Ou
A expressão lógica "OU".
Deve ter pelo menos dois itens.
Para construir, confira a seção ANOTAÇÕES das propriedades OU e crie uma tabela hash.

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
Para construir, consulte a seção ANOTAÇÕES para propriedades de MARCA e crie uma tabela hash.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

## Saídas

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## Notas

Aliases

PROPRIEDADES DE PARÂMETRO COMPLEXOS

Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas. Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: a expressão lógica "AND". Deve ter pelo menos dois itens.
  - `[And <IQueryFilter[]>]`: a expressão lógica "E". Deve ter pelo menos dois itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão
    - `Name <String>`: o nome da coluna a ser usada em comparação.
    - `Value <String[]>`: Matriz de valores a ser usado para comparação
  - `[Not <IQueryFilter>]`: a expressão lógica "NÃO".
  - `[Or <IQueryFilter[]>]`: a expressão lógica "OU". Deve ter pelo menos dois itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca

<IQueryComparisonExpression>DIMENSÕES: tem expressão de comparação para uma dimensão.
  - `Name <String>`: o nome da coluna a ser usada em comparação.
  - `Value <String[]>`: Matriz de valores a ser usado para comparação

NÃO: <IQueryFilter> A expressão lógica "NÃO".
  - `[And <IQueryFilter[]>]`: a expressão lógica "E". Deve ter pelo menos dois itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão
    - `Name <String>`: o nome da coluna a ser usada em comparação.
    - `Value <String[]>`: Matriz de valores a ser usado para comparação
  - `[Not <IQueryFilter>]`: a expressão lógica "NÃO".
  - `[Or <IQueryFilter[]>]`: a expressão lógica "OU". Deve ter pelo menos dois itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca

OU <IQueryFilter[]>: a expressão lógica "OU". Deve ter pelo menos dois itens.
  - `[And <IQueryFilter[]>]`: a expressão lógica "E". Deve ter pelo menos dois itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão
    - `Name <String>`: o nome da coluna a ser usada em comparação.
    - `Value <String[]>`: Matriz de valores a ser usado para comparação
  - `[Not <IQueryFilter>]`: a expressão lógica "NÃO".
  - `[Or <IQueryFilter[]>]`: a expressão lógica "OU". Deve ter pelo menos dois itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca

TAG: <IQueryComparisonExpression> Tem expressão de comparação para uma marca.
  - `Name <String>`: o nome da coluna a ser usada em comparação.
  - `Value <String[]>`: Matriz de valores a ser usado para comparação

## LINKS RELACIONADOS

