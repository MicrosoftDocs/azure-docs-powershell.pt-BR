---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: f74a031079ab35e1584d8c7e5536e2605ea665ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773590"
---
# <span data-ttu-id="f9c71-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f9c71-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="f9c71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9c71-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c71-103">Retorna informações sobre os agentes do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="f9c71-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="f9c71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9c71-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9c71-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9c71-105">DESCRIPTION</span></span>
<span data-ttu-id="f9c71-106">O cmdlet **Get-AzSqlSyncAgent** retorna informações sobre um ou mais agentes de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c71-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="f9c71-107">Especifique o nome de um agente de sincronização para ver informações somente para esse agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f9c71-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="f9c71-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9c71-108">EXAMPLES</span></span>

### <span data-ttu-id="f9c71-109">Exemplo 1: obter todas as instâncias do Azure SQL Sync Agent atribuídas a um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="f9c71-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="f9c71-110">Esse comando obtém informações sobre todos os agentes do Azure SQL Sync atribuídos a um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c71-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="f9c71-111">Exemplo 2: obter informações sobre um agente de sincronização do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9c71-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="f9c71-112">Esse comando obtém informações sobre o agente de sincronização do banco de dados SQL do Azure com o nome "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="f9c71-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="f9c71-113">Exemplo 3: obter todas as instâncias do agente de sincronização do SQL do Azure atribuídas a um SQL Server do Azure usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="f9c71-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="f9c71-114">Esse comando obtém informações sobre todos os agentes do Azure SQL Sync atribuídos a um SQL Server do Azure que começam com "SyncAgent".</span><span class="sxs-lookup"><span data-stu-id="f9c71-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="f9c71-115">OS</span><span class="sxs-lookup"><span data-stu-id="f9c71-115">PARAMETERS</span></span>

### <span data-ttu-id="f9c71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c71-116">-DefaultProfile</span></span>
<span data-ttu-id="f9c71-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f9c71-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9c71-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9c71-118">-Name</span></span>
<span data-ttu-id="f9c71-119">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f9c71-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f9c71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c71-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9c71-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9c71-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9c71-122">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f9c71-122">-ServerName</span></span>
<span data-ttu-id="f9c71-123">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="f9c71-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="f9c71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c71-124">CommonParameters</span></span>
<span data-ttu-id="f9c71-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9c71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c71-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9c71-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c71-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9c71-127">INPUTS</span></span>

### <span data-ttu-id="f9c71-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f9c71-128">System.String</span></span>

## <span data-ttu-id="f9c71-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9c71-129">OUTPUTS</span></span>

### <span data-ttu-id="f9c71-130">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="f9c71-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="f9c71-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9c71-131">NOTES</span></span>

## <span data-ttu-id="f9c71-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9c71-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9c71-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f9c71-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="f9c71-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="f9c71-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

