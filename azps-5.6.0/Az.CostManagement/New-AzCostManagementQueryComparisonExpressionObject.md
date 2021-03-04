---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: b41c5a30a1425778e69fbfff42cfe7062c6b71b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891404"
---
# <span data-ttu-id="c4c0b-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="c4c0b-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="c4c0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c0b-103">Criar um objeto na memória para QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="c4c0b-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="c4c0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c4c0b-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="c4c0b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c4c0b-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c0b-106">Criar um objeto na memória para QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="c4c0b-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="c4c0b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4c0b-107">EXAMPLES</span></span>

### <span data-ttu-id="c4c0b-108">Exemplo 1: Criar um objeto de expressão de comparação de consulta para exportação de gerenciamento de custos</span><span class="sxs-lookup"><span data-stu-id="c4c0b-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="c4c0b-109">Este comando cria um objeto de expressão de comparação de consulta para exportação de gerenciamento de custos.</span><span class="sxs-lookup"><span data-stu-id="c4c0b-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="c4c0b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c4c0b-110">PARAMETERS</span></span>

### <span data-ttu-id="c4c0b-111">-Name</span><span class="sxs-lookup"><span data-stu-id="c4c0b-111">-Name</span></span>
<span data-ttu-id="c4c0b-112">O nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="c4c0b-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="c4c0b-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="c4c0b-113">-Operator</span></span>
<span data-ttu-id="c4c0b-114">O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="c4c0b-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="c4c0b-115">-Value</span><span class="sxs-lookup"><span data-stu-id="c4c0b-115">-Value</span></span>
<span data-ttu-id="c4c0b-116">Matriz de valores a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="c4c0b-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="c4c0b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c0b-117">CommonParameters</span></span>
<span data-ttu-id="c4c0b-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c0b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c0b-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4c0b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c0b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4c0b-120">INPUTS</span></span>

## <span data-ttu-id="c4c0b-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c4c0b-121">OUTPUTS</span></span>

### <span data-ttu-id="c4c0b-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="c4c0b-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="c4c0b-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="c4c0b-123">NOTES</span></span>

<span data-ttu-id="c4c0b-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c4c0b-124">ALIASES</span></span>

## <span data-ttu-id="c4c0b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4c0b-125">RELATED LINKS</span></span>

