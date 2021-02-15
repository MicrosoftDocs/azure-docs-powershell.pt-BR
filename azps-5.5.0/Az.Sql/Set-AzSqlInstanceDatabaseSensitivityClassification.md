---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118931"
---
# <span data-ttu-id="742f2-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="742f2-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="742f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="742f2-102">SYNOPSIS</span></span>
<span data-ttu-id="742f2-103">Define os tipos de informações e os rótulos de sensibilidade das colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="742f2-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="742f2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="742f2-104">SYNTAX</span></span>

### <span data-ttu-id="742f2-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="742f2-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="742f2-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="742f2-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="742f2-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="742f2-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="742f2-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="742f2-108">DESCRIPTION</span></span>
<span data-ttu-id="742f2-109">O Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet define os tipos de informações e rótulos de sensibilidade de colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="742f2-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="742f2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="742f2-110">EXAMPLES</span></span>

### <span data-ttu-id="742f2-111">Exemplo 1: Definir o tipo de informações e o rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciado pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="742f2-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="742f2-112">Exemplo 2: Definir tipos de informações recomendadas e rótulos de sensibilidade de colunas em um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="742f2-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="742f2-113">Exemplo 3: Definir o tipo de informações e o rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciada pelo SQL do Azure, usando piping.</span><span class="sxs-lookup"><span data-stu-id="742f2-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="742f2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="742f2-114">PARAMETERS</span></span>

### <span data-ttu-id="742f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="742f2-115">-AsJob</span></span>
<span data-ttu-id="742f2-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="742f2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="742f2-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="742f2-117">-ClassificationObject</span></span>
<span data-ttu-id="742f2-118">Um objeto que representa uma Classificação de Sensibilidade do Banco de Dados de Instância Gerenciada do SQL.</span><span class="sxs-lookup"><span data-stu-id="742f2-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="742f2-119">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="742f2-119">-ColumnName</span></span>
<span data-ttu-id="742f2-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="742f2-120">Name of column.</span></span>

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

### <span data-ttu-id="742f2-121">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="742f2-121">-DatabaseName</span></span>
<span data-ttu-id="742f2-122">O nome do banco de dados de instância gerenciada do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="742f2-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="742f2-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="742f2-123">-DatabaseObject</span></span>
<span data-ttu-id="742f2-124">O objeto de banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="742f2-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="742f2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742f2-125">-DefaultProfile</span></span>
<span data-ttu-id="742f2-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="742f2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="742f2-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="742f2-127">-InformationType</span></span>
<span data-ttu-id="742f2-128">Um nome que descreve o tipo de informações dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="742f2-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="742f2-129">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="742f2-129">-InstanceName</span></span>
<span data-ttu-id="742f2-130">Nome da instância gerenciada pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="742f2-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="742f2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="742f2-131">-PassThru</span></span>
<span data-ttu-id="742f2-132">Especifica se o modelo de classificação de sensibilidade será saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="742f2-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="742f2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742f2-133">-ResourceGroupName</span></span>
<span data-ttu-id="742f2-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="742f2-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="742f2-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="742f2-135">-SchemaName</span></span>
<span data-ttu-id="742f2-136">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="742f2-136">Name of schema.</span></span>

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

### <span data-ttu-id="742f2-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="742f2-137">-SensitivityLabel</span></span>
<span data-ttu-id="742f2-138">Um nome que descreve a sensibilidade dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="742f2-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="742f2-139">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="742f2-139">-TableName</span></span>
<span data-ttu-id="742f2-140">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="742f2-140">Name of table.</span></span>

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

### <span data-ttu-id="742f2-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="742f2-141">-Confirm</span></span>
<span data-ttu-id="742f2-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="742f2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="742f2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="742f2-143">-WhatIf</span></span>
<span data-ttu-id="742f2-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="742f2-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="742f2-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="742f2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="742f2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742f2-146">CommonParameters</span></span>
<span data-ttu-id="742f2-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742f2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742f2-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="742f2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742f2-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="742f2-149">INPUTS</span></span>

### <span data-ttu-id="742f2-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="742f2-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="742f2-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="742f2-151">OUTPUTS</span></span>

### <span data-ttu-id="742f2-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="742f2-152">System.Boolean</span></span>

## <span data-ttu-id="742f2-153">Notas</span><span class="sxs-lookup"><span data-stu-id="742f2-153">NOTES</span></span>

## <span data-ttu-id="742f2-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="742f2-154">RELATED LINKS</span></span>

[<span data-ttu-id="742f2-155">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="742f2-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
