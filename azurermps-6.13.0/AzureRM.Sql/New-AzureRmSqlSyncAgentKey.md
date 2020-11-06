---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: cb4ca947d9f87cd6a0d3b4cdf476cf0176db2c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427129"
---
# <span data-ttu-id="3abe3-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="3abe3-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="3abe3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3abe3-102">SYNOPSIS</span></span>
<span data-ttu-id="3abe3-103">Cria uma chave do agente do SQL Sync do Azure.</span><span class="sxs-lookup"><span data-stu-id="3abe3-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3abe3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3abe3-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3abe3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3abe3-105">DESCRIPTION</span></span>
<span data-ttu-id="3abe3-106">O cmdlet **New-AzureRmSqlSyncAgentKey** cria uma chave do agente do SQL Sync do Azure.</span><span class="sxs-lookup"><span data-stu-id="3abe3-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="3abe3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3abe3-107">EXAMPLES</span></span>

### <span data-ttu-id="3abe3-108">Exemplo 1: criar uma chave do agente de sincronização para um agente de sincronização do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3abe3-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="3abe3-109">Esse comando cria uma chave do agente de sincronização para um agente do Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="3abe3-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="3abe3-110">OS</span><span class="sxs-lookup"><span data-stu-id="3abe3-110">PARAMETERS</span></span>

### <span data-ttu-id="3abe3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3abe3-111">-DefaultProfile</span></span>
<span data-ttu-id="3abe3-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3abe3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3abe3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3abe3-113">-ResourceGroupName</span></span>
<span data-ttu-id="3abe3-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3abe3-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="3abe3-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3abe3-115">-ServerName</span></span>
<span data-ttu-id="3abe3-116">O nome do Azure SQL Server no qual o agente de sincronização se encontra.</span><span class="sxs-lookup"><span data-stu-id="3abe3-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="3abe3-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="3abe3-117">-SyncAgentName</span></span>
<span data-ttu-id="3abe3-118">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="3abe3-118">The sync agent name.</span></span>

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

### <span data-ttu-id="3abe3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3abe3-119">-Confirm</span></span>
<span data-ttu-id="3abe3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3abe3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3abe3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3abe3-121">-WhatIf</span></span>
<span data-ttu-id="3abe3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3abe3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3abe3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3abe3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3abe3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3abe3-124">CommonParameters</span></span>
<span data-ttu-id="3abe3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3abe3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3abe3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3abe3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3abe3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3abe3-127">INPUTS</span></span>

### <span data-ttu-id="3abe3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3abe3-128">System.String</span></span>

## <span data-ttu-id="3abe3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3abe3-129">OUTPUTS</span></span>

### <span data-ttu-id="3abe3-130">Microsoft. Azure. Commands. Sql. datasync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="3abe3-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="3abe3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3abe3-131">NOTES</span></span>

## <span data-ttu-id="3abe3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3abe3-132">RELATED LINKS</span></span>
