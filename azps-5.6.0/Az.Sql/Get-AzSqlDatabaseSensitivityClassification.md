---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 32459ad76bb118e97ba29e1730c6006a69b4a3b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901418"
---
# <span data-ttu-id="c8f4e-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="c8f4e-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="c8f4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f4e-103">Obtém os tipos de informações atuais e rótulos de sensibilidade de colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="c8f4e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8f4e-104">SYNTAX</span></span>

### <span data-ttu-id="c8f4e-105">DatabaseObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8f4e-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8f4e-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f4e-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8f4e-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f4e-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8f4e-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f4e-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8f4e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8f4e-109">DESCRIPTION</span></span>
<span data-ttu-id="c8f4e-110">O Get-AzSqlDatabaseSensitivityClassification cmdlet retorna os tipos de informações atuais e os rótulos de sensibilidade das colunas no banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="c8f4e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8f4e-111">EXAMPLES</span></span>

### <span data-ttu-id="c8f4e-112">Exemplo 1: Obter tipos de informações atuais e rótulos de sensibilidade de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="c8f4e-113">Exemplo 2: Obter tipos de informações atuais e rótulos de sensibilidade de um banco de dados do Azure SQL com piping.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="c8f4e-114">Exemplo 3: obter o tipo de informação atual e o rótulo de sensibilidade de uma coluna específica de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="c8f4e-115">Exemplo 4: obter o tipo de informação atual e o rótulo de sensibilidade de uma coluna específica de um banco de dados do Azure SQL usando Piping.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="c8f4e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8f4e-116">PARAMETERS</span></span>

### <span data-ttu-id="c8f4e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8f4e-117">-AsJob</span></span>
<span data-ttu-id="c8f4e-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c8f4e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8f4e-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-119">-ColumnName</span></span>
<span data-ttu-id="c8f4e-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-120">Name of column.</span></span>

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

### <span data-ttu-id="c8f4e-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-121">-DatabaseName</span></span>
<span data-ttu-id="c8f4e-122">O nome do banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="c8f4e-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c8f4e-123">-DatabaseObject</span></span>
<span data-ttu-id="c8f4e-124">O objeto SQL banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-124">The SQL database object.</span></span>

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

### <span data-ttu-id="c8f4e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f4e-125">-DefaultProfile</span></span>
<span data-ttu-id="c8f4e-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f4e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-127">-ResourceGroupName</span></span>
<span data-ttu-id="c8f4e-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8f4e-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-129">-SchemaName</span></span>
<span data-ttu-id="c8f4e-130">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-130">Name of schema.</span></span>

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

### <span data-ttu-id="c8f4e-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-131">-ServerName</span></span>
<span data-ttu-id="c8f4e-132">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-132">SQL server name.</span></span>

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

### <span data-ttu-id="c8f4e-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="c8f4e-133">-TableName</span></span>
<span data-ttu-id="c8f4e-134">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-134">Name of table.</span></span>

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

### <span data-ttu-id="c8f4e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f4e-135">CommonParameters</span></span>
<span data-ttu-id="c8f4e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f4e-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8f4e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f4e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8f4e-138">INPUTS</span></span>

### <span data-ttu-id="c8f4e-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c8f4e-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c8f4e-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8f4e-140">OUTPUTS</span></span>

### <span data-ttu-id="c8f4e-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="c8f4e-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c8f4e-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8f4e-142">NOTES</span></span>

## <span data-ttu-id="c8f4e-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8f4e-143">RELATED LINKS</span></span>

[<span data-ttu-id="c8f4e-144">Saiba mais sobre a descoberta e classificação de dados SQL banco de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="c8f4e-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
