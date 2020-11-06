---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 6ae416cd9ac49bc4d7f54289cd9c5b43a377d20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430015"
---
# <span data-ttu-id="4cdd1-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4cdd1-101">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="4cdd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cdd1-102">SYNOPSIS</span></span>
<span data-ttu-id="4cdd1-103">Obtém um ou mais backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-103">Gets one or more long term retention backups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cdd1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cdd1-104">SYNTAX</span></span>

### <span data-ttu-id="4cdd1-105">Local (padrão)</span><span class="sxs-lookup"><span data-stu-id="4cdd1-105">Location (Default)</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cdd1-106">Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4cdd1-106">ServerName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cdd1-107">Backupname</span><span class="sxs-lookup"><span data-stu-id="4cdd1-107">BackupName</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 -DatabaseName <String> [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cdd1-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cdd1-108">GetBackupByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cdd1-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="4cdd1-109">GetBackupsByResourceId</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cdd1-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="4cdd1-110">GetBackupByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cdd1-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="4cdd1-111">GetBackupsByInputObject</span></span>
```
Get-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cdd1-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cdd1-112">DESCRIPTION</span></span>
<span data-ttu-id="4cdd1-113">O cmdlet **Get-AzureRmSqlDatabaseLongTermRetentionBackup** Obtém todos os backups de retenção de longo prazo para um local, servidor ou banco de dados, ou Obtém um backup de retenção de longo prazo específico.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-113">The **Get-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="4cdd1-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cdd1-114">EXAMPLES</span></span>

### <span data-ttu-id="4cdd1-115">Exemplo 1: obter todos os backups para um local</span><span class="sxs-lookup"><span data-stu-id="4cdd1-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope


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

<span data-ttu-id="4cdd1-116">Esse comando obtém todos os backups de retenção de longo prazo para todos os bancos de dados (que podem estar ativos ou excluídos) no northeurope.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope.</span></span>

### <span data-ttu-id="4cdd1-117">Exemplo 2: obter um backup de retenção de longo prazo específico</span><span class="sxs-lookup"><span data-stu-id="4cdd1-117">Example 2: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="4cdd1-118">Esse comando obtém o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="4cdd1-118">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="4cdd1-119">Exemplo 3: obter todos os backups de retenção de longo prazo para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="4cdd1-119">Example 3: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzureRmSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="4cdd1-120">Esse comando obtém todos os backups de retenção de longo prazo para database01</span><span class="sxs-lookup"><span data-stu-id="4cdd1-120">This command gets all long term retention backups for database01</span></span>

## <span data-ttu-id="4cdd1-121">OS</span><span class="sxs-lookup"><span data-stu-id="4cdd1-121">PARAMETERS</span></span>

### <span data-ttu-id="4cdd1-122">-Backupname</span><span class="sxs-lookup"><span data-stu-id="4cdd1-122">-BackupName</span></span>
<span data-ttu-id="4cdd1-123">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-123">The name of the backup.</span></span>

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

### <span data-ttu-id="4cdd1-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4cdd1-124">-DatabaseName</span></span>
<span data-ttu-id="4cdd1-125">O nome do banco de dados SQL do Azure do qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-125">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="4cdd1-126">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="4cdd1-126">-DatabaseState</span></span>
<span data-ttu-id="4cdd1-127">O estado do banco de dados cujos backups você deseja localizar, vivo, excluídos ou todos.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-127">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="4cdd1-128">Todos os padrões para todos</span><span class="sxs-lookup"><span data-stu-id="4cdd1-128">Defaults to All</span></span>

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

### <span data-ttu-id="4cdd1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cdd1-129">-DefaultProfile</span></span>
<span data-ttu-id="4cdd1-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cdd1-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cdd1-131">-InputObject</span></span>
<span data-ttu-id="4cdd1-132">O objeto de banco de dados para o qual obter backups.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-132">The database object to get backups for.</span></span>

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

### <span data-ttu-id="4cdd1-133">-Local</span><span class="sxs-lookup"><span data-stu-id="4cdd1-133">-Location</span></span>
<span data-ttu-id="4cdd1-134">O local do servidor de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-134">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="4cdd1-135">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="4cdd1-135">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="4cdd1-136">Se você deve ou não obter somente o backup mais recente por banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-136">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="4cdd1-137">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-137">Defaults to false.</span></span>

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

### <span data-ttu-id="4cdd1-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cdd1-138">-ResourceId</span></span>
<span data-ttu-id="4cdd1-139">A ID do recurso de banco de dados para obter backups.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-139">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="4cdd1-140">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="4cdd1-140">-ServerName</span></span>
<span data-ttu-id="4cdd1-141">O nome do Azure SQL Server em que os backups estão.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-141">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="4cdd1-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4cdd1-142">-Confirm</span></span>
<span data-ttu-id="4cdd1-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cdd1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cdd1-144">-WhatIf</span></span>
<span data-ttu-id="4cdd1-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cdd1-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cdd1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cdd1-147">CommonParameters</span></span>
<span data-ttu-id="4cdd1-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cdd1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cdd1-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cdd1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cdd1-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cdd1-150">INPUTS</span></span>

### <span data-ttu-id="4cdd1-151">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="4cdd1-151">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>
<span data-ttu-id="4cdd1-152">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4cdd1-152">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4cdd1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="4cdd1-153">System.String</span></span>

## <span data-ttu-id="4cdd1-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cdd1-154">OUTPUTS</span></span>

### <span data-ttu-id="4cdd1-155">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="4cdd1-155">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="4cdd1-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cdd1-156">NOTES</span></span>

## <span data-ttu-id="4cdd1-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cdd1-157">RELATED LINKS</span></span>

[<span data-ttu-id="4cdd1-158">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="4cdd1-158">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="4cdd1-159">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4cdd1-159">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4cdd1-160">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4cdd1-160">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="4cdd1-161">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4cdd1-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
