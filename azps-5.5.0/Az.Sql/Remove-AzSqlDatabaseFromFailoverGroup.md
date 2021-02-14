---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115731"
---
# <span data-ttu-id="dda6a-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dda6a-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="dda6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dda6a-102">SYNOPSIS</span></span>
<span data-ttu-id="dda6a-103">Remove um ou mais bancos de dados de um Grupo failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dda6a-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="dda6a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dda6a-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dda6a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dda6a-105">DESCRIPTION</span></span>
<span data-ttu-id="dda6a-106">Remove um ou mais bancos de dados do Grupo de Failover de Banco de Dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="dda6a-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="dda6a-107">Os bancos de dados e as relações de replicação são deixados intactos, mas não estarão mais acessíveis por meio dos pontos de extremidade do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="dda6a-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="dda6a-108">Para obter objetos de banco de dados com os quais preencher o parâmetro "-Banco de Dados", use (por exemplo) o cmdlet Get-AzSqlDatabase dados.</span><span class="sxs-lookup"><span data-stu-id="dda6a-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="dda6a-109">O servidor principal do Grupo de Failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="dda6a-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="dda6a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dda6a-110">EXAMPLES</span></span>

### <span data-ttu-id="dda6a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dda6a-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="dda6a-112">Esse comando remove um banco de dados de um Grupo de Failover ao insucesá-lo.</span><span class="sxs-lookup"><span data-stu-id="dda6a-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="dda6a-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dda6a-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="dda6a-114">Esse comando remove todos os bancos de dados de um Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="dda6a-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="dda6a-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dda6a-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="dda6a-116">Esse comando remove todos os bancos de dados em um Pool Elástica de um Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="dda6a-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="dda6a-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dda6a-117">PARAMETERS</span></span>

### <span data-ttu-id="dda6a-118">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="dda6a-118">-Database</span></span>
<span data-ttu-id="dda6a-119">Um ou mais bancos de dados SQL do Azure no servidor principal do Grupo de Failover a serem removidos do Grupo de Failover.</span><span class="sxs-lookup"><span data-stu-id="dda6a-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="dda6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda6a-120">-DefaultProfile</span></span>
<span data-ttu-id="dda6a-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dda6a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dda6a-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="dda6a-122">-FailoverGroupName</span></span>
<span data-ttu-id="dda6a-123">O nome do Grupo failover de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dda6a-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="dda6a-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="dda6a-124">-Force</span></span>
<span data-ttu-id="dda6a-125">Ignorar a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="dda6a-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="dda6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="dda6a-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dda6a-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="dda6a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dda6a-128">-ServerName</span></span>
<span data-ttu-id="dda6a-129">O nome do servidor de banco de dados SQL principal do Azure do Grupo failover.</span><span class="sxs-lookup"><span data-stu-id="dda6a-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="dda6a-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="dda6a-130">-Confirm</span></span>
<span data-ttu-id="dda6a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda6a-132">-WhatIf</span></span>
<span data-ttu-id="dda6a-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="dda6a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dda6a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dda6a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda6a-135">CommonParameters</span></span>
<span data-ttu-id="dda6a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda6a-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dda6a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda6a-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="dda6a-138">INPUTS</span></span>

### <span data-ttu-id="dda6a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dda6a-139">System.String</span></span>

### <span data-ttu-id="dda6a-140">System.Collections.Generic.List'1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="dda6a-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dda6a-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="dda6a-141">OUTPUTS</span></span>

### <span data-ttu-id="dda6a-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dda6a-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="dda6a-143">Notas</span><span class="sxs-lookup"><span data-stu-id="dda6a-143">NOTES</span></span>

## <span data-ttu-id="dda6a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dda6a-144">RELATED LINKS</span></span>

[<span data-ttu-id="dda6a-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dda6a-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dda6a-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dda6a-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dda6a-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dda6a-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dda6a-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dda6a-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="dda6a-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dda6a-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dda6a-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dda6a-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dda6a-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dda6a-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
