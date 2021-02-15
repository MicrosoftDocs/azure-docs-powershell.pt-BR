---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 608736e8ddb85b877995bed8a42b9bd629dcdba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112010"
---
# <span data-ttu-id="401b0-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="401b0-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="401b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="401b0-102">SYNOPSIS</span></span>
<span data-ttu-id="401b0-103">Criar um objeto na memória para QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="401b0-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="401b0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="401b0-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="401b0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="401b0-105">DESCRIPTION</span></span>
<span data-ttu-id="401b0-106">Criar um objeto na memória para QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="401b0-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="401b0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="401b0-107">EXAMPLES</span></span>

### <span data-ttu-id="401b0-108">Exemplo 1: Criar um objeto de expressão de comparação de consulta para exportação de gerenciamento de custos</span><span class="sxs-lookup"><span data-stu-id="401b0-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="401b0-109">Esse comando cria um objeto de expressão de comparação de consulta para exportação de gerenciamento de custos.</span><span class="sxs-lookup"><span data-stu-id="401b0-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="401b0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="401b0-110">PARAMETERS</span></span>

### <span data-ttu-id="401b0-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="401b0-111">-Name</span></span>
<span data-ttu-id="401b0-112">O nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="401b0-112">The name of the column to use in comparison.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401b0-113">-Operador</span><span class="sxs-lookup"><span data-stu-id="401b0-113">-Operator</span></span>
<span data-ttu-id="401b0-114">O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="401b0-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401b0-115">-Valor</span><span class="sxs-lookup"><span data-stu-id="401b0-115">-Value</span></span>
<span data-ttu-id="401b0-116">Matriz de valores a ser usada para comparação.</span><span class="sxs-lookup"><span data-stu-id="401b0-116">Array of values to use for comparison.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401b0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401b0-117">CommonParameters</span></span>
<span data-ttu-id="401b0-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="401b0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401b0-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="401b0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401b0-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="401b0-120">INPUTS</span></span>

## <span data-ttu-id="401b0-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="401b0-121">OUTPUTS</span></span>

### <span data-ttu-id="401b0-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="401b0-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="401b0-123">Notas</span><span class="sxs-lookup"><span data-stu-id="401b0-123">NOTES</span></span>

<span data-ttu-id="401b0-124">Aliases</span><span class="sxs-lookup"><span data-stu-id="401b0-124">ALIASES</span></span>

## <span data-ttu-id="401b0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="401b0-125">RELATED LINKS</span></span>

