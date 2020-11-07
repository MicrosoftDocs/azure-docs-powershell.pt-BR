---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e83845002e090afb962272bcf9c73e158a27e374
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773547"
---
# <span data-ttu-id="6eef0-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6eef0-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="6eef0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eef0-102">SYNOPSIS</span></span>
<span data-ttu-id="6eef0-103">Exclui um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="6eef0-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="6eef0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eef0-104">SYNTAX</span></span>

### <span data-ttu-id="6eef0-105">RemoveBackupDefault (padrão)</span><span class="sxs-lookup"><span data-stu-id="6eef0-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eef0-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="6eef0-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eef0-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="6eef0-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eef0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6eef0-108">DESCRIPTION</span></span>
<span data-ttu-id="6eef0-109">O cmdlet **Remove-AzSqlDatabaseLongTermRetentionBackup** exclui o backup especificado.</span><span class="sxs-lookup"><span data-stu-id="6eef0-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="6eef0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6eef0-110">EXAMPLES</span></span>

### <span data-ttu-id="6eef0-111">Exemplo 1: excluir um único backup com o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6eef0-111">Example 1: Delete a single backup with resource group</span></span>
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

<span data-ttu-id="6eef0-112">Exclui o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="6eef0-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="6eef0-113">Exemplo 2: excluir um único backup sem o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6eef0-113">Example 2: Delete a single backup without resource group</span></span>
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

<span data-ttu-id="6eef0-114">Exclui o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="6eef0-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="6eef0-115">Exemplo 3: excluir todos os backups de um local</span><span class="sxs-lookup"><span data-stu-id="6eef0-115">Example 3: Delete all backups for a location</span></span>
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

<span data-ttu-id="6eef0-116">Esse comando exclui todos os backups de retenção de longo prazo para o local do northeurope.</span><span class="sxs-lookup"><span data-stu-id="6eef0-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="6eef0-117">OS</span><span class="sxs-lookup"><span data-stu-id="6eef0-117">PARAMETERS</span></span>

### <span data-ttu-id="6eef0-118">-Backupname</span><span class="sxs-lookup"><span data-stu-id="6eef0-118">-BackupName</span></span>
<span data-ttu-id="6eef0-119">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="6eef0-119">The name of the backup.</span></span>

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

### <span data-ttu-id="6eef0-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6eef0-120">-DatabaseName</span></span>
<span data-ttu-id="6eef0-121">O nome do banco de dados SQL do Azure do qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="6eef0-121">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="6eef0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eef0-122">-DefaultProfile</span></span>
<span data-ttu-id="6eef0-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6eef0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eef0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6eef0-124">-Force</span></span>
<span data-ttu-id="6eef0-125">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="6eef0-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6eef0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eef0-126">-InputObject</span></span>
<span data-ttu-id="6eef0-127">O objeto de backup de retenção de longo prazo do banco de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="6eef0-127">The Database Long Term Retention Backup object to remove.</span></span>

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

### <span data-ttu-id="6eef0-128">-Local</span><span class="sxs-lookup"><span data-stu-id="6eef0-128">-Location</span></span>
<span data-ttu-id="6eef0-129">O local do servidor de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="6eef0-129">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="6eef0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eef0-130">-ResourceGroupName</span></span>
<span data-ttu-id="6eef0-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6eef0-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eef0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eef0-132">-ResourceId</span></span>
<span data-ttu-id="6eef0-133">A ID do recurso do backup de retenção de longo prazo do banco de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6eef0-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="6eef0-134">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6eef0-134">-ServerName</span></span>
<span data-ttu-id="6eef0-135">O nome do Azure SQL Server no qual o backup está.</span><span class="sxs-lookup"><span data-stu-id="6eef0-135">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="6eef0-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6eef0-136">-Confirm</span></span>
<span data-ttu-id="6eef0-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eef0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eef0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eef0-138">-WhatIf</span></span>
<span data-ttu-id="6eef0-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6eef0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eef0-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6eef0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eef0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eef0-141">CommonParameters</span></span>
<span data-ttu-id="6eef0-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eef0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eef0-143">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6eef0-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eef0-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6eef0-144">INPUTS</span></span>

### <span data-ttu-id="6eef0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6eef0-145">System.String</span></span>

## <span data-ttu-id="6eef0-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6eef0-146">OUTPUTS</span></span>

### <span data-ttu-id="6eef0-147">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="6eef0-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="6eef0-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6eef0-148">NOTES</span></span>

## <span data-ttu-id="6eef0-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eef0-149">RELATED LINKS</span></span>

[<span data-ttu-id="6eef0-150">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="6eef0-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="6eef0-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6eef0-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6eef0-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6eef0-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6eef0-153">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="6eef0-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)