---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 0010dad985755512e97aaccb14540ec16dc47cab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598819"
---
# <span data-ttu-id="19827-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19827-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="19827-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19827-102">SYNOPSIS</span></span>
<span data-ttu-id="19827-103">Remove um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="19827-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="19827-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19827-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19827-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19827-105">DESCRIPTION</span></span>
<span data-ttu-id="19827-106">O cmdlet **Remove-AzSqlSyncGroup** remove um grupo de sincronização do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="19827-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="19827-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19827-107">EXAMPLES</span></span>

### <span data-ttu-id="19827-108">Exemplo 1: remover um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="19827-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="19827-109">Esse comando Remove o grupo de sincronização do banco de dados SQL do Azure chamado syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="19827-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="19827-110">OS</span><span class="sxs-lookup"><span data-stu-id="19827-110">PARAMETERS</span></span>

### <span data-ttu-id="19827-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19827-111">-DatabaseName</span></span>
<span data-ttu-id="19827-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="19827-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="19827-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19827-113">-DefaultProfile</span></span>
<span data-ttu-id="19827-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="19827-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19827-115">-Force</span><span class="sxs-lookup"><span data-stu-id="19827-115">-Force</span></span>
<span data-ttu-id="19827-116">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="19827-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="19827-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="19827-117">-Name</span></span>
<span data-ttu-id="19827-118">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="19827-118">The sync group name.</span></span>

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

### <span data-ttu-id="19827-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19827-119">-PassThru</span></span>
<span data-ttu-id="19827-120">Define se retorna o grupo de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="19827-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="19827-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19827-121">-ResourceGroupName</span></span>
<span data-ttu-id="19827-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19827-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="19827-123">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="19827-123">-ServerName</span></span>
<span data-ttu-id="19827-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="19827-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="19827-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19827-125">-Confirm</span></span>
<span data-ttu-id="19827-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19827-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19827-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19827-127">-WhatIf</span></span>
<span data-ttu-id="19827-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19827-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19827-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19827-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19827-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19827-130">CommonParameters</span></span>
<span data-ttu-id="19827-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19827-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19827-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19827-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19827-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19827-133">INPUTS</span></span>

### <span data-ttu-id="19827-134">System. String</span><span class="sxs-lookup"><span data-stu-id="19827-134">System.String</span></span>

## <span data-ttu-id="19827-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19827-135">OUTPUTS</span></span>

### <span data-ttu-id="19827-136">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="19827-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="19827-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19827-137">NOTES</span></span>

## <span data-ttu-id="19827-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19827-138">RELATED LINKS</span></span>

[<span data-ttu-id="19827-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19827-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="19827-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19827-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="19827-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="19827-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

