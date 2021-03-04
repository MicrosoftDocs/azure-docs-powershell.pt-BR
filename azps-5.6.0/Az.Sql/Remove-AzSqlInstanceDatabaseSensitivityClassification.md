---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 369a9f0f9bb475d27512eb13047a5a4ffe334573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887316"
---
# <span data-ttu-id="485b4-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="485b4-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="485b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="485b4-102">SYNOPSIS</span></span>
<span data-ttu-id="485b4-103">Remove os tipos de informações e os rótulos de sensibilidade das colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="485b4-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="485b4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="485b4-104">SYNTAX</span></span>

### <span data-ttu-id="485b4-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="485b4-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485b4-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="485b4-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485b4-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="485b4-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="485b4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="485b4-108">DESCRIPTION</span></span>
<span data-ttu-id="485b4-109">O Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet remove os tipos de informações e os rótulos de sensibilidade das colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="485b4-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="485b4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="485b4-110">EXAMPLES</span></span>

### <span data-ttu-id="485b4-111">Exemplo 1: Remover o tipo de informação e o rótulo de sensibilidade de uma coluna em um banco de dados SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="485b4-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="485b4-112">Exemplo 2: Remover tipos de informações atuais e rótulos de sensibilidade de colunas em um banco de dados de instância gerenciada do Azure SQL com Piping.</span><span class="sxs-lookup"><span data-stu-id="485b4-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="485b4-113">Exemplo 3: Remover o tipo de informação e o rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciada do Azure SQL com Piping.</span><span class="sxs-lookup"><span data-stu-id="485b4-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="485b4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="485b4-114">PARAMETERS</span></span>

### <span data-ttu-id="485b4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="485b4-115">-AsJob</span></span>
<span data-ttu-id="485b4-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="485b4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="485b4-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="485b4-117">-ClassificationObject</span></span>
<span data-ttu-id="485b4-118">Um objeto que representa SQL Classificação de Sensibilidade de Banco de Dados de Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="485b4-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="485b4-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="485b4-119">-ColumnName</span></span>
<span data-ttu-id="485b4-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="485b4-120">Name of column.</span></span>

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

### <span data-ttu-id="485b4-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="485b4-121">-DatabaseName</span></span>
<span data-ttu-id="485b4-122">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="485b4-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="485b4-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="485b4-123">-DatabaseObject</span></span>
<span data-ttu-id="485b4-124">O objeto de banco de dados SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="485b4-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="485b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485b4-125">-DefaultProfile</span></span>
<span data-ttu-id="485b4-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="485b4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="485b4-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="485b4-127">-InstanceName</span></span>
<span data-ttu-id="485b4-128">O Azure SQL nome da instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="485b4-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="485b4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="485b4-129">-PassThru</span></span>
<span data-ttu-id="485b4-130">Especifica se o modelo de classificação de sensibilidade deve ser produzido no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="485b4-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="485b4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="485b4-131">-ResourceGroupName</span></span>
<span data-ttu-id="485b4-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="485b4-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="485b4-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="485b4-133">-SchemaName</span></span>
<span data-ttu-id="485b4-134">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="485b4-134">Name of schema.</span></span>

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

### <span data-ttu-id="485b4-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="485b4-135">-TableName</span></span>
<span data-ttu-id="485b4-136">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="485b4-136">Name of table.</span></span>

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

### <span data-ttu-id="485b4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="485b4-137">-Confirm</span></span>
<span data-ttu-id="485b4-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="485b4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="485b4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="485b4-139">-WhatIf</span></span>
<span data-ttu-id="485b4-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="485b4-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="485b4-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="485b4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="485b4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485b4-142">CommonParameters</span></span>
<span data-ttu-id="485b4-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485b4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485b4-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="485b4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485b4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="485b4-145">INPUTS</span></span>

### <span data-ttu-id="485b4-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="485b4-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="485b4-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="485b4-147">OUTPUTS</span></span>

### <span data-ttu-id="485b4-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="485b4-148">System.Boolean</span></span>

## <span data-ttu-id="485b4-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="485b4-149">NOTES</span></span>

## <span data-ttu-id="485b4-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="485b4-150">RELATED LINKS</span></span>

[<span data-ttu-id="485b4-151">Saiba mais sobre a descoberta e classificação de dados SQL banco de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="485b4-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
