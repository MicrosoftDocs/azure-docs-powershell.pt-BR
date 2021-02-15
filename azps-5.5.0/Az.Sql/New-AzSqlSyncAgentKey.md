---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118934"
---
# <span data-ttu-id="bbdd6-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="bbdd6-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="bbdd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbdd6-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdd6-103">Cria uma Chave do Agente de Sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="bbdd6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbdd6-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdd6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbdd6-105">DESCRIPTION</span></span>
<span data-ttu-id="bbdd6-106">O **cmdlet New-AzSqlSyncAgentKey** cria uma tecla do Azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="bbdd6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbdd6-107">EXAMPLES</span></span>

### <span data-ttu-id="bbdd6-108">Exemplo 1: Criar uma chave de agente de sincronização para um agente de sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="bbdd6-109">Esse comando cria uma chave do agente de sincronização para um Agente de Sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="bbdd6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbdd6-110">PARAMETERS</span></span>

### <span data-ttu-id="bbdd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdd6-111">-DefaultProfile</span></span>
<span data-ttu-id="bbdd6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bbdd6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbdd6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdd6-113">-ResourceGroupName</span></span>
<span data-ttu-id="bbdd6-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="bbdd6-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bbdd6-115">-ServerName</span></span>
<span data-ttu-id="bbdd6-116">O nome do SQL Server do Azure em que o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="bbdd6-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="bbdd6-117">-SyncAgentName</span></span>
<span data-ttu-id="bbdd6-118">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-118">The sync agent name.</span></span>

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

### <span data-ttu-id="bbdd6-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bbdd6-119">-Confirm</span></span>
<span data-ttu-id="bbdd6-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdd6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdd6-121">-WhatIf</span></span>
<span data-ttu-id="bbdd6-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdd6-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdd6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdd6-124">CommonParameters</span></span>
<span data-ttu-id="bbdd6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbdd6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdd6-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbdd6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdd6-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="bbdd6-127">INPUTS</span></span>

### <span data-ttu-id="bbdd6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bbdd6-128">System.String</span></span>

## <span data-ttu-id="bbdd6-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="bbdd6-129">OUTPUTS</span></span>

### <span data-ttu-id="bbdd6-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="bbdd6-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="bbdd6-131">Notas</span><span class="sxs-lookup"><span data-stu-id="bbdd6-131">NOTES</span></span>

## <span data-ttu-id="bbdd6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbdd6-132">RELATED LINKS</span></span>
