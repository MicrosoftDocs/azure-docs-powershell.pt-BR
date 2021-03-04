---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: c26cb74f1d9f9c30e63bb39ec7668216a5f3a297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886564"
---
# <span data-ttu-id="d9a54-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9a54-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="d9a54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9a54-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a54-103">Cria um membro de sincronização de SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a54-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d9a54-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d9a54-104">SYNTAX</span></span>

### <span data-ttu-id="d9a54-105">AzureSqlDatabase (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d9a54-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a54-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="d9a54-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a54-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d9a54-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a54-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d9a54-108">DESCRIPTION</span></span>
<span data-ttu-id="d9a54-109">O cmdlet **New-AzSqlSyncMember** cria um Membro de Sincronização de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d9a54-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d9a54-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9a54-110">EXAMPLES</span></span>

### <span data-ttu-id="d9a54-111">Exemplo 1: Criar um membro de sincronização para um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d9a54-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
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
SyncState                   : UnProvisioned
```

<span data-ttu-id="d9a54-112">Este comando cria um membro de sincronização para um banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a54-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="d9a54-113">Exemplo 2: Criar um membro de sincronização para um banco de dados SQL Server local</span><span class="sxs-lookup"><span data-stu-id="d9a54-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="d9a54-114">Este comando cria um membro de sincronização para um banco de dados SQL local.</span><span class="sxs-lookup"><span data-stu-id="d9a54-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="d9a54-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d9a54-115">PARAMETERS</span></span>

### <span data-ttu-id="d9a54-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9a54-116">-DatabaseName</span></span>
<span data-ttu-id="d9a54-117">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d9a54-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d9a54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a54-118">-DefaultProfile</span></span>
<span data-ttu-id="d9a54-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d9a54-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9a54-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d9a54-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="d9a54-121">A credencial (nome de usuário e senha) do Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d9a54-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9a54-122">-MemberDatabaseName</span></span>
<span data-ttu-id="d9a54-123">O nome SQL banco de dados do banco de dados membro do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a54-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="d9a54-124">-MemberDatabaseType</span></span>
<span data-ttu-id="d9a54-125">O tipo de banco de dados do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="d9a54-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="d9a54-126">-MemberServerName</span></span>
<span data-ttu-id="d9a54-127">O Azure SQL Server nome do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="d9a54-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d9a54-128">-Name</span></span>
<span data-ttu-id="d9a54-129">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d9a54-129">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a54-130">-ResourceGroupName</span></span>
<span data-ttu-id="d9a54-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9a54-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9a54-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9a54-132">-ServerName</span></span>
<span data-ttu-id="d9a54-133">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d9a54-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d9a54-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="d9a54-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="d9a54-135">A id do banco de dados SQL servidor que está conectado pelo agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d9a54-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="d9a54-136">-SyncAgentName</span></span>
<span data-ttu-id="d9a54-137">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d9a54-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a54-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="d9a54-139">O nome do grupo de recursos em que o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="d9a54-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d9a54-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="d9a54-141">A ID do recurso do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d9a54-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="d9a54-142">-SyncAgentServerName</span></span>
<span data-ttu-id="d9a54-143">O nome do Azure SQL Server onde o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="d9a54-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="d9a54-144">-SyncDirection</span></span>
<span data-ttu-id="d9a54-145">A direção de sincronização desse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d9a54-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a54-146">-SyncGroupName</span></span>
<span data-ttu-id="d9a54-147">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d9a54-147">The sync group name.</span></span>

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

### <span data-ttu-id="d9a54-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="d9a54-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="d9a54-149">A ID do recurso para o banco de dados de membros de sincronização, usada se UsePrivateLinkConnection estiver definida como true.</span><span class="sxs-lookup"><span data-stu-id="d9a54-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d9a54-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="d9a54-151">Use uma conexão de link privado ao se conectar a esse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d9a54-151">Use a private link connection when connecting to this sync member.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a54-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9a54-152">-Confirm</span></span>
<span data-ttu-id="d9a54-153">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9a54-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a54-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a54-154">-WhatIf</span></span>
<span data-ttu-id="d9a54-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9a54-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a54-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9a54-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a54-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a54-157">CommonParameters</span></span>
<span data-ttu-id="d9a54-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a54-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a54-159">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9a54-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a54-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9a54-160">INPUTS</span></span>

### <span data-ttu-id="d9a54-161">System.String</span><span class="sxs-lookup"><span data-stu-id="d9a54-161">System.String</span></span>

## <span data-ttu-id="d9a54-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d9a54-162">OUTPUTS</span></span>

### <span data-ttu-id="d9a54-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d9a54-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d9a54-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="d9a54-164">NOTES</span></span>

## <span data-ttu-id="d9a54-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9a54-165">RELATED LINKS</span></span>

[<span data-ttu-id="d9a54-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9a54-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="d9a54-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9a54-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="d9a54-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d9a54-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

