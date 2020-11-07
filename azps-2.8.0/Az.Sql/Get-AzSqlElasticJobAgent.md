---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 80835d33f75517bea6a91e65f110f441d20ab59c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773738"
---
# <span data-ttu-id="95790-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="95790-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="95790-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95790-102">SYNOPSIS</span></span>
<span data-ttu-id="95790-103">Obtém um agente de trabalho elástico do Azure SQL</span><span class="sxs-lookup"><span data-stu-id="95790-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="95790-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95790-104">SYNTAX</span></span>

### <span data-ttu-id="95790-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="95790-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95790-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="95790-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95790-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="95790-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95790-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95790-108">DESCRIPTION</span></span>
<span data-ttu-id="95790-109">O cmdlet Get-AzSqlElasticJobAgent Obtém um ou mais agentes de trabalho elásticos</span><span class="sxs-lookup"><span data-stu-id="95790-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="95790-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95790-110">EXAMPLES</span></span>

### <span data-ttu-id="95790-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95790-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="95790-112">Obtém um agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="95790-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="95790-113">OS</span><span class="sxs-lookup"><span data-stu-id="95790-113">PARAMETERS</span></span>

### <span data-ttu-id="95790-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95790-114">-DefaultProfile</span></span>
<span data-ttu-id="95790-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95790-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95790-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="95790-116">-Name</span></span>
<span data-ttu-id="95790-117">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="95790-117">The agent name</span></span>

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

### <span data-ttu-id="95790-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="95790-118">-ParentObject</span></span>
<span data-ttu-id="95790-119">O objeto de entrada do servidor</span><span class="sxs-lookup"><span data-stu-id="95790-119">The server input object</span></span>

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

### <span data-ttu-id="95790-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="95790-120">-ParentResourceId</span></span>
<span data-ttu-id="95790-121">A ID do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="95790-121">The server resource id</span></span>

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

### <span data-ttu-id="95790-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95790-122">-ResourceGroupName</span></span>
<span data-ttu-id="95790-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="95790-123">The resource group name</span></span>

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

### <span data-ttu-id="95790-124">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="95790-124">-ServerName</span></span>
<span data-ttu-id="95790-125">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="95790-125">The server name</span></span>

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

### <span data-ttu-id="95790-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95790-126">CommonParameters</span></span>
<span data-ttu-id="95790-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95790-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95790-128">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95790-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95790-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95790-129">INPUTS</span></span>

### <span data-ttu-id="95790-130">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="95790-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="95790-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95790-131">OUTPUTS</span></span>

### <span data-ttu-id="95790-132">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="95790-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="95790-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95790-133">NOTES</span></span>

## <span data-ttu-id="95790-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95790-134">RELATED LINKS</span></span>
