---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 30c0cca7fb1d8eab2c5d0abe4d6c0d556cc92d7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890971"
---
# <span data-ttu-id="c6b5f-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c6b5f-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="c6b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b5f-103">Remove um Agente de Sincronização do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="c6b5f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c6b5f-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6b5f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c6b5f-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b5f-106">O cmdlet **Remove-AzSqlSyncAgent** remove um Agente SQL Sync do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="c6b5f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6b5f-107">EXAMPLES</span></span>

### <span data-ttu-id="c6b5f-108">Exemplo 1: Remover um agente de sincronização</span><span class="sxs-lookup"><span data-stu-id="c6b5f-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="c6b5f-109">Este comando remove o Agente de Sincronização do Azure SQL chamado syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="c6b5f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c6b5f-110">PARAMETERS</span></span>

### <span data-ttu-id="c6b5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b5f-111">-DefaultProfile</span></span>
<span data-ttu-id="c6b5f-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c6b5f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6b5f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c6b5f-113">-Force</span></span>
<span data-ttu-id="c6b5f-114">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="c6b5f-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c6b5f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c6b5f-115">-Name</span></span>
<span data-ttu-id="c6b5f-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6b5f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6b5f-117">-PassThru</span></span>
<span data-ttu-id="c6b5f-118">Define se o agente de sincronização removido deve retornar</span><span class="sxs-lookup"><span data-stu-id="c6b5f-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="c6b5f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b5f-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6b5f-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6b5f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6b5f-121">-ServerName</span></span>
<span data-ttu-id="c6b5f-122">O nome do Azure SQL Server o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="c6b5f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6b5f-123">-Confirm</span></span>
<span data-ttu-id="c6b5f-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b5f-125">-WhatIf</span></span>
<span data-ttu-id="c6b5f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b5f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b5f-128">CommonParameters</span></span>
<span data-ttu-id="c6b5f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6b5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b5f-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6b5f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b5f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6b5f-131">INPUTS</span></span>

### <span data-ttu-id="c6b5f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c6b5f-132">System.String</span></span>

## <span data-ttu-id="c6b5f-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c6b5f-133">OUTPUTS</span></span>

### <span data-ttu-id="c6b5f-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="c6b5f-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="c6b5f-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="c6b5f-135">NOTES</span></span>

## <span data-ttu-id="c6b5f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6b5f-136">RELATED LINKS</span></span>

[<span data-ttu-id="c6b5f-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c6b5f-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="c6b5f-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c6b5f-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

