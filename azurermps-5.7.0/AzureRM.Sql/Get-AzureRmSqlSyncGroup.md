---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 71a4d20c6296c8a9d725cb9a16960d6c4a06646c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428735"
---
# <span data-ttu-id="607ba-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="607ba-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="607ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="607ba-102">SYNOPSIS</span></span>
<span data-ttu-id="607ba-103">Retorna informações sobre grupos de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="607ba-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="607ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="607ba-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="607ba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="607ba-105">DESCRIPTION</span></span>
<span data-ttu-id="607ba-106">O cmdlet **Get-AzureRmSqlSyncGroup** retorna informações sobre um ou mais grupos de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="607ba-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="607ba-107">Especifique o nome de um grupo de sincronização para ver informações somente para esse grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="607ba-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="607ba-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="607ba-108">EXAMPLES</span></span>

### <span data-ttu-id="607ba-109">Exemplo 1: obter todas as instâncias do grupo Azure SQL Sync atribuída a um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="607ba-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="607ba-110">Esse comando obtém informações sobre todos os grupos de sincronização do banco de dados SQL do Azure atribuídos a um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="607ba-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="607ba-111">Exemplo 2: obter informações sobre um grupo de sincronização do banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="607ba-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="607ba-112">Esse comando obtém informações sobre o grupo de sincronização do banco de dados SQL do Azure com o nome "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="607ba-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="607ba-113">OS</span><span class="sxs-lookup"><span data-stu-id="607ba-113">PARAMETERS</span></span>

### <span data-ttu-id="607ba-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="607ba-114">-DatabaseName</span></span>
<span data-ttu-id="607ba-115">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="607ba-115">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607ba-116">-DefaultProfile</span></span>
<span data-ttu-id="607ba-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="607ba-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="607ba-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="607ba-118">-Name</span></span>
<span data-ttu-id="607ba-119">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="607ba-119">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="607ba-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="607ba-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607ba-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="607ba-122">-ServerName</span></span>
<span data-ttu-id="607ba-123">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="607ba-123">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="607ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607ba-124">CommonParameters</span></span>
<span data-ttu-id="607ba-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607ba-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="607ba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607ba-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="607ba-127">INPUTS</span></span>

### <span data-ttu-id="607ba-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="607ba-128">None</span></span>
<span data-ttu-id="607ba-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="607ba-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="607ba-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="607ba-130">OUTPUTS</span></span>

### <span data-ttu-id="607ba-131">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="607ba-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="607ba-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="607ba-132">NOTES</span></span>

## <span data-ttu-id="607ba-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="607ba-133">RELATED LINKS</span></span>

[<span data-ttu-id="607ba-134">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="607ba-134">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="607ba-135">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="607ba-135">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="607ba-136">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="607ba-136">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

