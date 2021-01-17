---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427623"
---
# <span data-ttu-id="5094a-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="5094a-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="5094a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5094a-102">SYNOPSIS</span></span>
<span data-ttu-id="5094a-103">Desabilita as recomendações de sensibilidade (ignoradas) nas colunas no pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="5094a-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="5094a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5094a-104">SYNTAX</span></span>

### <span data-ttu-id="5094a-105">InputObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5094a-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5094a-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5094a-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5094a-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="5094a-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5094a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5094a-108">DESCRIPTION</span></span>
<span data-ttu-id="5094a-109">O cmdlet Disable-AzSynapseSqlPoolSensitivityRecommendation desabilita (ignora) as recomendações de sensibilidade em colunas no pool SQL.</span><span class="sxs-lookup"><span data-stu-id="5094a-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="5094a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5094a-110">EXAMPLES</span></span>

### <span data-ttu-id="5094a-111">Exemplo 1: desabilitar recomendações de sensibilidade em uma determinada coluna em um pool do SQL do Synapse do Azure.</span><span class="sxs-lookup"><span data-stu-id="5094a-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="5094a-112">Exemplo 2: Desabilite as recomendações de sensibilidade em colunas com recomendações de sensibilidade em um pool do SQL Synapse do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="5094a-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="5094a-113">Exemplo 3: Desabilite as recomendações de sensibilidade em uma determinada coluna em um pool do SQL Synapse do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="5094a-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="5094a-114">OS</span><span class="sxs-lookup"><span data-stu-id="5094a-114">PARAMETERS</span></span>

### <span data-ttu-id="5094a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5094a-115">-AsJob</span></span>
<span data-ttu-id="5094a-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5094a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5094a-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="5094a-117">-ColumnName</span></span>
<span data-ttu-id="5094a-118">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="5094a-118">Name of column.</span></span>

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

### <span data-ttu-id="5094a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5094a-119">-DefaultProfile</span></span>
<span data-ttu-id="5094a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5094a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5094a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5094a-121">-InputObject</span></span>
<span data-ttu-id="5094a-122">Um objeto que representa uma classificação de sensibilidade de pool do SQL.</span><span class="sxs-lookup"><span data-stu-id="5094a-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="5094a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5094a-123">-PassThru</span></span>
<span data-ttu-id="5094a-124">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="5094a-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5094a-125">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5094a-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5094a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5094a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5094a-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5094a-127">Resource group name.</span></span>

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

### <span data-ttu-id="5094a-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="5094a-128">-SchemaName</span></span>
<span data-ttu-id="5094a-129">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="5094a-129">Name of schema.</span></span>

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

### <span data-ttu-id="5094a-130">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="5094a-130">-SqlPoolName</span></span>
<span data-ttu-id="5094a-131">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5094a-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5094a-132">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="5094a-132">-SqlPoolObject</span></span>
<span data-ttu-id="5094a-133">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5094a-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5094a-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="5094a-134">-TableName</span></span>
<span data-ttu-id="5094a-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="5094a-135">Name of table.</span></span>

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

### <span data-ttu-id="5094a-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5094a-136">-WorkspaceName</span></span>
<span data-ttu-id="5094a-137">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="5094a-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5094a-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5094a-138">-Confirm</span></span>
<span data-ttu-id="5094a-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5094a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5094a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5094a-140">-WhatIf</span></span>
<span data-ttu-id="5094a-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5094a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5094a-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5094a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5094a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5094a-143">CommonParameters</span></span>
<span data-ttu-id="5094a-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5094a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5094a-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5094a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5094a-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5094a-146">INPUTS</span></span>

### <span data-ttu-id="5094a-147">Microsoft. Azure. Commands. Synapse. Models. dataclassation. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5094a-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="5094a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5094a-148">System.String</span></span>

### <span data-ttu-id="5094a-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5094a-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5094a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5094a-150">OUTPUTS</span></span>

### <span data-ttu-id="5094a-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5094a-151">System.Boolean</span></span>

## <span data-ttu-id="5094a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5094a-152">NOTES</span></span>

## <span data-ttu-id="5094a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5094a-153">RELATED LINKS</span></span>
