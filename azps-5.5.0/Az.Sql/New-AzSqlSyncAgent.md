---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110928"
---
# <span data-ttu-id="7323d-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7323d-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="7323d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7323d-102">SYNOPSIS</span></span>
<span data-ttu-id="7323d-103">Cria um Agente de Sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7323d-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7323d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7323d-104">SYNTAX</span></span>

### <span data-ttu-id="7323d-105">SyncDatabaseComponent (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7323d-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7323d-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="7323d-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7323d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7323d-107">DESCRIPTION</span></span>
<span data-ttu-id="7323d-108">O cmdlet **New-AzSqlSyncAgent cria** um Agente de Sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7323d-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7323d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7323d-109">EXAMPLES</span></span>

### <span data-ttu-id="7323d-110">Exemplo 1: Criar um agente de sincronização para um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7323d-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
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

<span data-ttu-id="7323d-111">Esse comando cria um agente de sincronização para um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7323d-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="7323d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7323d-112">PARAMETERS</span></span>

### <span data-ttu-id="7323d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7323d-113">-DefaultProfile</span></span>
<span data-ttu-id="7323d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7323d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7323d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7323d-115">-Name</span></span>
<span data-ttu-id="7323d-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7323d-116">The sync agent name.</span></span>

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

### <span data-ttu-id="7323d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7323d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7323d-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7323d-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="7323d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7323d-119">-ServerName</span></span>
<span data-ttu-id="7323d-120">O nome do SQL Server do Azure em que o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="7323d-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7323d-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7323d-121">-SyncDatabaseName</span></span>
<span data-ttu-id="7323d-122">O banco de dados usado para armazenar metadados relacionados à sincronização.</span><span class="sxs-lookup"><span data-stu-id="7323d-122">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="7323d-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7323d-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="7323d-124">O grupo de recursos ao banco de dados de sincronização de metadados pertence.</span><span class="sxs-lookup"><span data-stu-id="7323d-124">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="7323d-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="7323d-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="7323d-126">A ID do recurso do banco de dados de sincronização de metadados.</span><span class="sxs-lookup"><span data-stu-id="7323d-126">The resource ID of  the sync metadata database.</span></span>

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

### <span data-ttu-id="7323d-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="7323d-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="7323d-128">O servidor no qual o banco de dados de metadados de sincronização está hospedado.</span><span class="sxs-lookup"><span data-stu-id="7323d-128">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="7323d-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7323d-129">-Confirm</span></span>
<span data-ttu-id="7323d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7323d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7323d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7323d-131">-WhatIf</span></span>
<span data-ttu-id="7323d-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7323d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7323d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7323d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7323d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7323d-134">CommonParameters</span></span>
<span data-ttu-id="7323d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7323d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7323d-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7323d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7323d-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="7323d-137">INPUTS</span></span>

### <span data-ttu-id="7323d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7323d-138">System.String</span></span>

## <span data-ttu-id="7323d-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="7323d-139">OUTPUTS</span></span>

### <span data-ttu-id="7323d-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="7323d-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="7323d-141">Notas</span><span class="sxs-lookup"><span data-stu-id="7323d-141">NOTES</span></span>

## <span data-ttu-id="7323d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7323d-142">RELATED LINKS</span></span>

[<span data-ttu-id="7323d-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7323d-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="7323d-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7323d-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

