---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 50bd23f0c0be638683dae4acb5b43165a8c5b4f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599017"
---
# <span data-ttu-id="bd096-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="bd096-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="bd096-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd096-102">SYNOPSIS</span></span>
<span data-ttu-id="bd096-103">Obtém os tipos de informações atuais e os rótulos de sensibilidade de colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd096-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="bd096-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd096-104">SYNTAX</span></span>

### <span data-ttu-id="bd096-105">DatabaseObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bd096-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd096-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd096-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd096-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd096-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd096-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd096-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd096-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd096-109">DESCRIPTION</span></span>
<span data-ttu-id="bd096-110">O cmdlet Get-AzSqlDatabaseSensitivityClassification retorna os tipos de informações atuais e rótulos de sensibilidade de colunas no banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd096-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="bd096-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd096-111">EXAMPLES</span></span>

### <span data-ttu-id="bd096-112">Exemplo 1: obter tipos de informações atuais e rótulos de sensibilidade de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd096-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="bd096-113">Exemplo 2: obter tipos de informações atuais e rótulos de sensibilidade de um banco de dados SQL do Azure com tubulação.</span><span class="sxs-lookup"><span data-stu-id="bd096-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="bd096-114">Exemplo 3: obter tipo de informação atual e rótulo de sensibilidade de uma coluna específica de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd096-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="bd096-115">Exemplo 4: obter tipo de informação atual e rótulo de sensibilidade de uma coluna específica de um banco de dados SQL do Azure usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="bd096-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="bd096-116">OS</span><span class="sxs-lookup"><span data-stu-id="bd096-116">PARAMETERS</span></span>

### <span data-ttu-id="bd096-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd096-117">-AsJob</span></span>
<span data-ttu-id="bd096-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bd096-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd096-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="bd096-119">-ColumnName</span></span>
<span data-ttu-id="bd096-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="bd096-120">Name of column.</span></span>

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

### <span data-ttu-id="bd096-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd096-121">-DatabaseName</span></span>
<span data-ttu-id="bd096-122">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd096-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd096-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="bd096-123">-DatabaseObject</span></span>
<span data-ttu-id="bd096-124">O objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="bd096-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd096-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd096-125">-DefaultProfile</span></span>
<span data-ttu-id="bd096-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd096-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd096-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd096-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd096-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd096-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd096-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="bd096-129">-SchemaName</span></span>
<span data-ttu-id="bd096-130">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="bd096-130">Name of schema.</span></span>

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

### <span data-ttu-id="bd096-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bd096-131">-ServerName</span></span>
<span data-ttu-id="bd096-132">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bd096-132">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd096-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="bd096-133">-TableName</span></span>
<span data-ttu-id="bd096-134">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="bd096-134">Name of table.</span></span>

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

### <span data-ttu-id="bd096-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd096-135">CommonParameters</span></span>
<span data-ttu-id="bd096-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd096-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd096-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd096-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd096-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd096-138">INPUTS</span></span>

### <span data-ttu-id="bd096-139">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bd096-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bd096-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd096-140">OUTPUTS</span></span>

### <span data-ttu-id="bd096-141">Microsoft. Azure. Commands. Sql. dataclassation. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="bd096-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="bd096-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd096-142">NOTES</span></span>

## <span data-ttu-id="bd096-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd096-143">RELATED LINKS</span></span>

[<span data-ttu-id="bd096-144">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="bd096-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
