---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778026"
---
# <span data-ttu-id="388e1-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="388e1-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="388e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="388e1-102">SYNOPSIS</span></span>
<span data-ttu-id="388e1-103">Define os tipos de informações e rótulos de sensibilidade de colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="388e1-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="388e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="388e1-104">SYNTAX</span></span>

### <span data-ttu-id="388e1-105">ClassificationObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="388e1-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="388e1-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="388e1-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="388e1-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="388e1-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="388e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="388e1-108">DESCRIPTION</span></span>
<span data-ttu-id="388e1-109">O cmdlet Set-AzSqlDatabaseSensitivityClassification define os tipos de informações e rótulos de sensibilidade de colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="388e1-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="388e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="388e1-110">EXAMPLES</span></span>

### <span data-ttu-id="388e1-111">Exemplo 1: definir tipo de informação e rótulo de sensibilidade de uma coluna em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="388e1-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="388e1-112">Exemplo 2: definir tipos de informações recomendadas e rótulos de sensibilidade de colunas em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="388e1-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="388e1-113">Exemplo 3: definir tipo de informação e rótulo de sensibilidade de uma coluna em um banco de dados SQL do Azure, usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="388e1-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="388e1-114">OS</span><span class="sxs-lookup"><span data-stu-id="388e1-114">PARAMETERS</span></span>

### <span data-ttu-id="388e1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="388e1-115">-AsJob</span></span>
<span data-ttu-id="388e1-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="388e1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="388e1-117">-Classificationobject</span><span class="sxs-lookup"><span data-stu-id="388e1-117">-ClassificationObject</span></span>
<span data-ttu-id="388e1-118">Um objeto que representa uma classificação de sensibilidade de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="388e1-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="388e1-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="388e1-119">-ColumnName</span></span>
<span data-ttu-id="388e1-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="388e1-120">Name of column.</span></span>

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

### <span data-ttu-id="388e1-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="388e1-121">-DatabaseName</span></span>
<span data-ttu-id="388e1-122">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="388e1-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="388e1-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="388e1-123">-DatabaseObject</span></span>
<span data-ttu-id="388e1-124">O objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="388e1-124">The SQL database object.</span></span>

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

### <span data-ttu-id="388e1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388e1-125">-DefaultProfile</span></span>
<span data-ttu-id="388e1-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="388e1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="388e1-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="388e1-127">-InformationType</span></span>
<span data-ttu-id="388e1-128">Um nome que descreve o tipo de informação dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="388e1-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388e1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="388e1-129">-PassThru</span></span>
<span data-ttu-id="388e1-130">Especifica se o modelo de classificação de sensibilidade deve ser impresso no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="388e1-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="388e1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="388e1-131">-ResourceGroupName</span></span>
<span data-ttu-id="388e1-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="388e1-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="388e1-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="388e1-133">-SchemaName</span></span>
<span data-ttu-id="388e1-134">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="388e1-134">Name of schema.</span></span>

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

### <span data-ttu-id="388e1-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="388e1-135">-SensitivityLabel</span></span>
<span data-ttu-id="388e1-136">Um nome que descreve a sensibilidade dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="388e1-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388e1-137">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="388e1-137">-ServerName</span></span>
<span data-ttu-id="388e1-138">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="388e1-138">SQL server name.</span></span>

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

### <span data-ttu-id="388e1-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="388e1-139">-TableName</span></span>
<span data-ttu-id="388e1-140">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="388e1-140">Name of table.</span></span>

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

### <span data-ttu-id="388e1-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="388e1-141">-Confirm</span></span>
<span data-ttu-id="388e1-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="388e1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388e1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388e1-143">-WhatIf</span></span>
<span data-ttu-id="388e1-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="388e1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="388e1-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="388e1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388e1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388e1-146">CommonParameters</span></span>
<span data-ttu-id="388e1-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="388e1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388e1-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="388e1-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388e1-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="388e1-149">INPUTS</span></span>

### <span data-ttu-id="388e1-150">Microsoft. Azure. Commands. Sql. dataclassation. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="388e1-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="388e1-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="388e1-151">OUTPUTS</span></span>

### <span data-ttu-id="388e1-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="388e1-152">System.Boolean</span></span>

## <span data-ttu-id="388e1-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="388e1-153">NOTES</span></span>

## <span data-ttu-id="388e1-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="388e1-154">RELATED LINKS</span></span>

[<span data-ttu-id="388e1-155">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="388e1-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
