---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: 7737baa8459cc9acae86cbd3e632dd73f9433056
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439993"
---
# <span data-ttu-id="e92cc-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e92cc-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="e92cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e92cc-102">SYNOPSIS</span></span>
<span data-ttu-id="e92cc-103">Atualiza um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e92cc-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e92cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e92cc-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e92cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e92cc-105">DESCRIPTION</span></span>
<span data-ttu-id="e92cc-106">O cmdlet **Update-AzureRmSqlSyncGroup** modifica as propriedades de um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e92cc-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="e92cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e92cc-107">EXAMPLES</span></span>

### <span data-ttu-id="e92cc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e92cc-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
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

<span data-ttu-id="e92cc-109">Esse comando redefine a senha de administrador para o banco de dados membro.</span><span class="sxs-lookup"><span data-stu-id="e92cc-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="e92cc-110">OS</span><span class="sxs-lookup"><span data-stu-id="e92cc-110">PARAMETERS</span></span>

### <span data-ttu-id="e92cc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e92cc-111">-DatabaseName</span></span>
<span data-ttu-id="e92cc-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e92cc-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e92cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92cc-113">-DefaultProfile</span></span>
<span data-ttu-id="e92cc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e92cc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e92cc-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e92cc-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="e92cc-116">A credencial (nome de usuário e senha) do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="e92cc-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e92cc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e92cc-117">-Name</span></span>
<span data-ttu-id="e92cc-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e92cc-118">The sync member name.</span></span>

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

### <span data-ttu-id="e92cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e92cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="e92cc-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e92cc-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e92cc-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="e92cc-121">-ServerName</span></span>
<span data-ttu-id="e92cc-122">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e92cc-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e92cc-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e92cc-123">-SyncGroupName</span></span>
<span data-ttu-id="e92cc-124">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="e92cc-124">The sync group name.</span></span>

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

### <span data-ttu-id="e92cc-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e92cc-125">-Confirm</span></span>
<span data-ttu-id="e92cc-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e92cc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e92cc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e92cc-127">-WhatIf</span></span>
<span data-ttu-id="e92cc-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e92cc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e92cc-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e92cc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e92cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92cc-130">CommonParameters</span></span>
<span data-ttu-id="e92cc-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e92cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92cc-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e92cc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92cc-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e92cc-133">INPUTS</span></span>

### <span data-ttu-id="e92cc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e92cc-134">System.String</span></span>

## <span data-ttu-id="e92cc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e92cc-135">OUTPUTS</span></span>

### <span data-ttu-id="e92cc-136">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="e92cc-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="e92cc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e92cc-137">NOTES</span></span>

## <span data-ttu-id="e92cc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e92cc-138">RELATED LINKS</span></span>

[<span data-ttu-id="e92cc-139">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e92cc-139">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="e92cc-140">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e92cc-140">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="e92cc-141">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="e92cc-141">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

