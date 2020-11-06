---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: c195215bb38152287e1aa65457a5a0ff4b5452cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430831"
---
# <span data-ttu-id="dc5fa-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc5fa-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="dc5fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5fa-103">Adiciona um ou mais bancos de dados a um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc5fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc5fa-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc5fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5fa-106">Adiciona um ou mais bancos de dados em um servidor primário do grupo de failover do banco de dados SQL do Azure para esse grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="dc5fa-107">Os bancos de dados não devem ser bancos de dados secundários em relações de replicação existentes.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="dc5fa-108">O comando iniciará a replicação geográfica de todos os bancos de dados adicionados ao servidor secundário do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="dc5fa-109">Para obter objetos de banco de dados com os quais preencher o parâmetro '-banco de dados ', use (por exemplo) o cmdlet Get-AzureRmSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="dc5fa-110">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="dc5fa-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc5fa-111">EXAMPLES</span></span>

### <span data-ttu-id="dc5fa-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dc5fa-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="dc5fa-113">Esse comando adiciona um banco de dados a um grupo de failover ao canaliza-lo.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="dc5fa-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dc5fa-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="dc5fa-115">Esse comando adiciona todos os bancos de dados em um servidor a um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="dc5fa-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dc5fa-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="dc5fa-117">Esse comando adiciona todos os bancos de dados em um pool elástico a um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="dc5fa-118">OS</span><span class="sxs-lookup"><span data-stu-id="dc5fa-118">PARAMETERS</span></span>

### <span data-ttu-id="dc5fa-119">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="dc5fa-119">-Database</span></span>
<span data-ttu-id="dc5fa-120">Um ou mais bancos de dados SQL do Azure no servidor primário do grupo de failover a ser adicionado ao grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="dc5fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5fa-121">-DefaultProfile</span></span>
<span data-ttu-id="dc5fa-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dc5fa-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc5fa-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5fa-123">-FailoverGroupName</span></span>
<span data-ttu-id="dc5fa-124">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="dc5fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc5fa-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc5fa-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="dc5fa-127">-ServerName</span></span>
<span data-ttu-id="dc5fa-128">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="dc5fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5fa-129">CommonParameters</span></span>
<span data-ttu-id="dc5fa-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc5fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5fa-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5fa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5fa-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc5fa-132">INPUTS</span></span>

### <span data-ttu-id="dc5fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc5fa-133">System.String</span></span>

### <span data-ttu-id="dc5fa-134">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 4.11.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dc5fa-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dc5fa-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc5fa-135">OUTPUTS</span></span>

### <span data-ttu-id="dc5fa-136">Microsoft. Azure. Commands. Sql. failover. Model. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dc5fa-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="dc5fa-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc5fa-137">NOTES</span></span>

## <span data-ttu-id="dc5fa-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc5fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="dc5fa-139">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc5fa-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc5fa-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc5fa-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc5fa-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc5fa-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc5fa-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc5fa-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="dc5fa-143">Botão de AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc5fa-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc5fa-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dc5fa-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="dc5fa-145">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dc5fa-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
