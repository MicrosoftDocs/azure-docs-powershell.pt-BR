---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: c65c7a74d4b2edfcddf8b4e08ee3e538c32d31df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889715"
---
# <span data-ttu-id="f4ae1-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="f4ae1-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="f4ae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ae1-103">Atualiza um agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="f4ae1-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="f4ae1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f4ae1-104">SYNTAX</span></span>

### <span data-ttu-id="f4ae1-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4ae1-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ae1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4ae1-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ae1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4ae1-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ae1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f4ae1-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ae1-109">O cmdlet Set-AzSqlElasticJobAgent atualiza um agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="f4ae1-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="f4ae1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4ae1-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ae1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f4ae1-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="f4ae1-112">Atualiza um agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="f4ae1-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="f4ae1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f4ae1-113">PARAMETERS</span></span>

### <span data-ttu-id="f4ae1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ae1-114">-DefaultProfile</span></span>
<span data-ttu-id="f4ae1-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ae1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ae1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4ae1-116">-InputObject</span></span>
<span data-ttu-id="f4ae1-117">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="f4ae1-117">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ae1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f4ae1-118">-Name</span></span>
<span data-ttu-id="f4ae1-119">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="f4ae1-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ae1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ae1-120">-ResourceGroupName</span></span>
<span data-ttu-id="f4ae1-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f4ae1-121">The resource group name</span></span>

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

### <span data-ttu-id="f4ae1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ae1-122">-ResourceId</span></span>
<span data-ttu-id="f4ae1-123">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="f4ae1-123">The agent resource id</span></span>

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

### <span data-ttu-id="f4ae1-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4ae1-124">-ServerName</span></span>
<span data-ttu-id="f4ae1-125">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="f4ae1-125">The server name</span></span>

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

### <span data-ttu-id="f4ae1-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4ae1-126">-Tag</span></span>
<span data-ttu-id="f4ae1-127">As marcas a associar ao Agente de Banco de Dados do Azure SQL Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="f4ae1-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ae1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4ae1-128">-Confirm</span></span>
<span data-ttu-id="f4ae1-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ae1-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ae1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ae1-130">-WhatIf</span></span>
<span data-ttu-id="f4ae1-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4ae1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ae1-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4ae1-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ae1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ae1-133">CommonParameters</span></span>
<span data-ttu-id="f4ae1-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ae1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ae1-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4ae1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ae1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4ae1-136">INPUTS</span></span>

### <span data-ttu-id="f4ae1-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="f4ae1-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="f4ae1-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f4ae1-138">OUTPUTS</span></span>

### <span data-ttu-id="f4ae1-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="f4ae1-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="f4ae1-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="f4ae1-140">NOTES</span></span>

## <span data-ttu-id="f4ae1-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4ae1-141">RELATED LINKS</span></span>
