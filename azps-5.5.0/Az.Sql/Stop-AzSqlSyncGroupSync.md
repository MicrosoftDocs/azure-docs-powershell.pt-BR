---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112536"
---
# <span data-ttu-id="d5e87-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d5e87-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="d5e87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5e87-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e87-103">Interrompe uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d5e87-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="d5e87-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5e87-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5e87-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5e87-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e87-106">O cmdlet **Stop-AzSqlSyncGroupSync** interrompe uma sincronização de grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d5e87-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="d5e87-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5e87-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e87-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5e87-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="d5e87-109">Esse comando interrompe a sincronização que está em andamento para o mysg do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d5e87-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="d5e87-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5e87-110">PARAMETERS</span></span>

### <span data-ttu-id="d5e87-111">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="d5e87-111">-DatabaseName</span></span>
<span data-ttu-id="d5e87-112">O nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e87-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d5e87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e87-113">-DefaultProfile</span></span>
<span data-ttu-id="d5e87-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d5e87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5e87-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5e87-115">-PassThru</span></span>
<span data-ttu-id="d5e87-116">Define se o grupo de sincronização deve retornar</span><span class="sxs-lookup"><span data-stu-id="d5e87-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="d5e87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e87-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5e87-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d5e87-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d5e87-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5e87-119">-ServerName</span></span>
<span data-ttu-id="d5e87-120">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e87-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d5e87-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e87-121">-SyncGroupName</span></span>
<span data-ttu-id="d5e87-122">O nome do grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="d5e87-122">The sync group name.</span></span>

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

### <span data-ttu-id="d5e87-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d5e87-123">-Confirm</span></span>
<span data-ttu-id="d5e87-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5e87-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5e87-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5e87-125">-WhatIf</span></span>
<span data-ttu-id="d5e87-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d5e87-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5e87-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5e87-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5e87-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e87-128">CommonParameters</span></span>
<span data-ttu-id="d5e87-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5e87-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e87-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5e87-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e87-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="d5e87-131">INPUTS</span></span>

### <span data-ttu-id="d5e87-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d5e87-132">System.String</span></span>

## <span data-ttu-id="d5e87-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="d5e87-133">OUTPUTS</span></span>

### <span data-ttu-id="d5e87-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d5e87-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d5e87-135">Notas</span><span class="sxs-lookup"><span data-stu-id="d5e87-135">NOTES</span></span>

## <span data-ttu-id="d5e87-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5e87-136">RELATED LINKS</span></span>

[<span data-ttu-id="d5e87-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="d5e87-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

