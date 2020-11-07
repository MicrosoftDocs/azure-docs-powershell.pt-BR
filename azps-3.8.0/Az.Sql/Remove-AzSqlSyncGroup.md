---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943163"
---
# <span data-ttu-id="6c2e8-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6c2e8-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="6c2e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c2e8-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2e8-103">Remove um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="6c2e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c2e8-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c2e8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c2e8-105">DESCRIPTION</span></span>
<span data-ttu-id="6c2e8-106">O cmdlet **Remove-AzSqlSyncGroup** remove um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="6c2e8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c2e8-107">EXAMPLES</span></span>

### <span data-ttu-id="6c2e8-108">Exemplo 1: remover um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="6c2e8-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="6c2e8-109">Esse comando Remove o grupo de sincronização do banco de dados SQL do Azure chamado syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="6c2e8-110">OS</span><span class="sxs-lookup"><span data-stu-id="6c2e8-110">PARAMETERS</span></span>

### <span data-ttu-id="6c2e8-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6c2e8-111">-DatabaseName</span></span>
<span data-ttu-id="6c2e8-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6c2e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2e8-113">-DefaultProfile</span></span>
<span data-ttu-id="6c2e8-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6c2e8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c2e8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6c2e8-115">-Force</span></span>
<span data-ttu-id="6c2e8-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="6c2e8-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6c2e8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c2e8-117">-Name</span></span>
<span data-ttu-id="6c2e8-118">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2e8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c2e8-119">-PassThru</span></span>
<span data-ttu-id="6c2e8-120">Define se retorna o grupo de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="6c2e8-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="6c2e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c2e8-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c2e8-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="6c2e8-123">-ServerName</span></span>
<span data-ttu-id="6c2e8-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6c2e8-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c2e8-125">-Confirm</span></span>
<span data-ttu-id="6c2e8-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c2e8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c2e8-127">-WhatIf</span></span>
<span data-ttu-id="6c2e8-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c2e8-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c2e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2e8-130">CommonParameters</span></span>
<span data-ttu-id="6c2e8-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2e8-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c2e8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2e8-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c2e8-133">INPUTS</span></span>

### <span data-ttu-id="6c2e8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6c2e8-134">System.String</span></span>

## <span data-ttu-id="6c2e8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c2e8-135">OUTPUTS</span></span>

### <span data-ttu-id="6c2e8-136">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="6c2e8-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="6c2e8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c2e8-137">NOTES</span></span>

## <span data-ttu-id="6c2e8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c2e8-138">RELATED LINKS</span></span>

[<span data-ttu-id="6c2e8-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6c2e8-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="6c2e8-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6c2e8-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="6c2e8-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6c2e8-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

