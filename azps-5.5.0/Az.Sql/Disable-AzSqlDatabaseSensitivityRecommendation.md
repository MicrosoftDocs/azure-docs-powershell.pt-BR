---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115772"
---
# <span data-ttu-id="7a77e-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7a77e-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="7a77e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a77e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a77e-103">Desabilita (descarta) recomendações de sensibilidade em colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7a77e-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="7a77e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a77e-104">SYNTAX</span></span>

### <span data-ttu-id="7a77e-105">InputObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a77e-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a77e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a77e-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a77e-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a77e-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a77e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a77e-108">DESCRIPTION</span></span>
<span data-ttu-id="7a77e-109">O Disable-AzSqlDatabaseSensitivityRecommendation cmdlet desabilita (descarta) recomendações de sensibilidade em colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7a77e-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="7a77e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a77e-110">EXAMPLES</span></span>

### <span data-ttu-id="7a77e-111">Exemplo 1: Desabilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a77e-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7a77e-112">Exemplo 2: Desabilitar recomendações de sensibilidade em colunas que têm recomendações de sensibilidade em um banco de dados SQL do Azure usando o Piping.</span><span class="sxs-lookup"><span data-stu-id="7a77e-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="7a77e-113">Exemplo 3: Desabilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados SQL do Azure usando o Piping.</span><span class="sxs-lookup"><span data-stu-id="7a77e-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7a77e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a77e-114">PARAMETERS</span></span>

### <span data-ttu-id="7a77e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a77e-115">-AsJob</span></span>
<span data-ttu-id="7a77e-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7a77e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a77e-117">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="7a77e-117">-ColumnName</span></span>
<span data-ttu-id="7a77e-118">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="7a77e-118">Name of column.</span></span>

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

### <span data-ttu-id="7a77e-119">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="7a77e-119">-DatabaseName</span></span>
<span data-ttu-id="7a77e-120">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7a77e-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="7a77e-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7a77e-121">-DatabaseObject</span></span>
<span data-ttu-id="7a77e-122">O objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="7a77e-122">The SQL database object.</span></span>

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

### <span data-ttu-id="7a77e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a77e-123">-DefaultProfile</span></span>
<span data-ttu-id="7a77e-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a77e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a77e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a77e-125">-InputObject</span></span>
<span data-ttu-id="7a77e-126">Um objeto que representa uma Classificação de Sensibilidade do Banco de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="7a77e-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="7a77e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a77e-127">-PassThru</span></span>
<span data-ttu-id="7a77e-128">Especifica se o modelo de classificação de sensibilidade será saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a77e-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="7a77e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a77e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a77e-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7a77e-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a77e-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7a77e-131">-SchemaName</span></span>
<span data-ttu-id="7a77e-132">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="7a77e-132">Name of schema.</span></span>

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

### <span data-ttu-id="7a77e-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a77e-133">-ServerName</span></span>
<span data-ttu-id="7a77e-134">Nome do servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="7a77e-134">SQL server name.</span></span>

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

### <span data-ttu-id="7a77e-135">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="7a77e-135">-TableName</span></span>
<span data-ttu-id="7a77e-136">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="7a77e-136">Name of table.</span></span>

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

### <span data-ttu-id="7a77e-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7a77e-137">-Confirm</span></span>
<span data-ttu-id="7a77e-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a77e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a77e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a77e-139">-WhatIf</span></span>
<span data-ttu-id="7a77e-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7a77e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a77e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a77e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a77e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a77e-142">CommonParameters</span></span>
<span data-ttu-id="7a77e-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a77e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a77e-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a77e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a77e-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="7a77e-145">INPUTS</span></span>

### <span data-ttu-id="7a77e-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7a77e-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="7a77e-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="7a77e-147">OUTPUTS</span></span>

### <span data-ttu-id="7a77e-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a77e-148">System.Boolean</span></span>

## <span data-ttu-id="7a77e-149">Notas</span><span class="sxs-lookup"><span data-stu-id="7a77e-149">NOTES</span></span>

## <span data-ttu-id="7a77e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a77e-150">RELATED LINKS</span></span>

[<span data-ttu-id="7a77e-151">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="7a77e-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)