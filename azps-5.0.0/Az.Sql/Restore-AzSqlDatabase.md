---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115818"
---
# <span data-ttu-id="0009b-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0009b-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="0009b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0009b-102">SYNOPSIS</span></span>
<span data-ttu-id="0009b-103">Restaura um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0009b-103">Restores a SQL database.</span></span>

## <span data-ttu-id="0009b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0009b-104">SYNTAX</span></span>

### <span data-ttu-id="0009b-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0009b-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0009b-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0009b-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0009b-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0009b-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0009b-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0009b-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0009b-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0009b-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0009b-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="0009b-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0009b-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0009b-113">DESCRIPTION</span></span>
<span data-ttu-id="0009b-114">O cmdlet **Restore-AzSqlDatabase** restaura um banco de dados SQL de um backup com redundância geográfica, um backup de um banco de dados excluído, um backup de retenção de longo prazo ou um point-in-time em um banco de dados dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0009b-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="0009b-115">O banco de dados restaurado é criado como um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0009b-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="0009b-116">Você pode criar um banco de dados SQL elástico definindo o parâmetro *ElasticPoolName* como um pool elástico existente.</span><span class="sxs-lookup"><span data-stu-id="0009b-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="0009b-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0009b-117">EXAMPLES</span></span>

### <span data-ttu-id="0009b-118">Exemplo 1: restaurar um banco de dados de um point-in-time</span><span class="sxs-lookup"><span data-stu-id="0009b-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="0009b-119">O primeiro comando obtém o banco de dados SQL chamado Database01 e, em seguida, armazena-o na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="0009b-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="0009b-120">O segundo comando restaura o banco de dados no $Database a partir do backup point-in-time especificado para o banco de dados chamado RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="0009b-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="0009b-121">Exemplo 2: restaurar um banco de dados de um ponto no tempo para um pool elástico</span><span class="sxs-lookup"><span data-stu-id="0009b-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="0009b-122">O primeiro comando obtém o banco de dados SQL chamado Database01 e, em seguida, armazena-o na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="0009b-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="0009b-123">O segundo comando restaura o banco de dados no $Database a partir do backup point-in-time especificado para o banco de dados SQL chamado RestoredDatabase no pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="0009b-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="0009b-124">Exemplo 3: restaurar um banco de dados excluído</span><span class="sxs-lookup"><span data-stu-id="0009b-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="0009b-125">O primeiro comando obtém o backup do banco de dados excluído que você deseja restaurar usando [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="0009b-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="0009b-126">O segundo comando inicia a restauração a partir do backup de banco de dados excluído usando o cmdlet [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="0009b-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="0009b-127">Se o parâmetro-PointInTime não for especificado, o banco de dados será restaurado para o momento de exclusão.</span><span class="sxs-lookup"><span data-stu-id="0009b-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="0009b-128">Exemplo 4: restaurar um banco de dados excluído em um pool elástico</span><span class="sxs-lookup"><span data-stu-id="0009b-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="0009b-129">O primeiro comando obtém o backup do banco de dados excluído que você deseja restaurar usando [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="0009b-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="0009b-130">O segundo comando inicia a restauração a partir do backup de banco de dados excluído usando [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="0009b-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="0009b-131">Se o parâmetro-PointInTime não for especificado, o banco de dados será restaurado para o momento de exclusão.</span><span class="sxs-lookup"><span data-stu-id="0009b-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="0009b-132">Exemplo 5: Geo-Restore um banco de dados</span><span class="sxs-lookup"><span data-stu-id="0009b-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="0009b-133">O primeiro comando obtém o backup com redundância geográfica para o banco de dados chamado Database01 e, em seguida, armazena-o na variável $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="0009b-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="0009b-134">O segundo comando restaura o backup em $GeoBackup ao banco de dados SQL chamado RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="0009b-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="0009b-135">OS</span><span class="sxs-lookup"><span data-stu-id="0009b-135">PARAMETERS</span></span>

### <span data-ttu-id="0009b-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0009b-136">-AsJob</span></span>
<span data-ttu-id="0009b-137">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0009b-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0009b-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="0009b-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="0009b-139">A redundância do armazenamento de backup usada para armazenar backups para o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0009b-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="0009b-140">Opções são: local, região e geo.</span><span class="sxs-lookup"><span data-stu-id="0009b-140">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="0009b-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0009b-141">-ComputeGeneration</span></span>
<span data-ttu-id="0009b-142">A geração de computação a ser atribuída ao banco de dados restaurado</span><span class="sxs-lookup"><span data-stu-id="0009b-142">The compute generation to assign to the restored database</span></span>

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

