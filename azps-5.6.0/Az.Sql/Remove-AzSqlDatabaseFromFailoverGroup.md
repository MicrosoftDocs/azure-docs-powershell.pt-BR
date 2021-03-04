---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 556cece1b4fb22067918fb84dd1474c39d8c5aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886558"
---
# <span data-ttu-id="e24c1-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e24c1-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="e24c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e24c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e24c1-103">Remove um ou mais bancos de dados de um Grupo SQL Failover de Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="e24c1-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="e24c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e24c1-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e24c1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e24c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e24c1-106">Remove um ou mais bancos de dados do Grupo de Failover de Banco de Dados SQL Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="e24c1-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="e24c1-107">Os bancos de dados e as relações de replicação são deixados intactos, mas eles não estarão mais acessíveis por meio dos pontos de extremidade do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="e24c1-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="e24c1-108">Para obter objetos de banco de dados com os quais preencher o parâmetro '-Database', use (por exemplo) o cmdlet Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="e24c1-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="e24c1-109">O servidor principal do Grupo de Failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="e24c1-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="e24c1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e24c1-110">EXAMPLES</span></span>

### <span data-ttu-id="e24c1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e24c1-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="e24c1-112">Este comando remove um banco de dados de um Grupo de Failover canalização.</span><span class="sxs-lookup"><span data-stu-id="e24c1-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="e24c1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e24c1-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="e24c1-114">Este comando remove todos os bancos de dados de um Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="e24c1-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="e24c1-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e24c1-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="e24c1-116">Este comando remove todos os bancos de dados em um Pool Elastic de um Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="e24c1-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="e24c1-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e24c1-117">PARAMETERS</span></span>

### <span data-ttu-id="e24c1-118">-Database</span><span class="sxs-lookup"><span data-stu-id="e24c1-118">-Database</span></span>
<span data-ttu-id="e24c1-119">Um ou mais bancos de dados do Azure SQL no servidor principal do Grupo de Failover a ser removido do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="e24c1-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e24c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24c1-120">-DefaultProfile</span></span>
<span data-ttu-id="e24c1-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e24c1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e24c1-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="e24c1-122">-FailoverGroupName</span></span>
<span data-ttu-id="e24c1-123">O nome do Grupo de Failover SQL Banco de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="e24c1-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="e24c1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e24c1-124">-Force</span></span>
<span data-ttu-id="e24c1-125">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="e24c1-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="e24c1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e24c1-126">-ResourceGroupName</span></span>
<span data-ttu-id="e24c1-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e24c1-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="e24c1-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e24c1-128">-ServerName</span></span>
<span data-ttu-id="e24c1-129">O nome do Servidor de Banco de Dados do Azure SQL principal do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="e24c1-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="e24c1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e24c1-130">-Confirm</span></span>
<span data-ttu-id="e24c1-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e24c1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e24c1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24c1-132">-WhatIf</span></span>
<span data-ttu-id="e24c1-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e24c1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e24c1-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e24c1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e24c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24c1-135">CommonParameters</span></span>
<span data-ttu-id="e24c1-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e24c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24c1-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e24c1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24c1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e24c1-138">INPUTS</span></span>

### <span data-ttu-id="e24c1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e24c1-139">System.String</span></span>

### <span data-ttu-id="e24c1-140">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e24c1-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e24c1-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e24c1-141">OUTPUTS</span></span>

### <span data-ttu-id="e24c1-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e24c1-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="e24c1-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="e24c1-143">NOTES</span></span>

## <span data-ttu-id="e24c1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e24c1-144">RELATED LINKS</span></span>

[<span data-ttu-id="e24c1-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e24c1-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e24c1-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e24c1-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e24c1-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e24c1-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e24c1-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e24c1-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="e24c1-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e24c1-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e24c1-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e24c1-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="e24c1-151">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="e24c1-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
