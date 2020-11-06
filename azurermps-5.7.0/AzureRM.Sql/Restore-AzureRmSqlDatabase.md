---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: e7110511840542b8efed22b1267b76074434b94a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602343"
---
# <span data-ttu-id="e1f41-101">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1f41-101">Restore-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="e1f41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1f41-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f41-103">Restaura um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1f41-103">Restores a SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1f41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1f41-104">SYNTAX</span></span>

### <span data-ttu-id="e1f41-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-105">FromPointInTimeBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f41-106">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-106">FromDeletedDatabaseBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f41-107">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-107">FromGeoBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f41-108">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-108">FromLongTermRetentionBackup</span></span>
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f41-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1f41-109">DESCRIPTION</span></span>
<span data-ttu-id="e1f41-110">O cmdlet **Restore-AzureRmSqlDatabase** restaura um banco de dados SQL de um backup com redundância geográfica, um backup de um banco de dados excluído, um backup de retenção de longo prazo ou um point-in-time em um banco de dados dinâmico.</span><span class="sxs-lookup"><span data-stu-id="e1f41-110">The **Restore-AzureRmSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="e1f41-111">O banco de dados restaurado é criado como um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e1f41-111">The restored database is created as a new database.</span></span>

<span data-ttu-id="e1f41-112">Você pode criar um banco de dados SQL elástico definindo o parâmetro *ElasticPoolName* como um pool elástico existente.</span><span class="sxs-lookup"><span data-stu-id="e1f41-112">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="e1f41-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1f41-113">EXAMPLES</span></span>

### <span data-ttu-id="e1f41-114">Exemplo 1: restaurar um banco de dados de um point-in-time</span><span class="sxs-lookup"><span data-stu-id="e1f41-114">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="e1f41-115">O primeiro comando obtém o banco de dados SQL chamado Database01 e, em seguida, armazena-o na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="e1f41-115">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="e1f41-116">O segundo comando restaura o banco de dados no $Database a partir do backup point-in-time especificado para o banco de dados chamado RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="e1f41-116">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="e1f41-117">Exemplo 2: restaurar um banco de dados de um ponto no tempo para um pool elástico</span><span class="sxs-lookup"><span data-stu-id="e1f41-117">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="e1f41-118">O primeiro comando obtém o banco de dados SQL chamado Database01 e, em seguida, armazena-o na variável $Database.</span><span class="sxs-lookup"><span data-stu-id="e1f41-118">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="e1f41-119">O segundo comando restaura o banco de dados no $Database a partir do backup point-in-time especificado para o banco de dados SQL chamado RestoredDatabase no pool elástico chamado elasticpool01.</span><span class="sxs-lookup"><span data-stu-id="e1f41-119">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="e1f41-120">Exemplo 3: restaurar um banco de dados excluído</span><span class="sxs-lookup"><span data-stu-id="e1f41-120">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="e1f41-121">O primeiro comando obtém o backup do banco de dados excluído que você deseja restaurar usando [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="e1f41-121">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="e1f41-122">O segundo comando inicia a restauração a partir do backup de banco de dados excluído usando o cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="e1f41-122">The second command starts the restore from the deleted database backup by using the [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="e1f41-123">Se o parâmetro-PointInTime não for especificado, o banco de dados será restaurado para o momento de exclusão.</span><span class="sxs-lookup"><span data-stu-id="e1f41-123">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="e1f41-124">Exemplo 4: restaurar um banco de dados excluído em um pool elástico</span><span class="sxs-lookup"><span data-stu-id="e1f41-124">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="e1f41-125">O primeiro comando obtém o backup do banco de dados excluído que você deseja restaurar usando [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span><span class="sxs-lookup"><span data-stu-id="e1f41-125">The first command gets the deleted database backup that you want to restore by using [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="e1f41-126">O segundo comando inicia a restauração a partir do backup de banco de dados excluído usando [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span><span class="sxs-lookup"><span data-stu-id="e1f41-126">The second command starts the restore from the deleted database backup by using [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md).</span></span> <span data-ttu-id="e1f41-127">Se o parâmetro-PointInTime não for especificado, o banco de dados será restaurado para o momento de exclusão.</span><span class="sxs-lookup"><span data-stu-id="e1f41-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="e1f41-128">Exemplo 5: Geo-Restore um banco de dados</span><span class="sxs-lookup"><span data-stu-id="e1f41-128">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="e1f41-129">O primeiro comando obtém o backup com redundância geográfica para o banco de dados chamado Database01 e, em seguida, armazena-o na variável $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="e1f41-129">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>

<span data-ttu-id="e1f41-130">O segundo comando restaura o backup em $GeoBackup ao banco de dados SQL chamado RestoredDatabase.</span><span class="sxs-lookup"><span data-stu-id="e1f41-130">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="e1f41-131">OS</span><span class="sxs-lookup"><span data-stu-id="e1f41-131">PARAMETERS</span></span>

