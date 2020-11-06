---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: 34db2f2307d60f1653b0a806350d96fa9e3380af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598818"
---
# <span data-ttu-id="64137-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="64137-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="64137-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64137-102">SYNOPSIS</span></span>
<span data-ttu-id="64137-103">Remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="64137-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="64137-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64137-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64137-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64137-105">DESCRIPTION</span></span>
<span data-ttu-id="64137-106">O cmdlet **Remove-AzSqlSyncMember** remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="64137-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="64137-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64137-107">EXAMPLES</span></span>

### <span data-ttu-id="64137-108">Exemplo 1: remover um membro de sincronização</span><span class="sxs-lookup"><span data-stu-id="64137-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="64137-109">Esse comando Remove o membro de sincronização do banco de dados SQL do Azure chamado syncMember01.</span><span class="sxs-lookup"><span data-stu-id="64137-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="64137-110">OS</span><span class="sxs-lookup"><span data-stu-id="64137-110">PARAMETERS</span></span>

### <span data-ttu-id="64137-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64137-111">-DatabaseName</span></span>
<span data-ttu-id="64137-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="64137-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="64137-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64137-113">-DefaultProfile</span></span>
<span data-ttu-id="64137-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="64137-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64137-115">-Force</span><span class="sxs-lookup"><span data-stu-id="64137-115">-Force</span></span>
<span data-ttu-id="64137-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="64137-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="64137-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="64137-117">-Name</span></span>
<span data-ttu-id="64137-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="64137-118">The sync member name.</span></span>

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

### <span data-ttu-id="64137-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64137-119">-PassThru</span></span>
<span data-ttu-id="64137-120">Define se retornar o membro de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="64137-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="64137-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64137-121">-ResourceGroupName</span></span>
<span data-ttu-id="64137-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64137-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="64137-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="64137-123">-ServerName</span></span>
<span data-ttu-id="64137-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="64137-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="64137-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="64137-125">-SyncGroupName</span></span>
<span data-ttu-id="64137-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="64137-126">The sync group name.</span></span>

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

### <span data-ttu-id="64137-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64137-127">-Confirm</span></span>
<span data-ttu-id="64137-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64137-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64137-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64137-129">-WhatIf</span></span>
<span data-ttu-id="64137-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64137-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64137-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64137-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64137-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64137-132">CommonParameters</span></span>
<span data-ttu-id="64137-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64137-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64137-134">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64137-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64137-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64137-135">INPUTS</span></span>

### <span data-ttu-id="64137-136">System. String</span><span class="sxs-lookup"><span data-stu-id="64137-136">System.String</span></span>

## <span data-ttu-id="64137-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64137-137">OUTPUTS</span></span>

### <span data-ttu-id="64137-138">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="64137-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="64137-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64137-139">NOTES</span></span>

## <span data-ttu-id="64137-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64137-140">RELATED LINKS</span></span>

[<span data-ttu-id="64137-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="64137-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="64137-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="64137-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="64137-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="64137-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

