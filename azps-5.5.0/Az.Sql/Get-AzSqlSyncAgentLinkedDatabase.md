---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113951"
---
# <span data-ttu-id="7fa39-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="7fa39-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="7fa39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fa39-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa39-103">Retorna informações sobre bancos de dados do SQL Server vinculados por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7fa39-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="7fa39-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fa39-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fa39-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fa39-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa39-106">O cmdlet **Get-AzSqlSyncAgentLinkedDatabase** retorna informações sobre bancos de dados do SQL Server vinculados por um agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7fa39-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="7fa39-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7fa39-107">EXAMPLES</span></span>

### <span data-ttu-id="7fa39-108">Exemplo 1: Obter os bancos de dados vinculados do SQL Server para um agente de sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fa39-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="7fa39-109">O exemplo a seguir retorna os bancos de dados vinculados do SQL Server vinculados por um agente de sincronização SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7fa39-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="7fa39-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fa39-110">PARAMETERS</span></span>

### <span data-ttu-id="7fa39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa39-111">-DefaultProfile</span></span>
<span data-ttu-id="7fa39-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7fa39-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fa39-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa39-113">-ResourceGroupName</span></span>
<span data-ttu-id="7fa39-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fa39-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fa39-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7fa39-115">-ServerName</span></span>
<span data-ttu-id="7fa39-116">O nome do SQL Server do Azure em que o agente de sincronização está.</span><span class="sxs-lookup"><span data-stu-id="7fa39-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="7fa39-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="7fa39-117">-SyncAgentName</span></span>
<span data-ttu-id="7fa39-118">O nome do agente de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7fa39-118">The sync agent name.</span></span>

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

### <span data-ttu-id="7fa39-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa39-119">CommonParameters</span></span>
<span data-ttu-id="7fa39-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa39-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa39-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fa39-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa39-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="7fa39-122">INPUTS</span></span>

### <span data-ttu-id="7fa39-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7fa39-123">System.String</span></span>

## <span data-ttu-id="7fa39-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="7fa39-124">OUTPUTS</span></span>

### <span data-ttu-id="7fa39-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7fa39-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="7fa39-126">Notas</span><span class="sxs-lookup"><span data-stu-id="7fa39-126">NOTES</span></span>

## <span data-ttu-id="7fa39-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fa39-127">RELATED LINKS</span></span>
