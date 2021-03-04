---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: c9c3aff7d449c12cd3514518fc68d8ca50dbec0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891551"
---
# <span data-ttu-id="6cf55-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cf55-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="6cf55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf55-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf55-103">Retorna informações sobre os membros de sincronização SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="6cf55-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="6cf55-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6cf55-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf55-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6cf55-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf55-106">O cmdlet **Get-AzSqlSyncMember** retorna informações sobre um ou mais membros de sincronização de banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6cf55-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="6cf55-107">Especifique o nome de um membro de sincronização para ver informações apenas para esse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6cf55-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="6cf55-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cf55-108">EXAMPLES</span></span>

### <span data-ttu-id="6cf55-109">Exemplo 1: Obter todas as instâncias do Azure SQL Membro de Sincronização atribuído a um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="6cf55-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="6cf55-110">Este comando obtém informações sobre todo o Membro de Sincronização de Banco de Dados do Azure SQL atribuído ao grupo de sincronização SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="6cf55-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="6cf55-111">Exemplo 2: obter informações sobre um membro de sincronização de banco de dados do Azure SQL banco de dados</span><span class="sxs-lookup"><span data-stu-id="6cf55-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="6cf55-112">Este comando obtém informações sobre o Membro de Sincronização de Banco de Dados do Azure SQL com o nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="6cf55-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="6cf55-113">Exemplo 3: Obter todas as instâncias do Membro de Sincronização do Azure SQL atribuído a um grupo de sincronização usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="6cf55-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="6cf55-114">Este comando obtém informações sobre todos os Membros de Sincronização de Banco de Dados do Azure SQL atribuídos ao grupo de sincronização SyncGroup01 que começam com "SyncMember".</span><span class="sxs-lookup"><span data-stu-id="6cf55-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="6cf55-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6cf55-115">PARAMETERS</span></span>

### <span data-ttu-id="6cf55-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cf55-116">-DatabaseName</span></span>
<span data-ttu-id="6cf55-117">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6cf55-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6cf55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf55-118">-DefaultProfile</span></span>
<span data-ttu-id="6cf55-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6cf55-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cf55-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6cf55-120">-Name</span></span>
<span data-ttu-id="6cf55-121">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6cf55-121">The sync member name.</span></span>

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

### <span data-ttu-id="6cf55-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf55-122">-ResourceGroupName</span></span>
<span data-ttu-id="6cf55-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cf55-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cf55-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6cf55-124">-ServerName</span></span>
<span data-ttu-id="6cf55-125">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6cf55-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6cf55-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf55-126">-SyncGroupName</span></span>
<span data-ttu-id="6cf55-127">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6cf55-127">The sync group name.</span></span>

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

### <span data-ttu-id="6cf55-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf55-128">CommonParameters</span></span>
<span data-ttu-id="6cf55-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf55-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf55-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cf55-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf55-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cf55-131">INPUTS</span></span>

### <span data-ttu-id="6cf55-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6cf55-132">System.String</span></span>

## <span data-ttu-id="6cf55-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6cf55-133">OUTPUTS</span></span>

### <span data-ttu-id="6cf55-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="6cf55-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="6cf55-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="6cf55-135">NOTES</span></span>

## <span data-ttu-id="6cf55-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cf55-136">RELATED LINKS</span></span>

[<span data-ttu-id="6cf55-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cf55-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="6cf55-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cf55-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="6cf55-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6cf55-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

