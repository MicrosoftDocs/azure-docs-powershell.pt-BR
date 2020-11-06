---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: a779217b67cc73f25223661ae8671b4588a8cd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431294"
---
# <span data-ttu-id="59ad1-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="59ad1-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="59ad1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="59ad1-103">Cria um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="59ad1-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59ad1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59ad1-104">SYNTAX</span></span>

### <span data-ttu-id="59ad1-105">AzureSqlDatabase (padrão)</span><span class="sxs-lookup"><span data-stu-id="59ad1-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59ad1-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="59ad1-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59ad1-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="59ad1-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59ad1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59ad1-108">DESCRIPTION</span></span>
<span data-ttu-id="59ad1-109">O cmdlet **New-AzureRmSqlSyncMember** cria um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="59ad1-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="59ad1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59ad1-110">EXAMPLES</span></span>

### <span data-ttu-id="59ad1-111">Exemplo 1: criar um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="59ad1-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="59ad1-112">Esse comando cria um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="59ad1-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="59ad1-113">Exemplo 2: criar um membro de sincronização para um banco de dados do SQL Server local</span><span class="sxs-lookup"><span data-stu-id="59ad1-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="59ad1-114">Esse comando cria um membro de sincronização para um banco de dados SQL local.</span><span class="sxs-lookup"><span data-stu-id="59ad1-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="59ad1-115">OS</span><span class="sxs-lookup"><span data-stu-id="59ad1-115">PARAMETERS</span></span>

### <span data-ttu-id="59ad1-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59ad1-116">-DatabaseName</span></span>
<span data-ttu-id="59ad1-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="59ad1-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="59ad1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ad1-118">-DefaultProfile</span></span>
<span data-ttu-id="59ad1-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="59ad1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ad1-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="59ad1-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="59ad1-121">A credencial (nome de usuário e senha) do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="59ad1-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="59ad1-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="59ad1-122">-MemberDatabaseName</span></span>
<span data-ttu-id="59ad1-123">O nome do banco de dados SQL do Azure do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="59ad1-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="59ad1-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="59ad1-124">-MemberDatabaseType</span></span>
<span data-ttu-id="59ad1-125">O tipo de banco de dados do membro.</span><span class="sxs-lookup"><span data-stu-id="59ad1-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="59ad1-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="59ad1-126">-MemberServerName</span></span>
<span data-ttu-id="59ad1-127">O nome do SQL Server do Azure do banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="59ad1-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="59ad1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="59ad1-128">-Name</span></span>
<span data-ttu-id="59ad1-129">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="59ad1-129">The sync member name.</span></span>

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

### <span data-ttu-id="59ad1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ad1-130">-ResourceGroupName</span></span>
<span data-ttu-id="59ad1-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59ad1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="59ad1-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="59ad1-132">-ServerName</span></span>
<span data-ttu-id="59ad1-133">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="59ad1-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="59ad1-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="59ad1-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="59ad1-135">A ID do banco de dados do SQL Server que é conectada pelo agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="59ad1-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="59ad1-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="59ad1-136">-SyncAgentName</span></span>
<span data-ttu-id="59ad1-137">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="59ad1-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="59ad1-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ad1-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="59ad1-139">O nome do grupo de recursos onde está o agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="59ad1-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="59ad1-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="59ad1-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="59ad1-141">A ID do recurso do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="59ad1-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="59ad1-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="59ad1-142">-SyncAgentServerName</span></span>
<span data-ttu-id="59ad1-143">O nome do SQL Server do Azure no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="59ad1-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="59ad1-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="59ad1-144">-SyncDirection</span></span>
<span data-ttu-id="59ad1-145">A direção de sincronização deste membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="59ad1-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="59ad1-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="59ad1-146">-SyncGroupName</span></span>
<span data-ttu-id="59ad1-147">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="59ad1-147">The sync group name.</span></span>

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

### <span data-ttu-id="59ad1-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59ad1-148">-Confirm</span></span>
<span data-ttu-id="59ad1-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59ad1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59ad1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59ad1-150">-WhatIf</span></span>
<span data-ttu-id="59ad1-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59ad1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59ad1-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59ad1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59ad1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ad1-153">CommonParameters</span></span>
<span data-ttu-id="59ad1-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ad1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ad1-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59ad1-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ad1-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59ad1-156">INPUTS</span></span>

### <span data-ttu-id="59ad1-157">System. String</span><span class="sxs-lookup"><span data-stu-id="59ad1-157">System.String</span></span>

## <span data-ttu-id="59ad1-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59ad1-158">OUTPUTS</span></span>

### <span data-ttu-id="59ad1-159">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="59ad1-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="59ad1-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59ad1-160">NOTES</span></span>

## <span data-ttu-id="59ad1-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59ad1-161">RELATED LINKS</span></span>

[<span data-ttu-id="59ad1-162">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="59ad1-162">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="59ad1-163">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="59ad1-163">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="59ad1-164">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="59ad1-164">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

