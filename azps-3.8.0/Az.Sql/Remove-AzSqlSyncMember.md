---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943162"
---
# <span data-ttu-id="d3aa7-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d3aa7-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="d3aa7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="d3aa7-103">Remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d3aa7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3aa7-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3aa7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="d3aa7-106">O cmdlet **Remove-AzSqlSyncMember** remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d3aa7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3aa7-107">EXAMPLES</span></span>

### <span data-ttu-id="d3aa7-108">Exemplo 1: remover um membro de sincronização</span><span class="sxs-lookup"><span data-stu-id="d3aa7-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="d3aa7-109">Esse comando Remove o membro de sincronização do banco de dados SQL do Azure chamado syncMember01.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="d3aa7-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3aa7-110">PARAMETERS</span></span>

### <span data-ttu-id="d3aa7-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3aa7-111">-DatabaseName</span></span>
<span data-ttu-id="d3aa7-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d3aa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3aa7-113">-DefaultProfile</span></span>
<span data-ttu-id="d3aa7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d3aa7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3aa7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3aa7-115">-Force</span></span>
<span data-ttu-id="d3aa7-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="d3aa7-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d3aa7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3aa7-117">-Name</span></span>
<span data-ttu-id="d3aa7-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-118">The sync member name.</span></span>

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

### <span data-ttu-id="d3aa7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3aa7-119">-PassThru</span></span>
<span data-ttu-id="d3aa7-120">Define se retornar o membro de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="d3aa7-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="d3aa7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3aa7-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3aa7-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3aa7-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d3aa7-123">-ServerName</span></span>
<span data-ttu-id="d3aa7-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d3aa7-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d3aa7-125">-SyncGroupName</span></span>
<span data-ttu-id="d3aa7-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-126">The sync group name.</span></span>

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

### <span data-ttu-id="d3aa7-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3aa7-127">-Confirm</span></span>
<span data-ttu-id="d3aa7-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3aa7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3aa7-129">-WhatIf</span></span>
<span data-ttu-id="d3aa7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3aa7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3aa7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3aa7-132">CommonParameters</span></span>
<span data-ttu-id="d3aa7-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3aa7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3aa7-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3aa7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3aa7-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3aa7-135">INPUTS</span></span>

### <span data-ttu-id="d3aa7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d3aa7-136">System.String</span></span>

## <span data-ttu-id="d3aa7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3aa7-137">OUTPUTS</span></span>

### <span data-ttu-id="d3aa7-138">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d3aa7-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d3aa7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3aa7-139">NOTES</span></span>

## <span data-ttu-id="d3aa7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3aa7-140">RELATED LINKS</span></span>

[<span data-ttu-id="d3aa7-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d3aa7-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="d3aa7-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d3aa7-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="d3aa7-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d3aa7-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

