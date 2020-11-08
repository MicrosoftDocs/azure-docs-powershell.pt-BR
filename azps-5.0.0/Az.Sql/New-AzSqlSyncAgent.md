---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116653"
---
# <span data-ttu-id="161d7-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="161d7-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="161d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="161d7-102">SYNOPSIS</span></span>
<span data-ttu-id="161d7-103">Cria um agente do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="161d7-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="161d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="161d7-104">SYNTAX</span></span>

### <span data-ttu-id="161d7-105">SyncDatabaseComponent (padrão)</span><span class="sxs-lookup"><span data-stu-id="161d7-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="161d7-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="161d7-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="161d7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="161d7-107">DESCRIPTION</span></span>
<span data-ttu-id="161d7-108">O cmdlet **New-AzSqlSyncAgent** cria um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="161d7-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="161d7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="161d7-109">EXAMPLES</span></span>

### <span data-ttu-id="161d7-110">Exemplo 1: criar um agente de sincronização para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="161d7-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
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

<span data-ttu-id="161d7-111">Esse comando cria um agente de sincronização para um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="161d7-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="161d7-112">OS</span><span class="sxs-lookup"><span data-stu-id="161d7-112">PARAMETERS</span></span>

### <span data-ttu-id="161d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="161d7-113">-DefaultProfile</span></span>
<span data-ttu-id="161d7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="161d7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="161d7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="161d7-115">-Name</span></span>
<span data-ttu-id="161d7-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="161d7-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="161d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="161d7-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="161d7-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="161d7-119">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="161d7-119">-ServerName</span></span>
<span data-ttu-id="161d7-120">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="161d7-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="161d7-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="161d7-121">-SyncDatabaseName</span></span>
<span data-ttu-id="161d7-122">O banco de dados usado para armazenar metadados relacionados à sincronização.</span><span class="sxs-lookup"><span data-stu-id="161d7-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161d7-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="161d7-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="161d7-124">O grupo de recursos ao qual pertence o banco de dados sincronizar metadados.</span><span class="sxs-lookup"><span data-stu-id="161d7-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161d7-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="161d7-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="161d7-126">A ID do recurso do banco de dados de metadados de sincronização.</span><span class="sxs-lookup"><span data-stu-id="161d7-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161d7-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="161d7-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="161d7-128">O servidor no qual o banco de dados de metadados de sincronização está hospedado.</span><span class="sxs-lookup"><span data-stu-id="161d7-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161d7-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="161d7-129">-Confirm</span></span>
<span data-ttu-id="161d7-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="161d7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161d7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="161d7-131">-WhatIf</span></span>
<span data-ttu-id="161d7-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="161d7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="161d7-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="161d7-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="161d7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="161d7-134">CommonParameters</span></span>
<span data-ttu-id="161d7-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="161d7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="161d7-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="161d7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="161d7-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="161d7-137">INPUTS</span></span>

### <span data-ttu-id="161d7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="161d7-138">System.String</span></span>

## <span data-ttu-id="161d7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="161d7-139">OUTPUTS</span></span>

### <span data-ttu-id="161d7-140">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="161d7-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="161d7-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="161d7-141">NOTES</span></span>

## <span data-ttu-id="161d7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="161d7-142">RELATED LINKS</span></span>

[<span data-ttu-id="161d7-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="161d7-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="161d7-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="161d7-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

