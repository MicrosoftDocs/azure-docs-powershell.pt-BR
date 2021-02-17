---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 5846435df4921e425e12e908539849fda0bd2472
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399525"
---
# <span data-ttu-id="ea13a-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ea13a-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="ea13a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea13a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea13a-103">Cria um Membro de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea13a-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ea13a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea13a-104">SYNTAX</span></span>

### <span data-ttu-id="ea13a-105">AzureSqlDatabase (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ea13a-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea13a-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="ea13a-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea13a-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="ea13a-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea13a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea13a-108">DESCRIPTION</span></span>
<span data-ttu-id="ea13a-109">O **cmdlet New-AzSqlSyncMember** cria um Membro de Sincronização de Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea13a-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ea13a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ea13a-110">EXAMPLES</span></span>

### <span data-ttu-id="ea13a-111">Exemplo 1: Criar um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea13a-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="ea13a-112">Esse comando cria um membro de sincronização para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea13a-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="ea13a-113">Exemplo 2: Criar um membro de sincronização para um banco de dados do SQL Server local</span><span class="sxs-lookup"><span data-stu-id="ea13a-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="ea13a-114">Esse comando cria um membro de sincronização para um banco de dados SQL local.</span><span class="sxs-lookup"><span data-stu-id="ea13a-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="ea13a-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea13a-115">PARAMETERS</span></span>

### <span data-ttu-id="ea13a-116">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="ea13a-116">-DatabaseName</span></span>
<span data-ttu-id="ea13a-117">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea13a-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ea13a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea13a-118">-DefaultProfile</span></span>
<span data-ttu-id="ea13a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ea13a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea13a-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ea13a-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="ea13a-121">A credencial (nome de usuário e senha) do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea13a-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ea13a-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ea13a-122">-MemberDatabaseName</span></span>
<span data-ttu-id="ea13a-123">O nome do banco de dados SQL do Azure do banco de dados do membro.</span><span class="sxs-lookup"><span data-stu-id="ea13a-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="ea13a-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="ea13a-124">-MemberDatabaseType</span></span>
<span data-ttu-id="ea13a-125">O tipo de banco de dados do banco de dados do membro.</span><span class="sxs-lookup"><span data-stu-id="ea13a-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="ea13a-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="ea13a-126">-MemberServerName</span></span>
<span data-ttu-id="ea13a-127">O Nome do SQL Server do Azure do banco de dados do membro.</span><span class="sxs-lookup"><span data-stu-id="ea13a-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="ea13a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea13a-128">-Name</span></span>
<span data-ttu-id="ea13a-129">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea13a-129">The sync member name.</span></span>

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

### <span data-ttu-id="ea13a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea13a-130">-ResourceGroupName</span></span>
<span data-ttu-id="ea13a-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea13a-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea13a-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea13a-132">-ServerName</span></span>
<span data-ttu-id="ea13a-133">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea13a-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ea13a-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="ea13a-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="ea13a-135">A id do banco de dados do sql server que está conectado pelo agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea13a-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="ea13a-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="ea13a-136">-SyncAgentName</span></span>
<span data-ttu-id="ea13a-137">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea13a-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="ea13a-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea13a-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="ea13a-139">O nome do grupo de recursos no qual o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="ea13a-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="ea13a-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="ea13a-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="ea13a-141">A ID do recurso do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea13a-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="ea13a-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="ea13a-142">-SyncAgentServerName</span></span>
<span data-ttu-id="ea13a-143">O nome do SQL Server do Azure onde o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="ea13a-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="ea13a-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="ea13a-144">-SyncDirection</span></span>
<span data-ttu-id="ea13a-145">A direção de sincronização desse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea13a-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="ea13a-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ea13a-146">-SyncGroupName</span></span>
<span data-ttu-id="ea13a-147">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea13a-147">The sync group name.</span></span>

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

### <span data-ttu-id="ea13a-148">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ea13a-148">-Confirm</span></span>
<span data-ttu-id="ea13a-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea13a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea13a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea13a-150">-WhatIf</span></span>
<span data-ttu-id="ea13a-151">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ea13a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea13a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea13a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea13a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea13a-153">CommonParameters</span></span>
<span data-ttu-id="ea13a-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea13a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea13a-155">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea13a-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea13a-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="ea13a-156">INPUTS</span></span>

### <span data-ttu-id="ea13a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="ea13a-157">System.String</span></span>

## <span data-ttu-id="ea13a-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="ea13a-158">OUTPUTS</span></span>

### <span data-ttu-id="ea13a-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ea13a-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ea13a-160">Notas</span><span class="sxs-lookup"><span data-stu-id="ea13a-160">NOTES</span></span>

## <span data-ttu-id="ea13a-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea13a-161">RELATED LINKS</span></span>

[<span data-ttu-id="ea13a-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ea13a-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


[<span data-ttu-id="ea13a-163">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ea13a-163">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

