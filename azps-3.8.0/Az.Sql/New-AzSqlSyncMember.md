---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 1decf3d7b179123a116bb570199840118115313f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777624"
---
# <span data-ttu-id="6573c-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6573c-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="6573c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6573c-102">SYNOPSIS</span></span>
<span data-ttu-id="6573c-103">Cria um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6573c-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6573c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6573c-104">SYNTAX</span></span>

### <span data-ttu-id="6573c-105">AzureSqlDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="6573c-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6573c-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="6573c-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6573c-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="6573c-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6573c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6573c-108">DESCRIPTION</span></span>
<span data-ttu-id="6573c-109">O cmdlet **New-AzSqlSyncMember** cria um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6573c-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6573c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6573c-110">EXAMPLES</span></span>

### <span data-ttu-id="6573c-111">Exemplo 1: criar um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6573c-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="6573c-112">Esse comando cria um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6573c-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="6573c-113">Exemplo 2: criar um membro de sincronização para um banco de dados do SQL Server local</span><span class="sxs-lookup"><span data-stu-id="6573c-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="6573c-114">Esse comando cria um membro de sincronização para um banco de dados SQL local.</span><span class="sxs-lookup"><span data-stu-id="6573c-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="6573c-115">OS</span><span class="sxs-lookup"><span data-stu-id="6573c-115">PARAMETERS</span></span>

### <span data-ttu-id="6573c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6573c-116">-DatabaseName</span></span>
<span data-ttu-id="6573c-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6573c-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6573c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6573c-118">-DefaultProfile</span></span>
<span data-ttu-id="6573c-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6573c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6573c-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="6573c-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="6573c-121">A credencial (nome de usuário e senha) do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6573c-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6573c-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6573c-122">-MemberDatabaseName</span></span>
<span data-ttu-id="6573c-123">O nome do banco de dados SQL do Azure do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="6573c-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="6573c-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="6573c-124">-MemberDatabaseType</span></span>
<span data-ttu-id="6573c-125">O tipo de banco de dados do membro.</span><span class="sxs-lookup"><span data-stu-id="6573c-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="6573c-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="6573c-126">-MemberServerName</span></span>
<span data-ttu-id="6573c-127">O nome do SQL Server do Azure do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="6573c-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="6573c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="6573c-128">-Name</span></span>
<span data-ttu-id="6573c-129">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6573c-129">The sync member name.</span></span>

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

### <span data-ttu-id="6573c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6573c-130">-ResourceGroupName</span></span>
<span data-ttu-id="6573c-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6573c-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="6573c-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6573c-132">-ServerName</span></span>
<span data-ttu-id="6573c-133">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6573c-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6573c-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="6573c-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="6573c-135">A ID do banco de dados do SQL Server que é conectada pelo agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6573c-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="6573c-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="6573c-136">-SyncAgentName</span></span>
<span data-ttu-id="6573c-137">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6573c-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="6573c-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6573c-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="6573c-139">O nome do grupo de recursos onde está o agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6573c-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="6573c-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="6573c-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="6573c-141">A ID do recurso do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6573c-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="6573c-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="6573c-142">-SyncAgentServerName</span></span>
<span data-ttu-id="6573c-143">O nome do SQL Server do Azure no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="6573c-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="6573c-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="6573c-144">-SyncDirection</span></span>
<span data-ttu-id="6573c-145">A direção de sincronização deste membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6573c-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="6573c-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6573c-146">-SyncGroupName</span></span>
<span data-ttu-id="6573c-147">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6573c-147">The sync group name.</span></span>

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

### <span data-ttu-id="6573c-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6573c-148">-Confirm</span></span>
<span data-ttu-id="6573c-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6573c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6573c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6573c-150">-WhatIf</span></span>
<span data-ttu-id="6573c-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6573c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6573c-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6573c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6573c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6573c-153">CommonParameters</span></span>
<span data-ttu-id="6573c-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6573c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6573c-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6573c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6573c-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6573c-156">INPUTS</span></span>

### <span data-ttu-id="6573c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="6573c-157">System.String</span></span>

## <span data-ttu-id="6573c-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6573c-158">OUTPUTS</span></span>

### <span data-ttu-id="6573c-159">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="6573c-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="6573c-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6573c-160">NOTES</span></span>

## <span data-ttu-id="6573c-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6573c-161">RELATED LINKS</span></span>

[<span data-ttu-id="6573c-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6573c-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="6573c-163">Set-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6573c-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="6573c-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6573c-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

