---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111314"
---
# <span data-ttu-id="0da40-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="0da40-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="0da40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0da40-102">SYNOPSIS</span></span>
<span data-ttu-id="0da40-103">Remove os tipos de informações e os rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0da40-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0da40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0da40-104">SYNTAX</span></span>

### <span data-ttu-id="0da40-105">ClassificationObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0da40-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da40-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da40-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da40-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="0da40-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da40-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0da40-108">DESCRIPTION</span></span>
<span data-ttu-id="0da40-109">O cmdlet Remove-AzSqlInstanceDatabaseSensitivityClassification remove os tipos de informações e rótulos de sensibilidade de colunas no banco de dados instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0da40-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="0da40-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0da40-110">EXAMPLES</span></span>

### <span data-ttu-id="0da40-111">Exemplo 1: remover tipo de informação e rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0da40-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="0da40-112">Exemplo 2: remover tipos de informações atuais e rótulos de sensibilidade de colunas em um banco de dados de instância gerenciada SQL do Azure com tubulação.</span><span class="sxs-lookup"><span data-stu-id="0da40-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="0da40-113">Exemplo 3: remover tipo de informação e rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciada do Azure SQL com encanamento.</span><span class="sxs-lookup"><span data-stu-id="0da40-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="0da40-114">OS</span><span class="sxs-lookup"><span data-stu-id="0da40-114">PARAMETERS</span></span>

### <span data-ttu-id="0da40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0da40-115">-AsJob</span></span>
<span data-ttu-id="0da40-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0da40-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0da40-117">-Classificationobject</span><span class="sxs-lookup"><span data-stu-id="0da40-117">-ClassificationObject</span></span>
<span data-ttu-id="0da40-118">Um objeto que representa uma classificação de sensibilidade de banco de dados de instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="0da40-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da40-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="0da40-119">-ColumnName</span></span>
<span data-ttu-id="0da40-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="0da40-120">Name of column.</span></span>

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

### <span data-ttu-id="0da40-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0da40-121">-DatabaseName</span></span>
<span data-ttu-id="0da40-122">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0da40-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="0da40-123">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="0da40-123">-DatabaseObject</span></span>
<span data-ttu-id="0da40-124">O objeto de banco de dados instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0da40-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0da40-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da40-125">-DefaultProfile</span></span>
<span data-ttu-id="0da40-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0da40-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da40-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0da40-127">-InstanceName</span></span>
<span data-ttu-id="0da40-128">Nome da instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0da40-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="0da40-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0da40-129">-PassThru</span></span>
<span data-ttu-id="0da40-130">Especifica se o modelo de classificação de sensibilidade deve ser impresso no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="0da40-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="0da40-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da40-131">-ResourceGroupName</span></span>
<span data-ttu-id="0da40-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0da40-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="0da40-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0da40-133">-SchemaName</span></span>
<span data-ttu-id="0da40-134">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="0da40-134">Name of schema.</span></span>

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

### <span data-ttu-id="0da40-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="0da40-135">-TableName</span></span>
<span data-ttu-id="0da40-136">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="0da40-136">Name of table.</span></span>

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

### <span data-ttu-id="0da40-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0da40-137">-Confirm</span></span>
<span data-ttu-id="0da40-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da40-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da40-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da40-139">-WhatIf</span></span>
<span data-ttu-id="0da40-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0da40-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0da40-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0da40-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da40-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da40-142">CommonParameters</span></span>
<span data-ttu-id="0da40-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da40-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da40-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0da40-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da40-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0da40-145">INPUTS</span></span>

### <span data-ttu-id="0da40-146">Microsoft. Azure. Commands. Sql. dataclassation. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="0da40-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="0da40-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0da40-147">OUTPUTS</span></span>

### <span data-ttu-id="0da40-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0da40-148">System.Boolean</span></span>

## <span data-ttu-id="0da40-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0da40-149">NOTES</span></span>

## <span data-ttu-id="0da40-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0da40-150">RELATED LINKS</span></span>

[<span data-ttu-id="0da40-151">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="0da40-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
