---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433996"
---
# <span data-ttu-id="6a77f-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="6a77f-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="6a77f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a77f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a77f-103">Criar um objeto de memória para QueryFilter</span><span class="sxs-lookup"><span data-stu-id="6a77f-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="6a77f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a77f-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="6a77f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a77f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a77f-106">Criar um objeto de memória para QueryFilter</span><span class="sxs-lookup"><span data-stu-id="6a77f-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="6a77f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a77f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a77f-108">Exemplo 1: criar um objeto de filtro de consulta para exportação de gerenciamento de custos</span><span class="sxs-lookup"><span data-stu-id="6a77f-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="6a77f-109">Esse comando cria um objeto de filtro de consulta para exportação de gerenciamento de custos.</span><span class="sxs-lookup"><span data-stu-id="6a77f-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="6a77f-110">OS</span><span class="sxs-lookup"><span data-stu-id="6a77f-110">PARAMETERS</span></span>

### <span data-ttu-id="6a77f-111">-E</span><span class="sxs-lookup"><span data-stu-id="6a77f-111">-And</span></span>
<span data-ttu-id="6a77f-112">A expressão lógica "e".</span><span class="sxs-lookup"><span data-stu-id="6a77f-112">The logical "AND" expression.</span></span>
<span data-ttu-id="6a77f-113">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-113">Must have at least 2 items.</span></span>
<span data-ttu-id="6a77f-114">Para construir, consulte a seção de anotações para e propriedades e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6a77f-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a77f-115">-Dimensões</span><span class="sxs-lookup"><span data-stu-id="6a77f-115">-Dimensions</span></span>
<span data-ttu-id="6a77f-116">Tem expressão de comparação para dimensões.</span><span class="sxs-lookup"><span data-stu-id="6a77f-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="6a77f-117">Para construir, consulte a seção de notas para propriedades de dimensões e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6a77f-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a77f-118">-Não</span><span class="sxs-lookup"><span data-stu-id="6a77f-118">-Not</span></span>
<span data-ttu-id="6a77f-119">A expressão lógica "não".</span><span class="sxs-lookup"><span data-stu-id="6a77f-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="6a77f-120">Para construir, consulte a seção observações para não propriedades e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6a77f-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a77f-121">-Ou</span><span class="sxs-lookup"><span data-stu-id="6a77f-121">-Or</span></span>
<span data-ttu-id="6a77f-122">A expressão lógica "ou".</span><span class="sxs-lookup"><span data-stu-id="6a77f-122">The logical "OR" expression.</span></span>
<span data-ttu-id="6a77f-123">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-123">Must have at least 2 items.</span></span>
<span data-ttu-id="6a77f-124">Para construir, consulte a seção de anotações para ou propriedades e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6a77f-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a77f-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="6a77f-125">-Tag</span></span>
<span data-ttu-id="6a77f-126">Tem uma expressão de comparação para uma marca.</span><span class="sxs-lookup"><span data-stu-id="6a77f-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="6a77f-127">Para construir, consulte a seção de notas para propriedades de marca e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6a77f-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a77f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a77f-128">CommonParameters</span></span>
<span data-ttu-id="6a77f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a77f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a77f-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a77f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a77f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a77f-131">INPUTS</span></span>

## <span data-ttu-id="6a77f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a77f-132">OUTPUTS</span></span>

### <span data-ttu-id="6a77f-133">Microsoft. Azure. PowerShell. cmdlets. CostManagement. Models. Api20200601. QueryFilter</span><span class="sxs-lookup"><span data-stu-id="6a77f-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="6a77f-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a77f-134">NOTES</span></span>

<span data-ttu-id="6a77f-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6a77f-135">ALIASES</span></span>

