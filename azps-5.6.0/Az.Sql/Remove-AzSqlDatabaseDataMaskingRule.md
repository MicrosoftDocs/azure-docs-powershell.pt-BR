---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 2529057f7a2963c28175e18bacbc1aa3894a3eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886561"
---
# <span data-ttu-id="cddfd-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cddfd-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="cddfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cddfd-102">SYNOPSIS</span></span>
<span data-ttu-id="cddfd-103">Remove uma regra de mascaramento de dados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cddfd-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="cddfd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cddfd-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cddfd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cddfd-105">DESCRIPTION</span></span>
<span data-ttu-id="cddfd-106">O cmdlet **Remove-AzSqlDatabaseDataMaskingRule** remove uma regra específica de mascaramento de dados de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="cddfd-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="cddfd-107">Você pode remover uma regra de mascaramento de dados usando os parâmetros *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleId* para identificar a regra que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="cddfd-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="cddfd-108">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="cddfd-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cddfd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cddfd-109">EXAMPLES</span></span>

### <span data-ttu-id="cddfd-110">Exemplo 1: Remover uma regra de mascaramento de dados de banco de dados</span><span class="sxs-lookup"><span data-stu-id="cddfd-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="cddfd-111">Este comando remove o nome de regra Rule01 definido para o banco de dados Database01.</span><span class="sxs-lookup"><span data-stu-id="cddfd-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="cddfd-112">O banco de dados está localizado no Server01 e atribuído ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cddfd-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="cddfd-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cddfd-113">PARAMETERS</span></span>

### <span data-ttu-id="cddfd-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="cddfd-114">-ColumnName</span></span>
<span data-ttu-id="cddfd-115">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="cddfd-115">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddfd-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cddfd-116">-DatabaseName</span></span>
<span data-ttu-id="cddfd-117">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cddfd-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="cddfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddfd-118">-DefaultProfile</span></span>
<span data-ttu-id="cddfd-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cddfd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cddfd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cddfd-120">-Force</span></span>
<span data-ttu-id="cddfd-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cddfd-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cddfd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cddfd-122">-PassThru</span></span>
<span data-ttu-id="cddfd-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="cddfd-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cddfd-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="cddfd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cddfd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddfd-125">-ResourceGroupName</span></span>
<span data-ttu-id="cddfd-126">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="cddfd-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cddfd-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cddfd-127">-SchemaName</span></span>
<span data-ttu-id="cddfd-128">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="cddfd-128">Specifies the name of a schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddfd-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cddfd-129">-ServerName</span></span>
<span data-ttu-id="cddfd-130">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cddfd-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="cddfd-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="cddfd-131">-TableName</span></span>
<span data-ttu-id="cddfd-132">Especifica o nome de uma tabela SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cddfd-132">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cddfd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cddfd-133">-Confirm</span></span>
<span data-ttu-id="cddfd-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cddfd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cddfd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddfd-135">-WhatIf</span></span>
<span data-ttu-id="cddfd-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cddfd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cddfd-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cddfd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cddfd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddfd-138">CommonParameters</span></span>
<span data-ttu-id="cddfd-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cddfd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddfd-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cddfd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddfd-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cddfd-141">INPUTS</span></span>

### <span data-ttu-id="cddfd-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cddfd-142">System.String</span></span>

## <span data-ttu-id="cddfd-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cddfd-143">OUTPUTS</span></span>

### <span data-ttu-id="cddfd-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="cddfd-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="cddfd-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="cddfd-145">NOTES</span></span>

## <span data-ttu-id="cddfd-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cddfd-146">RELATED LINKS</span></span>

[<span data-ttu-id="cddfd-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cddfd-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cddfd-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cddfd-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cddfd-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="cddfd-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="cddfd-150">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="cddfd-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


