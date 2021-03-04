---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 58ef691f5f109f301ffae2636d739405000754ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886382"
---
# <span data-ttu-id="e594e-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="e594e-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="e594e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e594e-102">SYNOPSIS</span></span>
<span data-ttu-id="e594e-103">Remove os tipos de informações e os rótulos de sensibilidade das colunas no pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="e594e-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e594e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e594e-104">SYNTAX</span></span>

### <span data-ttu-id="e594e-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e594e-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e594e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e594e-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e594e-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e594e-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e594e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e594e-108">DESCRIPTION</span></span>
<span data-ttu-id="e594e-109">O Remove-AzSynapseSqlPoolSensitivityClassification cmdlet remove os tipos de informações e os rótulos de sensibilidade das colunas no pool SQL.</span><span class="sxs-lookup"><span data-stu-id="e594e-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e594e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e594e-110">EXAMPLES</span></span>

### <span data-ttu-id="e594e-111">Exemplo 1: Remover o tipo de informação e o rótulo de sensibilidade de uma coluna em um pool do Azure Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="e594e-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="e594e-112">Exemplo 2: Remover tipos de informações atuais e rótulos de sensibilidade de colunas em um pool SQL Azure Synapse usando Piping.</span><span class="sxs-lookup"><span data-stu-id="e594e-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="e594e-113">Exemplo 3: Remover o tipo de informação e o rótulo de sensibilidade de uma coluna em um pool SQL Azure Synapse usando Piping.</span><span class="sxs-lookup"><span data-stu-id="e594e-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="e594e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e594e-114">PARAMETERS</span></span>

### <span data-ttu-id="e594e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e594e-115">-AsJob</span></span>
<span data-ttu-id="e594e-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e594e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e594e-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="e594e-117">-ClassificationObject</span></span>
<span data-ttu-id="e594e-118">Um objeto que representa SQL Classificação de Sensibilidade do Pool.</span><span class="sxs-lookup"><span data-stu-id="e594e-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="e594e-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e594e-119">-ColumnName</span></span>
<span data-ttu-id="e594e-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="e594e-120">Name of column.</span></span>

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

### <span data-ttu-id="e594e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e594e-121">-DefaultProfile</span></span>
<span data-ttu-id="e594e-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e594e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e594e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e594e-123">-PassThru</span></span>
<span data-ttu-id="e594e-124">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e594e-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e594e-125">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="e594e-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e594e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e594e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e594e-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e594e-127">Resource group name.</span></span>

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

### <span data-ttu-id="e594e-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e594e-128">-SchemaName</span></span>
<span data-ttu-id="e594e-129">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="e594e-129">Name of schema.</span></span>

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

### <span data-ttu-id="e594e-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e594e-130">-SqlPoolName</span></span>
<span data-ttu-id="e594e-131">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e594e-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e594e-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e594e-132">-SqlPoolObject</span></span>
<span data-ttu-id="e594e-133">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="e594e-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e594e-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="e594e-134">-TableName</span></span>
<span data-ttu-id="e594e-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="e594e-135">Name of table.</span></span>

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

### <span data-ttu-id="e594e-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e594e-136">-WorkspaceName</span></span>
<span data-ttu-id="e594e-137">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="e594e-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e594e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e594e-138">-Confirm</span></span>
<span data-ttu-id="e594e-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e594e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e594e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e594e-140">-WhatIf</span></span>
<span data-ttu-id="e594e-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e594e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e594e-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e594e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e594e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e594e-143">CommonParameters</span></span>
<span data-ttu-id="e594e-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e594e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e594e-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e594e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e594e-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e594e-146">INPUTS</span></span>

### <span data-ttu-id="e594e-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e594e-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="e594e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e594e-148">System.String</span></span>

### <span data-ttu-id="e594e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e594e-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e594e-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e594e-150">OUTPUTS</span></span>

### <span data-ttu-id="e594e-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e594e-151">System.Boolean</span></span>

## <span data-ttu-id="e594e-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="e594e-152">NOTES</span></span>

## <span data-ttu-id="e594e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e594e-153">RELATED LINKS</span></span>
