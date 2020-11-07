---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: 8b0f67aa8e85ce9123b515f12c2e3a7da84f860d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773586"
---
# <span data-ttu-id="e9c89-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e9c89-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="e9c89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9c89-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c89-103">Retorna informações sobre os membros da sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c89-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="e9c89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9c89-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9c89-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9c89-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c89-106">O cmdlet **Get-AzSqlSyncMember** retorna informações sobre um ou mais membros de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c89-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="e9c89-107">Especifique o nome de um membro de sincronização para ver informações somente para esse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e9c89-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="e9c89-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9c89-108">EXAMPLES</span></span>

### <span data-ttu-id="e9c89-109">Exemplo 1: obter todas as instâncias do Azure SQL Sync member atribuída a um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="e9c89-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="e9c89-110">Esse comando obtém informações sobre todo o membro de sincronização do banco de dados SQL do Azure atribuído à SyncGroup01 do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e9c89-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="e9c89-111">Exemplo 2: obter informações sobre um membro de sincronização de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="e9c89-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="e9c89-112">Esse comando obtém informações sobre o membro de sincronização do banco de dados SQL do Azure com o nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="e9c89-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="e9c89-113">Exemplo 3: obter todas as instâncias do membro de sincronização do SQL do Azure atribuída a um grupo de sincronização usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="e9c89-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="e9c89-114">Esse comando obtém informações sobre todos os membros de sincronização do banco de dados SQL do Azure atribuídos ao grupo de sincronização SyncGroup01 que começam com "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="e9c89-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="e9c89-115">OS</span><span class="sxs-lookup"><span data-stu-id="e9c89-115">PARAMETERS</span></span>

### <span data-ttu-id="e9c89-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9c89-116">-DatabaseName</span></span>
<span data-ttu-id="e9c89-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c89-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e9c89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c89-118">-DefaultProfile</span></span>
<span data-ttu-id="e9c89-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e9c89-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9c89-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9c89-120">-Name</span></span>
<span data-ttu-id="e9c89-121">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e9c89-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e9c89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c89-122">-ResourceGroupName</span></span>
<span data-ttu-id="e9c89-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9c89-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9c89-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e9c89-124">-ServerName</span></span>
<span data-ttu-id="e9c89-125">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9c89-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e9c89-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c89-126">-SyncGroupName</span></span>
<span data-ttu-id="e9c89-127">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e9c89-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9c89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c89-128">CommonParameters</span></span>
<span data-ttu-id="e9c89-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c89-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9c89-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c89-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9c89-131">INPUTS</span></span>

### <span data-ttu-id="e9c89-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c89-132">System.String</span></span>

## <span data-ttu-id="e9c89-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9c89-133">OUTPUTS</span></span>

### <span data-ttu-id="e9c89-134">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e9c89-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e9c89-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9c89-135">NOTES</span></span>

## <span data-ttu-id="e9c89-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9c89-136">RELATED LINKS</span></span>

[<span data-ttu-id="e9c89-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e9c89-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="e9c89-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e9c89-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="e9c89-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e9c89-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

