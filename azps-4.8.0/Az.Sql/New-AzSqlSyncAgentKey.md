---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947556"
---
# <span data-ttu-id="2591b-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2591b-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="2591b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2591b-102">SYNOPSIS</span></span>
<span data-ttu-id="2591b-103">Cria uma chave do agente do SQL Sync do Azure.</span><span class="sxs-lookup"><span data-stu-id="2591b-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="2591b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2591b-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2591b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2591b-105">DESCRIPTION</span></span>
<span data-ttu-id="2591b-106">O cmdlet **New-AzSqlSyncAgentKey** cria uma chave do agente do SQL Sync do Azure.</span><span class="sxs-lookup"><span data-stu-id="2591b-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2591b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2591b-107">EXAMPLES</span></span>

### <span data-ttu-id="2591b-108">Exemplo 1: criar uma chave do agente de sincronização para um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="2591b-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2591b-109">Esse comando cria uma chave do agente de sincronização para um agente do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="2591b-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2591b-110">OS</span><span class="sxs-lookup"><span data-stu-id="2591b-110">PARAMETERS</span></span>

### <span data-ttu-id="2591b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2591b-111">-DefaultProfile</span></span>
<span data-ttu-id="2591b-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2591b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2591b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2591b-113">-ResourceGroupName</span></span>
<span data-ttu-id="2591b-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2591b-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2591b-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2591b-115">-ServerName</span></span>
<span data-ttu-id="2591b-116">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="2591b-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2591b-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2591b-117">-SyncAgentName</span></span>
<span data-ttu-id="2591b-118">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="2591b-118">The sync agent name.</span></span>

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

### <span data-ttu-id="2591b-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2591b-119">-Confirm</span></span>
<span data-ttu-id="2591b-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2591b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2591b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2591b-121">-WhatIf</span></span>
<span data-ttu-id="2591b-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2591b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2591b-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2591b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2591b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2591b-124">CommonParameters</span></span>
<span data-ttu-id="2591b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2591b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2591b-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2591b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2591b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2591b-127">INPUTS</span></span>

### <span data-ttu-id="2591b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2591b-128">System.String</span></span>

## <span data-ttu-id="2591b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2591b-129">OUTPUTS</span></span>

### <span data-ttu-id="2591b-130">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="2591b-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2591b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2591b-131">NOTES</span></span>

## <span data-ttu-id="2591b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2591b-132">RELATED LINKS</span></span>
