---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 35942c51aa383dbc7dcbe071083eee575228372a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886135"
---
# <span data-ttu-id="8662c-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="8662c-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="8662c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8662c-102">SYNOPSIS</span></span>
<span data-ttu-id="8662c-103">Cria uma chave do agente de sincronização SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8662c-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="8662c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8662c-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8662c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8662c-105">DESCRIPTION</span></span>
<span data-ttu-id="8662c-106">O cmdlet **New-AzSqlSyncAgentKey** cria uma chave do Agente de Sincronização do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="8662c-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="8662c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8662c-107">EXAMPLES</span></span>

### <span data-ttu-id="8662c-108">Exemplo 1: Criar uma chave de agente de sincronização para um agente de sincronização do Azure SQL sincronização.</span><span class="sxs-lookup"><span data-stu-id="8662c-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="8662c-109">Este comando cria uma chave de agente de sincronização para um agente de sincronização do Azure SQL Sincronização.</span><span class="sxs-lookup"><span data-stu-id="8662c-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="8662c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8662c-110">PARAMETERS</span></span>

### <span data-ttu-id="8662c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8662c-111">-DefaultProfile</span></span>
<span data-ttu-id="8662c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8662c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8662c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8662c-113">-ResourceGroupName</span></span>
<span data-ttu-id="8662c-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8662c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="8662c-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8662c-115">-ServerName</span></span>
<span data-ttu-id="8662c-116">O nome do Azure SQL Server o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="8662c-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="8662c-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="8662c-117">-SyncAgentName</span></span>
<span data-ttu-id="8662c-118">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="8662c-118">The sync agent name.</span></span>

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

### <span data-ttu-id="8662c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8662c-119">-Confirm</span></span>
<span data-ttu-id="8662c-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8662c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8662c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8662c-121">-WhatIf</span></span>
<span data-ttu-id="8662c-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8662c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8662c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8662c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8662c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8662c-124">CommonParameters</span></span>
<span data-ttu-id="8662c-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8662c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8662c-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8662c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8662c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8662c-127">INPUTS</span></span>

### <span data-ttu-id="8662c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8662c-128">System.String</span></span>

## <span data-ttu-id="8662c-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8662c-129">OUTPUTS</span></span>

### <span data-ttu-id="8662c-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="8662c-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="8662c-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="8662c-131">NOTES</span></span>

## <span data-ttu-id="8662c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8662c-132">RELATED LINKS</span></span>
