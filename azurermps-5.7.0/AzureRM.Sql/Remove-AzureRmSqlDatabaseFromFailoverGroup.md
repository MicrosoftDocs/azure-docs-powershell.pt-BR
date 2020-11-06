---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: ba0203b328b1ae75b1f671ed3e9437a47657bb1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432874"
---
# <span data-ttu-id="cffb0-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cffb0-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="cffb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cffb0-102">SYNOPSIS</span></span>
<span data-ttu-id="cffb0-103">Remove um ou mais bancos de dados de um grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cffb0-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cffb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cffb0-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cffb0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cffb0-105">DESCRIPTION</span></span>
<span data-ttu-id="cffb0-106">Remove um ou mais bancos de dados do grupo de failover de banco de dados SQL do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="cffb0-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="cffb0-107">Os bancos de dados e os relacionamentos de replicação são mantidos intactos, mas não poderão mais ser acessados por meio dos pontos de extremidade do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="cffb0-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="cffb0-108">Para obter objetos de banco de dados com os quais preencher o parâmetro '-banco de dados ', use (por exemplo) o cmdlet Get-AzureRmSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="cffb0-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="cffb0-109">O servidor primário do grupo de failover deve ser usado para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="cffb0-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="cffb0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cffb0-110">EXAMPLES</span></span>

### <span data-ttu-id="cffb0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cffb0-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="cffb0-112">Esse comando Remove um banco de dados de um grupo de failover canalizando-o.</span><span class="sxs-lookup"><span data-stu-id="cffb0-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="cffb0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cffb0-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="cffb0-114">Esse comando Remove todos os bancos de dados de um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="cffb0-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="cffb0-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cffb0-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="cffb0-116">Esse comando Remove todos os bancos de dados em um pool elástico de um grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="cffb0-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="cffb0-117">OS</span><span class="sxs-lookup"><span data-stu-id="cffb0-117">PARAMETERS</span></span>

### <span data-ttu-id="cffb0-118">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="cffb0-118">-Database</span></span>
<span data-ttu-id="cffb0-119">Um ou mais bancos de dados SQL do Azure no servidor primário do grupo de failover a ser removido do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="cffb0-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="cffb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cffb0-120">-DefaultProfile</span></span>
<span data-ttu-id="cffb0-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cffb0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="cffb0-122">-FailoverGroupName</span></span>
<span data-ttu-id="cffb0-123">O nome do grupo de failover do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cffb0-123">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cffb0-124">-Force</span></span>
<span data-ttu-id="cffb0-125">Ignore a mensagem de confirmação para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="cffb0-125">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cffb0-126">-ResourceGroupName</span></span>
<span data-ttu-id="cffb0-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cffb0-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="cffb0-128">-ServerName</span></span>
<span data-ttu-id="cffb0-129">O nome do servidor de banco de dados SQL do Azure principal do grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="cffb0-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cffb0-130">-Confirm</span></span>
<span data-ttu-id="cffb0-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cffb0-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cffb0-132">-WhatIf</span></span>
<span data-ttu-id="cffb0-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cffb0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cffb0-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cffb0-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cffb0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cffb0-135">CommonParameters</span></span>
<span data-ttu-id="cffb0-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cffb0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cffb0-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cffb0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cffb0-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cffb0-138">INPUTS</span></span>

### <span data-ttu-id="cffb0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cffb0-139">System.String</span></span>
<span data-ttu-id="cffb0-140">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cffb0-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cffb0-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cffb0-141">OUTPUTS</span></span>

### <span data-ttu-id="cffb0-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="cffb0-142">System.Object</span></span>

## <span data-ttu-id="cffb0-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cffb0-143">NOTES</span></span>

## <span data-ttu-id="cffb0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cffb0-144">RELATED LINKS</span></span>

[<span data-ttu-id="cffb0-145">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cffb0-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cffb0-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cffb0-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cffb0-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cffb0-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cffb0-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cffb0-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="cffb0-149">Botão de AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cffb0-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cffb0-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cffb0-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cffb0-151">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="cffb0-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)