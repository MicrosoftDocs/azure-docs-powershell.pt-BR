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
# <span data-ttu-id="71976-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="71976-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="71976-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71976-102">SYNOPSIS</span></span>
<span data-ttu-id="71976-103">Criar um objeto na memória para o QueryFilter</span><span class="sxs-lookup"><span data-stu-id="71976-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="71976-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71976-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="71976-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="71976-105">DESCRIPTION</span></span>
<span data-ttu-id="71976-106">Criar um objeto na memória para o QueryFilter</span><span class="sxs-lookup"><span data-stu-id="71976-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="71976-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71976-107">EXAMPLES</span></span>

### <span data-ttu-id="71976-108">Exemplo 1: Criar um objeto de filtro de consulta para exportação de gerenciamento de custos</span><span class="sxs-lookup"><span data-stu-id="71976-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="71976-109">esse comando cria um objeto de filtro de consulta para exportação de gerenciamento de custos.</span><span class="sxs-lookup"><span data-stu-id="71976-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="71976-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71976-110">PARAMETERS</span></span>

### <span data-ttu-id="71976-111">- E</span><span class="sxs-lookup"><span data-stu-id="71976-111">-And</span></span>
<span data-ttu-id="71976-112">A expressão lógica "E".</span><span class="sxs-lookup"><span data-stu-id="71976-112">The logical "AND" expression.</span></span>
<span data-ttu-id="71976-113">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-113">Must have at least 2 items.</span></span>
<span data-ttu-id="71976-114">Para construir, consulte a seção ANOTAÇÕES das propriedades E e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="71976-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="71976-115">-Dimensões</span><span class="sxs-lookup"><span data-stu-id="71976-115">-Dimensions</span></span>
<span data-ttu-id="71976-116">Tem expressão de comparação para uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="71976-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="71976-117">Para construir, consulte a seção ANOTAÇÕES para propriedades DIMENSIONS e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="71976-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="71976-118">-Não</span><span class="sxs-lookup"><span data-stu-id="71976-118">-Not</span></span>
<span data-ttu-id="71976-119">A expressão lógica "NÃO".</span><span class="sxs-lookup"><span data-stu-id="71976-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="71976-120">Para construir, consulte a seção ANOTAÇÕES para propriedades NÃO e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="71976-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71976-121">-Ou</span><span class="sxs-lookup"><span data-stu-id="71976-121">-Or</span></span>
<span data-ttu-id="71976-122">A expressão lógica "OU".</span><span class="sxs-lookup"><span data-stu-id="71976-122">The logical "OR" expression.</span></span>
<span data-ttu-id="71976-123">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-123">Must have at least 2 items.</span></span>
<span data-ttu-id="71976-124">Para construir, confira a seção ANOTAÇÕES das propriedades OU e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="71976-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="71976-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="71976-125">-Tag</span></span>
<span data-ttu-id="71976-126">Tem expressão de comparação para uma marca.</span><span class="sxs-lookup"><span data-stu-id="71976-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="71976-127">Para construir, consulte a seção ANOTAÇÕES para propriedades de MARCA e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="71976-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="71976-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71976-128">CommonParameters</span></span>
<span data-ttu-id="71976-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71976-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71976-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71976-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71976-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="71976-131">INPUTS</span></span>

## <span data-ttu-id="71976-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="71976-132">OUTPUTS</span></span>

### <span data-ttu-id="71976-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="71976-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="71976-134">Notas</span><span class="sxs-lookup"><span data-stu-id="71976-134">NOTES</span></span>

<span data-ttu-id="71976-135">Aliases</span><span class="sxs-lookup"><span data-stu-id="71976-135">ALIASES</span></span>

<span data-ttu-id="71976-136">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="71976-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71976-137">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="71976-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71976-138">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71976-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71976-139">AND <IQueryFilter[]>: a expressão lógica "AND".</span><span class="sxs-lookup"><span data-stu-id="71976-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="71976-140">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-141">`[And <IQueryFilter[]>]`: a expressão lógica "E".</span><span class="sxs-lookup"><span data-stu-id="71976-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="71976-142">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-143">`[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="71976-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="71976-144">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="71976-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="71976-145">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="71976-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="71976-146">`[Not <IQueryFilter>]`: a expressão lógica "NÃO".</span><span class="sxs-lookup"><span data-stu-id="71976-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="71976-147">`[Or <IQueryFilter[]>]`: a expressão lógica "OU".</span><span class="sxs-lookup"><span data-stu-id="71976-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="71976-148">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-149">`[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="71976-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="71976-150"><IQueryComparisonExpression>DIMENSÕES: tem expressão de comparação para uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="71976-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="71976-151">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="71976-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="71976-152">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="71976-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="71976-153">NÃO: <IQueryFilter> A expressão lógica "NÃO".</span><span class="sxs-lookup"><span data-stu-id="71976-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="71976-154">`[And <IQueryFilter[]>]`: a expressão lógica "E".</span><span class="sxs-lookup"><span data-stu-id="71976-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="71976-155">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-156">`[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="71976-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="71976-157">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="71976-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="71976-158">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="71976-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="71976-159">`[Not <IQueryFilter>]`: a expressão lógica "NÃO".</span><span class="sxs-lookup"><span data-stu-id="71976-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="71976-160">`[Or <IQueryFilter[]>]`: a expressão lógica "OU".</span><span class="sxs-lookup"><span data-stu-id="71976-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="71976-161">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-162">`[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="71976-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="71976-163">OU <IQueryFilter[]>: a expressão lógica "OU".</span><span class="sxs-lookup"><span data-stu-id="71976-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="71976-164">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-165">`[And <IQueryFilter[]>]`: a expressão lógica "E".</span><span class="sxs-lookup"><span data-stu-id="71976-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="71976-166">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-167">`[Dimensions <IQueryComparisonExpression>]`: Tem expressão de comparação para uma dimensão</span><span class="sxs-lookup"><span data-stu-id="71976-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="71976-168">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="71976-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="71976-169">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="71976-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="71976-170">`[Not <IQueryFilter>]`: a expressão lógica "NÃO".</span><span class="sxs-lookup"><span data-stu-id="71976-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="71976-171">`[Or <IQueryFilter[]>]`: a expressão lógica "OU".</span><span class="sxs-lookup"><span data-stu-id="71976-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="71976-172">Deve ter pelo menos dois itens.</span><span class="sxs-lookup"><span data-stu-id="71976-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="71976-173">`[Tag <IQueryComparisonExpression>]`: Tem expressão de comparação para uma marca</span><span class="sxs-lookup"><span data-stu-id="71976-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="71976-174">TAG: <IQueryComparisonExpression> Tem expressão de comparação para uma marca.</span><span class="sxs-lookup"><span data-stu-id="71976-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="71976-175">`Name <String>`: o nome da coluna a ser usada em comparação.</span><span class="sxs-lookup"><span data-stu-id="71976-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="71976-176">`Value <String[]>`: Matriz de valores a ser usado para comparação</span><span class="sxs-lookup"><span data-stu-id="71976-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="71976-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71976-177">RELATED LINKS</span></span>

