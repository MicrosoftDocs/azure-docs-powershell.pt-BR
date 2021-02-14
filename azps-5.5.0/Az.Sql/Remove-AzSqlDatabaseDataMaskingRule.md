---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115732"
---
# <span data-ttu-id="d6c07-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d6c07-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="d6c07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6c07-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c07-103">Remove uma regra de mascaramento de dados de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d6c07-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="d6c07-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6c07-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6c07-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6c07-105">DESCRIPTION</span></span>
<span data-ttu-id="d6c07-106">O cmdlet **Remove-AzSqlDatabaseDataMaskingRule** remove uma regra específica de mascaramento de dados de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c07-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="d6c07-107">Você pode remover uma regra de mascaramento de dados usando os parâmetros *ResourceGroupName,* *ServerName,* *DatabaseName* e *RuleId* para identificar a regra que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="d6c07-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="d6c07-108">Esse cmdlet também é suportado pelo serviço Banco de Dados de Extensão do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c07-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d6c07-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d6c07-109">EXAMPLES</span></span>

### <span data-ttu-id="d6c07-110">Exemplo 1: Remover uma regra de mascaramento de dados de banco de dados</span><span class="sxs-lookup"><span data-stu-id="d6c07-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="d6c07-111">Esse comando remove o nome da regra Rule01 definido para o Banco de Dados de Banco de Dados01.</span><span class="sxs-lookup"><span data-stu-id="d6c07-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="d6c07-112">O banco de dados está localizado no Server01 e atribuído ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d6c07-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d6c07-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6c07-113">PARAMETERS</span></span>

### <span data-ttu-id="d6c07-114">-Nomeda Coluna</span><span class="sxs-lookup"><span data-stu-id="d6c07-114">-ColumnName</span></span>
<span data-ttu-id="d6c07-115">Especifica o nome da coluna direcionada pela regra de mascaramento.</span><span class="sxs-lookup"><span data-stu-id="d6c07-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="d6c07-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="d6c07-116">-DatabaseName</span></span>
<span data-ttu-id="d6c07-117">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d6c07-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="d6c07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c07-118">-DefaultProfile</span></span>
<span data-ttu-id="d6c07-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d6c07-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6c07-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="d6c07-120">-Force</span></span>
<span data-ttu-id="d6c07-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d6c07-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6c07-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6c07-122">-PassThru</span></span>
<span data-ttu-id="d6c07-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d6c07-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d6c07-124">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="d6c07-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6c07-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c07-125">-ResourceGroupName</span></span>
<span data-ttu-id="d6c07-126">Especifica o nome do grupo de recursos ao qual o banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="d6c07-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d6c07-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d6c07-127">-SchemaName</span></span>
<span data-ttu-id="d6c07-128">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="d6c07-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="d6c07-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6c07-129">-ServerName</span></span>
<span data-ttu-id="d6c07-130">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d6c07-130">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d6c07-131">-Nomeda Tabela</span><span class="sxs-lookup"><span data-stu-id="d6c07-131">-TableName</span></span>
<span data-ttu-id="d6c07-132">Especifica o nome de uma tabela SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c07-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="d6c07-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d6c07-133">-Confirm</span></span>
<span data-ttu-id="d6c07-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6c07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6c07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c07-135">-WhatIf</span></span>
<span data-ttu-id="d6c07-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d6c07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6c07-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6c07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6c07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c07-138">CommonParameters</span></span>
<span data-ttu-id="d6c07-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6c07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c07-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6c07-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c07-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="d6c07-141">INPUTS</span></span>

### <span data-ttu-id="d6c07-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d6c07-142">System.String</span></span>

## <span data-ttu-id="d6c07-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="d6c07-143">OUTPUTS</span></span>

### <span data-ttu-id="d6c07-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="d6c07-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="d6c07-145">Notas</span><span class="sxs-lookup"><span data-stu-id="d6c07-145">NOTES</span></span>

## <span data-ttu-id="d6c07-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6c07-146">RELATED LINKS</span></span>

[<span data-ttu-id="d6c07-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d6c07-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d6c07-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d6c07-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d6c07-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="d6c07-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="d6c07-150">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d6c07-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


