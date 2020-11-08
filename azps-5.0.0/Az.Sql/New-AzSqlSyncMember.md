---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: f7fc860711c5037e6ce6390f9fb7d79ddfa7d6ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116650"
---
# <span data-ttu-id="140f3-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="140f3-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="140f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="140f3-102">SYNOPSIS</span></span>
<span data-ttu-id="140f3-103">Cria um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="140f3-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="140f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="140f3-104">SYNTAX</span></span>

### <span data-ttu-id="140f3-105">AzureSqlDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="140f3-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="140f3-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="140f3-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="140f3-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="140f3-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="140f3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="140f3-108">DESCRIPTION</span></span>
<span data-ttu-id="140f3-109">O cmdlet **New-AzSqlSyncMember** cria um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="140f3-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="140f3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="140f3-110">EXAMPLES</span></span>

### <span data-ttu-id="140f3-111">Exemplo 1: criar um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="140f3-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="140f3-112">Esse comando cria um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="140f3-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="140f3-113">Exemplo 2: criar um membro de sincronização para um banco de dados do SQL Server local</span><span class="sxs-lookup"><span data-stu-id="140f3-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="140f3-114">Esse comando cria um membro de sincronização para um banco de dados SQL local.</span><span class="sxs-lookup"><span data-stu-id="140f3-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="140f3-115">OS</span><span class="sxs-lookup"><span data-stu-id="140f3-115">PARAMETERS</span></span>

### <span data-ttu-id="140f3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="140f3-116">-DatabaseName</span></span>
<span data-ttu-id="140f3-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="140f3-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="140f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140f3-118">-DefaultProfile</span></span>
<span data-ttu-id="140f3-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="140f3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="140f3-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="140f3-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="140f3-121">A credencial (nome de usuário e senha) do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="140f3-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="140f3-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="140f3-122">-MemberDatabaseName</span></span>
<span data-ttu-id="140f3-123">O nome do banco de dados SQL do Azure do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="140f3-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="140f3-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="140f3-124">-MemberDatabaseType</span></span>
<span data-ttu-id="140f3-125">O tipo de banco de dados do membro.</span><span class="sxs-lookup"><span data-stu-id="140f3-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="140f3-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="140f3-126">-MemberServerName</span></span>
<span data-ttu-id="140f3-127">O nome do SQL Server do Azure do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="140f3-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="140f3-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="140f3-128">-Name</span></span>
<span data-ttu-id="140f3-129">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-129">The sync member name.</span></span>

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

### <span data-ttu-id="140f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="140f3-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="140f3-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="140f3-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="140f3-132">-ServerName</span></span>
<span data-ttu-id="140f3-133">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="140f3-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="140f3-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="140f3-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="140f3-135">A ID do banco de dados do SQL Server que é conectada pelo agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="140f3-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="140f3-136">-SyncAgentName</span></span>
<span data-ttu-id="140f3-137">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="140f3-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140f3-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="140f3-139">O nome do grupo de recursos onde está o agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="140f3-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="140f3-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="140f3-141">A ID do recurso do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="140f3-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="140f3-142">-SyncAgentServerName</span></span>
<span data-ttu-id="140f3-143">O nome do SQL Server do Azure no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="140f3-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="140f3-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="140f3-144">-SyncDirection</span></span>
<span data-ttu-id="140f3-145">A direção de sincronização deste membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="140f3-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="140f3-146">-SyncGroupName</span></span>
<span data-ttu-id="140f3-147">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-147">The sync group name.</span></span>

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

### <span data-ttu-id="140f3-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="140f3-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="140f3-149">A ID do recurso para o banco de dados do membro de sincronização, usado se UsePrivateLinkConnection for definido como true.</span><span class="sxs-lookup"><span data-stu-id="140f3-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="140f3-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="140f3-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="140f3-151">Use uma conexão de link particular quando se conectar a este membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="140f3-151">Use a private link connection when connecting to this sync member.</span></span>

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

### <span data-ttu-id="140f3-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="140f3-152">-Confirm</span></span>
<span data-ttu-id="140f3-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="140f3-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="140f3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="140f3-154">-WhatIf</span></span>
<span data-ttu-id="140f3-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="140f3-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="140f3-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="140f3-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="140f3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140f3-157">CommonParameters</span></span>
<span data-ttu-id="140f3-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="140f3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140f3-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="140f3-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140f3-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="140f3-160">INPUTS</span></span>

### <span data-ttu-id="140f3-161">System. String</span><span class="sxs-lookup"><span data-stu-id="140f3-161">System.String</span></span>

## <span data-ttu-id="140f3-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="140f3-162">OUTPUTS</span></span>

### <span data-ttu-id="140f3-163">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="140f3-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="140f3-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="140f3-164">NOTES</span></span>

## <span data-ttu-id="140f3-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="140f3-165">RELATED LINKS</span></span>

[<span data-ttu-id="140f3-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="140f3-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="140f3-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="140f3-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="140f3-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="140f3-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

