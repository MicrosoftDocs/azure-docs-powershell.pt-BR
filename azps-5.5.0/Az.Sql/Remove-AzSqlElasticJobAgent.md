---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110925"
---
# <span data-ttu-id="3f28a-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="3f28a-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="3f28a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f28a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f28a-103">Remove o agente de trabalho elástica</span><span class="sxs-lookup"><span data-stu-id="3f28a-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="3f28a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f28a-104">SYNTAX</span></span>

### <span data-ttu-id="3f28a-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3f28a-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f28a-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="3f28a-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f28a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3f28a-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f28a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f28a-108">DESCRIPTION</span></span>
<span data-ttu-id="3f28a-109">O cmdlet Remove-AzSqlElasticJobAgent remove um agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="3f28a-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="3f28a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f28a-110">EXAMPLES</span></span>

### <span data-ttu-id="3f28a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f28a-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="3f28a-112">Remove um agente de Trabalho Elástica</span><span class="sxs-lookup"><span data-stu-id="3f28a-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="3f28a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f28a-113">PARAMETERS</span></span>

### <span data-ttu-id="3f28a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f28a-114">-DefaultProfile</span></span>
<span data-ttu-id="3f28a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f28a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f28a-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3f28a-116">-Force</span></span>
<span data-ttu-id="3f28a-117">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="3f28a-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3f28a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f28a-118">-InputObject</span></span>
<span data-ttu-id="3f28a-119">O objeto do agente</span><span class="sxs-lookup"><span data-stu-id="3f28a-119">The agent object</span></span>

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

### <span data-ttu-id="3f28a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f28a-120">-Name</span></span>
<span data-ttu-id="3f28a-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="3f28a-121">The agent name</span></span>

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

### <span data-ttu-id="3f28a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f28a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f28a-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3f28a-123">The resource group name</span></span>

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

### <span data-ttu-id="3f28a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f28a-124">-ResourceId</span></span>
<span data-ttu-id="3f28a-125">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="3f28a-125">The agent resource id</span></span>

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

### <span data-ttu-id="3f28a-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3f28a-126">-ServerName</span></span>
<span data-ttu-id="3f28a-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="3f28a-127">The server name</span></span>

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

### <span data-ttu-id="3f28a-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3f28a-128">-Confirm</span></span>
<span data-ttu-id="3f28a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f28a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f28a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f28a-130">-WhatIf</span></span>
<span data-ttu-id="3f28a-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3f28a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f28a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f28a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f28a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f28a-133">CommonParameters</span></span>
<span data-ttu-id="3f28a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f28a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f28a-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f28a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f28a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f28a-136">INPUTS</span></span>

### <span data-ttu-id="3f28a-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3f28a-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3f28a-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f28a-138">OUTPUTS</span></span>

### <span data-ttu-id="3f28a-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="3f28a-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3f28a-140">Notas</span><span class="sxs-lookup"><span data-stu-id="3f28a-140">NOTES</span></span>

## <span data-ttu-id="3f28a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f28a-141">RELATED LINKS</span></span>