<span data-ttu-id="6a77f-136">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="6a77f-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a77f-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6a77f-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a77f-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a77f-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a77f-139">E <IQueryFilter [] >: a expressão lógica "e".</span><span class="sxs-lookup"><span data-stu-id="6a77f-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="6a77f-140">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-141">`[And <IQueryFilter[]>]`: A expressão lógica "e".</span><span class="sxs-lookup"><span data-stu-id="6a77f-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="6a77f-142">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-143">`[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="6a77f-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="6a77f-144">`Name <String>`: O nome da coluna a ser usada na comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="6a77f-145">`Operator <OperatorType>`: O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="6a77f-146">`Value <String[]>`: Matriz de valores a serem usados para comparação</span><span class="sxs-lookup"><span data-stu-id="6a77f-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="6a77f-147">`[Not <IQueryFilter>]`: A expressão lógica "não".</span><span class="sxs-lookup"><span data-stu-id="6a77f-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="6a77f-148">`[Or <IQueryFilter[]>]`: A expressão lógica "ou".</span><span class="sxs-lookup"><span data-stu-id="6a77f-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="6a77f-149">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-150">`[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="6a77f-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="6a77f-151">DIMENSÕES <IQueryComparisonExpression> : tem expressão de comparação para dimensões.</span><span class="sxs-lookup"><span data-stu-id="6a77f-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="6a77f-152">`Name <String>`: O nome da coluna a ser usada na comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="6a77f-153">`Operator <OperatorType>`: O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="6a77f-154">`Value <String[]>`: Matriz de valores a serem usados para comparação</span><span class="sxs-lookup"><span data-stu-id="6a77f-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="6a77f-155">Não <IQueryFilter> : a expressão lógica "não".</span><span class="sxs-lookup"><span data-stu-id="6a77f-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="6a77f-156">`[And <IQueryFilter[]>]`: A expressão lógica "e".</span><span class="sxs-lookup"><span data-stu-id="6a77f-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="6a77f-157">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-158">`[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="6a77f-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="6a77f-159">`Name <String>`: O nome da coluna a ser usada na comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="6a77f-160">`Operator <OperatorType>`: O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="6a77f-161">`Value <String[]>`: Matriz de valores a serem usados para comparação</span><span class="sxs-lookup"><span data-stu-id="6a77f-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="6a77f-162">`[Not <IQueryFilter>]`: A expressão lógica "não".</span><span class="sxs-lookup"><span data-stu-id="6a77f-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="6a77f-163">`[Or <IQueryFilter[]>]`: A expressão lógica "ou".</span><span class="sxs-lookup"><span data-stu-id="6a77f-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="6a77f-164">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-165">`[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="6a77f-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="6a77f-166">OU <IQueryFilter [] >: a expressão lógica "ou".</span><span class="sxs-lookup"><span data-stu-id="6a77f-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="6a77f-167">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-168">`[And <IQueryFilter[]>]`: A expressão lógica "e".</span><span class="sxs-lookup"><span data-stu-id="6a77f-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="6a77f-169">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-170">`[Dimensions <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="6a77f-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="6a77f-171">`Name <String>`: O nome da coluna a ser usada na comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="6a77f-172">`Operator <OperatorType>`: O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="6a77f-173">`Value <String[]>`: Matriz de valores a serem usados para comparação</span><span class="sxs-lookup"><span data-stu-id="6a77f-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="6a77f-174">`[Not <IQueryFilter>]`: A expressão lógica "não".</span><span class="sxs-lookup"><span data-stu-id="6a77f-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="6a77f-175">`[Or <IQueryFilter[]>]`: A expressão lógica "ou".</span><span class="sxs-lookup"><span data-stu-id="6a77f-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="6a77f-176">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="6a77f-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="6a77f-177">`[Tag <IQueryComparisonExpression>]`: Tem uma expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="6a77f-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="6a77f-178">MARCA <IQueryComparisonExpression> : tem uma expressão de comparação para uma marca.</span><span class="sxs-lookup"><span data-stu-id="6a77f-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="6a77f-179">`Name <String>`: O nome da coluna a ser usada na comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="6a77f-180">`Operator <OperatorType>`: O operador a ser usado para comparação.</span><span class="sxs-lookup"><span data-stu-id="6a77f-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="6a77f-181">`Value <String[]>`: Matriz de valores a serem usados para comparação</span><span class="sxs-lookup"><span data-stu-id="6a77f-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="6a77f-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a77f-182">RELATED LINKS</span></span>

