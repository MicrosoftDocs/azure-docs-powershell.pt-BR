---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118164"
---
# <span data-ttu-id="534b1-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="534b1-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="534b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="534b1-102">SYNOPSIS</span></span>
<span data-ttu-id="534b1-103">Retorna informações sobre os agentes do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="534b1-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="534b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="534b1-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="534b1-105">DESCRIPTION</span></span>
<span data-ttu-id="534b1-106">O cmdlet **Get-AzSqlSyncAgent** retorna informações sobre um ou mais agentes de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="534b1-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="534b1-107">Especifique o nome de um agente de sincronização para ver informações somente para esse agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="534b1-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="534b1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="534b1-108">EXAMPLES</span></span>

### <span data-ttu-id="534b1-109">Exemplo 1: obter todas as instâncias do Azure SQL Sync Agent atribuídas a um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="534b1-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="534b1-110">Esse comando obtém informações sobre todos os agentes do Azure SQL Sync atribuídos a um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="534b1-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="534b1-111">Exemplo 2: obter informações sobre um agente de sincronização do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="534b1-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="534b1-112">Esse comando obtém informações sobre o agente de sincronização do banco de dados SQL do Azure com o nome "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="534b1-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="534b1-113">Exemplo 3: obter todas as instâncias do agente de sincronização do SQL do Azure atribuídas a um SQL Server do Azure usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="534b1-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="534b1-114">Esse comando obtém informações sobre todos os agentes do Azure SQL Sync atribuídos a um SQL Server do Azure que começam com "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="534b1-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="534b1-115">OS</span><span class="sxs-lookup"><span data-stu-id="534b1-115">PARAMETERS</span></span>

### <span data-ttu-id="534b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534b1-116">-DefaultProfile</span></span>
<span data-ttu-id="534b1-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="534b1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="534b1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="534b1-118">-Name</span></span>
<span data-ttu-id="534b1-119">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="534b1-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="534b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="534b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="534b1-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="534b1-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="534b1-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="534b1-122">-ServerName</span></span>
<span data-ttu-id="534b1-123">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="534b1-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="534b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534b1-124">CommonParameters</span></span>
<span data-ttu-id="534b1-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534b1-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="534b1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534b1-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="534b1-127">INPUTS</span></span>

### <span data-ttu-id="534b1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="534b1-128">System.String</span></span>

## <span data-ttu-id="534b1-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="534b1-129">OUTPUTS</span></span>

### <span data-ttu-id="534b1-130">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="534b1-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="534b1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="534b1-131">NOTES</span></span>

## <span data-ttu-id="534b1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="534b1-132">RELATED LINKS</span></span>

[<span data-ttu-id="534b1-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="534b1-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="534b1-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="534b1-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

