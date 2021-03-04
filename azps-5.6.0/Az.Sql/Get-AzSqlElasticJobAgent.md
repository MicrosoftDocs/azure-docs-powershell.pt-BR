---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 6ff5bdb6a3de7b1704ee41de0b6ff0b0f736ec5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901400"
---
# <span data-ttu-id="ed13e-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="ed13e-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="ed13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed13e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed13e-103">Obtém um agente de trabalho SQL Elastic do Azure</span><span class="sxs-lookup"><span data-stu-id="ed13e-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="ed13e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed13e-104">SYNTAX</span></span>

### <span data-ttu-id="ed13e-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed13e-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed13e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed13e-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed13e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed13e-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed13e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed13e-108">DESCRIPTION</span></span>
<span data-ttu-id="ed13e-109">O cmdlet Get-AzSqlElasticJobAgent obtém um ou mais agentes de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="ed13e-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="ed13e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed13e-110">EXAMPLES</span></span>

### <span data-ttu-id="ed13e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed13e-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="ed13e-112">Obtém um agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="ed13e-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="ed13e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed13e-113">PARAMETERS</span></span>

### <span data-ttu-id="ed13e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed13e-114">-DefaultProfile</span></span>
<span data-ttu-id="ed13e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed13e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed13e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ed13e-116">-Name</span></span>
<span data-ttu-id="ed13e-117">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="ed13e-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed13e-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ed13e-118">-ParentObject</span></span>
<span data-ttu-id="ed13e-119">O objeto de entrada do servidor</span><span class="sxs-lookup"><span data-stu-id="ed13e-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed13e-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ed13e-120">-ParentResourceId</span></span>
<span data-ttu-id="ed13e-121">A id de recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="ed13e-121">The server resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed13e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed13e-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed13e-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed13e-123">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed13e-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed13e-124">-ServerName</span></span>
<span data-ttu-id="ed13e-125">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="ed13e-125">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed13e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed13e-126">CommonParameters</span></span>
<span data-ttu-id="ed13e-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed13e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed13e-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed13e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed13e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed13e-129">INPUTS</span></span>

### <span data-ttu-id="ed13e-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ed13e-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ed13e-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed13e-131">OUTPUTS</span></span>

### <span data-ttu-id="ed13e-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="ed13e-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="ed13e-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed13e-133">NOTES</span></span>

## <span data-ttu-id="ed13e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed13e-134">RELATED LINKS</span></span>
