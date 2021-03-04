---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: bfe2abe8a59114f69ec27f28ba0b270bfbbd72a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890958"
---
# <span data-ttu-id="40b2d-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="40b2d-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="40b2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="40b2d-103">Restaura um banco de SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="40b2d-103">Restores a SQL database.</span></span>

## <span data-ttu-id="40b2d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="40b2d-104">SYNTAX</span></span>

### <span data-ttu-id="40b2d-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40b2d-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="40b2d-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b2d-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b2d-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="40b2d-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40b2d-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b2d-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="40b2d-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b2d-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b2d-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="40b2d-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b2d-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="40b2d-113">DESCRIPTION</span></span>
<span data-ttu-id="40b2d-114">O cmdlet **Restore-AzSqlDatabase** restaura um banco de dados SQL de um backup geo-redundante, um backup de um banco de dados excluído, um backup de retenção de longo prazo ou um ponto no tempo em um banco de dados ao vivo.</span><span class="sxs-lookup"><span data-stu-id="40b2d-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="40b2d-115">O banco de dados restaurado é criado como um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="40b2d-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="40b2d-116">Você pode criar um banco de dados SQL elástica definindo o *parâmetro ElasticPoolName* para um pool elástica existente.</span><span class="sxs-lookup"><span data-stu-id="40b2d-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="40b2d-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40b2d-117">EXAMPLES</span></span>

### <span data-ttu-id="40b2d-118">Exemplo 1: Restaurar um banco de dados de um ponto no tempo</span><span class="sxs-lookup"><span data-stu-id="40b2d-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="40b2d-119">O primeiro comando obtém o SQL banco de dados chamado Database01 e o armazena na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="40b2d-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="40b2d-120">O segundo comando restaura o banco de dados em $Database do backup point-in-time especificado para o banco de dados chamado RestoreDatabase.</span><span class="sxs-lookup"><span data-stu-id="40b2d-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="40b2d-121">Exemplo 2: Restaurar um banco de dados de um ponto no tempo para um pool elástica</span><span class="sxs-lookup"><span data-stu-id="40b2d-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="40b2d-122">O primeiro comando obtém o SQL banco de dados chamado Database01 e o armazena na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="40b2d-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="40b2d-123">O segundo comando restaura o banco de dados em $Database do backup point-in-time especificado para o banco de dados SQL chamado RestoreDatabase no pool elástica chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="40b2d-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="40b2d-124">Exemplo 3: Restaurar um banco de dados excluído</span><span class="sxs-lookup"><span data-stu-id="40b2d-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="40b2d-125">O primeiro comando obtém o backup de banco de dados excluído que você deseja restaurar usando [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="40b2d-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="40b2d-126">O segundo comando inicia a restauração do backup de banco de dados excluído usando o cmdlet [Restore-AzSqlDatabase.](./Restore-AzSqlDatabase.md)</span><span class="sxs-lookup"><span data-stu-id="40b2d-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="40b2d-127">Se o parâmetro -PointInTime não for especificado, o banco de dados será restaurado para o tempo de exclusão.</span><span class="sxs-lookup"><span data-stu-id="40b2d-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="40b2d-128">Exemplo 4: Restaurar um banco de dados excluído em um pool elástica</span><span class="sxs-lookup"><span data-stu-id="40b2d-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="40b2d-129">O primeiro comando obtém o backup de banco de dados excluído que você deseja restaurar usando [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="40b2d-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="40b2d-130">O segundo comando inicia a restauração do backup de banco de dados excluído usando [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="40b2d-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="40b2d-131">Se o parâmetro -PointInTime não for especificado, o banco de dados será restaurado para o tempo de exclusão.</span><span class="sxs-lookup"><span data-stu-id="40b2d-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="40b2d-132">Exemplo 5: Geo-Restore um banco de dados</span><span class="sxs-lookup"><span data-stu-id="40b2d-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="40b2d-133">O primeiro comando obtém o backup geo-redundante para o banco de dados chamado Database01 e o armazena na variável $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="40b2d-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="40b2d-134">O segundo comando restaura o backup no $GeoBackup para o banco de dados SQL chamado RestoreDatabase.</span><span class="sxs-lookup"><span data-stu-id="40b2d-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="40b2d-135">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="40b2d-135">PARAMETERS</span></span>

