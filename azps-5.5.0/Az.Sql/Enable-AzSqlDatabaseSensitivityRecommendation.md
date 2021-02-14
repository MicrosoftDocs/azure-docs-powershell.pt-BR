---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110967"
---
# <span data-ttu-id="abfd9-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="abfd9-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="abfd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abfd9-102">SYNOPSIS</span></span>
<span data-ttu-id="abfd9-103">Habilita recomendações de sensibilidade em colunas (as recomendações são habilitadas por padrão em todas as colunas) no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="abfd9-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="abfd9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abfd9-104">SYNTAX</span></span>

### <span data-ttu-id="abfd9-105">InputObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="abfd9-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abfd9-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="abfd9-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abfd9-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="abfd9-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abfd9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="abfd9-108">DESCRIPTION</span></span>
<span data-ttu-id="abfd9-109">O Enable-AzSqlDatabaseSensitivityRecommendation cmdlet permite recomendações de sensibilidade em colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="abfd9-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="abfd9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="abfd9-110">EXAMPLES</span></span>

### <span data-ttu-id="abfd9-111">Exemplo 1: Habilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="abfd9-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="abfd9-112">Exemplo 2: Habilitar recomendações de sensibilidade em um determinado banco de dados SQL de coluna do Azure usando o Piping.</span><span class="sxs-lookup"><span data-stu-id="abfd9-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="abfd9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abfd9-113">PARAMETERS</span></span>

### <span data-ttu-id="abfd9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abfd9-114">-AsJob</span></span>
<span data-ttu-id="abfd9-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="abfd9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abfd9-116">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="abfd9-116">-ColumnName</span></span>
<span data-ttu-id="abfd9-117">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="abfd9-117">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abfd9-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="abfd9-118">-DatabaseName</span></span>
<span data-ttu-id="abfd9-119">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="abfd9-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="abfd9-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="abfd9-120">-DatabaseObject</span></span>
<span data-ttu-id="abfd9-121">O objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="abfd9-121">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abfd9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abfd9-122">-DefaultProfile</span></span>
<span data-ttu-id="abfd9-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abfd9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abfd9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abfd9-124">-InputObject</span></span>
<span data-ttu-id="abfd9-125">Um objeto que representa uma Classificação de Sensibilidade do Banco de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="abfd9-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abfd9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abfd9-126">-PassThru</span></span>
<span data-ttu-id="abfd9-127">Especifica se o modelo de classificação de sensibilidade será saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="abfd9-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="abfd9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abfd9-128">-ResourceGroupName</span></span>
<span data-ttu-id="abfd9-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="abfd9-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="abfd9-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="abfd9-130">-SchemaName</span></span>
<span data-ttu-id="abfd9-131">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="abfd9-131">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abfd9-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="abfd9-132">-ServerName</span></span>
<span data-ttu-id="abfd9-133">Nome do servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="abfd9-133">SQL server name.</span></span>

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

### <span data-ttu-id="abfd9-134">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="abfd9-134">-TableName</span></span>
<span data-ttu-id="abfd9-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="abfd9-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abfd9-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="abfd9-136">-Confirm</span></span>
<span data-ttu-id="abfd9-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abfd9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abfd9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abfd9-138">-WhatIf</span></span>
<span data-ttu-id="abfd9-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="abfd9-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abfd9-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abfd9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abfd9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abfd9-141">CommonParameters</span></span>
<span data-ttu-id="abfd9-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abfd9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abfd9-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abfd9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abfd9-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="abfd9-144">INPUTS</span></span>

### <span data-ttu-id="abfd9-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="abfd9-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="abfd9-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="abfd9-146">OUTPUTS</span></span>

### <span data-ttu-id="abfd9-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="abfd9-147">System.Boolean</span></span>

## <span data-ttu-id="abfd9-148">Notas</span><span class="sxs-lookup"><span data-stu-id="abfd9-148">NOTES</span></span>

## <span data-ttu-id="abfd9-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abfd9-149">RELATED LINKS</span></span>

[<span data-ttu-id="abfd9-150">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="abfd9-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)