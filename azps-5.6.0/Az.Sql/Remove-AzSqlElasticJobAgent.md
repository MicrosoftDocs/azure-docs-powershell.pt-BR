---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 3c6a92a205aef19b1e4cef4842de4cf0414c2397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886122"
---
# <span data-ttu-id="e500d-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="e500d-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="e500d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e500d-102">SYNOPSIS</span></span>
<span data-ttu-id="e500d-103">Remove o agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="e500d-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="e500d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e500d-104">SYNTAX</span></span>

### <span data-ttu-id="e500d-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e500d-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e500d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e500d-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e500d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e500d-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e500d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e500d-108">DESCRIPTION</span></span>
<span data-ttu-id="e500d-109">O cmdlet Remove-AzSqlElasticJobAgent remove um agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="e500d-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="e500d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e500d-110">EXAMPLES</span></span>

### <span data-ttu-id="e500d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e500d-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="e500d-112">Remove um agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="e500d-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="e500d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e500d-113">PARAMETERS</span></span>

### <span data-ttu-id="e500d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e500d-114">-DefaultProfile</span></span>
<span data-ttu-id="e500d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e500d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e500d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e500d-116">-Force</span></span>
<span data-ttu-id="e500d-117">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="e500d-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e500d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e500d-118">-InputObject</span></span>
<span data-ttu-id="e500d-119">O objeto agent</span><span class="sxs-lookup"><span data-stu-id="e500d-119">The agent object</span></span>

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

### <span data-ttu-id="e500d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e500d-120">-Name</span></span>
<span data-ttu-id="e500d-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="e500d-121">The agent name</span></span>

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

### <span data-ttu-id="e500d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e500d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e500d-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e500d-123">The resource group name</span></span>

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

### <span data-ttu-id="e500d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e500d-124">-ResourceId</span></span>
<span data-ttu-id="e500d-125">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="e500d-125">The agent resource id</span></span>

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

### <span data-ttu-id="e500d-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e500d-126">-ServerName</span></span>
<span data-ttu-id="e500d-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="e500d-127">The server name</span></span>

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

### <span data-ttu-id="e500d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e500d-128">-Confirm</span></span>
<span data-ttu-id="e500d-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e500d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e500d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e500d-130">-WhatIf</span></span>
<span data-ttu-id="e500d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e500d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e500d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e500d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e500d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e500d-133">CommonParameters</span></span>
<span data-ttu-id="e500d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e500d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e500d-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e500d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e500d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e500d-136">INPUTS</span></span>

### <span data-ttu-id="e500d-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e500d-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e500d-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e500d-138">OUTPUTS</span></span>

### <span data-ttu-id="e500d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e500d-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e500d-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="e500d-140">NOTES</span></span>

## <span data-ttu-id="e500d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e500d-141">RELATED LINKS</span></span>
