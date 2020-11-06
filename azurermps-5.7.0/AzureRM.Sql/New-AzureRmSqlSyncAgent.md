---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 6e1d647c390d8d0f92192a63c3a395005074cfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431558"
---
# <span data-ttu-id="cabe8-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cabe8-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="cabe8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cabe8-102">SYNOPSIS</span></span>
<span data-ttu-id="cabe8-103">Cria um agente do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="cabe8-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cabe8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cabe8-104">SYNTAX</span></span>

### <span data-ttu-id="cabe8-105">SyncDatabaseComponent (padrão)</span><span class="sxs-lookup"><span data-stu-id="cabe8-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cabe8-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="cabe8-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cabe8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cabe8-107">DESCRIPTION</span></span>
<span data-ttu-id="cabe8-108">O cmdlet **New-AzureRmSqlSyncAgent** cria um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cabe8-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="cabe8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cabe8-109">EXAMPLES</span></span>

### <span data-ttu-id="cabe8-110">Exemplo 1: criar um agente de sincronização para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="cabe8-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="cabe8-111">Esse comando cria um agente de sincronização para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="cabe8-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="cabe8-112">OS</span><span class="sxs-lookup"><span data-stu-id="cabe8-112">PARAMETERS</span></span>

### <span data-ttu-id="cabe8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabe8-113">-DefaultProfile</span></span>
<span data-ttu-id="cabe8-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cabe8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cabe8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cabe8-115">-Name</span></span>
<span data-ttu-id="cabe8-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="cabe8-116">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cabe8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabe8-117">-ResourceGroupName</span></span>
<span data-ttu-id="cabe8-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cabe8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cabe8-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="cabe8-119">-ServerName</span></span>
<span data-ttu-id="cabe8-120">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="cabe8-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="cabe8-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cabe8-121">-SyncDatabaseName</span></span>
<span data-ttu-id="cabe8-122">O banco de dados usado para armazenar metadados relacionados à sincronização.</span><span class="sxs-lookup"><span data-stu-id="cabe8-122">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabe8-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabe8-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="cabe8-124">O grupo de recursos ao qual pertence o banco de dados sincronizar metadados.</span><span class="sxs-lookup"><span data-stu-id="cabe8-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabe8-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="cabe8-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="cabe8-126">A ID do recurso do banco de dados de metadados de sincronização.</span><span class="sxs-lookup"><span data-stu-id="cabe8-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabe8-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="cabe8-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="cabe8-128">O servidor no qual o banco de dados de metadados de sincronização está hospedado.</span><span class="sxs-lookup"><span data-stu-id="cabe8-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabe8-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cabe8-129">-Confirm</span></span>
<span data-ttu-id="cabe8-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cabe8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabe8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cabe8-131">-WhatIf</span></span>
<span data-ttu-id="cabe8-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cabe8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cabe8-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cabe8-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cabe8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabe8-134">CommonParameters</span></span>
<span data-ttu-id="cabe8-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabe8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabe8-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabe8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabe8-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cabe8-137">INPUTS</span></span>

### <span data-ttu-id="cabe8-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cabe8-138">None</span></span>
<span data-ttu-id="cabe8-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cabe8-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cabe8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cabe8-140">OUTPUTS</span></span>

### <span data-ttu-id="cabe8-141">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="cabe8-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="cabe8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cabe8-142">NOTES</span></span>

## <span data-ttu-id="cabe8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cabe8-143">RELATED LINKS</span></span>

[<span data-ttu-id="cabe8-144">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cabe8-144">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="cabe8-145">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="cabe8-145">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

