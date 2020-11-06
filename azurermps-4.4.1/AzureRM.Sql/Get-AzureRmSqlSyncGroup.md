---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: e581f0bd94e58f725055c0dc1a4f1d704b891c86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602191"
---
# <span data-ttu-id="c30e3-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c30e3-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="c30e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c30e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c30e3-103">Retorna informações sobre grupos de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c30e3-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c30e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c30e3-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c30e3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c30e3-105">DESCRIPTION</span></span>
<span data-ttu-id="c30e3-106">O cmdlet **Get-AzureRmSqlSyncGroup** retorna informações sobre um ou mais grupos de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c30e3-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="c30e3-107">Especifique o nome de um grupo de sincronização para ver informações somente para esse grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c30e3-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="c30e3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c30e3-108">EXAMPLES</span></span>

### <span data-ttu-id="c30e3-109">Exemplo 1: obter todas as instâncias do grupo Azure SQL Sync atribuída a um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c30e3-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="c30e3-110">Esse comando obtém informações sobre todos os grupos de sincronização do banco de dados SQL do Azure atribuídos a um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c30e3-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="c30e3-111">Exemplo 2: obter informações sobre um grupo de sincronização do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="c30e3-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="c30e3-112">Esse comando obtém informações sobre o grupo de sincronização do banco de dados SQL do Azure com o nome "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="c30e3-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="c30e3-113">OS</span><span class="sxs-lookup"><span data-stu-id="c30e3-113">PARAMETERS</span></span>

### <span data-ttu-id="c30e3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c30e3-114">-DatabaseName</span></span>
<span data-ttu-id="c30e3-115">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="c30e3-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="c30e3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c30e3-116">-Name</span></span>
<span data-ttu-id="c30e3-117">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c30e3-117">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30e3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30e3-118">-ResourceGroupName</span></span>
<span data-ttu-id="c30e3-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c30e3-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="c30e3-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c30e3-120">-ServerName</span></span>
<span data-ttu-id="c30e3-121">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c30e3-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="c30e3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30e3-122">-DefaultProfile</span></span>
<span data-ttu-id="c30e3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c30e3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c30e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30e3-124">CommonParameters</span></span>
<span data-ttu-id="c30e3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c30e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30e3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c30e3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30e3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c30e3-127">INPUTS</span></span>

## <span data-ttu-id="c30e3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c30e3-128">OUTPUTS</span></span>

### <span data-ttu-id="c30e3-129">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="c30e3-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="c30e3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c30e3-130">NOTES</span></span>

## <span data-ttu-id="c30e3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c30e3-131">RELATED LINKS</span></span>

[<span data-ttu-id="c30e3-132">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c30e3-132">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="c30e3-133">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c30e3-133">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="c30e3-134">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c30e3-134">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

