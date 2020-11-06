---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: fdee39766c7793b4d326077e5c18e0328a5e4c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598917"
---
# <span data-ttu-id="2b503-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="2b503-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b503-102">SYNOPSIS</span></span>
<span data-ttu-id="2b503-103">Retorna informações sobre grupos de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b503-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="2b503-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b503-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b503-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b503-105">DESCRIPTION</span></span>
<span data-ttu-id="2b503-106">O cmdlet **Get-AzSqlSyncGroup** retorna informações sobre um ou mais grupos de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b503-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="2b503-107">Especifique o nome de um grupo de sincronização para ver informações somente para esse grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="2b503-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="2b503-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b503-108">EXAMPLES</span></span>

### <span data-ttu-id="2b503-109">Exemplo 1: obter todas as instâncias do grupo Azure SQL Sync atribuída a um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="2b503-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="2b503-110">Esse comando obtém informações sobre todos os grupos de sincronização do banco de dados SQL do Azure atribuídos a um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b503-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="2b503-111">Exemplo 2: obter informações sobre um grupo de sincronização do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="2b503-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="2b503-112">Esse comando obtém informações sobre o grupo de sincronização do banco de dados SQL do Azure com o nome "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="2b503-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="2b503-113">Exemplo 3: obter todas as instâncias do grupo de sincronização do SQL do Azure atribuídas a um banco de dados SQL do Azure usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="2b503-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="2b503-114">Esse comando obtém informações sobre todos os grupos de sincronização do banco de dados SQL do Azure atribuídos a um banco de dados SQL do Azure que começam com "Sync Group".</span><span class="sxs-lookup"><span data-stu-id="2b503-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="2b503-115">OS</span><span class="sxs-lookup"><span data-stu-id="2b503-115">PARAMETERS</span></span>

### <span data-ttu-id="2b503-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b503-116">-DatabaseName</span></span>
<span data-ttu-id="2b503-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b503-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b503-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b503-118">-DefaultProfile</span></span>
<span data-ttu-id="2b503-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2b503-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b503-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b503-120">-Name</span></span>
<span data-ttu-id="2b503-121">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="2b503-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="2b503-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b503-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b503-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b503-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b503-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2b503-124">-ServerName</span></span>
<span data-ttu-id="2b503-125">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2b503-125">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b503-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b503-126">CommonParameters</span></span>
<span data-ttu-id="2b503-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b503-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b503-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b503-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b503-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b503-129">INPUTS</span></span>

### <span data-ttu-id="2b503-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2b503-130">System.String</span></span>

## <span data-ttu-id="2b503-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b503-131">OUTPUTS</span></span>

### <span data-ttu-id="2b503-132">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="2b503-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="2b503-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b503-133">NOTES</span></span>

## <span data-ttu-id="2b503-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b503-134">RELATED LINKS</span></span>

[<span data-ttu-id="2b503-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="2b503-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="2b503-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

