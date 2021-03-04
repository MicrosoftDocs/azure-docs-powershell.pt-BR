---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 40d1fe07db7720bfb9fdad061ac3d57298d86a8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888630"
---
# <span data-ttu-id="5233b-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="5233b-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="5233b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5233b-102">SYNOPSIS</span></span>
<span data-ttu-id="5233b-103">Habilita recomendações de sensibilidade em colunas (as recomendações são habilitadas por padrão em todas as colunas) no pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="5233b-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="5233b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5233b-104">SYNTAX</span></span>

### <span data-ttu-id="5233b-105">InputObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5233b-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5233b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5233b-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5233b-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5233b-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5233b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5233b-108">DESCRIPTION</span></span>
<span data-ttu-id="5233b-109">O Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet permite recomendações de sensibilidade em colunas no pool de SQL.</span><span class="sxs-lookup"><span data-stu-id="5233b-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="5233b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5233b-110">EXAMPLES</span></span>

### <span data-ttu-id="5233b-111">Exemplo 1: Habilitar recomendações de sensibilidade em uma determinada coluna em um pool do Azure Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="5233b-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="5233b-112">Exemplo 2: Habilitar recomendações de sensibilidade em uma determinada coluna do Azure Synapse SQL pool usando Piping.</span><span class="sxs-lookup"><span data-stu-id="5233b-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="5233b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5233b-113">PARAMETERS</span></span>

### <span data-ttu-id="5233b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5233b-114">-AsJob</span></span>
<span data-ttu-id="5233b-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5233b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5233b-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5233b-116">-ColumnName</span></span>
<span data-ttu-id="5233b-117">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="5233b-117">Name of column.</span></span>

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

### <span data-ttu-id="5233b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5233b-118">-DefaultProfile</span></span>
<span data-ttu-id="5233b-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5233b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5233b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5233b-120">-InputObject</span></span>
<span data-ttu-id="5233b-121">Um objeto que representa SQL Classificação de Sensibilidade do Pool.</span><span class="sxs-lookup"><span data-stu-id="5233b-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="5233b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5233b-122">-PassThru</span></span>
<span data-ttu-id="5233b-123">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="5233b-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5233b-124">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="5233b-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5233b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5233b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5233b-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5233b-126">Resource group name.</span></span>

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

### <span data-ttu-id="5233b-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5233b-127">-SchemaName</span></span>
<span data-ttu-id="5233b-128">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="5233b-128">Name of schema.</span></span>

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

### <span data-ttu-id="5233b-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="5233b-129">-SqlPoolName</span></span>
<span data-ttu-id="5233b-130">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5233b-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5233b-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="5233b-131">-SqlPoolObject</span></span>
<span data-ttu-id="5233b-132">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5233b-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5233b-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="5233b-133">-TableName</span></span>
<span data-ttu-id="5233b-134">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="5233b-134">Name of table.</span></span>

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

### <span data-ttu-id="5233b-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5233b-135">-WorkspaceName</span></span>
<span data-ttu-id="5233b-136">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="5233b-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5233b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5233b-137">-Confirm</span></span>
<span data-ttu-id="5233b-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5233b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5233b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5233b-139">-WhatIf</span></span>
<span data-ttu-id="5233b-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5233b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5233b-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5233b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5233b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5233b-142">CommonParameters</span></span>
<span data-ttu-id="5233b-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5233b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5233b-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5233b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5233b-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5233b-145">INPUTS</span></span>

### <span data-ttu-id="5233b-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5233b-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="5233b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5233b-147">System.String</span></span>

### <span data-ttu-id="5233b-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5233b-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5233b-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5233b-149">OUTPUTS</span></span>

### <span data-ttu-id="5233b-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5233b-150">System.Boolean</span></span>

## <span data-ttu-id="5233b-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="5233b-151">NOTES</span></span>

## <span data-ttu-id="5233b-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5233b-152">RELATED LINKS</span></span>
