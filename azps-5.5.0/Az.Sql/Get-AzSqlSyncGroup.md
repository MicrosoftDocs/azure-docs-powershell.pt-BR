---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111327"
---
# <span data-ttu-id="df943-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df943-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="df943-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df943-102">SYNOPSIS</span></span>
<span data-ttu-id="df943-103">Retorna informações sobre os Grupos de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="df943-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="df943-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df943-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df943-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="df943-105">DESCRIPTION</span></span>
<span data-ttu-id="df943-106">O cmdlet **Get-AzSqlSyncGroup** retorna informações sobre um ou mais Grupos de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="df943-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="df943-107">Especifique o nome de um grupo de sincronização para ver informações somente para esse grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="df943-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="df943-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df943-108">EXAMPLES</span></span>

### <span data-ttu-id="df943-109">Exemplo 1: Obter todas as instâncias do Azure SQL Sync Group atribuídas a um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="df943-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="df943-110">Esse comando obtém informações sobre todos os Grupos de Sincronização de Banco de Dados SQL do Azure atribuídos a um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="df943-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="df943-111">Exemplo 2: Obter informações sobre um Grupo de Sincronização de Banco de Dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="df943-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="df943-112">Este comando obtém informações sobre o Grupo de Sincronização de Banco de Dados SQL do Azure com o nome "SyncGroup01"</span><span class="sxs-lookup"><span data-stu-id="df943-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="df943-113">Exemplo 3: Obter todas as instâncias do Azure SQL Sync Group atribuídas a um banco de dados SQL do Azure usando filtragem</span><span class="sxs-lookup"><span data-stu-id="df943-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
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

<span data-ttu-id="df943-114">Esse comando obtém informações sobre todos os Grupos de Sincronização de Banco de Dados SQL do Azure atribuídos a um banco de dados SQL do Azure que começam com "SyncGroup".</span><span class="sxs-lookup"><span data-stu-id="df943-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="df943-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df943-115">PARAMETERS</span></span>

### <span data-ttu-id="df943-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="df943-116">-DatabaseName</span></span>
<span data-ttu-id="df943-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="df943-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="df943-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df943-118">-DefaultProfile</span></span>
<span data-ttu-id="df943-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="df943-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df943-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="df943-120">-Name</span></span>
<span data-ttu-id="df943-121">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="df943-121">The sync group name.</span></span>

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

### <span data-ttu-id="df943-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df943-122">-ResourceGroupName</span></span>
<span data-ttu-id="df943-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df943-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="df943-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df943-124">-ServerName</span></span>
<span data-ttu-id="df943-125">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="df943-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="df943-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df943-126">CommonParameters</span></span>
<span data-ttu-id="df943-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df943-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df943-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df943-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df943-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="df943-129">INPUTS</span></span>

### <span data-ttu-id="df943-130">System.String</span><span class="sxs-lookup"><span data-stu-id="df943-130">System.String</span></span>

## <span data-ttu-id="df943-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="df943-131">OUTPUTS</span></span>

### <span data-ttu-id="df943-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="df943-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="df943-133">Notas</span><span class="sxs-lookup"><span data-stu-id="df943-133">NOTES</span></span>

## <span data-ttu-id="df943-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df943-134">RELATED LINKS</span></span>

[<span data-ttu-id="df943-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df943-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="df943-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df943-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="df943-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="df943-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

