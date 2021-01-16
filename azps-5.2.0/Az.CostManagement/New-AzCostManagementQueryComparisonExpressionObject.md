---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258817"
---
# <span data-ttu-id="d2ced-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="d2ced-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="d2ced-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2ced-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ced-103">Criar um objeto de memória para QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="d2ced-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="d2ced-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2ced-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="d2ced-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2ced-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ced-106">Criar um objeto de memória para QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="d2ced-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="d2ced-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2ced-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ced-108">Exemplo 1: criar um objeto de expressão de comparação de consulta para exportação de gerenciamento de custos</span><span class="sxs-lookup"><span data-stu-id="d2ced-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="d2ced-109">Esse comando cria um objeto de expressão de comparação de consulta para exportação de gerenciamento de custos.</span><span class="sxs-lookup"><span data-stu-id="d2ced-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="d2ced-110">OS</span><span class="sxs-lookup"><span data-stu-id="d2ced-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ced-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2ced-111">-Name</span></span>
<span data-ttu-id="d2ced-112">O nome da coluna a ser usada na comparação.</span><span class="sxs-lookup"><span data-stu-id="d2ced-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="d2ced-113">-Operador</span><span class="sxs-lookup"><span data-stu-id="d2ced-113">-Operator</span></span>
<span data-ttu-id="d2ced-114">O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="d2ced-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="d2ced-115">-Valor</span><span class="sxs-lookup"><span data-stu-id="d2ced-115">-Value</span></span>
<span data-ttu-id="d2ced-116">Matriz de valores a serem usados para comparação.</span><span class="sxs-lookup"><span data-stu-id="d2ced-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="d2ced-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ced-117">CommonParameters</span></span>
<span data-ttu-id="d2ced-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ced-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ced-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2ced-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ced-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2ced-120">INPUTS</span></span>

## <span data-ttu-id="d2ced-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2ced-121">OUTPUTS</span></span>

### <span data-ttu-id="d2ced-122">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="d2ced-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="d2ced-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2ced-123">NOTES</span></span>

<span data-ttu-id="d2ced-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d2ced-124">ALIASES</span></span>

## <span data-ttu-id="d2ced-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2ced-125">RELATED LINKS</span></span>

