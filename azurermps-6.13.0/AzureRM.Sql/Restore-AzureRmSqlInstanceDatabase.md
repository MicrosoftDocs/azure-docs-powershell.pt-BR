---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440714"
---
# <span data-ttu-id="430fc-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="430fc-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="430fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="430fc-102">SYNOPSIS</span></span>
<span data-ttu-id="430fc-103">Restaura um banco de dados de instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="430fc-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="430fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="430fc-104">SYNTAX</span></span>

### <span data-ttu-id="430fc-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="430fc-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="430fc-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="430fc-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="430fc-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="430fc-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="430fc-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="430fc-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="430fc-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="430fc-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="430fc-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="430fc-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="430fc-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="430fc-111">DESCRIPTION</span></span>
<span data-ttu-id="430fc-112">O cmdlet **Restore-AzureRmSqlInstanceDatabase** restaura um banco de dados de instância de um ponto no tempo em um banco de dados dinâmico.</span><span class="sxs-lookup"><span data-stu-id="430fc-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="430fc-113">O banco de dados restaurado é criado como um novo banco de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="430fc-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="430fc-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="430fc-114">EXAMPLES</span></span>

### <span data-ttu-id="430fc-115">Exemplo 1: restaurar um banco de dados de instância de um point-in-time</span><span class="sxs-lookup"><span data-stu-id="430fc-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="430fc-116">O comando restaura o banco de dados de instância Database01 do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored.</span><span class="sxs-lookup"><span data-stu-id="430fc-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="430fc-117">Exemplo 2: restaurar um banco de dados de instância de um ponto no tempo para outra instância em um grupo de recursos diferente</span><span class="sxs-lookup"><span data-stu-id="430fc-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="430fc-118">O comando restaura o banco de dados de instância Database01 na instância managedInstance1 no grupo de recursos ResourceGroup01 do backup point-in-time especificado para o banco de dados de instância chamado Database01_restored na instância managedInstance2 na ResourceGroup02 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="430fc-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="430fc-119">OS</span><span class="sxs-lookup"><span data-stu-id="430fc-119">PARAMETERS</span></span>

### <span data-ttu-id="430fc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="430fc-120">-AsJob</span></span>
<span data-ttu-id="430fc-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="430fc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="430fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="430fc-122">-DefaultProfile</span></span>
<span data-ttu-id="430fc-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="430fc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="430fc-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="430fc-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="430fc-125">Restaure a partir de um backup point-in-time.</span><span class="sxs-lookup"><span data-stu-id="430fc-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="430fc-126">-InputObject</span></span>
<span data-ttu-id="430fc-127">O objeto de banco de dados de instância a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="430fc-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="430fc-128">-InstanceName</span></span>
<span data-ttu-id="430fc-129">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="430fc-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="430fc-130">-Name</span></span>
<span data-ttu-id="430fc-131">O nome do banco de dados de instância a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="430fc-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="430fc-132">-PointInTime</span></span>
<span data-ttu-id="430fc-133">O ponto no tempo para o qual restaurar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="430fc-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="430fc-134">-ResourceGroupName</span></span>
<span data-ttu-id="430fc-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="430fc-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="430fc-136">-ResourceId</span></span>
<span data-ttu-id="430fc-137">A ID do recurso do objeto de banco de dados de instância a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="430fc-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-138">-TargetInstanceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="430fc-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="430fc-139">O nome do banco de dados de instância de destino para restauração.</span><span class="sxs-lookup"><span data-stu-id="430fc-139">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="430fc-140">-TargetInstanceName</span><span class="sxs-lookup"><span data-stu-id="430fc-140">-TargetInstanceName</span></span>
<span data-ttu-id="430fc-141">O nome da instância de destino a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="430fc-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="430fc-142">Se não for especificado, a instância de destino será a mesma que a instância de origem.</span><span class="sxs-lookup"><span data-stu-id="430fc-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="430fc-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="430fc-144">O nome do grupo de recursos de destino para restauração.</span><span class="sxs-lookup"><span data-stu-id="430fc-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="430fc-145">Se não for especificado, o grupo de recursos de destino será o mesmo que o grupo de recursos de origem.</span><span class="sxs-lookup"><span data-stu-id="430fc-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="430fc-146">-Confirm</span></span>
<span data-ttu-id="430fc-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="430fc-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="430fc-148">-WhatIf</span></span>
<span data-ttu-id="430fc-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="430fc-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="430fc-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="430fc-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fc-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430fc-151">CommonParameters</span></span>
<span data-ttu-id="430fc-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="430fc-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430fc-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="430fc-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430fc-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="430fc-154">INPUTS</span></span>

### <span data-ttu-id="430fc-155">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="430fc-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="430fc-156">System. String</span><span class="sxs-lookup"><span data-stu-id="430fc-156">System.String</span></span>

## <span data-ttu-id="430fc-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="430fc-157">OUTPUTS</span></span>

### <span data-ttu-id="430fc-158">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="430fc-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="430fc-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="430fc-159">NOTES</span></span>

## <span data-ttu-id="430fc-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="430fc-160">RELATED LINKS</span></span>
