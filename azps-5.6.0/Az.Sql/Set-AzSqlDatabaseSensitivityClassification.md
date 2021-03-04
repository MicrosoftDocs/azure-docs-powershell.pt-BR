---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 88e08a15c864386d2e073f83f437d0db537f2ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892029"
---
# <span data-ttu-id="69193-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="69193-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="69193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69193-102">SYNOPSIS</span></span>
<span data-ttu-id="69193-103">Define os tipos de informações e os rótulos de sensibilidade das colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="69193-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="69193-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="69193-104">SYNTAX</span></span>

### <span data-ttu-id="69193-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="69193-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69193-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="69193-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69193-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="69193-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69193-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="69193-108">DESCRIPTION</span></span>
<span data-ttu-id="69193-109">O Set-AzSqlDatabaseSensitivityClassification cmdlet define os tipos de informações e os rótulos de sensibilidade das colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="69193-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="69193-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69193-110">EXAMPLES</span></span>

### <span data-ttu-id="69193-111">Exemplo 1: Definir o tipo de informação e o rótulo de sensibilidade de uma coluna em um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="69193-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="69193-112">Exemplo 2: Definir tipos de informações recomendados e rótulos de sensibilidade de colunas em um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="69193-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="69193-113">Exemplo 3: Definir o tipo de informação e o rótulo de sensibilidade de uma coluna em um banco de dados do Azure SQL, usando a canalização.</span><span class="sxs-lookup"><span data-stu-id="69193-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="69193-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="69193-114">PARAMETERS</span></span>

### <span data-ttu-id="69193-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69193-115">-AsJob</span></span>
<span data-ttu-id="69193-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="69193-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69193-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="69193-117">-ClassificationObject</span></span>
<span data-ttu-id="69193-118">Um objeto que representa uma classificação SQL de Sensibilidade do Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="69193-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="69193-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="69193-119">-ColumnName</span></span>
<span data-ttu-id="69193-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="69193-120">Name of column.</span></span>

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

### <span data-ttu-id="69193-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69193-121">-DatabaseName</span></span>
<span data-ttu-id="69193-122">O nome do banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="69193-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="69193-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="69193-123">-DatabaseObject</span></span>
<span data-ttu-id="69193-124">O objeto SQL banco de dados.</span><span class="sxs-lookup"><span data-stu-id="69193-124">The SQL database object.</span></span>

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

### <span data-ttu-id="69193-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69193-125">-DefaultProfile</span></span>
<span data-ttu-id="69193-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69193-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69193-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="69193-127">-InformationType</span></span>
<span data-ttu-id="69193-128">Um nome que descreve o tipo de informação dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="69193-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="69193-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69193-129">-PassThru</span></span>
<span data-ttu-id="69193-130">Especifica se o modelo de classificação de sensibilidade deve ser produzido no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="69193-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="69193-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69193-131">-ResourceGroupName</span></span>
<span data-ttu-id="69193-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69193-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="69193-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="69193-133">-SchemaName</span></span>
<span data-ttu-id="69193-134">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="69193-134">Name of schema.</span></span>

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

### <span data-ttu-id="69193-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="69193-135">-SensitivityLabel</span></span>
<span data-ttu-id="69193-136">Um nome que descreve a sensibilidade dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="69193-136">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="69193-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69193-137">-ServerName</span></span>
<span data-ttu-id="69193-138">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="69193-138">SQL server name.</span></span>

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

### <span data-ttu-id="69193-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="69193-139">-TableName</span></span>
<span data-ttu-id="69193-140">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="69193-140">Name of table.</span></span>

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

### <span data-ttu-id="69193-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69193-141">-Confirm</span></span>
<span data-ttu-id="69193-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69193-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69193-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69193-143">-WhatIf</span></span>
<span data-ttu-id="69193-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="69193-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69193-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69193-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69193-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69193-146">CommonParameters</span></span>
<span data-ttu-id="69193-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69193-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69193-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69193-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69193-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69193-149">INPUTS</span></span>

### <span data-ttu-id="69193-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="69193-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="69193-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="69193-151">OUTPUTS</span></span>

### <span data-ttu-id="69193-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69193-152">System.Boolean</span></span>

## <span data-ttu-id="69193-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="69193-153">NOTES</span></span>

## <span data-ttu-id="69193-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69193-154">RELATED LINKS</span></span>

[<span data-ttu-id="69193-155">Saiba mais sobre a descoberta e classificação de dados SQL banco de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="69193-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
