---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 95c5829c3d715b1510c1a58e8baf5e7809f9cd8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901435"
---
# <span data-ttu-id="f855d-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f855d-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="f855d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f855d-102">SYNOPSIS</span></span>
<span data-ttu-id="f855d-103">Desabilita (descarta) recomendações de sensibilidade em colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f855d-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="f855d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f855d-104">SYNTAX</span></span>

### <span data-ttu-id="f855d-105">InputObjectParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f855d-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f855d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f855d-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f855d-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f855d-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f855d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f855d-108">DESCRIPTION</span></span>
<span data-ttu-id="f855d-109">O Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet desabilita (descarta) recomendações de sensibilidade em colunas no banco de dados de instâncias gerenciadas do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f855d-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="f855d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f855d-110">EXAMPLES</span></span>

### <span data-ttu-id="f855d-111">Exemplo 1: Desabilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f855d-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="f855d-112">Exemplo 2: Desabilite as recomendações de sensibilidade em colunas que tenham recomendações de sensibilidade em um banco de dados de instância gerenciada do Azure SQL com Piping.</span><span class="sxs-lookup"><span data-stu-id="f855d-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="f855d-113">Exemplo 3: Desabilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciada do Azure SQL com Piping.</span><span class="sxs-lookup"><span data-stu-id="f855d-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="f855d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f855d-114">PARAMETERS</span></span>

### <span data-ttu-id="f855d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f855d-115">-AsJob</span></span>
<span data-ttu-id="f855d-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f855d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f855d-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f855d-117">-ColumnName</span></span>
<span data-ttu-id="f855d-118">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="f855d-118">Name of column.</span></span>

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

### <span data-ttu-id="f855d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f855d-119">-DatabaseName</span></span>
<span data-ttu-id="f855d-120">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f855d-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="f855d-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f855d-121">-DatabaseObject</span></span>
<span data-ttu-id="f855d-122">O objeto de banco de dados SQL instância gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="f855d-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="f855d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f855d-123">-DefaultProfile</span></span>
<span data-ttu-id="f855d-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f855d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f855d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f855d-125">-InputObject</span></span>
<span data-ttu-id="f855d-126">Um objeto que representa SQL Classificação de Sensibilidade de Banco de Dados de Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f855d-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="f855d-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f855d-127">-InstanceName</span></span>
<span data-ttu-id="f855d-128">O Azure SQL nome da instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f855d-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="f855d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f855d-129">-PassThru</span></span>
<span data-ttu-id="f855d-130">Especifica se o modelo de classificação de sensibilidade deve ser produzido no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="f855d-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="f855d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f855d-131">-ResourceGroupName</span></span>
<span data-ttu-id="f855d-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f855d-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="f855d-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f855d-133">-SchemaName</span></span>
<span data-ttu-id="f855d-134">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="f855d-134">Name of schema.</span></span>

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

### <span data-ttu-id="f855d-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="f855d-135">-TableName</span></span>
<span data-ttu-id="f855d-136">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="f855d-136">Name of table.</span></span>

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

### <span data-ttu-id="f855d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f855d-137">-Confirm</span></span>
<span data-ttu-id="f855d-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f855d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f855d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f855d-139">-WhatIf</span></span>
<span data-ttu-id="f855d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f855d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f855d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f855d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f855d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f855d-142">CommonParameters</span></span>
<span data-ttu-id="f855d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f855d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f855d-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f855d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f855d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f855d-145">INPUTS</span></span>

### <span data-ttu-id="f855d-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f855d-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="f855d-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f855d-147">OUTPUTS</span></span>

### <span data-ttu-id="f855d-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f855d-148">System.Boolean</span></span>

## <span data-ttu-id="f855d-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="f855d-149">NOTES</span></span>

## <span data-ttu-id="f855d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f855d-150">RELATED LINKS</span></span>

[<span data-ttu-id="f855d-151">Saiba mais sobre a descoberta e classificação de dados SQL banco de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f855d-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)