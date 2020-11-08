---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111336"
---
# <span data-ttu-id="dd0e4-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd0e4-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="dd0e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0e4-103">Remove um ou mais bancos de dados de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="dd0e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd0e4-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd0e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd0e4-105">DESCRIPTION</span></span>
<span data-ttu-id="dd0e4-106">Remove um ou mais bancos de dados do grupo de failover de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="dd0e4-107">Os bancos de dados e os relacionamentos de replicação são mantidos intactos, mas não poderão mais ser acessados por meio dos pontos de extremidade do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="dd0e4-108">Para obter objetos de banco de dados com os quais preencher o parâmetro '-banco de dados ', use (por exemplo) o cmdlet Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="dd0e4-109">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="dd0e4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd0e4-110">EXAMPLES</span></span>

### <span data-ttu-id="dd0e4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd0e4-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="dd0e4-112">Esse comando Remove um banco de dados de um grupo de failover canalizando-o.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="dd0e4-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dd0e4-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="dd0e4-114">Esse comando Remove todos os bancos de dados de um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="dd0e4-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dd0e4-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="dd0e4-116">Esse comando Remove todos os bancos de dados em um pool elástico de um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="dd0e4-117">OS</span><span class="sxs-lookup"><span data-stu-id="dd0e4-117">PARAMETERS</span></span>

### <span data-ttu-id="dd0e4-118">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="dd0e4-118">-Database</span></span>
<span data-ttu-id="dd0e4-119">Um ou mais bancos de dados SQL do Azure no servidor primário do grupo de failover a ser removido do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="dd0e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0e4-120">-DefaultProfile</span></span>
<span data-ttu-id="dd0e4-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dd0e4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd0e4-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="dd0e4-122">-FailoverGroupName</span></span>
<span data-ttu-id="dd0e4-123">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="dd0e4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dd0e4-124">-Force</span></span>
<span data-ttu-id="dd0e4-125">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="dd0e4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd0e4-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd0e4-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd0e4-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="dd0e4-128">-ServerName</span></span>
<span data-ttu-id="dd0e4-129">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="dd0e4-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dd0e4-130">-Confirm</span></span>
<span data-ttu-id="dd0e4-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd0e4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd0e4-132">-WhatIf</span></span>
<span data-ttu-id="dd0e4-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd0e4-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd0e4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0e4-135">CommonParameters</span></span>
<span data-ttu-id="dd0e4-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd0e4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0e4-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd0e4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0e4-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd0e4-138">INPUTS</span></span>

### <span data-ttu-id="dd0e4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dd0e4-139">System.String</span></span>

### <span data-ttu-id="dd0e4-140">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. cmdlets. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dd0e4-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dd0e4-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd0e4-141">OUTPUTS</span></span>

### <span data-ttu-id="dd0e4-142">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dd0e4-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="dd0e4-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd0e4-143">NOTES</span></span>

## <span data-ttu-id="dd0e4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd0e4-144">RELATED LINKS</span></span>

[<span data-ttu-id="dd0e4-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd0e4-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd0e4-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd0e4-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd0e4-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd0e4-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd0e4-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd0e4-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="dd0e4-149">Botão de AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd0e4-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd0e4-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dd0e4-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dd0e4-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dd0e4-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
