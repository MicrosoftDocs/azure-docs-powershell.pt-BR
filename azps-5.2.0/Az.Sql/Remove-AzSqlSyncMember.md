---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256655"
---
# <span data-ttu-id="f832c-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f832c-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="f832c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f832c-102">SYNOPSIS</span></span>
<span data-ttu-id="f832c-103">Remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f832c-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f832c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f832c-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f832c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f832c-105">DESCRIPTION</span></span>
<span data-ttu-id="f832c-106">O cmdlet **Remove-AzSqlSyncMember** remove um membro de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f832c-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f832c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f832c-107">EXAMPLES</span></span>

### <span data-ttu-id="f832c-108">Exemplo 1: remover um membro de sincronização</span><span class="sxs-lookup"><span data-stu-id="f832c-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="f832c-109">Esse comando Remove o membro de sincronização do banco de dados SQL do Azure chamado syncMember01.</span><span class="sxs-lookup"><span data-stu-id="f832c-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="f832c-110">OS</span><span class="sxs-lookup"><span data-stu-id="f832c-110">PARAMETERS</span></span>

### <span data-ttu-id="f832c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f832c-111">-DatabaseName</span></span>
<span data-ttu-id="f832c-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f832c-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f832c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f832c-113">-DefaultProfile</span></span>
<span data-ttu-id="f832c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f832c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f832c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f832c-115">-Force</span></span>
<span data-ttu-id="f832c-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="f832c-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f832c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f832c-117">-Name</span></span>
<span data-ttu-id="f832c-118">O nome do membro de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f832c-118">The sync member name.</span></span>

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

### <span data-ttu-id="f832c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f832c-119">-PassThru</span></span>
<span data-ttu-id="f832c-120">Define se retornar o membro de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="f832c-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="f832c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f832c-121">-ResourceGroupName</span></span>
<span data-ttu-id="f832c-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f832c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f832c-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f832c-123">-ServerName</span></span>
<span data-ttu-id="f832c-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f832c-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f832c-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f832c-125">-SyncGroupName</span></span>
<span data-ttu-id="f832c-126">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f832c-126">The sync group name.</span></span>

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

### <span data-ttu-id="f832c-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f832c-127">-Confirm</span></span>
<span data-ttu-id="f832c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f832c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f832c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f832c-129">-WhatIf</span></span>
<span data-ttu-id="f832c-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f832c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f832c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f832c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f832c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f832c-132">CommonParameters</span></span>
<span data-ttu-id="f832c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f832c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f832c-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f832c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f832c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f832c-135">INPUTS</span></span>

### <span data-ttu-id="f832c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f832c-136">System.String</span></span>

## <span data-ttu-id="f832c-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f832c-137">OUTPUTS</span></span>

### <span data-ttu-id="f832c-138">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="f832c-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f832c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f832c-139">NOTES</span></span>

## <span data-ttu-id="f832c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f832c-140">RELATED LINKS</span></span>

[<span data-ttu-id="f832c-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f832c-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="f832c-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f832c-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="f832c-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f832c-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

