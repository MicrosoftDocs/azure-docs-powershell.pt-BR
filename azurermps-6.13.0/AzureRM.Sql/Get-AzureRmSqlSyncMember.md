---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: 30a73047282508adc0c2aa0d0d64a61f9f70e71a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440018"
---
# <span data-ttu-id="ed7d8-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ed7d8-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="ed7d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7d8-103">Retorna informações sobre os membros da sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed7d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed7d8-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed7d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed7d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ed7d8-106">O cmdlet **Get-AzureRmSqlSyncMember** retorna informações sobre um ou mais membros de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="ed7d8-107">Especifique o nome de um membro de sincronização para ver informações somente para esse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="ed7d8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed7d8-108">EXAMPLES</span></span>

### <span data-ttu-id="ed7d8-109">Exemplo 1: obter todas as instâncias do Azure SQL Sync member atribuída a um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="ed7d8-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="ed7d8-110">Esse comando obtém informações sobre todo o membro de sincronização do banco de dados SQL do Azure atribuído à SyncGroup01 do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="ed7d8-111">Exemplo 2: obter informações sobre um membro de sincronização de banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ed7d8-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="ed7d8-112">Esse comando obtém informações sobre o membro de sincronização do banco de dados SQL do Azure com o nome "SyncMember01"</span><span class="sxs-lookup"><span data-stu-id="ed7d8-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="ed7d8-113">OS</span><span class="sxs-lookup"><span data-stu-id="ed7d8-113">PARAMETERS</span></span>

### <span data-ttu-id="ed7d8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed7d8-114">-DatabaseName</span></span>
<span data-ttu-id="ed7d8-115">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ed7d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7d8-116">-DefaultProfile</span></span>
<span data-ttu-id="ed7d8-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ed7d8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed7d8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed7d8-118">-Name</span></span>
<span data-ttu-id="ed7d8-119">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-119">The sync member name.</span></span>

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

### <span data-ttu-id="ed7d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed7d8-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed7d8-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ed7d8-122">-ServerName</span></span>
<span data-ttu-id="ed7d8-123">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ed7d8-124">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7d8-124">-SyncGroupName</span></span>
<span data-ttu-id="ed7d8-125">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-125">The sync group name.</span></span>

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

### <span data-ttu-id="ed7d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7d8-126">CommonParameters</span></span>
<span data-ttu-id="ed7d8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed7d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7d8-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7d8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7d8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed7d8-129">INPUTS</span></span>

### <span data-ttu-id="ed7d8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ed7d8-130">System.String</span></span>

## <span data-ttu-id="ed7d8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed7d8-131">OUTPUTS</span></span>

### <span data-ttu-id="ed7d8-132">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ed7d8-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ed7d8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed7d8-133">NOTES</span></span>

## <span data-ttu-id="ed7d8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed7d8-134">RELATED LINKS</span></span>

[<span data-ttu-id="ed7d8-135">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ed7d8-135">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="ed7d8-136">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ed7d8-136">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="ed7d8-137">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ed7d8-137">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

