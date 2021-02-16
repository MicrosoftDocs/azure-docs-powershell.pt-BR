---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118611"
---
# <span data-ttu-id="cbad3-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="cbad3-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="cbad3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbad3-102">SYNOPSIS</span></span>
<span data-ttu-id="cbad3-103">Habilita recomendações de sensibilidade em colunas (as recomendações são habilitadas por padrão em todas as colunas) no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cbad3-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="cbad3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbad3-104">SYNTAX</span></span>

### <span data-ttu-id="cbad3-105">InputObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbad3-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbad3-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbad3-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbad3-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbad3-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbad3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbad3-108">DESCRIPTION</span></span>
<span data-ttu-id="cbad3-109">O Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet permite recomendações de sensibilidade em colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cbad3-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="cbad3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cbad3-110">EXAMPLES</span></span>

### <span data-ttu-id="cbad3-111">Exemplo 1: Habilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cbad3-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="cbad3-112">Exemplo 2: Habilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciado pelo SQL do Azure com Piping.</span><span class="sxs-lookup"><span data-stu-id="cbad3-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="cbad3-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbad3-113">PARAMETERS</span></span>

### <span data-ttu-id="cbad3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbad3-114">-AsJob</span></span>
<span data-ttu-id="cbad3-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbad3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbad3-116">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="cbad3-116">-ColumnName</span></span>
<span data-ttu-id="cbad3-117">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="cbad3-117">Name of column.</span></span>

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

### <span data-ttu-id="cbad3-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="cbad3-118">-DatabaseName</span></span>
<span data-ttu-id="cbad3-119">O nome do banco de dados de instância gerenciada do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbad3-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="cbad3-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cbad3-120">-DatabaseObject</span></span>
<span data-ttu-id="cbad3-121">O objeto de banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cbad3-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="cbad3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbad3-122">-DefaultProfile</span></span>
<span data-ttu-id="cbad3-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbad3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbad3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbad3-124">-InputObject</span></span>
<span data-ttu-id="cbad3-125">Um objeto que representa uma Classificação de Sensibilidade do Banco de Dados de Instância Gerenciada do SQL.</span><span class="sxs-lookup"><span data-stu-id="cbad3-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbad3-126">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="cbad3-126">-InstanceName</span></span>
<span data-ttu-id="cbad3-127">Nome da instância gerenciada pelo SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cbad3-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="cbad3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbad3-128">-PassThru</span></span>
<span data-ttu-id="cbad3-129">Especifica se o modelo de classificação de sensibilidade será saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="cbad3-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="cbad3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbad3-130">-ResourceGroupName</span></span>
<span data-ttu-id="cbad3-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbad3-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="cbad3-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cbad3-132">-SchemaName</span></span>
<span data-ttu-id="cbad3-133">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="cbad3-133">Name of schema.</span></span>

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

### <span data-ttu-id="cbad3-134">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="cbad3-134">-TableName</span></span>
<span data-ttu-id="cbad3-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="cbad3-135">Name of table.</span></span>

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

### <span data-ttu-id="cbad3-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cbad3-136">-Confirm</span></span>
<span data-ttu-id="cbad3-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbad3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbad3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbad3-138">-WhatIf</span></span>
<span data-ttu-id="cbad3-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cbad3-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbad3-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbad3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbad3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbad3-141">CommonParameters</span></span>
<span data-ttu-id="cbad3-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbad3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbad3-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbad3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbad3-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="cbad3-144">INPUTS</span></span>

### <span data-ttu-id="cbad3-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="cbad3-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="cbad3-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="cbad3-146">OUTPUTS</span></span>

### <span data-ttu-id="cbad3-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cbad3-147">System.Boolean</span></span>

## <span data-ttu-id="cbad3-148">Notas</span><span class="sxs-lookup"><span data-stu-id="cbad3-148">NOTES</span></span>

## <span data-ttu-id="cbad3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbad3-149">RELATED LINKS</span></span>

[<span data-ttu-id="cbad3-150">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="cbad3-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)