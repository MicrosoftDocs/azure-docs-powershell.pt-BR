---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947540"
---
# <span data-ttu-id="d77a9-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d77a9-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="d77a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d77a9-102">SYNOPSIS</span></span>
<span data-ttu-id="d77a9-103">Atualiza um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77a9-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d77a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d77a9-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d77a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d77a9-105">DESCRIPTION</span></span>
<span data-ttu-id="d77a9-106">O cmdlet **Update-AzSqlSyncGroup** modifica as propriedades de um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77a9-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d77a9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d77a9-107">EXAMPLES</span></span>

### <span data-ttu-id="d77a9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d77a9-108">Example 1</span></span>
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

<span data-ttu-id="d77a9-109">Esse comando redefine a senha de administrador para o banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="d77a9-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="d77a9-110">OS</span><span class="sxs-lookup"><span data-stu-id="d77a9-110">PARAMETERS</span></span>

### <span data-ttu-id="d77a9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d77a9-111">-DatabaseName</span></span>
<span data-ttu-id="d77a9-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77a9-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d77a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77a9-113">-DefaultProfile</span></span>
<span data-ttu-id="d77a9-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d77a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d77a9-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d77a9-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="d77a9-116">A credencial (nome de usuário e senha) do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d77a9-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d77a9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d77a9-117">-Name</span></span>
<span data-ttu-id="d77a9-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d77a9-118">The sync member name.</span></span>

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

### <span data-ttu-id="d77a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d77a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="d77a9-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d77a9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="d77a9-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d77a9-121">-ServerName</span></span>
<span data-ttu-id="d77a9-122">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d77a9-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d77a9-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d77a9-123">-SyncGroupName</span></span>
<span data-ttu-id="d77a9-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d77a9-124">The sync group name.</span></span>

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

### <span data-ttu-id="d77a9-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="d77a9-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="d77a9-126">A ID do recurso para o banco de dados do membro de sincronização, usado se UsePrivateLinkConnection for definido como true.</span><span class="sxs-lookup"><span data-stu-id="d77a9-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="d77a9-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d77a9-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="d77a9-128">Se o link privado deve ser usado ao conectar-se a este membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d77a9-128">Whether to use private link when connecting to this sync member.</span></span>

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

### <span data-ttu-id="d77a9-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d77a9-129">-Confirm</span></span>
<span data-ttu-id="d77a9-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d77a9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d77a9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d77a9-131">-WhatIf</span></span>
<span data-ttu-id="d77a9-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d77a9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d77a9-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d77a9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d77a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77a9-134">CommonParameters</span></span>
<span data-ttu-id="d77a9-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d77a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77a9-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d77a9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77a9-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d77a9-137">INPUTS</span></span>

### <span data-ttu-id="d77a9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d77a9-138">System.String</span></span>

## <span data-ttu-id="d77a9-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d77a9-139">OUTPUTS</span></span>

### <span data-ttu-id="d77a9-140">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d77a9-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d77a9-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d77a9-141">NOTES</span></span>

## <span data-ttu-id="d77a9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d77a9-142">RELATED LINKS</span></span>

[<span data-ttu-id="d77a9-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d77a9-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="d77a9-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d77a9-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="d77a9-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d77a9-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

