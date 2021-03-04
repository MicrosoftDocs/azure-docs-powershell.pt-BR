---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 5ba899cba4c45c3d13858d8e274b333d613106dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886397"
---
# <span data-ttu-id="5c8cc-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="5c8cc-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="5c8cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8cc-103">Obtém um backup geo-redundante de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="5c8cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5c8cc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c8cc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5c8cc-105">DESCRIPTION</span></span>
<span data-ttu-id="5c8cc-106">O cmdlet **Get-AzSqlDatabaseGeoBackup** obtém um backup geo-redundante especificado de um banco de dados SQL ou todos os backups geo-redundantes disponíveis em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="5c8cc-107">Um backup geo-redundante é um recurso restaurador usando arquivos de dados de uma localização geográfica separada.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="5c8cc-108">Você pode usar Geo-Restore para restaurar um backup geo-redundante no caso de uma paralisação regional para recuperar seu banco de dados para uma nova região.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="5c8cc-109">Esse cmdlet também é suportado pelo serviço SQL Server Banco de Dados de Extensão no Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5c8cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c8cc-110">EXAMPLES</span></span>

### <span data-ttu-id="5c8cc-111">Exemplo 1: Obter todos os backups geo-redundantes em um servidor</span><span class="sxs-lookup"><span data-stu-id="5c8cc-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="5c8cc-112">Esse comando obtém todos os backups geo-redundantes disponíveis em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="5c8cc-113">Exemplo 2: Obter um backup geo-redundante especificado</span><span class="sxs-lookup"><span data-stu-id="5c8cc-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="5c8cc-114">Este comando obtém o backup geo-redundante do banco de dados chamado ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="5c8cc-115">Exemplo 3: Obter todos os backups geo-redundantes em um servidor usando filtragem</span><span class="sxs-lookup"><span data-stu-id="5c8cc-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="5c8cc-116">Esse comando obtém todos os backups geo-redundantes disponíveis em um servidor especificado que começa com "Contoso".</span><span class="sxs-lookup"><span data-stu-id="5c8cc-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="5c8cc-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5c8cc-117">PARAMETERS</span></span>

### <span data-ttu-id="5c8cc-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c8cc-118">-DatabaseName</span></span>
<span data-ttu-id="5c8cc-119">Especifica o nome do banco de dados a ser obter.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c8cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8cc-120">-DefaultProfile</span></span>
<span data-ttu-id="5c8cc-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5c8cc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c8cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c8cc-123">Especifica o nome do grupo de recursos ao qual o SQL de banco de dados é atribuído.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="5c8cc-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5c8cc-124">-ServerName</span></span>
<span data-ttu-id="5c8cc-125">Especifica o nome do servidor que hospeda o backup a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="5c8cc-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c8cc-126">-Confirm</span></span>
<span data-ttu-id="5c8cc-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c8cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c8cc-128">-WhatIf</span></span>
<span data-ttu-id="5c8cc-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c8cc-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c8cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8cc-131">CommonParameters</span></span>
<span data-ttu-id="5c8cc-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c8cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8cc-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c8cc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8cc-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c8cc-134">INPUTS</span></span>

### <span data-ttu-id="5c8cc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5c8cc-135">System.String</span></span>

## <span data-ttu-id="5c8cc-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5c8cc-136">OUTPUTS</span></span>

### <span data-ttu-id="5c8cc-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="5c8cc-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="5c8cc-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="5c8cc-138">NOTES</span></span>

## <span data-ttu-id="5c8cc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c8cc-139">RELATED LINKS</span></span>

[<span data-ttu-id="5c8cc-140">Visão geral: continuidade de negócios na nuvem e recuperação de desastre de banco de dados com SQL Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="5c8cc-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="5c8cc-141">Recuperar um banco de dados SQL do Azure de uma paralisação</span><span class="sxs-lookup"><span data-stu-id="5c8cc-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="5c8cc-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c8cc-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="5c8cc-143">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="5c8cc-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
