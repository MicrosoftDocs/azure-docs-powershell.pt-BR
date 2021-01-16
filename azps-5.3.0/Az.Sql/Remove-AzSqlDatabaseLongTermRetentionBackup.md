---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: be2e9342407cea6ba3da0bf239ee73e7b726dd82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98264708"
---
# <span data-ttu-id="e1c3d-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e1c3d-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="e1c3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c3d-103">Exclui um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="e1c3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1c3d-104">SYNTAX</span></span>

### <span data-ttu-id="e1c3d-105">RemoveBackupDefault (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1c3d-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1c3d-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="e1c3d-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1c3d-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1c3d-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c3d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="e1c3d-109">O cmdlet **Remove-AzSqlDatabaseLongTermRetentionBackup** exclui o backup especificado.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="e1c3d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="e1c3d-111">Exemplo 1: excluir um único backup com o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e1c3d-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


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

<span data-ttu-id="e1c3d-112">Exclui o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="e1c3d-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="e1c3d-113">Exemplo 2: excluir um único backup sem o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e1c3d-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


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

<span data-ttu-id="e1c3d-114">Exclui o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="e1c3d-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="e1c3d-115">Exemplo 3: excluir todos os backups de um local</span><span class="sxs-lookup"><span data-stu-id="e1c3d-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="e1c3d-116">Esse comando exclui todos os backups de retenção de longo prazo para o local do northeurope.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="e1c3d-117">OS</span><span class="sxs-lookup"><span data-stu-id="e1c3d-117">PARAMETERS</span></span>

### <span data-ttu-id="e1c3d-118">-Backupname</span><span class="sxs-lookup"><span data-stu-id="e1c3d-118">-BackupName</span></span>
<span data-ttu-id="e1c3d-119">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-119">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1c3d-120">-DatabaseName</span></span>
<span data-ttu-id="e1c3d-121">O nome do banco de dados SQL do Azure do qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-121">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c3d-122">-DefaultProfile</span></span>
<span data-ttu-id="e1c3d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1c3d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e1c3d-124">-Force</span></span>
<span data-ttu-id="e1c3d-125">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="e1c3d-125">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1c3d-126">-InputObject</span></span>
<span data-ttu-id="e1c3d-127">O objeto de backup de retenção de longo prazo do banco de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-128">-Local</span><span class="sxs-lookup"><span data-stu-id="e1c3d-128">-Location</span></span>
<span data-ttu-id="e1c3d-129">O local do servidor de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-129">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="e1c3d-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1c3d-132">-ResourceId</span></span>
<span data-ttu-id="e1c3d-133">A ID do recurso do backup de retenção de longo prazo do banco de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-134">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e1c3d-134">-ServerName</span></span>
<span data-ttu-id="e1c3d-135">O nome do Azure SQL Server no qual o backup está.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-135">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c3d-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1c3d-136">-Confirm</span></span>
<span data-ttu-id="e1c3d-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c3d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c3d-138">-WhatIf</span></span>
<span data-ttu-id="e1c3d-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1c3d-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c3d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c3d-141">CommonParameters</span></span>
<span data-ttu-id="e1c3d-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c3d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c3d-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1c3d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c3d-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1c3d-144">INPUTS</span></span>

### <span data-ttu-id="e1c3d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e1c3d-145">System.String</span></span>

## <span data-ttu-id="e1c3d-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1c3d-146">OUTPUTS</span></span>

### <span data-ttu-id="e1c3d-147">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="e1c3d-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="e1c3d-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1c3d-148">NOTES</span></span>

## <span data-ttu-id="e1c3d-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1c3d-149">RELATED LINKS</span></span>

[<span data-ttu-id="e1c3d-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="e1c3d-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="e1c3d-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1c3d-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e1c3d-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1c3d-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="e1c3d-153">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e1c3d-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)