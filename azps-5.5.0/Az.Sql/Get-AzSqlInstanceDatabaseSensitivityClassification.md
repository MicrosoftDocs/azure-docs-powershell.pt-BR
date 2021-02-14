---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fe8cffb4ab9d79828795cc1148a3c109cfbfdddb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115761"
---
# <span data-ttu-id="46d5c-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="46d5c-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="46d5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="46d5c-103">Obtém os tipos de informações atuais e rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="46d5c-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="46d5c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46d5c-104">SYNTAX</span></span>

### <span data-ttu-id="46d5c-105">DatabaseObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46d5c-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46d5c-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="46d5c-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46d5c-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="46d5c-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46d5c-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="46d5c-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46d5c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="46d5c-109">DESCRIPTION</span></span>
<span data-ttu-id="46d5c-110">O Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet retorna os tipos de informações atuais e rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="46d5c-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="46d5c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46d5c-111">EXAMPLES</span></span>

### <span data-ttu-id="46d5c-112">Exemplo 1: Obter tipos de informações atuais e rótulos de sensibilidade de um banco de dados de instância gerenciado pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="46d5c-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="46d5c-113">Exemplo 2: Obter tipos de informações atuais e rótulos de sensibilidade de um banco de dados de Instância gerenciado pelo SQL do Azure com a Piping.</span><span class="sxs-lookup"><span data-stu-id="46d5c-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="46d5c-114">Exemplo 3: Obter o tipo de informação atual e o rótulo de sensibilidade de uma coluna específica de um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="46d5c-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="46d5c-115">Exemplo 4: Obter o tipo de informações atuais e o rótulo de sensibilidade de uma coluna específica de um banco de dados de instância gerenciada do Azure SQL usando o Piping.</span><span class="sxs-lookup"><span data-stu-id="46d5c-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="46d5c-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46d5c-116">PARAMETERS</span></span>

### <span data-ttu-id="46d5c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46d5c-117">-AsJob</span></span>
<span data-ttu-id="46d5c-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="46d5c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46d5c-119">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="46d5c-119">-ColumnName</span></span>
<span data-ttu-id="46d5c-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="46d5c-120">Name of column.</span></span>

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

### <span data-ttu-id="46d5c-121">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="46d5c-121">-DatabaseName</span></span>
<span data-ttu-id="46d5c-122">O nome do banco de dados de instância gerenciada do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="46d5c-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="46d5c-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="46d5c-123">-DatabaseObject</span></span>
<span data-ttu-id="46d5c-124">O objeto de banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="46d5c-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d5c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d5c-125">-DefaultProfile</span></span>
<span data-ttu-id="46d5c-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46d5c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d5c-127">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="46d5c-127">-InstanceName</span></span>
<span data-ttu-id="46d5c-128">Nome da instância gerenciada pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="46d5c-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="46d5c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d5c-129">-ResourceGroupName</span></span>
<span data-ttu-id="46d5c-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46d5c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="46d5c-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="46d5c-131">-SchemaName</span></span>
<span data-ttu-id="46d5c-132">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="46d5c-132">Name of schema.</span></span>

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

### <span data-ttu-id="46d5c-133">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="46d5c-133">-TableName</span></span>
<span data-ttu-id="46d5c-134">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="46d5c-134">Name of table.</span></span>

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

### <span data-ttu-id="46d5c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d5c-135">CommonParameters</span></span>
<span data-ttu-id="46d5c-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d5c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d5c-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46d5c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d5c-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="46d5c-138">INPUTS</span></span>

### <span data-ttu-id="46d5c-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="46d5c-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="46d5c-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="46d5c-140">OUTPUTS</span></span>

### <span data-ttu-id="46d5c-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="46d5c-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="46d5c-142">Notas</span><span class="sxs-lookup"><span data-stu-id="46d5c-142">NOTES</span></span>

## <span data-ttu-id="46d5c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46d5c-143">RELATED LINKS</span></span>

[<span data-ttu-id="46d5c-144">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="46d5c-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
