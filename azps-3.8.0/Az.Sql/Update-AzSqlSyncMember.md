---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777939"
---
# <span data-ttu-id="b2974-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2974-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="b2974-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2974-102">SYNOPSIS</span></span>
<span data-ttu-id="b2974-103">Atualiza um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2974-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="b2974-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2974-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2974-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2974-105">DESCRIPTION</span></span>
<span data-ttu-id="b2974-106">O cmdlet **Update-AzSqlSyncGroup** modifica as propriedades de um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2974-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="b2974-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2974-107">EXAMPLES</span></span>

### <span data-ttu-id="b2974-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2974-108">Example 1</span></span>
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

<span data-ttu-id="b2974-109">Esse comando redefine a senha de administrador para o banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="b2974-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="b2974-110">OS</span><span class="sxs-lookup"><span data-stu-id="b2974-110">PARAMETERS</span></span>

### <span data-ttu-id="b2974-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2974-111">-DatabaseName</span></span>
<span data-ttu-id="b2974-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2974-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b2974-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2974-113">-DefaultProfile</span></span>
<span data-ttu-id="b2974-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b2974-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2974-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="b2974-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="b2974-116">A credencial (nome de usuário e senha) do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2974-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2974-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2974-117">-Name</span></span>
<span data-ttu-id="b2974-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b2974-118">The sync member name.</span></span>

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

### <span data-ttu-id="b2974-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2974-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2974-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2974-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2974-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b2974-121">-ServerName</span></span>
<span data-ttu-id="b2974-122">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b2974-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="b2974-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b2974-123">-SyncGroupName</span></span>
<span data-ttu-id="b2974-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b2974-124">The sync group name.</span></span>

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

### <span data-ttu-id="b2974-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2974-125">-Confirm</span></span>
<span data-ttu-id="b2974-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2974-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2974-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2974-127">-WhatIf</span></span>
<span data-ttu-id="b2974-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2974-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2974-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2974-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2974-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2974-130">CommonParameters</span></span>
<span data-ttu-id="b2974-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2974-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2974-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2974-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2974-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2974-133">INPUTS</span></span>

### <span data-ttu-id="b2974-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b2974-134">System.String</span></span>

## <span data-ttu-id="b2974-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2974-135">OUTPUTS</span></span>

### <span data-ttu-id="b2974-136">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="b2974-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="b2974-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2974-137">NOTES</span></span>

## <span data-ttu-id="b2974-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2974-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2974-139">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2974-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="b2974-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2974-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="b2974-141">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="b2974-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

