---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116070"
---
# <span data-ttu-id="aef55-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="aef55-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="aef55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aef55-102">SYNOPSIS</span></span>
<span data-ttu-id="aef55-103">Desabilita (descarta) recomendações de sensibilidade em colunas no pool sql.</span><span class="sxs-lookup"><span data-stu-id="aef55-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="aef55-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aef55-104">SYNTAX</span></span>

### <span data-ttu-id="aef55-105">InputObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aef55-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef55-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="aef55-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef55-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="aef55-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aef55-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="aef55-108">DESCRIPTION</span></span>
<span data-ttu-id="aef55-109">O Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet desabilita (descarta) recomendações de sensibilidade em colunas no pool sql.</span><span class="sxs-lookup"><span data-stu-id="aef55-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="aef55-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aef55-110">EXAMPLES</span></span>

### <span data-ttu-id="aef55-111">Exemplo 1: Desabilitar recomendações de sensibilidade em uma determinada coluna em um pool SQL do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="aef55-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="aef55-112">Exemplo 2: Desabilitar recomendações de sensibilidade em colunas que têm recomendações de sensibilidade em um pool SQL do Azure Synapse usando o Piping.</span><span class="sxs-lookup"><span data-stu-id="aef55-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="aef55-113">Exemplo 3: Desabilitar recomendações de sensibilidade em uma determinada coluna em um pool SQL synapse do Azure usando o Piping.</span><span class="sxs-lookup"><span data-stu-id="aef55-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="aef55-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aef55-114">PARAMETERS</span></span>

### <span data-ttu-id="aef55-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aef55-115">-AsJob</span></span>
<span data-ttu-id="aef55-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aef55-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-117">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="aef55-117">-ColumnName</span></span>
<span data-ttu-id="aef55-118">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="aef55-118">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef55-119">-DefaultProfile</span></span>
<span data-ttu-id="aef55-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aef55-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aef55-121">-InputObject</span></span>
<span data-ttu-id="aef55-122">Um objeto que representa uma Classificação de Sensibilidade do Sql Pool.</span><span class="sxs-lookup"><span data-stu-id="aef55-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aef55-123">-PassThru</span></span>
<span data-ttu-id="aef55-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="aef55-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="aef55-125">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="aef55-125">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef55-126">-ResourceGroupName</span></span>
<span data-ttu-id="aef55-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aef55-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="aef55-128">-SchemaName</span></span>
<span data-ttu-id="aef55-129">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="aef55-129">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="aef55-130">-SqlPoolName</span></span>
<span data-ttu-id="aef55-131">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="aef55-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="aef55-132">-SqlPoolObject</span></span>
<span data-ttu-id="aef55-133">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="aef55-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-134">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="aef55-134">-TableName</span></span>
<span data-ttu-id="aef55-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="aef55-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-136">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="aef55-136">-WorkspaceName</span></span>
<span data-ttu-id="aef55-137">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="aef55-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aef55-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aef55-138">-Confirm</span></span>
<span data-ttu-id="aef55-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aef55-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef55-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef55-140">-WhatIf</span></span>
<span data-ttu-id="aef55-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aef55-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef55-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aef55-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef55-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef55-143">CommonParameters</span></span>
<span data-ttu-id="aef55-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef55-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef55-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aef55-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef55-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="aef55-146">INPUTS</span></span>

### <span data-ttu-id="aef55-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="aef55-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="aef55-148">System.String</span><span class="sxs-lookup"><span data-stu-id="aef55-148">System.String</span></span>

### <span data-ttu-id="aef55-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="aef55-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="aef55-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="aef55-150">OUTPUTS</span></span>

### <span data-ttu-id="aef55-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aef55-151">System.Boolean</span></span>

## <span data-ttu-id="aef55-152">Notas</span><span class="sxs-lookup"><span data-stu-id="aef55-152">NOTES</span></span>

## <span data-ttu-id="aef55-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aef55-153">RELATED LINKS</span></span>
