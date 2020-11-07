---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 5c43820c57531ca5a844e1ab429c26d85fecceee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773682"
---
# <span data-ttu-id="24772-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="24772-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="24772-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24772-102">SYNOPSIS</span></span>
<span data-ttu-id="24772-103">Obtém as regras de máscara de dados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="24772-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="24772-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24772-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24772-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24772-105">DESCRIPTION</span></span>
<span data-ttu-id="24772-106">O cmdlet **Get-AzSqlDatabaseDataMaskingRule** Obtém uma regra de máscara de dados específica ou todas as regras de máscara de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="24772-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="24772-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *nome_do_servidor* e *DatabaseName* para identificar o banco de dados e o parâmetro *RuleId* para especificar qual regra esse cmdlet retorna.</span><span class="sxs-lookup"><span data-stu-id="24772-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="24772-108">Se você não fornecer *RuleId* , todas as regras de máscara de dados para esse banco de dados SQL do Azure serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="24772-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="24772-109">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="24772-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="24772-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24772-110">EXAMPLES</span></span>

### <span data-ttu-id="24772-111">Exemplo 1: obter todas as regras de máscara de dados de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="24772-111">Example 1: Get all data masking rules from a database</span></span>
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

### <span data-ttu-id="24772-112">Exemplo 2: obter a regra de máscara de dados definida no esquema "dbo", tabela "tabela1" e coluna "Coluna1".</span><span class="sxs-lookup"><span data-stu-id="24772-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
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

## <span data-ttu-id="24772-113">OS</span><span class="sxs-lookup"><span data-stu-id="24772-113">PARAMETERS</span></span>

### <span data-ttu-id="24772-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="24772-114">-ColumnName</span></span>
<span data-ttu-id="24772-115">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="24772-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="24772-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24772-116">-DatabaseName</span></span>
<span data-ttu-id="24772-117">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="24772-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="24772-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24772-118">-DefaultProfile</span></span>
<span data-ttu-id="24772-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="24772-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24772-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24772-120">-ResourceGroupName</span></span>
<span data-ttu-id="24772-121">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="24772-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="24772-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="24772-122">-SchemaName</span></span>
<span data-ttu-id="24772-123">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="24772-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="24772-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="24772-124">-ServerName</span></span>
<span data-ttu-id="24772-125">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="24772-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="24772-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="24772-126">-TableName</span></span>
<span data-ttu-id="24772-127">Especifica o nome de uma tabela SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="24772-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="24772-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24772-128">-Confirm</span></span>
<span data-ttu-id="24772-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24772-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24772-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24772-130">-WhatIf</span></span>
<span data-ttu-id="24772-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24772-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24772-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24772-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24772-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24772-133">CommonParameters</span></span>
<span data-ttu-id="24772-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24772-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24772-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24772-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24772-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24772-136">INPUTS</span></span>

### <span data-ttu-id="24772-137">System. String</span><span class="sxs-lookup"><span data-stu-id="24772-137">System.String</span></span>

## <span data-ttu-id="24772-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24772-138">OUTPUTS</span></span>

### <span data-ttu-id="24772-139">Microsoft. Azure. Commands. Sql. datamasking. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="24772-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="24772-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24772-140">NOTES</span></span>

## <span data-ttu-id="24772-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24772-141">RELATED LINKS</span></span>

[<span data-ttu-id="24772-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="24772-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="24772-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="24772-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="24772-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="24772-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="24772-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="24772-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="24772-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="24772-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


