---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118165"
---
# <span data-ttu-id="e6b96-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="e6b96-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="e6b96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6b96-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b96-103">Retorna informações sobre o backup redundante do banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e6b96-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="e6b96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6b96-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6b96-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b96-106">O cmdlet **Get-AzSqlInstanceDatabaseGeoBackup** Obtém um ou mais backups redundantes bancos de dados SQL do Azure de uma instância gerenciada de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b96-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="e6b96-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6b96-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b96-108">Exemplo 1: obter todos os backups redundantes do banco de dados em uma instância</span><span class="sxs-lookup"><span data-stu-id="e6b96-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="e6b96-109">Esse comando obtém todos os backups redundantes do banco de dados na instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e6b96-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="e6b96-110">Exemplo 2: obter um backup redundante do banco de dados por nome em uma instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="e6b96-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="e6b96-111">Esse comando obtém um backup redundante do banco de dados chamado managedDatabase1 de uma instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="e6b96-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="e6b96-112">Exemplo 3: obter todos os backups redundantes do banco de dados em uma instância usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="e6b96-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="e6b96-113">Esse comando obtém todos os backups redundantes do banco de dados na instância chamada managedInstance1 que começam com "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="e6b96-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="e6b96-114">OS</span><span class="sxs-lookup"><span data-stu-id="e6b96-114">PARAMETERS</span></span>

### <span data-ttu-id="e6b96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b96-115">-DefaultProfile</span></span>
<span data-ttu-id="e6b96-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b96-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e6b96-117">-InstanceName</span></span>
<span data-ttu-id="e6b96-118">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="e6b96-118">The name of the instance.</span></span>

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

### <span data-ttu-id="e6b96-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6b96-119">-Name</span></span>
<span data-ttu-id="e6b96-120">O nome do banco de dados de instância a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="e6b96-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b96-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b96-121">-ResourceGroupName</span></span>
<span data-ttu-id="e6b96-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6b96-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b96-123">CommonParameters</span></span>
<span data-ttu-id="e6b96-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b96-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6b96-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b96-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6b96-126">INPUTS</span></span>

### <span data-ttu-id="e6b96-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e6b96-127">None</span></span>

## <span data-ttu-id="e6b96-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6b96-128">OUTPUTS</span></span>

### <span data-ttu-id="e6b96-129">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e6b96-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="e6b96-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6b96-130">NOTES</span></span>

## <span data-ttu-id="e6b96-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6b96-131">RELATED LINKS</span></span>
