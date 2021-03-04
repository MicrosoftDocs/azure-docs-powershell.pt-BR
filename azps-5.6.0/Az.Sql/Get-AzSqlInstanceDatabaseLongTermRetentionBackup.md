---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 464334aa67be554a20c7d1b15e7d591a25979809
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888172"
---
# <span data-ttu-id="3a4fb-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3a4fb-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="3a4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4fb-103">Obtém backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="3a4fb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a4fb-104">SYNTAX</span></span>

### <span data-ttu-id="3a4fb-105">Local (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3a4fb-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4fb-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="3a4fb-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4fb-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a4fb-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4fb-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="3a4fb-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4fb-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a4fb-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4fb-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a4fb-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4fb-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a4fb-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a4fb-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a4fb-112">DESCRIPTION</span></span>
<span data-ttu-id="3a4fb-113">{{ Preencha a Descrição }}</span><span class="sxs-lookup"><span data-stu-id="3a4fb-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="3a4fb-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a4fb-114">EXAMPLES</span></span>

### <span data-ttu-id="3a4fb-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a4fb-115">Example 1</span></span>
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

<span data-ttu-id="3a4fb-116">Obtém todos os backups de retenção de longo prazo para um banco de dados específico.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="3a4fb-117">O Grupo de Recursos é opcional.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="3a4fb-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a4fb-118">PARAMETERS</span></span>

### <span data-ttu-id="3a4fb-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="3a4fb-119">-BackupName</span></span>
<span data-ttu-id="3a4fb-120">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a4fb-121">-DatabaseName</span></span>
<span data-ttu-id="3a4fb-122">O nome do Banco de Dados Gerenciado em que os backups estão.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="3a4fb-123">-DatabaseState</span></span>
<span data-ttu-id="3a4fb-124">O estado do banco de dados cujos backups você deseja encontrar, Alive, Deleted ou All.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="3a4fb-125">Padrões para Todos</span><span class="sxs-lookup"><span data-stu-id="3a4fb-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4fb-126">-DefaultProfile</span></span>
<span data-ttu-id="3a4fb-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a4fb-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a4fb-128">-InputObject</span></span>
<span data-ttu-id="3a4fb-129">O objeto database para o que fazer backups.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3a4fb-130">-InstanceName</span></span>
<span data-ttu-id="3a4fb-131">O nome da Instância Gerenciada em que os backups estão.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-132">-Location</span><span class="sxs-lookup"><span data-stu-id="3a4fb-132">-Location</span></span>
<span data-ttu-id="3a4fb-133">O local da Instância Gerenciada de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="3a4fb-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="3a4fb-135">Se só será ou não o backup mais recente por banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="3a4fb-136">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4fb-137">-ResourceGroupName</span></span>
<span data-ttu-id="3a4fb-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a4fb-139">-ResourceId</span></span>
<span data-ttu-id="3a4fb-140">A ID de Recurso do banco de dados para obter backups.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4fb-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a4fb-141">-Confirm</span></span>
<span data-ttu-id="3a4fb-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a4fb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a4fb-143">-WhatIf</span></span>
<span data-ttu-id="3a4fb-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a4fb-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a4fb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4fb-146">CommonParameters</span></span>
<span data-ttu-id="3a4fb-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a4fb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4fb-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a4fb-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4fb-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a4fb-149">INPUTS</span></span>

### <span data-ttu-id="3a4fb-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3a4fb-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="3a4fb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3a4fb-151">System.String</span></span>

## <span data-ttu-id="3a4fb-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a4fb-152">OUTPUTS</span></span>

### <span data-ttu-id="3a4fb-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="3a4fb-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="3a4fb-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a4fb-154">NOTES</span></span>

## <span data-ttu-id="3a4fb-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a4fb-155">RELATED LINKS</span></span>

[<span data-ttu-id="3a4fb-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="3a4fb-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="3a4fb-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a4fb-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3a4fb-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a4fb-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="3a4fb-159">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="3a4fb-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)