### <span data-ttu-id="e1f41-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1f41-132">-AsJob</span></span>
<span data-ttu-id="e1f41-133">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e1f41-133">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="e1f41-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f41-134">-DefaultProfile</span></span>
<span data-ttu-id="e1f41-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e1f41-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1f41-136">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="e1f41-136">-DeletionDate</span></span>
<span data-ttu-id="e1f41-137">Especifica a data de exclusão como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="e1f41-137">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="e1f41-138">Para obter um objeto **DateTime** , use o cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="e1f41-138">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-139">-Edição</span><span class="sxs-lookup"><span data-stu-id="e1f41-139">-Edition</span></span>
<span data-ttu-id="e1f41-140">Especifica a edição do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1f41-140">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="e1f41-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e1f41-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1f41-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e1f41-142">None</span></span>
- <span data-ttu-id="e1f41-143">Gratifica</span><span class="sxs-lookup"><span data-stu-id="e1f41-143">Premium</span></span>
- <span data-ttu-id="e1f41-144">Basic</span><span class="sxs-lookup"><span data-stu-id="e1f41-144">Basic</span></span>
- <span data-ttu-id="e1f41-145">Oficial</span><span class="sxs-lookup"><span data-stu-id="e1f41-145">Standard</span></span>
- <span data-ttu-id="e1f41-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="e1f41-146">DataWarehouse</span></span>
- <span data-ttu-id="e1f41-147">Gratuito</span><span class="sxs-lookup"><span data-stu-id="e1f41-147">Free</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-148">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e1f41-148">-ElasticPoolName</span></span>
<span data-ttu-id="e1f41-149">Especifica o nome do pool elástico no qual colocar o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1f41-149">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-150">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-150">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="e1f41-151">Indica que esse cmdlet restaura um banco de dados de um backup de um banco de dados SQL excluído.</span><span class="sxs-lookup"><span data-stu-id="e1f41-151">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="e1f41-152">Você pode usar o cmdlet Get-AzureRMSqlDeletedDatabaseBackup para obter o backup de um banco de dados SQL excluído.</span><span class="sxs-lookup"><span data-stu-id="e1f41-152">You can use the Get-AzureRMSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-153">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-153">-FromGeoBackup</span></span>
<span data-ttu-id="e1f41-154">Indica que esse cmdlet restaura um banco de dados SQL de um backup com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="e1f41-154">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="e1f41-155">Você pode usar o cmdlet Get-AzureRMSqlDatabaseGeoBackup para obter um backup com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="e1f41-155">You can use the Get-AzureRMSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromGeoBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-156">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-156">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="e1f41-157">Indica que esse cmdlet restaura um banco de dados SQL de um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="e1f41-157">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-158">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-158">-FromPointInTimeBackup</span></span>
<span data-ttu-id="e1f41-159">Indica que esse cmdlet restaura um banco de dados SQL de um backup point-in-time.</span><span class="sxs-lookup"><span data-stu-id="e1f41-159">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-160">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e1f41-160">-PointInTime</span></span>
<span data-ttu-id="e1f41-161">Especifica o ponto no tempo, como um objeto **DateTime** , ao qual você deseja restaurar seu banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1f41-161">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="e1f41-162">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="e1f41-162">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>

<span data-ttu-id="e1f41-163">Use esse parâmetro juntamente com o parâmetro *FromPointInTimeBackup* .</span><span class="sxs-lookup"><span data-stu-id="e1f41-163">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FromPointInTimeBackup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f41-164">-ResourceGroupName</span></span>
<span data-ttu-id="e1f41-165">Especifica o nome do grupo de recursos para o qual esse cmdlet atribui o banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1f41-165">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="e1f41-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1f41-166">-ResourceId</span></span>
<span data-ttu-id="e1f41-167">Especifica a ID do recurso a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="e1f41-167">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-168">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e1f41-168">-ServerName</span></span>
<span data-ttu-id="e1f41-169">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e1f41-169">Specifies the name of the SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-170">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="e1f41-170">-ServiceObjectiveName</span></span>
<span data-ttu-id="e1f41-171">Especifica o nome do objetivo do serviço.</span><span class="sxs-lookup"><span data-stu-id="e1f41-171">Specifies the name of the service objective.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-172">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1f41-172">-TargetDatabaseName</span></span>
<span data-ttu-id="e1f41-173">Especifica o nome do banco de dados para o qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="e1f41-173">Specifies the name of the database to restore to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f41-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f41-174">CommonParameters</span></span>
<span data-ttu-id="e1f41-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f41-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f41-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f41-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f41-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1f41-177">INPUTS</span></span>

### <span data-ttu-id="e1f41-178">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e1f41-178">None</span></span>
<span data-ttu-id="e1f41-179">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e1f41-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1f41-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1f41-180">OUTPUTS</span></span>

### <span data-ttu-id="e1f41-181">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e1f41-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e1f41-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1f41-182">NOTES</span></span>

## <span data-ttu-id="e1f41-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1f41-183">RELATED LINKS</span></span>

[<span data-ttu-id="e1f41-184">Recuperar um banco de dados SQL do Azure de uma interrupção</span><span class="sxs-lookup"><span data-stu-id="e1f41-184">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="e1f41-185">Recuperar um banco de dados SQL do Azure a partir de um erro de usuário</span><span class="sxs-lookup"><span data-stu-id="e1f41-185">Recover an Azure SQL Database from a user error</span></span>](https://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="e1f41-186">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1f41-186">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="e1f41-187">Get-AzureRMSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-187">Get-AzureRMSqlDatabaseGeoBackup</span></span>](./Get-AzureRMSqlDatabaseGeoBackup.md)

[<span data-ttu-id="e1f41-188">Get-AzureRMSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="e1f41-188">Get-AzureRMSqlDeletedDatabaseBackup</span></span>](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="e1f41-189">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e1f41-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

