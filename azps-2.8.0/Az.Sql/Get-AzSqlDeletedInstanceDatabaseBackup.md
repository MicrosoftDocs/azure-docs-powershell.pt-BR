---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: ce68b8c8a03fbfe99adbb6070df072dd8ebb0cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773636"
---
# <span data-ttu-id="22283-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="22283-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="22283-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22283-102">SYNOPSIS</span></span>
<span data-ttu-id="22283-103">Obtém um banco de dados excluído que você pode restaurar.</span><span class="sxs-lookup"><span data-stu-id="22283-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="22283-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22283-104">SYNTAX</span></span>

### <span data-ttu-id="22283-105">DeletedDatabaseList (padrão)</span><span class="sxs-lookup"><span data-stu-id="22283-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22283-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="22283-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22283-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22283-107">DESCRIPTION</span></span>
<span data-ttu-id="22283-108">O cmdlet **Get-AzSqlDeletedInstanceDatabaseBackup** Obtém um backup de banco de dados de instância SQL especificado, que você pode restaurar ou todos os backups excluídos que podem ser restaurados.</span><span class="sxs-lookup"><span data-stu-id="22283-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="22283-109">Esse cmdlet também é compatível com o serviço de banco de dados instância SQL Stretch no Azure.</span><span class="sxs-lookup"><span data-stu-id="22283-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="22283-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22283-110">EXAMPLES</span></span>

### <span data-ttu-id="22283-111">Exemplo 1: obter todos os backups de banco de dados excluídos em um servidor</span><span class="sxs-lookup"><span data-stu-id="22283-111">Example 1: Get all deleted database backups on a server</span></span>
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

<span data-ttu-id="22283-112">Esse comando obtém todos os backups de banco de dados excluídos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="22283-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="22283-113">Exemplo 2: obter um backup de banco de dados excluído especificado</span><span class="sxs-lookup"><span data-stu-id="22283-113">Example 2: Get a specified deleted database backup</span></span>
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

## <span data-ttu-id="22283-114">OS</span><span class="sxs-lookup"><span data-stu-id="22283-114">PARAMETERS</span></span>

### <span data-ttu-id="22283-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22283-115">-DatabaseName</span></span>
<span data-ttu-id="22283-116">O nome do banco de dados de instância SQL do Azure para a recuperação de backups.</span><span class="sxs-lookup"><span data-stu-id="22283-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="22283-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22283-117">-DefaultProfile</span></span>
<span data-ttu-id="22283-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22283-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22283-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="22283-119">-DeletionDate</span></span>
<span data-ttu-id="22283-120">A data de exclusão do banco de dados de instância SQL do Azure para recuperar backups para, com a precisão de milissegundos (por exemplo, 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="22283-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="22283-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="22283-121">-InstanceName</span></span>
<span data-ttu-id="22283-122">O nome da instância gerenciada SQL do Azure na qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="22283-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="22283-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22283-123">-ResourceGroupName</span></span>
<span data-ttu-id="22283-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22283-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="22283-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22283-125">CommonParameters</span></span>
<span data-ttu-id="22283-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22283-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22283-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22283-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22283-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22283-128">INPUTS</span></span>

### <span data-ttu-id="22283-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="22283-129">None</span></span>

## <span data-ttu-id="22283-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22283-130">OUTPUTS</span></span>

### <span data-ttu-id="22283-131">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="22283-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="22283-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22283-132">NOTES</span></span>

## <span data-ttu-id="22283-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22283-133">RELATED LINKS</span></span>
