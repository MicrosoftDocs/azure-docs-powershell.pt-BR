---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: 5adb6d79904b617b0ddbeaae28c9c7860c028fb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598820"
---
# <span data-ttu-id="33076-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="33076-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="33076-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33076-102">SYNOPSIS</span></span>
<span data-ttu-id="33076-103">Remove um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="33076-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="33076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33076-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33076-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33076-105">DESCRIPTION</span></span>
<span data-ttu-id="33076-106">O cmdlet **Remove-AzSqlSyncAgent** remove um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="33076-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="33076-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33076-107">EXAMPLES</span></span>

### <span data-ttu-id="33076-108">Exemplo 1: remover um agente de sincronização</span><span class="sxs-lookup"><span data-stu-id="33076-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="33076-109">Esse comando Remove o agente SQL Sync do Azure chamado syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="33076-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="33076-110">OS</span><span class="sxs-lookup"><span data-stu-id="33076-110">PARAMETERS</span></span>

### <span data-ttu-id="33076-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33076-111">-DefaultProfile</span></span>
<span data-ttu-id="33076-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="33076-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33076-113">-Force</span><span class="sxs-lookup"><span data-stu-id="33076-113">-Force</span></span>
<span data-ttu-id="33076-114">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="33076-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="33076-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="33076-115">-Name</span></span>
<span data-ttu-id="33076-116">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="33076-116">The sync agent name.</span></span>

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

### <span data-ttu-id="33076-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33076-117">-PassThru</span></span>
<span data-ttu-id="33076-118">Define se o retorne o agente de sincronização removido</span><span class="sxs-lookup"><span data-stu-id="33076-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="33076-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33076-119">-ResourceGroupName</span></span>
<span data-ttu-id="33076-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33076-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="33076-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="33076-121">-ServerName</span></span>
<span data-ttu-id="33076-122">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="33076-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="33076-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33076-123">-Confirm</span></span>
<span data-ttu-id="33076-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33076-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33076-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33076-125">-WhatIf</span></span>
<span data-ttu-id="33076-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33076-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33076-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33076-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33076-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33076-128">CommonParameters</span></span>
<span data-ttu-id="33076-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33076-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33076-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33076-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33076-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33076-131">INPUTS</span></span>

### <span data-ttu-id="33076-132">System. String</span><span class="sxs-lookup"><span data-stu-id="33076-132">System.String</span></span>

## <span data-ttu-id="33076-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33076-133">OUTPUTS</span></span>

### <span data-ttu-id="33076-134">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="33076-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="33076-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33076-135">NOTES</span></span>

## <span data-ttu-id="33076-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33076-136">RELATED LINKS</span></span>

[<span data-ttu-id="33076-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="33076-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="33076-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="33076-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

