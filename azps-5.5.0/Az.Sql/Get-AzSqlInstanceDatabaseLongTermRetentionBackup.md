---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110947"
---
# <span data-ttu-id="17b9f-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="17b9f-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="17b9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="17b9f-103">Obtém backups de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="17b9f-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="17b9f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17b9f-104">SYNTAX</span></span>

### <span data-ttu-id="17b9f-105">Local (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17b9f-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9f-106">Instancename</span><span class="sxs-lookup"><span data-stu-id="17b9f-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9f-107">Databasename</span><span class="sxs-lookup"><span data-stu-id="17b9f-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9f-108">Nome do Backup</span><span class="sxs-lookup"><span data-stu-id="17b9f-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9f-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="17b9f-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9f-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="17b9f-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9f-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="17b9f-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17b9f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="17b9f-112">DESCRIPTION</span></span>
<span data-ttu-id="17b9f-113">{{ Preencha a Descrição }}</span><span class="sxs-lookup"><span data-stu-id="17b9f-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="17b9f-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17b9f-114">EXAMPLES</span></span>

### <span data-ttu-id="17b9f-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17b9f-115">Example 1</span></span>
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

<span data-ttu-id="17b9f-116">Obtém todos os backups de retenção de longo prazo para um determinado banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17b9f-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="17b9f-117">O Grupo de Recursos é opcional.</span><span class="sxs-lookup"><span data-stu-id="17b9f-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="17b9f-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17b9f-118">PARAMETERS</span></span>

### <span data-ttu-id="17b9f-119">-Nome do Backup</span><span class="sxs-lookup"><span data-stu-id="17b9f-119">-BackupName</span></span>
<span data-ttu-id="17b9f-120">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="17b9f-120">The name of the backup.</span></span>

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

### <span data-ttu-id="17b9f-121">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="17b9f-121">-DatabaseName</span></span>
<span data-ttu-id="17b9f-122">O nome do Banco de Dados Gerenciado em que os backups estão.</span><span class="sxs-lookup"><span data-stu-id="17b9f-122">The name of the Managed Database the backups are under.</span></span>

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

### <span data-ttu-id="17b9f-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="17b9f-123">-DatabaseState</span></span>
<span data-ttu-id="17b9f-124">O estado do banco de dados cujos backups você deseja encontrar, Vivo, Excluído ou Tudo.</span><span class="sxs-lookup"><span data-stu-id="17b9f-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="17b9f-125">Padrões para Todos</span><span class="sxs-lookup"><span data-stu-id="17b9f-125">Defaults to All</span></span>

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

### <span data-ttu-id="17b9f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b9f-126">-DefaultProfile</span></span>
<span data-ttu-id="17b9f-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17b9f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b9f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17b9f-128">-InputObject</span></span>
<span data-ttu-id="17b9f-129">O objeto de banco de dados para o que obter backups.</span><span class="sxs-lookup"><span data-stu-id="17b9f-129">The database object to get backups for.</span></span>

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

### <span data-ttu-id="17b9f-130">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="17b9f-130">-InstanceName</span></span>
<span data-ttu-id="17b9f-131">O nome da Instância Gerenciada em que os backups estão.</span><span class="sxs-lookup"><span data-stu-id="17b9f-131">The name of the Managed Instance the backups are under.</span></span>

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

### <span data-ttu-id="17b9f-132">-Local</span><span class="sxs-lookup"><span data-stu-id="17b9f-132">-Location</span></span>
<span data-ttu-id="17b9f-133">O local da Instância Gerenciada de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="17b9f-133">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="17b9f-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="17b9f-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="17b9f-135">Se você quer ou não obter o backup mais recente por banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17b9f-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="17b9f-136">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="17b9f-136">Defaults to false.</span></span>

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

### <span data-ttu-id="17b9f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b9f-137">-ResourceGroupName</span></span>
<span data-ttu-id="17b9f-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17b9f-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="17b9f-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17b9f-139">-ResourceId</span></span>
<span data-ttu-id="17b9f-140">A ID de recurso do banco de dados para obter backups.</span><span class="sxs-lookup"><span data-stu-id="17b9f-140">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="17b9f-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="17b9f-141">-Confirm</span></span>
<span data-ttu-id="17b9f-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17b9f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b9f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b9f-143">-WhatIf</span></span>
<span data-ttu-id="17b9f-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="17b9f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17b9f-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17b9f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b9f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b9f-146">CommonParameters</span></span>
<span data-ttu-id="17b9f-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b9f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b9f-148">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17b9f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b9f-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="17b9f-149">INPUTS</span></span>

### <span data-ttu-id="17b9f-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="17b9f-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="17b9f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="17b9f-151">System.String</span></span>

## <span data-ttu-id="17b9f-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="17b9f-152">OUTPUTS</span></span>

### <span data-ttu-id="17b9f-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="17b9f-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="17b9f-154">Notas</span><span class="sxs-lookup"><span data-stu-id="17b9f-154">NOTES</span></span>

## <span data-ttu-id="17b9f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17b9f-155">RELATED LINKS</span></span>

[<span data-ttu-id="17b9f-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="17b9f-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="17b9f-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17b9f-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="17b9f-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17b9f-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="17b9f-159">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="17b9f-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)