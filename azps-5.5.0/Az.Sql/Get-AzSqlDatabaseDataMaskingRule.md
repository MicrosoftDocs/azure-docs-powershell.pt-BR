---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8813d405ebc8fadafa037afb884240dcdbb95383
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116154"
---
# <span data-ttu-id="a0876-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0876-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="a0876-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0876-102">SYNOPSIS</span></span>
<span data-ttu-id="a0876-103">Obtém as regras de mascaramento de dados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a0876-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="a0876-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0876-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0876-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0876-105">DESCRIPTION</span></span>
<span data-ttu-id="a0876-106">O cmdlet **Get-AzSqlDatabaseDataMaskingRule** obtém uma regra específica de mascaramento de dados ou todas as regras de mascaramento de dados para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0876-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="a0876-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados e o parâmetro *RuleId* para especificar qual regra esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="a0876-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="a0876-108">Se você não fornecer *RuleId,* todas as regras de mascaramento de dados para esse banco de dados SQL do Azure serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="a0876-108">If you do not provide *RuleId*, all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="a0876-109">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="a0876-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0876-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a0876-110">EXAMPLES</span></span>

### <span data-ttu-id="a0876-111">Exemplo 1: Obter todas as regras de mascaramento de dados de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="a0876-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="a0876-112">Exemplo 2: Definir a regra de mascaramento de dados no esquema "dbo", tabela "tabela1" e coluna "coluna1".</span><span class="sxs-lookup"><span data-stu-id="a0876-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="a0876-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0876-113">PARAMETERS</span></span>

### <span data-ttu-id="a0876-114">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="a0876-114">-ColumnName</span></span>
<span data-ttu-id="a0876-115">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="a0876-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="a0876-116">-DatabaseName</span></span>
<span data-ttu-id="a0876-117">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a0876-117">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0876-118">-DefaultProfile</span></span>
<span data-ttu-id="a0876-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a0876-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0876-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0876-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0876-121">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="a0876-121">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a0876-122">-SchemaName</span></span>
<span data-ttu-id="a0876-123">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="a0876-123">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0876-124">-ServerName</span></span>
<span data-ttu-id="a0876-125">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a0876-125">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-126">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="a0876-126">-TableName</span></span>
<span data-ttu-id="a0876-127">Especifica o nome de uma tabela SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0876-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a0876-128">-Confirm</span></span>
<span data-ttu-id="a0876-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0876-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0876-130">-WhatIf</span></span>
<span data-ttu-id="a0876-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a0876-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0876-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0876-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0876-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0876-133">CommonParameters</span></span>
<span data-ttu-id="a0876-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0876-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0876-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0876-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0876-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="a0876-136">INPUTS</span></span>

### <span data-ttu-id="a0876-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a0876-137">System.String</span></span>

## <span data-ttu-id="a0876-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="a0876-138">OUTPUTS</span></span>

### <span data-ttu-id="a0876-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="a0876-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="a0876-140">Notas</span><span class="sxs-lookup"><span data-stu-id="a0876-140">NOTES</span></span>

## <span data-ttu-id="a0876-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0876-141">RELATED LINKS</span></span>

[<span data-ttu-id="a0876-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a0876-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a0876-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0876-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a0876-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0876-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a0876-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a0876-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a0876-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a0876-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


