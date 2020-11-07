---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954609"
---
# <span data-ttu-id="618df-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="618df-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="618df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="618df-102">SYNOPSIS</span></span>
<span data-ttu-id="618df-103">Retorna informações sobre os membros da sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="618df-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="618df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="618df-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="618df-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="618df-105">DESCRIPTION</span></span>
<span data-ttu-id="618df-106">O cmdlet **Get-AzSqlSyncMember** retorna informações sobre um ou mais membros de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="618df-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="618df-107">Especifique o nome de um membro de sincronização para ver informações somente para esse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="618df-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="618df-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="618df-108">EXAMPLES</span></span>

### <span data-ttu-id="618df-109">Exemplo 1: obter todas as instâncias do Azure SQL Sync member atribuída a um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="618df-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="618df-110">Esse comando obtém informações sobre todo o membro de sincronização do banco de dados SQL do Azure atribuído à SyncGroup01 do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="618df-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="618df-111">Exemplo 2: obter informações sobre um membro de sincronização de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="618df-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="618df-112">Esse comando obtém informações sobre o membro de sincronização do banco de dados SQL do Azure com o nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="618df-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="618df-113">Exemplo 3: obter todas as instâncias do membro de sincronização do SQL do Azure atribuída a um grupo de sincronização usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="618df-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="618df-114">Esse comando obtém informações sobre todos os membros de sincronização do banco de dados SQL do Azure atribuídos ao grupo de sincronização SyncGroup01 que começam com "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="618df-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="618df-115">OS</span><span class="sxs-lookup"><span data-stu-id="618df-115">PARAMETERS</span></span>

### <span data-ttu-id="618df-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="618df-116">-DatabaseName</span></span>
<span data-ttu-id="618df-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="618df-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="618df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618df-118">-DefaultProfile</span></span>
<span data-ttu-id="618df-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="618df-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="618df-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="618df-120">-Name</span></span>
<span data-ttu-id="618df-121">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="618df-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="618df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="618df-122">-ResourceGroupName</span></span>
<span data-ttu-id="618df-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="618df-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="618df-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="618df-124">-ServerName</span></span>
<span data-ttu-id="618df-125">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="618df-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="618df-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="618df-126">-SyncGroupName</span></span>
<span data-ttu-id="618df-127">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="618df-127">The sync group name.</span></span>

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

### <span data-ttu-id="618df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618df-128">CommonParameters</span></span>
<span data-ttu-id="618df-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="618df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618df-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="618df-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618df-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="618df-131">INPUTS</span></span>

### <span data-ttu-id="618df-132">System. String</span><span class="sxs-lookup"><span data-stu-id="618df-132">System.String</span></span>

## <span data-ttu-id="618df-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="618df-133">OUTPUTS</span></span>

### <span data-ttu-id="618df-134">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="618df-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="618df-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="618df-135">NOTES</span></span>

## <span data-ttu-id="618df-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="618df-136">RELATED LINKS</span></span>

[<span data-ttu-id="618df-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="618df-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="618df-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="618df-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="618df-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="618df-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

