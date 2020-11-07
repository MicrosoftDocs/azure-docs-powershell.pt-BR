---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 5b7208c52908e560d7b2eb0abc46befafdbaf41b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940874"
---
# <span data-ttu-id="50038-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="50038-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="50038-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50038-102">SYNOPSIS</span></span>
<span data-ttu-id="50038-103">Restaura um banco de dados de instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="50038-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="50038-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50038-104">SYNTAX</span></span>

### <span data-ttu-id="50038-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="50038-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50038-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="50038-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50038-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="50038-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50038-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="50038-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50038-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="50038-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50038-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="50038-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50038-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="50038-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50038-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="50038-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50038-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="50038-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50038-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="50038-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50038-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="50038-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50038-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="50038-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50038-117">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50038-117">DESCRIPTION</span></span>
<span data-ttu-id="50038-118">O cmdlet **Restore-AzSqlInstanceDatabase** restaura um banco de dados de instância de um backup com redundância geográfica, um ponto no tempo em um banco de dados dinâmico ou um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="50038-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="50038-119">O banco de dados restaurado é criado como um novo banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="50038-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="50038-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50038-120">EXAMPLES</span></span>

### <span data-ttu-id="50038-121">Exemplo 1: restaurar um banco de dados de instância de um point-in-time</span><span class="sxs-lookup"><span data-stu-id="50038-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="50038-122">O comando restaura o banco de dados de instância Database01 do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="50038-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="50038-123">Exemplo 2: restaurar um banco de dados de instância de um ponto no tempo para outra instância em um grupo de recursos diferente</span><span class="sxs-lookup"><span data-stu-id="50038-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="50038-124">O comando restaura o banco de dados de instância Database01 na instância managedInstance1 no grupo de recursos ResourceGroup01 do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored na instância managedInstance2 na ResourceGroup02 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="50038-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="50038-125">Exemplo 3: Geo-Restore um banco de dados de instância</span><span class="sxs-lookup"><span data-stu-id="50038-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="50038-126">O primeiro comando obtém o backup com redundância geográfica para o banco de dados chamado Database01 e, em seguida, armazena-o na variável $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="50038-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="50038-127">O segundo comando restaura o backup em $GeoBackup ao banco de dados de instância chamado Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="50038-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="50038-128">Exemplo 4: restaurar um banco de dados de instância excluído de um point-in-time</span><span class="sxs-lookup"><span data-stu-id="50038-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="50038-129">O primeiro comando obtém os bancos de dados de instância excluídos chamados ' DB1 ' na instância ' managedInstance1 '.</span><span class="sxs-lookup"><span data-stu-id="50038-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="50038-130">O segundo comando restaura o banco de dados buscado, do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="50038-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="50038-131">Exemplo 5: restaurar um banco de dados de instância excluído de um point-in-time</span><span class="sxs-lookup"><span data-stu-id="50038-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="50038-132">O primeiro comando obtém os bancos de dados de instância excluídos chamados ' DB1 ' na instância ' managedInstance1 '.</span><span class="sxs-lookup"><span data-stu-id="50038-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="50038-133">O segundo comando restaura o banco de dados buscado, do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored usando objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="50038-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="50038-134">Exemplo 6: restaurar um banco de dados do backup EPD.</span><span class="sxs-lookup"><span data-stu-id="50038-134">Example 6: Restore a database from LTR backup.</span></span> 
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="50038-135">Restaura o backup EPD com o ID de recurso especificado (que pode ser encontrado executando Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span><span class="sxs-lookup"><span data-stu-id="50038-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="50038-136">OS</span><span class="sxs-lookup"><span data-stu-id="50038-136">PARAMETERS</span></span>

### <span data-ttu-id="50038-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50038-137">-AsJob</span></span>
<span data-ttu-id="50038-138">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="50038-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50038-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50038-139">-DefaultProfile</span></span>
<span data-ttu-id="50038-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="50038-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="50038-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="50038-141">-DeletionDate</span></span>
<span data-ttu-id="50038-142">A data de exclusão do banco de dados excluído.</span><span class="sxs-lookup"><span data-stu-id="50038-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="50038-143">-FromGeoBackup</span></span>
<span data-ttu-id="50038-144">Restaure a partir de um backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="50038-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="50038-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="50038-146">Restaure a partir de um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="50038-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="50038-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="50038-148">Restaure a partir de um backup point-in-time.</span><span class="sxs-lookup"><span data-stu-id="50038-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-149">-Geobackupobject</span><span class="sxs-lookup"><span data-stu-id="50038-149">-GeoBackupObject</span></span>
<span data-ttu-id="50038-150">O objeto de banco de dados instância recuperável para restauração</span><span class="sxs-lookup"><span data-stu-id="50038-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50038-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50038-151">-InputObject</span></span>
<span data-ttu-id="50038-152">O objeto de banco de dados de instância a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="50038-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50038-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="50038-153">-InstanceName</span></span>
<span data-ttu-id="50038-154">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="50038-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="50038-155">-Name</span></span>
<span data-ttu-id="50038-156">O nome do banco de dados de instância a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="50038-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-157">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="50038-157">-PointInTime</span></span>
<span data-ttu-id="50038-158">O ponto no tempo para o qual restaurar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50038-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50038-159">-ResourceGroupName</span></span>
<span data-ttu-id="50038-160">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="50038-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50038-161">-ResourceId</span></span>
<span data-ttu-id="50038-162">A ID do recurso do objeto de banco de dados de instância a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="50038-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50038-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50038-163">-SubscriptionId</span></span>
<span data-ttu-id="50038-164">ID da assinatura de origem.</span><span class="sxs-lookup"><span data-stu-id="50038-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-165">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="50038-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="50038-166">O nome do banco de dados de instância de destino para restauração.</span><span class="sxs-lookup"><span data-stu-id="50038-166">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="50038-167">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="50038-167">-TargetInstanceName</span></span>
<span data-ttu-id="50038-168">O nome da instância de destino a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="50038-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="50038-169">Se não for especificado, a instância de destino será a mesma que a instância de origem.</span><span class="sxs-lookup"><span data-stu-id="50038-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50038-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="50038-171">O nome do grupo de recursos de destino para restauração.</span><span class="sxs-lookup"><span data-stu-id="50038-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="50038-172">Se não for especificado, o grupo de recursos de destino será o mesmo que o grupo de recursos de origem.</span><span class="sxs-lookup"><span data-stu-id="50038-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50038-173">-Confirme</span><span class="sxs-lookup"><span data-stu-id="50038-173">-Confirm</span></span>
<span data-ttu-id="50038-174">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50038-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50038-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50038-175">-WhatIf</span></span>
<span data-ttu-id="50038-176">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50038-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50038-177">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50038-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50038-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50038-178">CommonParameters</span></span>
<span data-ttu-id="50038-179">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50038-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50038-180">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50038-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50038-181">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50038-181">INPUTS</span></span>

### <span data-ttu-id="50038-182">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="50038-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="50038-183">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="50038-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="50038-184">System. String</span><span class="sxs-lookup"><span data-stu-id="50038-184">System.String</span></span>

## <span data-ttu-id="50038-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50038-185">OUTPUTS</span></span>

### <span data-ttu-id="50038-186">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="50038-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="50038-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50038-187">NOTES</span></span>

## <span data-ttu-id="50038-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50038-188">RELATED LINKS</span></span>
