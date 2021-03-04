---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: 1d41e42b673eccc692c317f3e9d1d20c5551da4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891611"
---
# <span data-ttu-id="3df94-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="3df94-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="3df94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df94-102">SYNOPSIS</span></span>
<span data-ttu-id="3df94-103">Obtém um banco de dados excluído que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="3df94-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="3df94-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3df94-104">SYNTAX</span></span>

### <span data-ttu-id="3df94-105">DeletedDatabaseList (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3df94-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3df94-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="3df94-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3df94-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3df94-107">DESCRIPTION</span></span>
<span data-ttu-id="3df94-108">O cmd SQL let **Get-AzSqlDeletedInstanceDatabaseBackup** obtém um backup de banco de dados de instância excluído especificado que você pode restaurar ou todos os backups excluídos que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="3df94-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="3df94-109">Esse cmdlet também é suportado pelo serviço de banco de dados de extensão SQL instância no Azure.</span><span class="sxs-lookup"><span data-stu-id="3df94-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3df94-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3df94-110">EXAMPLES</span></span>

### <span data-ttu-id="3df94-111">Exemplo 1: Obter todos os backups de banco de dados excluídos em um servidor</span><span class="sxs-lookup"><span data-stu-id="3df94-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="3df94-112">Esse comando obtém todos os backups de banco de dados excluídos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="3df94-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="3df94-113">Exemplo 2: Obter um backup de banco de dados excluído especificado</span><span class="sxs-lookup"><span data-stu-id="3df94-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="3df94-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3df94-114">PARAMETERS</span></span>

### <span data-ttu-id="3df94-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3df94-115">-DatabaseName</span></span>
<span data-ttu-id="3df94-116">O nome do Banco de Dados SQL instância do Azure para o que recuperar backups.</span><span class="sxs-lookup"><span data-stu-id="3df94-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df94-117">-DefaultProfile</span></span>
<span data-ttu-id="3df94-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3df94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df94-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="3df94-119">-DeletionDate</span></span>
<span data-ttu-id="3df94-120">A data de exclusão do Banco de Dados de Instância do Azure SQL para recuperar backups, com precisão de milissegundos (por exemplo, 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="3df94-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df94-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3df94-121">-InstanceName</span></span>
<span data-ttu-id="3df94-122">O nome da Instância Gerenciada do Azure SQL em que o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="3df94-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df94-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df94-123">-ResourceGroupName</span></span>
<span data-ttu-id="3df94-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3df94-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df94-125">CommonParameters</span></span>
<span data-ttu-id="3df94-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df94-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3df94-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df94-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3df94-128">INPUTS</span></span>

### <span data-ttu-id="3df94-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3df94-129">None</span></span>

## <span data-ttu-id="3df94-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3df94-130">OUTPUTS</span></span>

### <span data-ttu-id="3df94-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="3df94-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="3df94-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="3df94-132">NOTES</span></span>

## <span data-ttu-id="3df94-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3df94-133">RELATED LINKS</span></span>