### <span data-ttu-id="0009b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0009b-143">-DefaultProfile</span></span>
<span data-ttu-id="0009b-144">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0009b-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0009b-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="0009b-145">-DeletionDate</span></span>
<span data-ttu-id="0009b-146">Especifica a data de exclusão como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="0009b-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="0009b-147">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="0009b-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="0009b-148">-Edição</span><span class="sxs-lookup"><span data-stu-id="0009b-148">-Edition</span></span>
<span data-ttu-id="0009b-149">Especifica a edição do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0009b-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="0009b-150">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0009b-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0009b-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0009b-151">None</span></span>
- <span data-ttu-id="0009b-152">Basic</span><span class="sxs-lookup"><span data-stu-id="0009b-152">Basic</span></span>
- <span data-ttu-id="0009b-153">Oficial</span><span class="sxs-lookup"><span data-stu-id="0009b-153">Standard</span></span>
- <span data-ttu-id="0009b-154">Gratifica</span><span class="sxs-lookup"><span data-stu-id="0009b-154">Premium</span></span>
- <span data-ttu-id="0009b-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="0009b-155">DataWarehouse</span></span>
- <span data-ttu-id="0009b-156">Gratuito</span><span class="sxs-lookup"><span data-stu-id="0009b-156">Free</span></span>
- <span data-ttu-id="0009b-157">Automático</span><span class="sxs-lookup"><span data-stu-id="0009b-157">Stretch</span></span>
- <span data-ttu-id="0009b-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0009b-158">GeneralPurpose</span></span>
- <span data-ttu-id="0009b-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0009b-159">BusinessCritical</span></span>

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

### <span data-ttu-id="0009b-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0009b-160">-ElasticPoolName</span></span>
<span data-ttu-id="0009b-161">Especifica o nome do pool elástico no qual colocar o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0009b-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

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

### <span data-ttu-id="0009b-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="0009b-163">Indica que esse cmdlet restaura um banco de dados de um backup de um banco de dados SQL excluído.</span><span class="sxs-lookup"><span data-stu-id="0009b-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="0009b-164">Você pode usar o cmdlet Get-AzSqlDeletedDatabaseBackup para obter o backup de um banco de dados SQL excluído.</span><span class="sxs-lookup"><span data-stu-id="0009b-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

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

### <span data-ttu-id="0009b-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-165">-FromGeoBackup</span></span>
<span data-ttu-id="0009b-166">Indica que esse cmdlet restaura um banco de dados SQL de um backup com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="0009b-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="0009b-167">Você pode usar o cmdlet Get-AzSqlDatabaseGeoBackup para obter um backup com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="0009b-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

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

### <span data-ttu-id="0009b-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="0009b-169">Indica que esse cmdlet restaura um banco de dados SQL de um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="0009b-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

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

### <span data-ttu-id="0009b-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="0009b-171">Indica que esse cmdlet restaura um banco de dados SQL de um backup point-in-time.</span><span class="sxs-lookup"><span data-stu-id="0009b-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

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

### <span data-ttu-id="0009b-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0009b-172">-LicenseType</span></span>
<span data-ttu-id="0009b-173">O tipo de licença para o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0009b-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0009b-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="0009b-174">-PointInTime</span></span>
<span data-ttu-id="0009b-175">Especifica o ponto no tempo, como um objeto **DateTime** , ao qual você deseja restaurar seu banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0009b-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="0009b-176">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="0009b-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0009b-177">Use esse parâmetro juntamente com o parâmetro *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="0009b-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

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

### <span data-ttu-id="0009b-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0009b-178">-ResourceGroupName</span></span>
<span data-ttu-id="0009b-179">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0009b-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="0009b-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0009b-180">-ResourceId</span></span>
<span data-ttu-id="0009b-181">Especifica a ID do recurso a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="0009b-181">Specifies the ID of the resource to restore.</span></span>

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

### <span data-ttu-id="0009b-182">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0009b-182">-ServerName</span></span>
<span data-ttu-id="0009b-183">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0009b-183">Specifies the name of the SQL database server.</span></span>

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

### <span data-ttu-id="0009b-184">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="0009b-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="0009b-185">Especifica o nome do objetivo do serviço.</span><span class="sxs-lookup"><span data-stu-id="0009b-185">Specifies the name of the service objective.</span></span>

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

### <span data-ttu-id="0009b-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0009b-186">-TargetDatabaseName</span></span>
<span data-ttu-id="0009b-187">Especifica o nome do banco de dados para o qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="0009b-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="0009b-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="0009b-188">-VCore</span></span>
<span data-ttu-id="0009b-189">Os números Vcores do banco de dados SQL restaurado do Azure.</span><span class="sxs-lookup"><span data-stu-id="0009b-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

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

### <span data-ttu-id="0009b-190">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0009b-190">-Confirm</span></span>
<span data-ttu-id="0009b-191">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0009b-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0009b-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0009b-192">-WhatIf</span></span>
<span data-ttu-id="0009b-193">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0009b-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0009b-194">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0009b-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0009b-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0009b-195">CommonParameters</span></span>
<span data-ttu-id="0009b-196">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0009b-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0009b-197">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0009b-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0009b-198">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0009b-198">INPUTS</span></span>

### <span data-ttu-id="0009b-199">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0009b-199">System.DateTime</span></span>

### <span data-ttu-id="0009b-200">System. String</span><span class="sxs-lookup"><span data-stu-id="0009b-200">System.String</span></span>

## <span data-ttu-id="0009b-201">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0009b-201">OUTPUTS</span></span>

### <span data-ttu-id="0009b-202">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0009b-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0009b-203">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0009b-203">NOTES</span></span>

## <span data-ttu-id="0009b-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0009b-204">RELATED LINKS</span></span>

[<span data-ttu-id="0009b-205">Recuperar um banco de dados SQL do Azure de uma interrupção</span><span class="sxs-lookup"><span data-stu-id="0009b-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="0009b-206">Recuperar um banco de dados SQL do Azure a partir de um erro de usuário</span><span class="sxs-lookup"><span data-stu-id="0009b-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="0009b-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0009b-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0009b-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="0009b-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="0009b-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="0009b-210">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0009b-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

