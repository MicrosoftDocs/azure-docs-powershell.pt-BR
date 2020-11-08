---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116710"
---
# <span data-ttu-id="d0443-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="d0443-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="d0443-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0443-102">SYNOPSIS</span></span>
<span data-ttu-id="d0443-103">Permite recomendações de sensibilidade em colunas (as recomendações são habilitadas por padrão em todas as colunas) no banco de dados instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0443-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="d0443-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0443-104">SYNTAX</span></span>

### <span data-ttu-id="d0443-105">InputObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0443-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0443-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0443-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0443-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0443-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0443-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0443-108">DESCRIPTION</span></span>
<span data-ttu-id="d0443-109">O cmdlet Enable-AzSqlInstanceDatabaseSensitivityRecommendation permite recomendações de sensibilidade em colunas no banco de dados instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d0443-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="d0443-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0443-110">EXAMPLES</span></span>

### <span data-ttu-id="d0443-111">Exemplo 1: habilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d0443-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="d0443-112">Exemplo 2: habilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciada SQL do Azure com encanamento.</span><span class="sxs-lookup"><span data-stu-id="d0443-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="d0443-113">OS</span><span class="sxs-lookup"><span data-stu-id="d0443-113">PARAMETERS</span></span>

### <span data-ttu-id="d0443-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0443-114">-AsJob</span></span>
<span data-ttu-id="d0443-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d0443-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0443-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="d0443-116">-ColumnName</span></span>
<span data-ttu-id="d0443-117">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="d0443-117">Name of column.</span></span>

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

### <span data-ttu-id="d0443-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0443-118">-DatabaseName</span></span>
<span data-ttu-id="d0443-119">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d0443-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="d0443-120">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="d0443-120">-DatabaseObject</span></span>
<span data-ttu-id="d0443-121">O objeto de banco de dados instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0443-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="d0443-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0443-122">-DefaultProfile</span></span>
<span data-ttu-id="d0443-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0443-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0443-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0443-124">-InputObject</span></span>
<span data-ttu-id="d0443-125">Um objeto que representa uma classificação de sensibilidade de banco de dados de instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="d0443-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="d0443-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d0443-126">-InstanceName</span></span>
<span data-ttu-id="d0443-127">Nome da instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0443-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="d0443-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0443-128">-PassThru</span></span>
<span data-ttu-id="d0443-129">Especifica se o modelo de classificação de sensibilidade deve ser impresso no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="d0443-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="d0443-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0443-130">-ResourceGroupName</span></span>
<span data-ttu-id="d0443-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0443-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0443-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d0443-132">-SchemaName</span></span>
<span data-ttu-id="d0443-133">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="d0443-133">Name of schema.</span></span>

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

### <span data-ttu-id="d0443-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="d0443-134">-TableName</span></span>
<span data-ttu-id="d0443-135">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="d0443-135">Name of table.</span></span>

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

### <span data-ttu-id="d0443-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d0443-136">-Confirm</span></span>
<span data-ttu-id="d0443-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0443-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0443-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0443-138">-WhatIf</span></span>
<span data-ttu-id="d0443-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d0443-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0443-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0443-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0443-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0443-141">CommonParameters</span></span>
<span data-ttu-id="d0443-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0443-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0443-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0443-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0443-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0443-144">INPUTS</span></span>

### <span data-ttu-id="d0443-145">Microsoft. Azure. Commands. Sql. dataclassation. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="d0443-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="d0443-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0443-146">OUTPUTS</span></span>

### <span data-ttu-id="d0443-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0443-147">System.Boolean</span></span>

## <span data-ttu-id="d0443-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0443-148">NOTES</span></span>

## <span data-ttu-id="d0443-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0443-149">RELATED LINKS</span></span>

[<span data-ttu-id="d0443-150">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="d0443-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)