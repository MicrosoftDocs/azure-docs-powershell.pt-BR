---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: ea8390de90fff5fb1e228884b131551a5be86e48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890574"
---
# <span data-ttu-id="a81cc-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a81cc-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="a81cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a81cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a81cc-103">Interrompe uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a81cc-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="a81cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a81cc-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a81cc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a81cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a81cc-106">O cmdlet **Stop-AzSqlSyncGroupSync** interrompe uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a81cc-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="a81cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a81cc-107">EXAMPLES</span></span>

### <span data-ttu-id="a81cc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a81cc-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="a81cc-109">Este comando interrompe a sincronização que está em andamento para o mysg do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a81cc-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="a81cc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a81cc-110">PARAMETERS</span></span>

### <span data-ttu-id="a81cc-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a81cc-111">-DatabaseName</span></span>
<span data-ttu-id="a81cc-112">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a81cc-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a81cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81cc-113">-DefaultProfile</span></span>
<span data-ttu-id="a81cc-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a81cc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a81cc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a81cc-115">-PassThru</span></span>
<span data-ttu-id="a81cc-116">Define se o grupo de sincronização retornará</span><span class="sxs-lookup"><span data-stu-id="a81cc-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="a81cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a81cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="a81cc-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a81cc-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a81cc-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a81cc-119">-ServerName</span></span>
<span data-ttu-id="a81cc-120">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a81cc-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a81cc-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a81cc-121">-SyncGroupName</span></span>
<span data-ttu-id="a81cc-122">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="a81cc-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a81cc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a81cc-123">-Confirm</span></span>
<span data-ttu-id="a81cc-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a81cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a81cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a81cc-125">-WhatIf</span></span>
<span data-ttu-id="a81cc-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a81cc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a81cc-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a81cc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a81cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81cc-128">CommonParameters</span></span>
<span data-ttu-id="a81cc-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a81cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81cc-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a81cc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81cc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a81cc-131">INPUTS</span></span>

### <span data-ttu-id="a81cc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a81cc-132">System.String</span></span>

## <span data-ttu-id="a81cc-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a81cc-133">OUTPUTS</span></span>

### <span data-ttu-id="a81cc-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a81cc-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a81cc-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="a81cc-135">NOTES</span></span>

## <span data-ttu-id="a81cc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a81cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="a81cc-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a81cc-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

