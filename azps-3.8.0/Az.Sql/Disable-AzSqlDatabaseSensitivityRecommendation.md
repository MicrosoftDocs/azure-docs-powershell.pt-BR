---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778045"
---
# <span data-ttu-id="bd589-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="bd589-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="bd589-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd589-102">SYNOPSIS</span></span>
<span data-ttu-id="bd589-103">Desabilita as recomendações de sensibilidade (ignoradas) nas colunas do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd589-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="bd589-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd589-104">SYNTAX</span></span>

### <span data-ttu-id="bd589-105">InputObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bd589-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd589-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd589-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd589-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd589-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd589-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd589-108">DESCRIPTION</span></span>
<span data-ttu-id="bd589-109">O cmdlet Disable-AzSqlDatabaseSensitivityRecommendation desabilita (ignora) as recomendações de sensibilidade em colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd589-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="bd589-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd589-110">EXAMPLES</span></span>

### <span data-ttu-id="bd589-111">Exemplo 1: Desabilite as recomendações de sensibilidade em uma determinada coluna em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd589-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="bd589-112">Exemplo 2: Desabilite as recomendações de sensibilidade em colunas com recomendações de sensibilidade em um banco de dados SQL do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="bd589-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="bd589-113">Exemplo 3: Desabilite as recomendações de sensibilidade em uma determinada coluna em um banco de dados SQL do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="bd589-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="bd589-114">OS</span><span class="sxs-lookup"><span data-stu-id="bd589-114">PARAMETERS</span></span>

### <span data-ttu-id="bd589-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd589-115">-AsJob</span></span>
<span data-ttu-id="bd589-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bd589-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd589-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="bd589-117">-ColumnName</span></span>
<span data-ttu-id="bd589-118">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="bd589-118">Name of column.</span></span>

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

### <span data-ttu-id="bd589-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd589-119">-DatabaseName</span></span>
<span data-ttu-id="bd589-120">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd589-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="bd589-121">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="bd589-121">-DatabaseObject</span></span>
<span data-ttu-id="bd589-122">O objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="bd589-122">The SQL database object.</span></span>

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

### <span data-ttu-id="bd589-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd589-123">-DefaultProfile</span></span>
<span data-ttu-id="bd589-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd589-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd589-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd589-125">-InputObject</span></span>
<span data-ttu-id="bd589-126">Um objeto que representa uma classificação de sensibilidade de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="bd589-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="bd589-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd589-127">-PassThru</span></span>
<span data-ttu-id="bd589-128">Especifica se o modelo de classificação de sensibilidade deve ser impresso no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="bd589-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="bd589-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd589-129">-ResourceGroupName</span></span>
<span data-ttu-id="bd589-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd589-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd589-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bd589-131">-SchemaName</span></span>
<span data-ttu-id="bd589-132">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="bd589-132">Name of schema.</span></span>

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

### <span data-ttu-id="bd589-133">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bd589-133">-ServerName</span></span>
<span data-ttu-id="bd589-134">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bd589-134">SQL server name.</span></span>

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

### <span data-ttu-id="bd589-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="bd589-135">-TableName</span></span>
<span data-ttu-id="bd589-136">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="bd589-136">Name of table.</span></span>

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

### <span data-ttu-id="bd589-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd589-137">-Confirm</span></span>
<span data-ttu-id="bd589-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd589-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd589-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd589-139">-WhatIf</span></span>
<span data-ttu-id="bd589-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd589-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd589-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd589-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd589-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd589-142">CommonParameters</span></span>
<span data-ttu-id="bd589-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd589-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd589-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd589-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd589-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd589-145">INPUTS</span></span>

### <span data-ttu-id="bd589-146">Microsoft. Azure. Commands. Sql. dataclassation. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="bd589-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="bd589-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd589-147">OUTPUTS</span></span>

### <span data-ttu-id="bd589-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd589-148">System.Boolean</span></span>

## <span data-ttu-id="bd589-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd589-149">NOTES</span></span>

## <span data-ttu-id="bd589-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd589-150">RELATED LINKS</span></span>

[<span data-ttu-id="bd589-151">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="bd589-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)