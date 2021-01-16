---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258813"
---
# New-AzCostManagementQueryFilterObject

## Sinopse
Criar um objeto de memória para QueryFilter

## SYNTAX

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## DESCRITIVO
Criar um objeto de memória para QueryFilter

## EXEMPLOS

### Exemplo 1: criar um objeto de filtro de consulta para exportação de gerenciamento de custos
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

Esse comando cria um objeto de filtro de consulta para exportação de gerenciamento de custos.

## OS

### -E
A expressão lógica "e".
Deve ter pelo menos 2 itens.
Para construir, consulte a seção de anotações para e propriedades e crie uma tabela de hash.

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
Para construir, consulte a seção de notas para propriedades de dimensões e crie uma tabela de hash.

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
A expressão lógica "não".
Para construir, consulte a seção observações para não propriedades e crie uma tabela de hash.

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
A expressão lógica "ou".
Deve ter pelo menos 2 itens.
Para construir, consulte a seção de anotações para ou propriedades e crie uma tabela de hash.

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

### -Marca
Tem uma expressão de comparação para uma marca.
Para construir, consulte a seção de notas para propriedades de marca e crie uma tabela de hash.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. QueryFilter

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


E <IQueryFilter [] >: a expressão lógica "e". Deve ter pelo menos 2 itens.
  - `[And <IQueryFilter[]>]`: A expressão lógica "e". Deve ter pelo menos 2 itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão
    - `Name <String>`: O nome da coluna a ser usada na comparação.
    - `Operator <OperatorType>`: O operador a ser usado para comparação.
    - `Value <String[]>`: Matriz de valores a serem usados para comparação
  - `[Not <IQueryFilter>]`: A expressão lógica "não".
  - `[Or <IQueryFilter[]>]`: A expressão lógica "ou". Deve ter pelo menos 2 itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca

DIMENSÕES <IQueryComparisonExpression> : tem expressão de comparação para dimensões.
  - `Name <String>`: O nome da coluna a ser usada na comparação.
  - `Operator <OperatorType>`: O operador a ser usado para comparação.
  - `Value <String[]>`: Matriz de valores a serem usados para comparação

Não <IQueryFilter> : a expressão lógica "não".
  - `[And <IQueryFilter[]>]`: A expressão lógica "e". Deve ter pelo menos 2 itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão
    - `Name <String>`: O nome da coluna a ser usada na comparação.
    - `Operator <OperatorType>`: O operador a ser usado para comparação.
    - `Value <String[]>`: Matriz de valores a serem usados para comparação
  - `[Not <IQueryFilter>]`: A expressão lógica "não".
  - `[Or <IQueryFilter[]>]`: A expressão lógica "ou". Deve ter pelo menos 2 itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca

OU <IQueryFilter [] >: a expressão lógica "ou". Deve ter pelo menos 2 itens.
  - `[And <IQueryFilter[]>]`: A expressão lógica "e". Deve ter pelo menos 2 itens.
  - `[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão
    - `Name <String>`: O nome da coluna a ser usada na comparação.
    - `Operator <OperatorType>`: O operador a ser usado para comparação.
    - `Value <String[]>`: Matriz de valores a serem usados para comparação
  - `[Not <IQueryFilter>]`: A expressão lógica "não".
  - `[Or <IQueryFilter[]>]`: A expressão lógica "ou". Deve ter pelo menos 2 itens.
  - `[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca

MARCA <IQueryComparisonExpression> : tem uma expressão de comparação para uma marca.
  - `Name <String>`: O nome da coluna a ser usada na comparação.
  - `Operator <OperatorType>`: O operador a ser usado para comparação.
  - `Value <String[]>`: Matriz de valores a serem usados para comparação

## LINKS RELACIONADOS

