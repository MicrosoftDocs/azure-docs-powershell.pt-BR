---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fac62ac0e75587e19a9ba0a5e99461693ce31c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886304"
---
# <span data-ttu-id="38c56-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="38c56-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="38c56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38c56-102">SYNOPSIS</span></span>
<span data-ttu-id="38c56-103">Define os tipos de informações e os rótulos de sensibilidade das colunas no banco de dados de instância SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="38c56-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="38c56-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38c56-104">SYNTAX</span></span>

### <span data-ttu-id="38c56-105">ClassificationObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38c56-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c56-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="38c56-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c56-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="38c56-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c56-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38c56-108">DESCRIPTION</span></span>
<span data-ttu-id="38c56-109">O Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet define os tipos de informações e os rótulos de sensibilidade das colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="38c56-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="38c56-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38c56-110">EXAMPLES</span></span>

### <span data-ttu-id="38c56-111">Exemplo 1: Definir o tipo de informação e o rótulo de sensibilidade de uma coluna em um banco de dados de instância SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="38c56-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="38c56-112">Exemplo 2: definir tipos de informações recomendados e rótulos de sensibilidade de colunas em um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="38c56-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="38c56-113">Exemplo 3: Definir o tipo de informação e o rótulo de sensibilidade de uma coluna em um banco de dados de instância gerenciada do Azure SQL, usando a canalização.</span><span class="sxs-lookup"><span data-stu-id="38c56-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="38c56-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38c56-114">PARAMETERS</span></span>

### <span data-ttu-id="38c56-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38c56-115">-AsJob</span></span>
<span data-ttu-id="38c56-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="38c56-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38c56-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="38c56-117">-ClassificationObject</span></span>
<span data-ttu-id="38c56-118">Um objeto que representa SQL Classificação de Sensibilidade de Banco de Dados de Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="38c56-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="38c56-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="38c56-119">-ColumnName</span></span>
<span data-ttu-id="38c56-120">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="38c56-120">Name of column.</span></span>

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

### <span data-ttu-id="38c56-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="38c56-121">-DatabaseName</span></span>
<span data-ttu-id="38c56-122">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="38c56-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="38c56-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="38c56-123">-DatabaseObject</span></span>
<span data-ttu-id="38c56-124">O objeto de banco de dados SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="38c56-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="38c56-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c56-125">-DefaultProfile</span></span>
<span data-ttu-id="38c56-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38c56-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38c56-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="38c56-127">-InformationType</span></span>
<span data-ttu-id="38c56-128">Um nome que descreve o tipo de informação dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="38c56-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="38c56-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="38c56-129">-InstanceName</span></span>
<span data-ttu-id="38c56-130">O Azure SQL nome da instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="38c56-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="38c56-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38c56-131">-PassThru</span></span>
<span data-ttu-id="38c56-132">Especifica se o modelo de classificação de sensibilidade deve ser produzido no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="38c56-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="38c56-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c56-133">-ResourceGroupName</span></span>
<span data-ttu-id="38c56-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38c56-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="38c56-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="38c56-135">-SchemaName</span></span>
<span data-ttu-id="38c56-136">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="38c56-136">Name of schema.</span></span>

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

### <span data-ttu-id="38c56-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="38c56-137">-SensitivityLabel</span></span>
<span data-ttu-id="38c56-138">Um nome que descreve a sensibilidade dos dados armazenados na coluna.</span><span class="sxs-lookup"><span data-stu-id="38c56-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="38c56-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="38c56-139">-TableName</span></span>
<span data-ttu-id="38c56-140">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="38c56-140">Name of table.</span></span>

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

### <span data-ttu-id="38c56-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38c56-141">-Confirm</span></span>
<span data-ttu-id="38c56-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c56-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c56-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c56-143">-WhatIf</span></span>
<span data-ttu-id="38c56-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38c56-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38c56-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38c56-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c56-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c56-146">CommonParameters</span></span>
<span data-ttu-id="38c56-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c56-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c56-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38c56-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c56-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38c56-149">INPUTS</span></span>

### <span data-ttu-id="38c56-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="38c56-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="38c56-151">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38c56-151">OUTPUTS</span></span>

### <span data-ttu-id="38c56-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38c56-152">System.Boolean</span></span>

## <span data-ttu-id="38c56-153">NOTES</span><span class="sxs-lookup"><span data-stu-id="38c56-153">NOTES</span></span>

## <span data-ttu-id="38c56-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38c56-154">RELATED LINKS</span></span>

[<span data-ttu-id="38c56-155">Saiba mais sobre a descoberta e classificação de dados SQL banco de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="38c56-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
