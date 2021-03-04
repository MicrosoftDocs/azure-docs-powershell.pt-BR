---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: b27aee4c665dd2725bfd8643cb12ca005a5c4e1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901388"
---
# <span data-ttu-id="78e9c-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="78e9c-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="78e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="78e9c-103">Retorna informações sobre SQL Server bancos de dados vinculados por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="78e9c-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="78e9c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="78e9c-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78e9c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="78e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="78e9c-106">O cmdlet **Get-AzSqlSyncAgentLinkedDatabase** retorna informações sobre SQL Server bancos de dados vinculados por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="78e9c-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="78e9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="78e9c-108">Exemplo 1: obter os bancos de dados SQL Server vinculados para um agente de sincronização do Azure SQL sincronização.</span><span class="sxs-lookup"><span data-stu-id="78e9c-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="78e9c-109">O exemplo a seguir retorna os bancos SQL Server vinculados por um agente de sincronização do Azure SQL sincronização.</span><span class="sxs-lookup"><span data-stu-id="78e9c-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="78e9c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="78e9c-110">PARAMETERS</span></span>

### <span data-ttu-id="78e9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e9c-111">-DefaultProfile</span></span>
<span data-ttu-id="78e9c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="78e9c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78e9c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e9c-113">-ResourceGroupName</span></span>
<span data-ttu-id="78e9c-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78e9c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="78e9c-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78e9c-115">-ServerName</span></span>
<span data-ttu-id="78e9c-116">O nome do Azure SQL Server o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="78e9c-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="78e9c-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="78e9c-117">-SyncAgentName</span></span>
<span data-ttu-id="78e9c-118">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="78e9c-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e9c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e9c-119">CommonParameters</span></span>
<span data-ttu-id="78e9c-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e9c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e9c-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78e9c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e9c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78e9c-122">INPUTS</span></span>

### <span data-ttu-id="78e9c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="78e9c-123">System.String</span></span>

## <span data-ttu-id="78e9c-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="78e9c-124">OUTPUTS</span></span>

### <span data-ttu-id="78e9c-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="78e9c-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="78e9c-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="78e9c-126">NOTES</span></span>

## <span data-ttu-id="78e9c-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78e9c-127">RELATED LINKS</span></span>
