---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 9408e51cfcdab3cd2c82617ee7f8cb9bc7d3918a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944276"
---
# <span data-ttu-id="17b7c-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="17b7c-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="17b7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="17b7c-103">Obtém backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="17b7c-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="17b7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17b7c-104">SYNTAX</span></span>

### <span data-ttu-id="17b7c-105">Local (padrão)</span><span class="sxs-lookup"><span data-stu-id="17b7c-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b7c-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="17b7c-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b7c-107">NomeDoBancoDeDados</span><span class="sxs-lookup"><span data-stu-id="17b7c-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b7c-108">Backupname</span><span class="sxs-lookup"><span data-stu-id="17b7c-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b7c-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="17b7c-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b7c-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="17b7c-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b7c-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="17b7c-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17b7c-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17b7c-112">DESCRIPTION</span></span>
<span data-ttu-id="17b7c-113">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="17b7c-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="17b7c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17b7c-114">EXAMPLES</span></span>

### <span data-ttu-id="17b7c-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17b7c-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="17b7c-116">Obtém todos os backups de retenção de longo prazo para um determinado banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17b7c-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="17b7c-117">O grupo de recursos é opcional.</span><span class="sxs-lookup"><span data-stu-id="17b7c-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="17b7c-118">OS</span><span class="sxs-lookup"><span data-stu-id="17b7c-118">PARAMETERS</span></span>

### <span data-ttu-id="17b7c-119">-Backupname</span><span class="sxs-lookup"><span data-stu-id="17b7c-119">-BackupName</span></span>
<span data-ttu-id="17b7c-120">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="17b7c-120">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="17b7c-121">-DatabaseName</span></span>
<span data-ttu-id="17b7c-122">O nome do banco de dados gerenciado no qual os backups estão.</span><span class="sxs-lookup"><span data-stu-id="17b7c-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="17b7c-123">-DatabaseState</span></span>
<span data-ttu-id="17b7c-124">O estado do banco de dados cujos backups você deseja localizar, vivo, excluídos ou todos.</span><span class="sxs-lookup"><span data-stu-id="17b7c-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="17b7c-125">Todos os padrões para todos</span><span class="sxs-lookup"><span data-stu-id="17b7c-125">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b7c-126">-DefaultProfile</span></span>
<span data-ttu-id="17b7c-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17b7c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17b7c-128">-InputObject</span></span>
<span data-ttu-id="17b7c-129">O objeto de banco de dados para o qual obter backups.</span><span class="sxs-lookup"><span data-stu-id="17b7c-129">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="17b7c-130">-InstanceName</span></span>
<span data-ttu-id="17b7c-131">O nome da instância gerenciada na qual os backups estão.</span><span class="sxs-lookup"><span data-stu-id="17b7c-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-132">-Local</span><span class="sxs-lookup"><span data-stu-id="17b7c-132">-Location</span></span>
<span data-ttu-id="17b7c-133">O local da instância gerenciada de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="17b7c-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="17b7c-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="17b7c-135">Se você deve ou não obter somente o backup mais recente por banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17b7c-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="17b7c-136">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="17b7c-136">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b7c-137">-ResourceGroupName</span></span>
<span data-ttu-id="17b7c-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17b7c-138">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17b7c-139">-ResourceId</span></span>
<span data-ttu-id="17b7c-140">A ID do recurso de banco de dados para obter backups.</span><span class="sxs-lookup"><span data-stu-id="17b7c-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17b7c-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17b7c-141">-Confirm</span></span>
<span data-ttu-id="17b7c-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17b7c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b7c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b7c-143">-WhatIf</span></span>
<span data-ttu-id="17b7c-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17b7c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17b7c-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17b7c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b7c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b7c-146">CommonParameters</span></span>
<span data-ttu-id="17b7c-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b7c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b7c-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17b7c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b7c-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17b7c-149">INPUTS</span></span>

### <span data-ttu-id="17b7c-150">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="17b7c-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="17b7c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="17b7c-151">System.String</span></span>

## <span data-ttu-id="17b7c-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17b7c-152">OUTPUTS</span></span>

### <span data-ttu-id="17b7c-153">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="17b7c-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="17b7c-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17b7c-154">NOTES</span></span>

## <span data-ttu-id="17b7c-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17b7c-155">RELATED LINKS</span></span>

[<span data-ttu-id="17b7c-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="17b7c-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="17b7c-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17b7c-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="17b7c-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17b7c-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="17b7c-159">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="17b7c-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)