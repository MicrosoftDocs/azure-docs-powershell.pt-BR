---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956196"
---
# <span data-ttu-id="dae9c-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="dae9c-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="dae9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dae9c-102">SYNOPSIS</span></span>
<span data-ttu-id="dae9c-103">Desabilita as recomendações de sensibilidade (ignoradas) nas colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dae9c-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="dae9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dae9c-104">SYNTAX</span></span>

### <span data-ttu-id="dae9c-105">InputObjectParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dae9c-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae9c-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae9c-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae9c-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae9c-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae9c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dae9c-108">DESCRIPTION</span></span>
<span data-ttu-id="dae9c-109">O cmdlet Disable-AzSqlInstanceDatabaseSensitivityRecommendation desabilita (ignora) as recomendações de sensibilidade em colunas no banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dae9c-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="dae9c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dae9c-110">EXAMPLES</span></span>

### <span data-ttu-id="dae9c-111">Exemplo 1: desabilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dae9c-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="dae9c-112">Exemplo 2: desabilitar recomendações de sensibilidade em colunas com recomendações de sensibilidade em um banco de dados de instância gerenciada SQL do Azure com tubulação.</span><span class="sxs-lookup"><span data-stu-id="dae9c-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="dae9c-113">Exemplo 3: desabilitar recomendações de sensibilidade em uma determinada coluna em um banco de dados de instância gerenciada SQL do Azure com encanamento.</span><span class="sxs-lookup"><span data-stu-id="dae9c-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="dae9c-114">OS</span><span class="sxs-lookup"><span data-stu-id="dae9c-114">PARAMETERS</span></span>

### <span data-ttu-id="dae9c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dae9c-115">-AsJob</span></span>
<span data-ttu-id="dae9c-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dae9c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dae9c-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="dae9c-117">-ColumnName</span></span>
<span data-ttu-id="dae9c-118">Nome da coluna.</span><span class="sxs-lookup"><span data-stu-id="dae9c-118">Name of column.</span></span>

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

### <span data-ttu-id="dae9c-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dae9c-119">-DatabaseName</span></span>
<span data-ttu-id="dae9c-120">O nome do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dae9c-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="dae9c-121">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="dae9c-121">-DatabaseObject</span></span>
<span data-ttu-id="dae9c-122">O objeto de banco de dados instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dae9c-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="dae9c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae9c-123">-DefaultProfile</span></span>
<span data-ttu-id="dae9c-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dae9c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae9c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dae9c-125">-InputObject</span></span>
<span data-ttu-id="dae9c-126">Um objeto que representa uma classificação de sensibilidade de banco de dados de instância gerenciada SQL.</span><span class="sxs-lookup"><span data-stu-id="dae9c-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="dae9c-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="dae9c-127">-InstanceName</span></span>
<span data-ttu-id="dae9c-128">Nome da instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dae9c-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="dae9c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dae9c-129">-PassThru</span></span>
<span data-ttu-id="dae9c-130">Especifica se o modelo de classificação de sensibilidade deve ser impresso no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="dae9c-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="dae9c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae9c-131">-ResourceGroupName</span></span>
<span data-ttu-id="dae9c-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dae9c-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="dae9c-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dae9c-133">-SchemaName</span></span>
<span data-ttu-id="dae9c-134">Nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="dae9c-134">Name of schema.</span></span>

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

### <span data-ttu-id="dae9c-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="dae9c-135">-TableName</span></span>
<span data-ttu-id="dae9c-136">Nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="dae9c-136">Name of table.</span></span>

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

### <span data-ttu-id="dae9c-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dae9c-137">-Confirm</span></span>
<span data-ttu-id="dae9c-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae9c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae9c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae9c-139">-WhatIf</span></span>
<span data-ttu-id="dae9c-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dae9c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dae9c-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dae9c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae9c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae9c-142">CommonParameters</span></span>
<span data-ttu-id="dae9c-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae9c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae9c-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dae9c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae9c-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dae9c-145">INPUTS</span></span>

### <span data-ttu-id="dae9c-146">Microsoft. Azure. Commands. Sql. dataclassation. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="dae9c-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="dae9c-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dae9c-147">OUTPUTS</span></span>

### <span data-ttu-id="dae9c-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dae9c-148">System.Boolean</span></span>

## <span data-ttu-id="dae9c-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dae9c-149">NOTES</span></span>

## <span data-ttu-id="dae9c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dae9c-150">RELATED LINKS</span></span>

[<span data-ttu-id="dae9c-151">Saiba mais sobre a descoberta e a classificação de dados do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="dae9c-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)