### <span data-ttu-id="40b2d-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40b2d-136">-AsJob</span></span>
<span data-ttu-id="40b2d-137">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="40b2d-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40b2d-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="40b2d-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="40b2d-139">A redundância de armazenamento de backup usada para armazenar backups para o banco de dados SQL Backup.</span><span class="sxs-lookup"><span data-stu-id="40b2d-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="40b2d-140">As opções são: Local, Zona e Geo.</span><span class="sxs-lookup"><span data-stu-id="40b2d-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="40b2d-141">-ComputeGeneration</span></span>
<span data-ttu-id="40b2d-142">A geração de computação a ser atribuído ao banco de dados restaurado</span><span class="sxs-lookup"><span data-stu-id="40b2d-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b2d-143">-DefaultProfile</span></span>
<span data-ttu-id="40b2d-144">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="40b2d-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40b2d-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="40b2d-145">-DeletionDate</span></span>
<span data-ttu-id="40b2d-146">Especifica a data de exclusão como um **objeto DateTime.**</span><span class="sxs-lookup"><span data-stu-id="40b2d-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="40b2d-147">Para obter um **objeto DateTime,** use o Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40b2d-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="40b2d-148">-Edition</span></span>
<span data-ttu-id="40b2d-149">Especifica a edição do banco de dados SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="40b2d-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="40b2d-150">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="40b2d-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="40b2d-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="40b2d-151">None</span></span>
- <span data-ttu-id="40b2d-152">Básico</span><span class="sxs-lookup"><span data-stu-id="40b2d-152">Basic</span></span>
- <span data-ttu-id="40b2d-153">Standard</span><span class="sxs-lookup"><span data-stu-id="40b2d-153">Standard</span></span>
- <span data-ttu-id="40b2d-154">Premium</span><span class="sxs-lookup"><span data-stu-id="40b2d-154">Premium</span></span>
- <span data-ttu-id="40b2d-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="40b2d-155">DataWarehouse</span></span>
- <span data-ttu-id="40b2d-156">Gratuito</span><span class="sxs-lookup"><span data-stu-id="40b2d-156">Free</span></span>
- <span data-ttu-id="40b2d-157">Stretch</span><span class="sxs-lookup"><span data-stu-id="40b2d-157">Stretch</span></span>
- <span data-ttu-id="40b2d-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="40b2d-158">GeneralPurpose</span></span>
- <span data-ttu-id="40b2d-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="40b2d-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="40b2d-160">-ElasticPoolName</span></span>
<span data-ttu-id="40b2d-161">Especifica o nome do pool elástica no qual o banco de dados SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="40b2d-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="40b2d-163">Indica que esse cmdlet restaura um banco de dados de um backup de um banco de dados SQL excluído.</span><span class="sxs-lookup"><span data-stu-id="40b2d-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="40b2d-164">Você pode usar o cmdlet Get-AzSqlDeletedDatabaseBackup para obter o backup de um banco de dados SQL excluído.</span><span class="sxs-lookup"><span data-stu-id="40b2d-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-165">-FromGeoBackup</span></span>
<span data-ttu-id="40b2d-166">Indica que esse cmdlet restaura um banco de dados SQL de um backup geo-redundante.</span><span class="sxs-lookup"><span data-stu-id="40b2d-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="40b2d-167">Você pode usar o cmdlet Get-AzSqlDatabaseGeoBackup para obter um backup geo-redundante.</span><span class="sxs-lookup"><span data-stu-id="40b2d-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="40b2d-169">Indica que esse cmdlet restaura um banco de dados SQL de um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="40b2d-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="40b2d-171">Indica que esse cmdlet restaura um banco de dados SQL de um backup point-in-time.</span><span class="sxs-lookup"><span data-stu-id="40b2d-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="40b2d-172">-LicenseType</span></span>
<span data-ttu-id="40b2d-173">O tipo de licença para o banco de dados do Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="40b2d-173">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="40b2d-174">-PointInTime</span></span>
<span data-ttu-id="40b2d-175">Especifica o ponto no tempo, como um **objeto DateTime,** para o SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="40b2d-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="40b2d-176">Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="40b2d-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="40b2d-177">Use esse parâmetro junto com o *parâmetro FromPointInTimeBackup.*</span><span class="sxs-lookup"><span data-stu-id="40b2d-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b2d-178">-ResourceGroupName</span></span>
<span data-ttu-id="40b2d-179">Especifica o nome do grupo de recursos ao qual este cmdlet atribui o SQL de dados.</span><span class="sxs-lookup"><span data-stu-id="40b2d-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="40b2d-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40b2d-180">-ResourceId</span></span>
<span data-ttu-id="40b2d-181">Especifica a ID do recurso a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="40b2d-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40b2d-182">-ServerName</span></span>
<span data-ttu-id="40b2d-183">Especifica o nome do servidor SQL banco de dados.</span><span class="sxs-lookup"><span data-stu-id="40b2d-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="40b2d-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="40b2d-185">Especifica o nome do objetivo do serviço.</span><span class="sxs-lookup"><span data-stu-id="40b2d-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="40b2d-186">-TargetDatabaseName</span></span>
<span data-ttu-id="40b2d-187">Especifica o nome do banco de dados a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="40b2d-187">Specifies the name of the database to restore to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="40b2d-188">-VCore</span></span>
<span data-ttu-id="40b2d-189">Os números de Vcore do Banco de Dados Sql restaurado do Azure.</span><span class="sxs-lookup"><span data-stu-id="40b2d-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40b2d-190">-Confirm</span></span>
<span data-ttu-id="40b2d-191">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40b2d-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b2d-192">-WhatIf</span></span>
<span data-ttu-id="40b2d-193">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40b2d-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40b2d-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40b2d-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b2d-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b2d-195">CommonParameters</span></span>
<span data-ttu-id="40b2d-196">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b2d-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b2d-197">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40b2d-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b2d-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40b2d-198">INPUTS</span></span>

### <span data-ttu-id="40b2d-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="40b2d-199">System.DateTime</span></span>

### <span data-ttu-id="40b2d-200">System.String</span><span class="sxs-lookup"><span data-stu-id="40b2d-200">System.String</span></span>

## <span data-ttu-id="40b2d-201">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="40b2d-201">OUTPUTS</span></span>

### <span data-ttu-id="40b2d-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="40b2d-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="40b2d-203">NOTES</span><span class="sxs-lookup"><span data-stu-id="40b2d-203">NOTES</span></span>

## <span data-ttu-id="40b2d-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40b2d-204">RELATED LINKS</span></span>

[<span data-ttu-id="40b2d-205">Recuperar um banco de dados SQL do Azure de uma paralisação</span><span class="sxs-lookup"><span data-stu-id="40b2d-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="40b2d-206">Recuperar um banco de dados do Azure SQL de um erro de usuário</span><span class="sxs-lookup"><span data-stu-id="40b2d-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="40b2d-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="40b2d-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="40b2d-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="40b2d-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="40b2d-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="40b2d-210">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="40b2d-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

