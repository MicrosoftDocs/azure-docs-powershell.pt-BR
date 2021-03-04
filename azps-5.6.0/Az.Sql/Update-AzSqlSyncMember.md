---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 3c4b50a4d4f4c01365d853e64cb3a53ea9c05d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890559"
---
# <span data-ttu-id="f2b13-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f2b13-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="f2b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b13-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b13-103">Atualiza um membro de sincronização de SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b13-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f2b13-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2b13-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b13-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2b13-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b13-106">O cmdlet **Update-AzSqlSyncGroup** modifica propriedades de um membro de sincronização de banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f2b13-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f2b13-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2b13-107">EXAMPLES</span></span>

### <span data-ttu-id="f2b13-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2b13-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="f2b13-109">Esse comando redefine a senha do administrador para o banco de dados de membros.</span><span class="sxs-lookup"><span data-stu-id="f2b13-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="f2b13-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2b13-110">PARAMETERS</span></span>

### <span data-ttu-id="f2b13-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2b13-111">-DatabaseName</span></span>
<span data-ttu-id="f2b13-112">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f2b13-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f2b13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b13-113">-DefaultProfile</span></span>
<span data-ttu-id="f2b13-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f2b13-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2b13-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="f2b13-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="f2b13-116">A credencial (nome de usuário e senha) do Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f2b13-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b13-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f2b13-117">-Name</span></span>
<span data-ttu-id="f2b13-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f2b13-118">The sync member name.</span></span>

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

### <span data-ttu-id="f2b13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b13-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2b13-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f2b13-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f2b13-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f2b13-121">-ServerName</span></span>
<span data-ttu-id="f2b13-122">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f2b13-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f2b13-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b13-123">-SyncGroupName</span></span>
<span data-ttu-id="f2b13-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f2b13-124">The sync group name.</span></span>

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

### <span data-ttu-id="f2b13-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b13-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="f2b13-126">A ID do recurso para o banco de dados de membros de sincronização, usada se UsePrivateLinkConnection estiver definida como true.</span><span class="sxs-lookup"><span data-stu-id="f2b13-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="f2b13-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f2b13-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="f2b13-128">Se deve usar o link privado ao se conectar a esse membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f2b13-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b13-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2b13-129">-Confirm</span></span>
<span data-ttu-id="f2b13-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2b13-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b13-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b13-131">-WhatIf</span></span>
<span data-ttu-id="f2b13-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2b13-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b13-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2b13-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b13-134">CommonParameters</span></span>
<span data-ttu-id="f2b13-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b13-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2b13-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b13-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2b13-137">INPUTS</span></span>

### <span data-ttu-id="f2b13-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f2b13-138">System.String</span></span>

## <span data-ttu-id="f2b13-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2b13-139">OUTPUTS</span></span>

### <span data-ttu-id="f2b13-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="f2b13-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f2b13-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2b13-141">NOTES</span></span>

## <span data-ttu-id="f2b13-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2b13-142">RELATED LINKS</span></span>

[<span data-ttu-id="f2b13-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f2b13-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="f2b13-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f2b13-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="f2b13-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f2b13-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

