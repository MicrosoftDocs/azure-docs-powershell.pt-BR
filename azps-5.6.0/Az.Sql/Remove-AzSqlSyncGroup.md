---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: ce69f6b087a7ed61f415e3d6a649f757bb10178f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890964"
---
# <span data-ttu-id="38a33-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="38a33-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="38a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38a33-102">SYNOPSIS</span></span>
<span data-ttu-id="38a33-103">Remove um grupo de sincronização SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="38a33-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="38a33-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38a33-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38a33-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38a33-105">DESCRIPTION</span></span>
<span data-ttu-id="38a33-106">O cmdlet **Remove-AzSqlSyncGroup** remove um Grupo de Sincronização de Banco de Dados do Azure SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="38a33-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="38a33-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38a33-107">EXAMPLES</span></span>

### <span data-ttu-id="38a33-108">Exemplo 1: Remover um grupo de sincronização</span><span class="sxs-lookup"><span data-stu-id="38a33-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="38a33-109">Este comando remove o Grupo de Sincronização de Banco de Dados do Azure SQL chamado syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="38a33-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="38a33-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38a33-110">PARAMETERS</span></span>

### <span data-ttu-id="38a33-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="38a33-111">-DatabaseName</span></span>
<span data-ttu-id="38a33-112">O nome do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="38a33-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="38a33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a33-113">-DefaultProfile</span></span>
<span data-ttu-id="38a33-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="38a33-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38a33-115">-Force</span><span class="sxs-lookup"><span data-stu-id="38a33-115">-Force</span></span>
<span data-ttu-id="38a33-116">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="38a33-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="38a33-117">-Name</span><span class="sxs-lookup"><span data-stu-id="38a33-117">-Name</span></span>
<span data-ttu-id="38a33-118">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="38a33-118">The sync group name.</span></span>

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

### <span data-ttu-id="38a33-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38a33-119">-PassThru</span></span>
<span data-ttu-id="38a33-120">Define se retorna o grupo de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="38a33-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="38a33-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a33-121">-ResourceGroupName</span></span>
<span data-ttu-id="38a33-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38a33-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="38a33-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38a33-123">-ServerName</span></span>
<span data-ttu-id="38a33-124">O nome do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="38a33-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="38a33-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38a33-125">-Confirm</span></span>
<span data-ttu-id="38a33-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38a33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a33-127">-WhatIf</span></span>
<span data-ttu-id="38a33-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38a33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a33-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38a33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38a33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a33-130">CommonParameters</span></span>
<span data-ttu-id="38a33-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a33-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a33-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a33-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38a33-133">INPUTS</span></span>

### <span data-ttu-id="38a33-134">System.String</span><span class="sxs-lookup"><span data-stu-id="38a33-134">System.String</span></span>

## <span data-ttu-id="38a33-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38a33-135">OUTPUTS</span></span>

### <span data-ttu-id="38a33-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="38a33-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="38a33-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="38a33-137">NOTES</span></span>

## <span data-ttu-id="38a33-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38a33-138">RELATED LINKS</span></span>

[<span data-ttu-id="38a33-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="38a33-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="38a33-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="38a33-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="38a33-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="38a33-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

