---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598812"
---
# <span data-ttu-id="0f725-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0f725-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="0f725-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f725-102">SYNOPSIS</span></span>
<span data-ttu-id="0f725-103">Restaura um banco de dados de instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f725-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="0f725-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f725-104">SYNTAX</span></span>

### <span data-ttu-id="0f725-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="0f725-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f725-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0f725-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f725-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="0f725-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f725-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="0f725-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f725-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0f725-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f725-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="0f725-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f725-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0f725-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f725-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0f725-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f725-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="0f725-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f725-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f725-114">DESCRIPTION</span></span>
<span data-ttu-id="0f725-115">O cmdlet **Restore-AzSqlInstanceDatabase** restaura um banco de dados de instância de um backup com redundância geográfica ou um ponto no tempo em um banco de dados dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0f725-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="0f725-116">O banco de dados restaurado é criado como um novo banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="0f725-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="0f725-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f725-117">EXAMPLES</span></span>

### <span data-ttu-id="0f725-118">Exemplo 1: restaurar um banco de dados de instância de um point-in-time</span><span class="sxs-lookup"><span data-stu-id="0f725-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="0f725-119">O comando restaura o banco de dados de instância Database01 do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="0f725-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="0f725-120">Exemplo 2: restaurar um banco de dados de instância de um ponto no tempo para outra instância em um grupo de recursos diferente</span><span class="sxs-lookup"><span data-stu-id="0f725-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="0f725-121">O comando restaura o banco de dados de instância Database01 na instância managedInstance1 no grupo de recursos ResourceGroup01 do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored na instância managedInstance2 na ResourceGroup02 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f725-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="0f725-122">Exemplo 3: Geo-Restore um banco de dados de instância</span><span class="sxs-lookup"><span data-stu-id="0f725-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="0f725-123">O primeiro comando obtém o backup com redundância geográfica para o banco de dados chamado Database01 e, em seguida, armazena-o na variável $GeoBackup.</span><span class="sxs-lookup"><span data-stu-id="0f725-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="0f725-124">O segundo comando restaura o backup em $GeoBackup ao banco de dados de instância chamado Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="0f725-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="0f725-125">OS</span><span class="sxs-lookup"><span data-stu-id="0f725-125">PARAMETERS</span></span>

### <span data-ttu-id="0f725-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f725-126">-AsJob</span></span>
<span data-ttu-id="0f725-127">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f725-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f725-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f725-128">-DefaultProfile</span></span>
<span data-ttu-id="0f725-129">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0f725-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="0f725-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="0f725-130">-FromGeoBackup</span></span>
<span data-ttu-id="0f725-131">Restaure a partir de um backup geográfico.</span><span class="sxs-lookup"><span data-stu-id="0f725-131">Restore from a geo backup.</span></span>

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

### <span data-ttu-id="0f725-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="0f725-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="0f725-133">Restaure a partir de um backup point-in-time.</span><span class="sxs-lookup"><span data-stu-id="0f725-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-134">-Geobackupobject</span><span class="sxs-lookup"><span data-stu-id="0f725-134">-GeoBackupObject</span></span>
<span data-ttu-id="0f725-135">O objeto de banco de dados instância recuperável para restauração</span><span class="sxs-lookup"><span data-stu-id="0f725-135">The recoverable instance database object to restore</span></span>

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

### <span data-ttu-id="0f725-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f725-136">-InputObject</span></span>
<span data-ttu-id="0f725-137">O objeto de banco de dados de instância a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="0f725-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0f725-138">-InstanceName</span></span>
<span data-ttu-id="0f725-139">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="0f725-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f725-140">-Name</span></span>
<span data-ttu-id="0f725-141">O nome do banco de dados de instância a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="0f725-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-142">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="0f725-142">-PointInTime</span></span>
<span data-ttu-id="0f725-143">O ponto no tempo para o qual restaurar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f725-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f725-144">-ResourceGroupName</span></span>
<span data-ttu-id="0f725-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f725-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f725-146">-ResourceId</span></span>
<span data-ttu-id="0f725-147">A ID do recurso do objeto de banco de dados de instância a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="0f725-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
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

### <span data-ttu-id="0f725-148">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f725-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="0f725-149">O nome do banco de dados de instância de destino para restauração.</span><span class="sxs-lookup"><span data-stu-id="0f725-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="0f725-150">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="0f725-150">-TargetInstanceName</span></span>
<span data-ttu-id="0f725-151">O nome da instância de destino a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="0f725-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="0f725-152">Se não for especificado, a instância de destino será a mesma que a instância de origem.</span><span class="sxs-lookup"><span data-stu-id="0f725-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f725-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="0f725-154">O nome do grupo de recursos de destino para restauração.</span><span class="sxs-lookup"><span data-stu-id="0f725-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="0f725-155">Se não for especificado, o grupo de recursos de destino será o mesmo que o grupo de recursos de origem.</span><span class="sxs-lookup"><span data-stu-id="0f725-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f725-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0f725-156">-Confirm</span></span>
<span data-ttu-id="0f725-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f725-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f725-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f725-158">-WhatIf</span></span>
<span data-ttu-id="0f725-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f725-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f725-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f725-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f725-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f725-161">CommonParameters</span></span>
<span data-ttu-id="0f725-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f725-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f725-163">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f725-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f725-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f725-164">INPUTS</span></span>

### <span data-ttu-id="0f725-165">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0f725-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="0f725-166">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0f725-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="0f725-167">System. String</span><span class="sxs-lookup"><span data-stu-id="0f725-167">System.String</span></span>

## <span data-ttu-id="0f725-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f725-168">OUTPUTS</span></span>

### <span data-ttu-id="0f725-169">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0f725-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="0f725-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f725-170">NOTES</span></span>

## <span data-ttu-id="0f725-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f725-171">RELATED LINKS</span></span>
