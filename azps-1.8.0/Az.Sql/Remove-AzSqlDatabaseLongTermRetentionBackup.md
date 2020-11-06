---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 8fd76e227951afefcbb8f7b04cf4ae3616ef5ef7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598858"
---
# <span data-ttu-id="32bcc-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="32bcc-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="32bcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="32bcc-103">Exclui um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="32bcc-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="32bcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32bcc-104">SYNTAX</span></span>

### <span data-ttu-id="32bcc-105">RemoveBackupDefault (padrão)</span><span class="sxs-lookup"><span data-stu-id="32bcc-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bcc-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="32bcc-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bcc-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="32bcc-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32bcc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32bcc-108">DESCRIPTION</span></span>
<span data-ttu-id="32bcc-109">O cmdlet **Remove-AzSqlDatabaseLongTermRetentionBackup** exclui o backup especificado.</span><span class="sxs-lookup"><span data-stu-id="32bcc-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="32bcc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32bcc-110">EXAMPLES</span></span>

### <span data-ttu-id="32bcc-111">Exemplo 1: excluir um único backup</span><span class="sxs-lookup"><span data-stu-id="32bcc-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


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

<span data-ttu-id="32bcc-112">Exclui o backup com o nome 601061b7-D10B-46e0-BF77-a2bfb16a6add; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="32bcc-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="32bcc-113">Exemplo 2: excluir todos os backups de um local</span><span class="sxs-lookup"><span data-stu-id="32bcc-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="32bcc-114">Esse comando exclui todos os backups de retenção de longo prazo para o local do northeurope.</span><span class="sxs-lookup"><span data-stu-id="32bcc-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="32bcc-115">OS</span><span class="sxs-lookup"><span data-stu-id="32bcc-115">PARAMETERS</span></span>

### <span data-ttu-id="32bcc-116">-Backupname</span><span class="sxs-lookup"><span data-stu-id="32bcc-116">-BackupName</span></span>
<span data-ttu-id="32bcc-117">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="32bcc-117">The name of the backup.</span></span>

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

### <span data-ttu-id="32bcc-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32bcc-118">-DatabaseName</span></span>
<span data-ttu-id="32bcc-119">O nome do banco de dados SQL do Azure do qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="32bcc-119">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="32bcc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bcc-120">-DefaultProfile</span></span>
<span data-ttu-id="32bcc-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32bcc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32bcc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="32bcc-122">-Force</span></span>
<span data-ttu-id="32bcc-123">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="32bcc-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="32bcc-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32bcc-124">-InputObject</span></span>
<span data-ttu-id="32bcc-125">O objeto de backup de retenção de longo prazo do banco de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="32bcc-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bcc-126">-Local</span><span class="sxs-lookup"><span data-stu-id="32bcc-126">-Location</span></span>
<span data-ttu-id="32bcc-127">O local do servidor de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="32bcc-127">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="32bcc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32bcc-128">-ResourceId</span></span>
<span data-ttu-id="32bcc-129">A ID do recurso do backup de retenção de longo prazo do banco de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="32bcc-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="32bcc-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="32bcc-130">-ServerName</span></span>
<span data-ttu-id="32bcc-131">O nome do Azure SQL Server no qual o backup está.</span><span class="sxs-lookup"><span data-stu-id="32bcc-131">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="32bcc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32bcc-132">-Confirm</span></span>
<span data-ttu-id="32bcc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32bcc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32bcc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bcc-134">-WhatIf</span></span>
<span data-ttu-id="32bcc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32bcc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32bcc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32bcc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32bcc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bcc-137">CommonParameters</span></span>
<span data-ttu-id="32bcc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32bcc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bcc-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32bcc-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bcc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32bcc-140">INPUTS</span></span>

### <span data-ttu-id="32bcc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="32bcc-141">System.String</span></span>

## <span data-ttu-id="32bcc-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32bcc-142">OUTPUTS</span></span>

### <span data-ttu-id="32bcc-143">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="32bcc-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="32bcc-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32bcc-144">NOTES</span></span>

## <span data-ttu-id="32bcc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32bcc-145">RELATED LINKS</span></span>

[<span data-ttu-id="32bcc-146">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="32bcc-146">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="32bcc-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="32bcc-147">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="32bcc-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="32bcc-148">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="32bcc-149">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="32bcc-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)