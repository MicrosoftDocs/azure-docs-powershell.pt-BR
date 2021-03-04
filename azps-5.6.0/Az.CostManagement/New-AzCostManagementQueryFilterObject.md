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
# <span data-ttu-id="27e58-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="27e58-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="27e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27e58-102">SYNOPSIS</span></span>
<span data-ttu-id="27e58-103">Criar um objeto na memória para QueryFilter</span><span class="sxs-lookup"><span data-stu-id="27e58-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="27e58-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="27e58-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="27e58-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="27e58-105">DESCRIPTION</span></span>
<span data-ttu-id="27e58-106">Criar um objeto na memória para QueryFilter</span><span class="sxs-lookup"><span data-stu-id="27e58-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="27e58-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27e58-107">EXAMPLES</span></span>

### <span data-ttu-id="27e58-108">Exemplo 1: Criar um objeto filter de consulta para exportação de gerenciamento de custos</span><span class="sxs-lookup"><span data-stu-id="27e58-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="27e58-109">este comando cria um objeto filter de consulta para exportação de gerenciamento de custos.</span><span class="sxs-lookup"><span data-stu-id="27e58-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="27e58-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="27e58-110">PARAMETERS</span></span>

### <span data-ttu-id="27e58-111">-And</span><span class="sxs-lookup"><span data-stu-id="27e58-111">-And</span></span>
<span data-ttu-id="27e58-112">A expressão lógica "AND".</span><span class="sxs-lookup"><span data-stu-id="27e58-112">The logical "AND" expression.</span></span>
<span data-ttu-id="27e58-113">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-113">Must have at least 2 items.</span></span>
<span data-ttu-id="27e58-114">Para construir, consulte a seção NOTES para propriedades AND e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="27e58-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="27e58-115">-Dimensões</span><span class="sxs-lookup"><span data-stu-id="27e58-115">-Dimensions</span></span>
<span data-ttu-id="27e58-116">Tem expressão de comparação para dimensões.</span><span class="sxs-lookup"><span data-stu-id="27e58-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="27e58-117">Para construir, consulte a seção NOTES para propriedades DIMENSIONS e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="27e58-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="27e58-118">-Not</span><span class="sxs-lookup"><span data-stu-id="27e58-118">-Not</span></span>
<span data-ttu-id="27e58-119">A expressão lógica "NOT".</span><span class="sxs-lookup"><span data-stu-id="27e58-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="27e58-120">Para construir, consulte a seção NOTES para propriedades NOT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="27e58-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27e58-121">-Or</span><span class="sxs-lookup"><span data-stu-id="27e58-121">-Or</span></span>
<span data-ttu-id="27e58-122">A expressão "OR" lógica.</span><span class="sxs-lookup"><span data-stu-id="27e58-122">The logical "OR" expression.</span></span>
<span data-ttu-id="27e58-123">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-123">Must have at least 2 items.</span></span>
<span data-ttu-id="27e58-124">Para construir, consulte a seção NOTES para propriedades OR e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="27e58-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="27e58-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="27e58-125">-Tag</span></span>
<span data-ttu-id="27e58-126">Tem expressão de comparação para uma marca.</span><span class="sxs-lookup"><span data-stu-id="27e58-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="27e58-127">Para construir, consulte a seção NOTES para propriedades TAG e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="27e58-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="27e58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e58-128">CommonParameters</span></span>
<span data-ttu-id="27e58-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e58-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27e58-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e58-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27e58-131">INPUTS</span></span>

## <span data-ttu-id="27e58-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="27e58-132">OUTPUTS</span></span>

### <span data-ttu-id="27e58-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="27e58-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="27e58-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="27e58-134">NOTES</span></span>

<span data-ttu-id="27e58-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="27e58-135">ALIASES</span></span>

<span data-ttu-id="27e58-136">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="27e58-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27e58-137">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="27e58-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27e58-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27e58-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27e58-139">AND <IQueryFilter[]>: a expressão lógica "AND".</span><span class="sxs-lookup"><span data-stu-id="27e58-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="27e58-140">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-141">`[And <IQueryFilter[]>]`: a expressão lógica "AND".</span><span class="sxs-lookup"><span data-stu-id="27e58-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="27e58-142">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-143">`[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="27e58-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="27e58-144">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="27e58-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="27e58-145">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="27e58-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="27e58-146">`[Not <IQueryFilter>]`: a expressão lógica "NOT".</span><span class="sxs-lookup"><span data-stu-id="27e58-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="27e58-147">`[Or <IQueryFilter[]>]`: A expressão "OR" lógica.</span><span class="sxs-lookup"><span data-stu-id="27e58-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="27e58-148">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-149">`[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="27e58-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="27e58-150">DIMENSÕES <IQueryComparisonExpression> : tem expressão de comparação para uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="27e58-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="27e58-151">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="27e58-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="27e58-152">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="27e58-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="27e58-153">NÃO <IQueryFilter> : a expressão lógica "NOT".</span><span class="sxs-lookup"><span data-stu-id="27e58-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="27e58-154">`[And <IQueryFilter[]>]`: a expressão lógica "AND".</span><span class="sxs-lookup"><span data-stu-id="27e58-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="27e58-155">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-156">`[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="27e58-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="27e58-157">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="27e58-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="27e58-158">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="27e58-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="27e58-159">`[Not <IQueryFilter>]`: a expressão lógica "NOT".</span><span class="sxs-lookup"><span data-stu-id="27e58-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="27e58-160">`[Or <IQueryFilter[]>]`: A expressão "OR" lógica.</span><span class="sxs-lookup"><span data-stu-id="27e58-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="27e58-161">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-162">`[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="27e58-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="27e58-163">OU <IQueryFilter[]>: a expressão lógica "OR".</span><span class="sxs-lookup"><span data-stu-id="27e58-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="27e58-164">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-165">`[And <IQueryFilter[]>]`: a expressão lógica "AND".</span><span class="sxs-lookup"><span data-stu-id="27e58-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="27e58-166">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-167">`[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="27e58-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="27e58-168">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="27e58-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="27e58-169">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="27e58-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="27e58-170">`[Not <IQueryFilter>]`: a expressão lógica "NOT".</span><span class="sxs-lookup"><span data-stu-id="27e58-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="27e58-171">`[Or <IQueryFilter[]>]`: A expressão "OR" lógica.</span><span class="sxs-lookup"><span data-stu-id="27e58-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="27e58-172">Deve ter pelo menos 2 itens.</span><span class="sxs-lookup"><span data-stu-id="27e58-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="27e58-173">`[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="27e58-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="27e58-174">TAG <IQueryComparisonExpression> : tem expressão de comparação para uma marca.</span><span class="sxs-lookup"><span data-stu-id="27e58-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="27e58-175">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="27e58-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="27e58-176">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="27e58-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="27e58-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27e58-177">RELATED LINKS</span></span>

