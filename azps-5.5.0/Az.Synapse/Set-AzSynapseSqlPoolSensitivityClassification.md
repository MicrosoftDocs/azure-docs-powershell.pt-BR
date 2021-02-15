---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: bb47d791f23df044e5a4677835f85b6f107f2822
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112385"
---
# <span data-ttu-id="e92b5-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="e92b5-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="e92b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e92b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e92b5-103">Define os tipos de informações e os rótulos de sensibilidade das colunas no pool SQL.</span><span class="sxs-lookup"><span data-stu-id="e92b5-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e92b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e92b5-104">SYNTAX</span></span>

### <span data-ttu-id="e92b5-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e92b5-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e92b5-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e92b5-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e92b5-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e92b5-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e92b5-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e92b5-108">DESCRIPTION</span></span>
<span data-ttu-id="e92b5-109">O Set-AzSynapseSqlPoolSensitivityClassification cmdlet define os tipos de informações e rótulos de sensibilidade das colunas no pool SQL.</span><span class="sxs-lookup"><span data-stu-id="e92b5-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e92b5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e92b5-110">EXAMPLES</span></span>

### <span data-ttu-id="e92b5-111">Exemplo 1: Definir o tipo de informações e o rótulo de sensibilidade de uma coluna em um pool SQL synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="e92b5-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="e92b5-112">Exemplo 2: Definir tipos de informações recomendadas e rótulos de sensibilidade de colunas em um pool SQL synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="e92b5-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="e92b5-113">Exemplo 3: Definir o tipo de informações e o rótulo de sensibilidade de uma coluna em um pool SQL do Azure Synapse, usando piping.</span><span class="sxs-lookup"><span data-stu-id="e92b5-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="e92b5-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e92b5-114">PARAMETERS</span></span>

### <span data-ttu-id="e92b5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e92b5-115">-AsJob</span></span>
<span data-ttu-id="e92b5-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e92b5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e92b5-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="e92b5-117">-ClassificationObject</span></span>
<span data-ttu-id="e92b5-118">Um objeto que representa uma Classificação de Sensibilidade do Sql Pool.</span><span class="sxs-lookup"><span data-stu-id="e92b5-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e92b5-119">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="e92b5-119">-ColumnName</span></span>
<span data-ttu-id="e92b5-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="e92b5-120">Name of column.</span></span>

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

### <span data-ttu-id="e92b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92b5-121">-DefaultProfile</span></span>
<span data-ttu-id="e92b5-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e92b5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e92b5-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="e92b5-123">-InformationType</span></span>
<span data-ttu-id="e92b5-124">Um nome que descreve o tipo de informações dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="e92b5-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92b5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e92b5-125">-PassThru</span></span>
<span data-ttu-id="e92b5-126">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e92b5-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e92b5-127">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e92b5-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e92b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="e92b5-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e92b5-129">Resource group name.</span></span>

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

### <span data-ttu-id="e92b5-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e92b5-130">-SchemaName</span></span>
<span data-ttu-id="e92b5-131">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="e92b5-131">Name of schema.</span></span>

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

### <span data-ttu-id="e92b5-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="e92b5-132">-SensitivityLabel</span></span>
<span data-ttu-id="e92b5-133">Um nome que descreve a sensibilidade dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="e92b5-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92b5-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e92b5-134">-SqlPoolName</span></span>
<span data-ttu-id="e92b5-135">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e92b5-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e92b5-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e92b5-136">-SqlPoolObject</span></span>
<span data-ttu-id="e92b5-137">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e92b5-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e92b5-138">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="e92b5-138">-TableName</span></span>
<span data-ttu-id="e92b5-139">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="e92b5-139">Name of table.</span></span>

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

### <span data-ttu-id="e92b5-140">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="e92b5-140">-WorkspaceName</span></span>
<span data-ttu-id="e92b5-141">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="e92b5-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e92b5-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e92b5-142">-Confirm</span></span>
<span data-ttu-id="e92b5-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e92b5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e92b5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e92b5-144">-WhatIf</span></span>
<span data-ttu-id="e92b5-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e92b5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e92b5-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e92b5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e92b5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92b5-147">CommonParameters</span></span>
<span data-ttu-id="e92b5-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e92b5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92b5-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e92b5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92b5-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="e92b5-150">INPUTS</span></span>

### <span data-ttu-id="e92b5-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e92b5-151">System.String</span></span>

### <span data-ttu-id="e92b5-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e92b5-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="e92b5-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e92b5-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e92b5-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="e92b5-154">OUTPUTS</span></span>

### <span data-ttu-id="e92b5-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e92b5-155">System.Boolean</span></span>

## <span data-ttu-id="e92b5-156">Notas</span><span class="sxs-lookup"><span data-stu-id="e92b5-156">NOTES</span></span>

## <span data-ttu-id="e92b5-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e92b5-157">RELATED LINKS</span></span>
