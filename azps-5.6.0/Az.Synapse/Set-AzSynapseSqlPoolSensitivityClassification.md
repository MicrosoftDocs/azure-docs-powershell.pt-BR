---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 2eec7ea6f89bea726cdbee483162ec455e5722aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890537"
---
# <span data-ttu-id="6aa25-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="6aa25-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="6aa25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa25-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa25-103">Define os tipos de informações e os rótulos de sensibilidade das colunas no pool SQL.</span><span class="sxs-lookup"><span data-stu-id="6aa25-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="6aa25-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6aa25-104">SYNTAX</span></span>

### <span data-ttu-id="6aa25-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6aa25-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aa25-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aa25-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aa25-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="6aa25-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aa25-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6aa25-108">DESCRIPTION</span></span>
<span data-ttu-id="6aa25-109">O Set-AzSynapseSqlPoolSensitivityClassification cmdlet define os tipos de informações e os rótulos de sensibilidade das colunas no pool SQL.</span><span class="sxs-lookup"><span data-stu-id="6aa25-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="6aa25-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6aa25-110">EXAMPLES</span></span>

### <span data-ttu-id="6aa25-111">Exemplo 1: definir o tipo de informação e o rótulo de sensibilidade de uma coluna em um pool SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="6aa25-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="6aa25-112">Exemplo 2: Definir tipos de informações recomendados e rótulos de sensibilidade de colunas em um pool SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="6aa25-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="6aa25-113">Exemplo 3: definir o tipo de informação e o rótulo de sensibilidade de uma coluna em um pool do Azure Synapse SQL, usando a canalização.</span><span class="sxs-lookup"><span data-stu-id="6aa25-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="6aa25-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6aa25-114">PARAMETERS</span></span>

### <span data-ttu-id="6aa25-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aa25-115">-AsJob</span></span>
<span data-ttu-id="6aa25-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6aa25-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6aa25-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="6aa25-117">-ClassificationObject</span></span>
<span data-ttu-id="6aa25-118">Um objeto que representa SQL Classificação de Sensibilidade do Pool.</span><span class="sxs-lookup"><span data-stu-id="6aa25-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="6aa25-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="6aa25-119">-ColumnName</span></span>
<span data-ttu-id="6aa25-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="6aa25-120">Name of column.</span></span>

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

### <span data-ttu-id="6aa25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa25-121">-DefaultProfile</span></span>
<span data-ttu-id="6aa25-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa25-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa25-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="6aa25-123">-InformationType</span></span>
<span data-ttu-id="6aa25-124">Um nome que descreve o tipo de informação dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="6aa25-124">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="6aa25-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aa25-125">-PassThru</span></span>
<span data-ttu-id="6aa25-126">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="6aa25-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6aa25-127">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="6aa25-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6aa25-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa25-128">-ResourceGroupName</span></span>
<span data-ttu-id="6aa25-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6aa25-129">Resource group name.</span></span>

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

### <span data-ttu-id="6aa25-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="6aa25-130">-SchemaName</span></span>
<span data-ttu-id="6aa25-131">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="6aa25-131">Name of schema.</span></span>

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

### <span data-ttu-id="6aa25-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="6aa25-132">-SensitivityLabel</span></span>
<span data-ttu-id="6aa25-133">Um nome que descreve a sensibilidade dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="6aa25-133">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="6aa25-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="6aa25-134">-SqlPoolName</span></span>
<span data-ttu-id="6aa25-135">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6aa25-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6aa25-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="6aa25-136">-SqlPoolObject</span></span>
<span data-ttu-id="6aa25-137">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6aa25-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6aa25-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="6aa25-138">-TableName</span></span>
<span data-ttu-id="6aa25-139">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="6aa25-139">Name of table.</span></span>

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

### <span data-ttu-id="6aa25-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6aa25-140">-WorkspaceName</span></span>
<span data-ttu-id="6aa25-141">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="6aa25-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6aa25-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aa25-142">-Confirm</span></span>
<span data-ttu-id="6aa25-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa25-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa25-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa25-144">-WhatIf</span></span>
<span data-ttu-id="6aa25-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6aa25-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aa25-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6aa25-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa25-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa25-147">CommonParameters</span></span>
<span data-ttu-id="6aa25-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa25-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa25-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aa25-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa25-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6aa25-150">INPUTS</span></span>

### <span data-ttu-id="6aa25-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6aa25-151">System.String</span></span>

### <span data-ttu-id="6aa25-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="6aa25-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="6aa25-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6aa25-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6aa25-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6aa25-154">OUTPUTS</span></span>

### <span data-ttu-id="6aa25-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6aa25-155">System.Boolean</span></span>

## <span data-ttu-id="6aa25-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="6aa25-156">NOTES</span></span>

## <span data-ttu-id="6aa25-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6aa25-157">RELATED LINKS</span></span>
