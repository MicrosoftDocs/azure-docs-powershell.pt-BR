---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 3041d7a25ad87e6e2b9242043645a66219ac7e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431572"
---
# <span data-ttu-id="7126f-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7126f-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="7126f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7126f-102">SYNOPSIS</span></span>
<span data-ttu-id="7126f-103">Retorna informações sobre os agentes do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="7126f-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7126f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7126f-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7126f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7126f-105">DESCRIPTION</span></span>
<span data-ttu-id="7126f-106">O cmdlet **Get-AzureRmSqlSyncAgent** retorna informações sobre um ou mais agentes de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7126f-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="7126f-107">Especifique o nome de um agente de sincronização para ver informações somente para esse agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7126f-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="7126f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7126f-108">EXAMPLES</span></span>

### <span data-ttu-id="7126f-109">Exemplo 1: obter todas as instâncias do Azure SQL Sync Agent atribuídas a um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="7126f-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="7126f-110">Esse comando obtém informações sobre todos os agentes do Azure SQL Sync atribuídos a um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="7126f-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="7126f-111">Exemplo 2: obter informações sobre um agente de sincronização do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="7126f-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="7126f-112">Esse comando obtém informações sobre o agente de sincronização do banco de dados SQL do Azure com o nome "SyncAgent01"</span><span class="sxs-lookup"><span data-stu-id="7126f-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="7126f-113">OS</span><span class="sxs-lookup"><span data-stu-id="7126f-113">PARAMETERS</span></span>

### <span data-ttu-id="7126f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7126f-114">-DefaultProfile</span></span>
<span data-ttu-id="7126f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7126f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7126f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7126f-116">-Name</span></span>
<span data-ttu-id="7126f-117">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7126f-117">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7126f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7126f-118">-ResourceGroupName</span></span>
<span data-ttu-id="7126f-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7126f-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="7126f-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7126f-120">-ServerName</span></span>
<span data-ttu-id="7126f-121">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="7126f-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7126f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7126f-122">CommonParameters</span></span>
<span data-ttu-id="7126f-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7126f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7126f-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7126f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7126f-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7126f-125">INPUTS</span></span>

### <span data-ttu-id="7126f-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7126f-126">None</span></span>
<span data-ttu-id="7126f-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7126f-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7126f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7126f-128">OUTPUTS</span></span>

### <span data-ttu-id="7126f-129">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="7126f-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="7126f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7126f-130">NOTES</span></span>

## <span data-ttu-id="7126f-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7126f-131">RELATED LINKS</span></span>

[<span data-ttu-id="7126f-132">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7126f-132">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="7126f-133">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7126f-133">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

