---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778109"
---
# <span data-ttu-id="daa84-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="daa84-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="daa84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daa84-102">SYNOPSIS</span></span>
<span data-ttu-id="daa84-103">Permite recomendações de sensibilidade em colunas (as recomendações são habilitadas por padrão em todas as colunas) no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="daa84-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="daa84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daa84-104">SYNTAX</span></span>

### <span data-ttu-id="daa84-105">InputObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="daa84-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daa84-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="daa84-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daa84-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="daa84-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa84-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daa84-108">DESCRIPTION</span></span>
<span data-ttu-id="daa84-109">O cmdlet Enable-AzSqlDatabaseSensitivityRecommendation permite recomendações de sensibilidade em colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="daa84-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="daa84-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daa84-110">EXAMPLES</span></span>

### <span data-ttu-id="daa84-111">Exemplo 1: habilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="daa84-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="daa84-112">Exemplo 2: habilitar recomendações de sensibilidade em um determinado banco de dados SQL do Azure de coluna usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="daa84-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="daa84-113">OS</span><span class="sxs-lookup"><span data-stu-id="daa84-113">PARAMETERS</span></span>

### <span data-ttu-id="daa84-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daa84-114">-AsJob</span></span>
<span data-ttu-id="daa84-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="daa84-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="daa84-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="daa84-116">-ColumnName</span></span>
<span data-ttu-id="daa84-117">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="daa84-117">Name of column.</span></span>

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

### <span data-ttu-id="daa84-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="daa84-118">-DatabaseName</span></span>
<span data-ttu-id="daa84-119">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="daa84-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="daa84-120">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="daa84-120">-DatabaseObject</span></span>
<span data-ttu-id="daa84-121">O objeto de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="daa84-121">The SQL database object.</span></span>

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

### <span data-ttu-id="daa84-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa84-122">-DefaultProfile</span></span>
<span data-ttu-id="daa84-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daa84-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa84-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daa84-124">-InputObject</span></span>
<span data-ttu-id="daa84-125">Um objeto que representa uma classificação de sensibilidade de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="daa84-125">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="daa84-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="daa84-126">-PassThru</span></span>
<span data-ttu-id="daa84-127">Especifica se o modelo de classificação de sensibilidade deve ser impresso no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa84-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="daa84-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa84-128">-ResourceGroupName</span></span>
<span data-ttu-id="daa84-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="daa84-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="daa84-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="daa84-130">-SchemaName</span></span>
<span data-ttu-id="daa84-131">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="daa84-131">Name of schema.</span></span>

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

### <span data-ttu-id="daa84-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="daa84-132">-ServerName</span></span>
<span data-ttu-id="daa84-133">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="daa84-133">SQL server name.</span></span>

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

### <span data-ttu-id="daa84-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="daa84-134">-TableName</span></span>
<span data-ttu-id="daa84-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="daa84-135">Name of table.</span></span>

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

### <span data-ttu-id="daa84-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="daa84-136">-Confirm</span></span>
<span data-ttu-id="daa84-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa84-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa84-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa84-138">-WhatIf</span></span>
<span data-ttu-id="daa84-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="daa84-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="daa84-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daa84-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa84-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa84-141">CommonParameters</span></span>
<span data-ttu-id="daa84-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa84-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa84-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daa84-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa84-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daa84-144">INPUTS</span></span>

### <span data-ttu-id="daa84-145">Microsoft. Azure. Commands. Sql. dataclassation. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="daa84-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="daa84-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daa84-146">OUTPUTS</span></span>

### <span data-ttu-id="daa84-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="daa84-147">System.Boolean</span></span>

## <span data-ttu-id="daa84-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daa84-148">NOTES</span></span>

## <span data-ttu-id="daa84-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daa84-149">RELATED LINKS</span></span>

[<span data-ttu-id="daa84-150">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="daa84-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)