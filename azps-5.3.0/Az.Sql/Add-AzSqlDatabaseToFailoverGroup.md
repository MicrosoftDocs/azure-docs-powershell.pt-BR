---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271236"
---
# <span data-ttu-id="6b557-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6b557-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="6b557-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b557-102">SYNOPSIS</span></span>
<span data-ttu-id="6b557-103">Adiciona um ou mais bancos de dados a um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b557-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="6b557-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b557-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b557-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b557-105">DESCRIPTION</span></span>
<span data-ttu-id="6b557-106">Adiciona um ou mais bancos de dados em um servidor primário do grupo de failover do banco de dados SQL do Azure para esse grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="6b557-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="6b557-107">Os bancos de dados não devem ser bancos de dados secundários em relações de replicação existentes.</span><span class="sxs-lookup"><span data-stu-id="6b557-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="6b557-108">O comando iniciará a replicação geográfica de todos os bancos de dados adicionados ao servidor secundário do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="6b557-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="6b557-109">Para obter objetos de banco de dados com os quais preencher o parâmetro '-banco de dados ', use (por exemplo) o cmdlet Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="6b557-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="6b557-110">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="6b557-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="6b557-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b557-111">EXAMPLES</span></span>

### <span data-ttu-id="6b557-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b557-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="6b557-113">Esse comando adiciona um banco de dados a um grupo de failover ao canaliza-lo.</span><span class="sxs-lookup"><span data-stu-id="6b557-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="6b557-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b557-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="6b557-115">Esse comando adiciona todos os bancos de dados em um servidor a um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="6b557-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="6b557-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6b557-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="6b557-117">Esse comando adiciona todos os bancos de dados em um pool elástico a um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="6b557-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="6b557-118">OS</span><span class="sxs-lookup"><span data-stu-id="6b557-118">PARAMETERS</span></span>

### <span data-ttu-id="6b557-119">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="6b557-119">-Database</span></span>
<span data-ttu-id="6b557-120">Um ou mais bancos de dados SQL do Azure no servidor primário do grupo de failover a ser adicionado ao grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="6b557-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="6b557-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b557-121">-DefaultProfile</span></span>
<span data-ttu-id="6b557-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6b557-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b557-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="6b557-123">-FailoverGroupName</span></span>
<span data-ttu-id="6b557-124">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b557-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="6b557-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b557-125">-ResourceGroupName</span></span>
<span data-ttu-id="6b557-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b557-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="6b557-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6b557-127">-ServerName</span></span>
<span data-ttu-id="6b557-128">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="6b557-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="6b557-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b557-129">CommonParameters</span></span>
<span data-ttu-id="6b557-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b557-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b557-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b557-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b557-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b557-132">INPUTS</span></span>

### <span data-ttu-id="6b557-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6b557-133">System.String</span></span>

### <span data-ttu-id="6b557-134">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. cmdlets. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6b557-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6b557-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b557-135">OUTPUTS</span></span>

### <span data-ttu-id="6b557-136">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6b557-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="6b557-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b557-137">NOTES</span></span>

## <span data-ttu-id="6b557-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b557-138">RELATED LINKS</span></span>

[<span data-ttu-id="6b557-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6b557-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6b557-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6b557-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6b557-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6b557-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6b557-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6b557-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="6b557-143">Botão de AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6b557-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6b557-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6b557-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="6b557-145">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="6b557-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
