---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 593a9c4764afd70003ee5c807be069eff977c6e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599023"
---
# <span data-ttu-id="2ed7f-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2ed7f-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="2ed7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ed7f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed7f-103">Obtém um ou mais backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="2ed7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ed7f-104">SYNTAX</span></span>

### <span data-ttu-id="2ed7f-105">Local (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ed7f-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed7f-106">Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2ed7f-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed7f-107">Backupname</span><span class="sxs-lookup"><span data-stu-id="2ed7f-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed7f-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ed7f-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed7f-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ed7f-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed7f-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ed7f-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed7f-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ed7f-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ed7f-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ed7f-112">DESCRIPTION</span></span>
<span data-ttu-id="2ed7f-113">O cmdlet **Get-AzSqlDatabaseLongTermRetentionBackup** Obtém todos os backups de retenção de longo prazo para um local, servidor ou banco de dados, ou Obtém um backup de retenção de longo prazo específico.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="2ed7f-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ed7f-114">EXAMPLES</span></span>

### <span data-ttu-id="2ed7f-115">Exemplo 1: obter todos os backups para um local</span><span class="sxs-lookup"><span data-stu-id="2ed7f-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2ed7f-116">Esse comando obtém todos os backups de retenção de longo prazo para todos os bancos de dados (que podem estar ativos ou excluídos) no northeurope.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="2ed7f-117">Exemplo 2: obter um backup de retenção de longo prazo específico</span><span class="sxs-lookup"><span data-stu-id="2ed7f-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2ed7f-118">Esse comando obtém o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="2ed7f-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="2ed7f-119">Exemplo 3: obter todos os backups de retenção de longo prazo para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="2ed7f-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2ed7f-120">Esse comando obtém todos os backups de retenção de longo prazo para database01</span><span class="sxs-lookup"><span data-stu-id="2ed7f-120">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="2ed7f-121">Exemplo 4: obter backups de retenção de longo prazo usando filtragem</span><span class="sxs-lookup"><span data-stu-id="2ed7f-121">Example 4: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="2ed7f-122">Esse comando obtém todos os backups com o nome que começa com "601061b7"</span><span class="sxs-lookup"><span data-stu-id="2ed7f-122">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="2ed7f-123">OS</span><span class="sxs-lookup"><span data-stu-id="2ed7f-123">PARAMETERS</span></span>

### <span data-ttu-id="2ed7f-124">-Backupname</span><span class="sxs-lookup"><span data-stu-id="2ed7f-124">-BackupName</span></span>
<span data-ttu-id="2ed7f-125">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-125">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="2ed7f-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ed7f-126">-DatabaseName</span></span>
<span data-ttu-id="2ed7f-127">O nome do banco de dados SQL do Azure do qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-127">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed7f-128">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="2ed7f-128">-DatabaseState</span></span>
<span data-ttu-id="2ed7f-129">O estado do banco de dados cujos backups você deseja localizar, vivo, excluídos ou todos.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-129">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="2ed7f-130">Todos os padrões para todos</span><span class="sxs-lookup"><span data-stu-id="2ed7f-130">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed7f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed7f-131">-DefaultProfile</span></span>
<span data-ttu-id="2ed7f-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ed7f-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ed7f-133">-InputObject</span></span>
<span data-ttu-id="2ed7f-134">O objeto de banco de dados para o qual obter backups.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-134">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed7f-135">-Local</span><span class="sxs-lookup"><span data-stu-id="2ed7f-135">-Location</span></span>
<span data-ttu-id="2ed7f-136">O local do servidor de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-136">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed7f-137">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="2ed7f-137">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="2ed7f-138">Se você deve ou não obter somente o backup mais recente por banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-138">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="2ed7f-139">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-139">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed7f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ed7f-140">-ResourceId</span></span>
<span data-ttu-id="2ed7f-141">A ID do recurso de banco de dados para obter backups.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-141">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed7f-142">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2ed7f-142">-ServerName</span></span>
<span data-ttu-id="2ed7f-143">O nome do Azure SQL Server em que os backups estão.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-143">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed7f-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2ed7f-144">-Confirm</span></span>
<span data-ttu-id="2ed7f-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed7f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed7f-146">-WhatIf</span></span>
<span data-ttu-id="2ed7f-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed7f-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed7f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed7f-149">CommonParameters</span></span>
<span data-ttu-id="2ed7f-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed7f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed7f-151">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ed7f-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed7f-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ed7f-152">INPUTS</span></span>

### <span data-ttu-id="2ed7f-153">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2ed7f-153">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="2ed7f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2ed7f-154">System.String</span></span>

## <span data-ttu-id="2ed7f-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ed7f-155">OUTPUTS</span></span>

### <span data-ttu-id="2ed7f-156">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="2ed7f-156">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="2ed7f-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ed7f-157">NOTES</span></span>

## <span data-ttu-id="2ed7f-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ed7f-158">RELATED LINKS</span></span>

[<span data-ttu-id="2ed7f-159">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2ed7f-159">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2ed7f-160">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2ed7f-160">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2ed7f-161">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2ed7f-161">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2ed7f-162">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2ed7f-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)