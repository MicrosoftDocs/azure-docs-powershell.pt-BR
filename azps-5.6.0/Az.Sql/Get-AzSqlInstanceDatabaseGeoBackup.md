---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd66238627c96d2b3b1a8aaa2ebc7e2505515d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891585"
---
# <span data-ttu-id="92e71-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="92e71-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="92e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e71-102">SYNOPSIS</span></span>
<span data-ttu-id="92e71-103">Retorna informações sobre o backup redundante SQL banco de dados de Instância Gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="92e71-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="92e71-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92e71-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e71-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92e71-105">DESCRIPTION</span></span>
<span data-ttu-id="92e71-106">O cmdlet **Get-AzSqlInstanceDatabaseGeoBackup** obtém um ou mais backups redundantes de bancos de dados do Azure SQL de uma Instância Gerenciada de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="92e71-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="92e71-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92e71-107">EXAMPLES</span></span>

### <span data-ttu-id="92e71-108">Exemplo 1: Obter todos os backups redundantes do banco de dados em uma instância</span><span class="sxs-lookup"><span data-stu-id="92e71-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="92e71-109">Esse comando obtém todos os backups redundantes do banco de dados na instância denominada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="92e71-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="92e71-110">Exemplo 2: Obter um backup redundante de banco de dados pelo nome em uma instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="92e71-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="92e71-111">Esse comando obtém um backup redundante de banco de dados chamado managedDatabase1 de uma instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="92e71-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="92e71-112">Exemplo 3: Obter todos os backups redundantes de banco de dados em uma instância usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="92e71-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="92e71-113">Esse comando obtém todos os backups redundantes do banco de dados na instância denominada managedInstance1 que começa com "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="92e71-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="92e71-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92e71-114">PARAMETERS</span></span>

### <span data-ttu-id="92e71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e71-115">-DefaultProfile</span></span>
<span data-ttu-id="92e71-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92e71-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e71-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="92e71-117">-InstanceName</span></span>
<span data-ttu-id="92e71-118">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="92e71-118">The name of the instance.</span></span>

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

### <span data-ttu-id="92e71-119">-Name</span><span class="sxs-lookup"><span data-stu-id="92e71-119">-Name</span></span>
<span data-ttu-id="92e71-120">O nome do banco de dados de instância a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="92e71-120">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="92e71-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e71-121">-ResourceGroupName</span></span>
<span data-ttu-id="92e71-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92e71-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="92e71-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e71-123">CommonParameters</span></span>
<span data-ttu-id="92e71-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e71-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e71-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92e71-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e71-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92e71-126">INPUTS</span></span>

### <span data-ttu-id="92e71-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="92e71-127">None</span></span>

## <span data-ttu-id="92e71-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92e71-128">OUTPUTS</span></span>

### <span data-ttu-id="92e71-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="92e71-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="92e71-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="92e71-130">NOTES</span></span>

## <span data-ttu-id="92e71-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92e71-131">RELATED LINKS</span></span>
