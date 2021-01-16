---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272342"
---
# <span data-ttu-id="af7e6-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="af7e6-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="af7e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="af7e6-103">Remove os tipos de informações e os rótulos de sensibilidade de colunas no pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="af7e6-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="af7e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af7e6-104">SYNTAX</span></span>

### <span data-ttu-id="af7e6-105">ClassificationObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="af7e6-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af7e6-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7e6-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af7e6-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="af7e6-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af7e6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af7e6-108">DESCRIPTION</span></span>
<span data-ttu-id="af7e6-109">O cmdlet Remove-AzSynapseSqlPoolSensitivityClassification remove os tipos de informações e rótulos de sensibilidade de colunas no pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="af7e6-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="af7e6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af7e6-110">EXAMPLES</span></span>

### <span data-ttu-id="af7e6-111">Exemplo 1: remover tipo de informação e rótulo de sensibilidade de uma coluna em um pool do SQL do Synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="af7e6-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="af7e6-112">Exemplo 2: remover tipos de informações atuais e rótulos de sensibilidade de colunas em um pool do SQL Synapse do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="af7e6-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="af7e6-113">Exemplo 3: remover tipo de informação e rótulo de sensibilidade de uma coluna em um pool do SQL Synapse do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="af7e6-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="af7e6-114">OS</span><span class="sxs-lookup"><span data-stu-id="af7e6-114">PARAMETERS</span></span>

### <span data-ttu-id="af7e6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af7e6-115">-AsJob</span></span>
<span data-ttu-id="af7e6-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="af7e6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af7e6-117">-Classificationobject</span><span class="sxs-lookup"><span data-stu-id="af7e6-117">-ClassificationObject</span></span>
<span data-ttu-id="af7e6-118">Um objeto que representa uma classificação de sensibilidade de pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="af7e6-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="af7e6-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="af7e6-119">-ColumnName</span></span>
<span data-ttu-id="af7e6-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="af7e6-120">Name of column.</span></span>

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

### <span data-ttu-id="af7e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7e6-121">-DefaultProfile</span></span>
<span data-ttu-id="af7e6-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af7e6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af7e6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af7e6-123">-PassThru</span></span>
<span data-ttu-id="af7e6-124">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="af7e6-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="af7e6-125">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="af7e6-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="af7e6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7e6-126">-ResourceGroupName</span></span>
<span data-ttu-id="af7e6-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af7e6-127">Resource group name.</span></span>

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

### <span data-ttu-id="af7e6-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="af7e6-128">-SchemaName</span></span>
<span data-ttu-id="af7e6-129">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="af7e6-129">Name of schema.</span></span>

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

### <span data-ttu-id="af7e6-130">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="af7e6-130">-SqlPoolName</span></span>
<span data-ttu-id="af7e6-131">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="af7e6-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="af7e6-132">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="af7e6-132">-SqlPoolObject</span></span>
<span data-ttu-id="af7e6-133">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="af7e6-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="af7e6-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="af7e6-134">-TableName</span></span>
<span data-ttu-id="af7e6-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="af7e6-135">Name of table.</span></span>

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

### <span data-ttu-id="af7e6-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af7e6-136">-WorkspaceName</span></span>
<span data-ttu-id="af7e6-137">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="af7e6-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="af7e6-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af7e6-138">-Confirm</span></span>
<span data-ttu-id="af7e6-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af7e6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af7e6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af7e6-140">-WhatIf</span></span>
<span data-ttu-id="af7e6-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af7e6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af7e6-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af7e6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af7e6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7e6-143">CommonParameters</span></span>
<span data-ttu-id="af7e6-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af7e6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7e6-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af7e6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7e6-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af7e6-146">INPUTS</span></span>

### <span data-ttu-id="af7e6-147">Microsoft. Azure. Commands. Synapse. Models. dataclassation. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="af7e6-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="af7e6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="af7e6-148">System.String</span></span>

### <span data-ttu-id="af7e6-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="af7e6-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="af7e6-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af7e6-150">OUTPUTS</span></span>

### <span data-ttu-id="af7e6-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af7e6-151">System.Boolean</span></span>

## <span data-ttu-id="af7e6-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af7e6-152">NOTES</span></span>

## <span data-ttu-id="af7e6-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af7e6-153">RELATED LINKS</span></span>
