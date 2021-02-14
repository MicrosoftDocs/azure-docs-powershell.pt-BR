---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111307"
---
# <span data-ttu-id="7e294-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7e294-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="7e294-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e294-102">SYNOPSIS</span></span>
<span data-ttu-id="7e294-103">Remove um Agente de Sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e294-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7e294-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e294-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e294-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e294-105">DESCRIPTION</span></span>
<span data-ttu-id="7e294-106">O cmdlet **Remove-AzSqlSyncAgent** remove um Agente de Sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e294-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="7e294-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7e294-107">EXAMPLES</span></span>

### <span data-ttu-id="7e294-108">Exemplo 1: Remover um agente de sincronização</span><span class="sxs-lookup"><span data-stu-id="7e294-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="7e294-109">Esse comando remove o Agente de Sincronização SQL do Azure chamado syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="7e294-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="7e294-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e294-110">PARAMETERS</span></span>

### <span data-ttu-id="7e294-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e294-111">-DefaultProfile</span></span>
<span data-ttu-id="7e294-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7e294-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e294-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="7e294-113">-Force</span></span>
<span data-ttu-id="7e294-114">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="7e294-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7e294-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e294-115">-Name</span></span>
<span data-ttu-id="7e294-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7e294-116">The sync agent name.</span></span>

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

### <span data-ttu-id="7e294-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e294-117">-PassThru</span></span>
<span data-ttu-id="7e294-118">Define se retorna o agente de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="7e294-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="7e294-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e294-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e294-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7e294-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e294-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e294-121">-ServerName</span></span>
<span data-ttu-id="7e294-122">O nome do SQL Server do Azure em que o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="7e294-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7e294-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7e294-123">-Confirm</span></span>
<span data-ttu-id="7e294-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e294-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e294-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e294-125">-WhatIf</span></span>
<span data-ttu-id="7e294-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7e294-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e294-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e294-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e294-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e294-128">CommonParameters</span></span>
<span data-ttu-id="7e294-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e294-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e294-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e294-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e294-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="7e294-131">INPUTS</span></span>

### <span data-ttu-id="7e294-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7e294-132">System.String</span></span>

## <span data-ttu-id="7e294-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="7e294-133">OUTPUTS</span></span>

### <span data-ttu-id="7e294-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="7e294-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="7e294-135">Notas</span><span class="sxs-lookup"><span data-stu-id="7e294-135">NOTES</span></span>

## <span data-ttu-id="7e294-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e294-136">RELATED LINKS</span></span>

[<span data-ttu-id="7e294-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7e294-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="7e294-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="7e294-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

