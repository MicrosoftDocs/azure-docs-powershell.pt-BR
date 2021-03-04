---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 58a6ee3d51af355c0824025f856ed1646fa23cf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890960"
---
# <span data-ttu-id="6e00f-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e00f-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="6e00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e00f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e00f-103">Remove um membro de sincronização de SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e00f-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6e00f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e00f-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e00f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e00f-105">DESCRIPTION</span></span>
<span data-ttu-id="6e00f-106">O cmdlet **Remove-AzSqlSyncMember** remove um membro de sincronização de banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6e00f-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="6e00f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e00f-107">EXAMPLES</span></span>

### <span data-ttu-id="6e00f-108">Exemplo 1: Remover um membro de sincronização</span><span class="sxs-lookup"><span data-stu-id="6e00f-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="6e00f-109">Este comando remove o Membro de Sincronização de Banco de Dados do Azure SQL chamado syncMember01.</span><span class="sxs-lookup"><span data-stu-id="6e00f-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="6e00f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e00f-110">PARAMETERS</span></span>

### <span data-ttu-id="6e00f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e00f-111">-DatabaseName</span></span>
<span data-ttu-id="6e00f-112">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6e00f-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6e00f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e00f-113">-DefaultProfile</span></span>
<span data-ttu-id="6e00f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6e00f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e00f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6e00f-115">-Force</span></span>
<span data-ttu-id="6e00f-116">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="6e00f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6e00f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6e00f-117">-Name</span></span>
<span data-ttu-id="6e00f-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6e00f-118">The sync member name.</span></span>

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

### <span data-ttu-id="6e00f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e00f-119">-PassThru</span></span>
<span data-ttu-id="6e00f-120">Define se retorna o membro de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="6e00f-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="6e00f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e00f-121">-ResourceGroupName</span></span>
<span data-ttu-id="6e00f-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e00f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e00f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e00f-123">-ServerName</span></span>
<span data-ttu-id="6e00f-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6e00f-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6e00f-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6e00f-125">-SyncGroupName</span></span>
<span data-ttu-id="6e00f-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6e00f-126">The sync group name.</span></span>

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

### <span data-ttu-id="6e00f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e00f-127">-Confirm</span></span>
<span data-ttu-id="6e00f-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e00f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e00f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e00f-129">-WhatIf</span></span>
<span data-ttu-id="6e00f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e00f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e00f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e00f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e00f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e00f-132">CommonParameters</span></span>
<span data-ttu-id="6e00f-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e00f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e00f-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e00f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e00f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e00f-135">INPUTS</span></span>

### <span data-ttu-id="6e00f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6e00f-136">System.String</span></span>

## <span data-ttu-id="6e00f-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e00f-137">OUTPUTS</span></span>

### <span data-ttu-id="6e00f-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="6e00f-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="6e00f-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e00f-139">NOTES</span></span>

## <span data-ttu-id="6e00f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e00f-140">RELATED LINKS</span></span>

[<span data-ttu-id="6e00f-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e00f-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="6e00f-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e00f-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="6e00f-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="6e00f-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

