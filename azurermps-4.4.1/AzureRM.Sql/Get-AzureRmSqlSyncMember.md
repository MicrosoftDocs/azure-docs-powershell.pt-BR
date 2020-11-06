---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: bd828a88b870174b870d3acb963cdcb3b3c58ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427755"
---
# <span data-ttu-id="1eef1-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1eef1-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="1eef1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eef1-102">SYNOPSIS</span></span>
<span data-ttu-id="1eef1-103">Retorna informações sobre os membros da sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eef1-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eef1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eef1-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1eef1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eef1-105">DESCRIPTION</span></span>
<span data-ttu-id="1eef1-106">O cmdlet **Get-AzureRmSqlSyncMember** retorna informações sobre um ou mais membros de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eef1-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="1eef1-107">Especifique o nome de um membro de sincronização para ver informações somente para esse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1eef1-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="1eef1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eef1-108">EXAMPLES</span></span>

### <span data-ttu-id="1eef1-109">Exemplo 1: obter todas as instâncias do Azure SQL Sync member atribuída a um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="1eef1-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="1eef1-110">Esse comando obtém informações sobre todo o membro de sincronização do banco de dados SQL do Azure atribuído à SyncGroup01 do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1eef1-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="1eef1-111">Exemplo 2: obter informações sobre um membro de sincronização de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="1eef1-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="1eef1-112">Esse comando obtém informações sobre o membro de sincronização do banco de dados SQL do Azure com o nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="1eef1-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="1eef1-113">OS</span><span class="sxs-lookup"><span data-stu-id="1eef1-113">PARAMETERS</span></span>

### <span data-ttu-id="1eef1-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1eef1-114">-DatabaseName</span></span>
<span data-ttu-id="1eef1-115">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eef1-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1eef1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eef1-116">-Name</span></span>
<span data-ttu-id="1eef1-117">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1eef1-117">The sync member name.</span></span>

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

### <span data-ttu-id="1eef1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eef1-118">-ResourceGroupName</span></span>
<span data-ttu-id="1eef1-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1eef1-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="1eef1-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="1eef1-120">-ServerName</span></span>
<span data-ttu-id="1eef1-121">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1eef1-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1eef1-122">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1eef1-122">-SyncGroupName</span></span>
<span data-ttu-id="1eef1-123">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1eef1-123">The sync group name.</span></span>

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

### <span data-ttu-id="1eef1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eef1-124">-DefaultProfile</span></span>
<span data-ttu-id="1eef1-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eef1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eef1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eef1-126">CommonParameters</span></span>
<span data-ttu-id="1eef1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eef1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eef1-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eef1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eef1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eef1-129">INPUTS</span></span>

## <span data-ttu-id="1eef1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eef1-130">OUTPUTS</span></span>

### <span data-ttu-id="1eef1-131">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="1eef1-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="1eef1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eef1-132">NOTES</span></span>

## <span data-ttu-id="1eef1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eef1-133">RELATED LINKS</span></span>

[<span data-ttu-id="1eef1-134">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1eef1-134">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="1eef1-135">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1eef1-135">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="1eef1-136">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="1eef1-136">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

