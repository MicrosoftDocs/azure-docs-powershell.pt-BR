---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264760"
---
# <span data-ttu-id="ec1c4-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ec1c4-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="ec1c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1c4-103">Obtém um ou mais backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="ec1c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec1c4-104">SYNTAX</span></span>

### <span data-ttu-id="ec1c4-105">Local (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec1c4-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec1c4-106">Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ec1c4-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec1c4-107">Backupname</span><span class="sxs-lookup"><span data-stu-id="ec1c4-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec1c4-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec1c4-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec1c4-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec1c4-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec1c4-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec1c4-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec1c4-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec1c4-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec1c4-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec1c4-112">DESCRIPTION</span></span>
<span data-ttu-id="ec1c4-113">O cmdlet **Get-AzSqlDatabaseLongTermRetentionBackup** Obtém todos os backups de retenção de longo prazo para um local, servidor ou banco de dados, ou Obtém um backup de retenção de longo prazo específico.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="ec1c4-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec1c4-114">EXAMPLES</span></span>

### <span data-ttu-id="ec1c4-115">Exemplo 1: obter todos os backups para um local</span><span class="sxs-lookup"><span data-stu-id="ec1c4-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="ec1c4-116">Esse comando obtém todos os backups de retenção de longo prazo para todos os bancos de dados (que podem estar ativos ou excluídos) no northeurope, o grupo de recursos só será definido se o servidor estiver ao vivo.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="ec1c4-117">Exemplo 2: obter todos os backups para um local em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ec1c4-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="ec1c4-118">Esse comando obtém todos os backups de retenção de longo prazo para todos os bancos de dados (que podem estar ativos ou excluídos) em um grupo de recursos no northeurope.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="ec1c4-119">Exemplo 3: obter um backup de retenção de longo prazo específico</span><span class="sxs-lookup"><span data-stu-id="ec1c4-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="ec1c4-120">Esse comando obtém o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="ec1c4-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="ec1c4-121">Exemplo 4: obter todos os backups de retenção de longo prazo para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="ec1c4-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="ec1c4-122">Esse comando obtém todos os backups de retenção de longo prazo para database01</span><span class="sxs-lookup"><span data-stu-id="ec1c4-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="ec1c4-123">Exemplo 5: obter backups de retenção de longo prazo usando filtragem</span><span class="sxs-lookup"><span data-stu-id="ec1c4-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="ec1c4-124">Esse comando obtém todos os backups com o nome que começa com "601061b7"</span><span class="sxs-lookup"><span data-stu-id="ec1c4-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="ec1c4-125">OS</span><span class="sxs-lookup"><span data-stu-id="ec1c4-125">PARAMETERS</span></span>

### <span data-ttu-id="ec1c4-126">-Backupname</span><span class="sxs-lookup"><span data-stu-id="ec1c4-126">-BackupName</span></span>
<span data-ttu-id="ec1c4-127">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1c4-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ec1c4-128">-DatabaseName</span></span>
<span data-ttu-id="ec1c4-129">O nome do banco de dados SQL do Azure do qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="ec1c4-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="ec1c4-130">-DatabaseState</span></span>
<span data-ttu-id="ec1c4-131">O estado do banco de dados cujos backups você deseja localizar, vivo, excluídos ou todos.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="ec1c4-132">Todos os padrões para todos</span><span class="sxs-lookup"><span data-stu-id="ec1c4-132">Defaults to All</span></span>

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

### <span data-ttu-id="ec1c4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec1c4-133">-DefaultProfile</span></span>
<span data-ttu-id="ec1c4-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec1c4-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec1c4-135">-InputObject</span></span>
<span data-ttu-id="ec1c4-136">O objeto de banco de dados para o qual obter backups.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="ec1c4-137">-Local</span><span class="sxs-lookup"><span data-stu-id="ec1c4-137">-Location</span></span>
<span data-ttu-id="ec1c4-138">O local do servidor de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="ec1c4-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="ec1c4-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="ec1c4-140">Se você deve ou não obter somente o backup mais recente por banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="ec1c4-141">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-141">Defaults to false.</span></span>

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

### <span data-ttu-id="ec1c4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec1c4-142">-ResourceGroupName</span></span>
<span data-ttu-id="ec1c4-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1c4-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec1c4-144">-ResourceId</span></span>
<span data-ttu-id="ec1c4-145">A ID do recurso de banco de dados para obter backups.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="ec1c4-146">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ec1c4-146">-ServerName</span></span>
<span data-ttu-id="ec1c4-147">O nome do Azure SQL Server em que os backups estão.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="ec1c4-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ec1c4-148">-Confirm</span></span>
<span data-ttu-id="ec1c4-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec1c4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec1c4-150">-WhatIf</span></span>
<span data-ttu-id="ec1c4-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec1c4-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec1c4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1c4-153">CommonParameters</span></span>
<span data-ttu-id="ec1c4-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec1c4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1c4-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec1c4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1c4-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec1c4-156">INPUTS</span></span>

### <span data-ttu-id="ec1c4-157">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ec1c4-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="ec1c4-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ec1c4-158">System.String</span></span>

## <span data-ttu-id="ec1c4-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec1c4-159">OUTPUTS</span></span>

### <span data-ttu-id="ec1c4-160">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="ec1c4-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="ec1c4-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec1c4-161">NOTES</span></span>

## <span data-ttu-id="ec1c4-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec1c4-162">RELATED LINKS</span></span>

[<span data-ttu-id="ec1c4-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ec1c4-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ec1c4-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec1c4-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ec1c4-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ec1c4-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ec1c4-166">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="ec1c4-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)