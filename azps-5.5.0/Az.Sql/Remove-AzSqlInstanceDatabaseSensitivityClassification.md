---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113722"
---
# <span data-ttu-id="8e816-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="8e816-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="8e816-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e816-102">SYNOPSIS</span></span>
<span data-ttu-id="8e816-103">Remove os tipos de informações e rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8e816-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="8e816-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e816-104">SYNTAX</span></span>

### <span data-ttu-id="8e816-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e816-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e816-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e816-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e816-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e816-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e816-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e816-108">DESCRIPTION</span></span>
<span data-ttu-id="8e816-109">O Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet remove os tipos de informações e rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8e816-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="8e816-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e816-110">EXAMPLES</span></span>

### <span data-ttu-id="8e816-111">Exemplo 1: Remover o tipo de informações e o rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciado pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e816-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="8e816-112">Exemplo 2: Remover tipos de informações atuais e rótulos de sensibilidade de colunas em um banco de dados de instância gerenciada do Azure SQL com Piping.</span><span class="sxs-lookup"><span data-stu-id="8e816-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="8e816-113">Exemplo 3: Remover o tipo de informações e o rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciado pelo SQL do Azure com Piping.</span><span class="sxs-lookup"><span data-stu-id="8e816-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="8e816-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e816-114">PARAMETERS</span></span>

### <span data-ttu-id="8e816-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e816-115">-AsJob</span></span>
<span data-ttu-id="8e816-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8e816-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e816-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="8e816-117">-ClassificationObject</span></span>
<span data-ttu-id="8e816-118">Um objeto que representa uma Classificação de Sensibilidade do Banco de Dados de Instância Gerenciada do SQL.</span><span class="sxs-lookup"><span data-stu-id="8e816-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="8e816-119">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="8e816-119">-ColumnName</span></span>
<span data-ttu-id="8e816-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="8e816-120">Name of column.</span></span>

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

### <span data-ttu-id="8e816-121">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="8e816-121">-DatabaseName</span></span>
<span data-ttu-id="8e816-122">O nome do banco de dados de instância gerenciada do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e816-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="8e816-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8e816-123">-DatabaseObject</span></span>
<span data-ttu-id="8e816-124">O objeto de banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="8e816-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="8e816-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e816-125">-DefaultProfile</span></span>
<span data-ttu-id="8e816-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e816-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e816-127">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="8e816-127">-InstanceName</span></span>
<span data-ttu-id="8e816-128">Nome da instância gerenciada pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8e816-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="8e816-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e816-129">-PassThru</span></span>
<span data-ttu-id="8e816-130">Especifica se o modelo de classificação de sensibilidade será saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e816-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8e816-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e816-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e816-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e816-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e816-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8e816-133">-SchemaName</span></span>
<span data-ttu-id="8e816-134">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="8e816-134">Name of schema.</span></span>

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

### <span data-ttu-id="8e816-135">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="8e816-135">-TableName</span></span>
<span data-ttu-id="8e816-136">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="8e816-136">Name of table.</span></span>

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

### <span data-ttu-id="8e816-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8e816-137">-Confirm</span></span>
<span data-ttu-id="8e816-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e816-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e816-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e816-139">-WhatIf</span></span>
<span data-ttu-id="8e816-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8e816-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e816-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e816-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e816-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e816-142">CommonParameters</span></span>
<span data-ttu-id="8e816-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e816-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e816-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e816-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e816-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e816-145">INPUTS</span></span>

### <span data-ttu-id="8e816-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8e816-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="8e816-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e816-147">OUTPUTS</span></span>

### <span data-ttu-id="8e816-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e816-148">System.Boolean</span></span>

## <span data-ttu-id="8e816-149">Notas</span><span class="sxs-lookup"><span data-stu-id="8e816-149">NOTES</span></span>

## <span data-ttu-id="8e816-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e816-150">RELATED LINKS</span></span>

[<span data-ttu-id="8e816-151">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="8e816-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
