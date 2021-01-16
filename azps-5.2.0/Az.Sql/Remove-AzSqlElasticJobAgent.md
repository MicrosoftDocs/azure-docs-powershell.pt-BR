---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261648"
---
# <span data-ttu-id="16cbc-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="16cbc-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="16cbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="16cbc-103">Remove o agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="16cbc-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="16cbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16cbc-104">SYNTAX</span></span>

### <span data-ttu-id="16cbc-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="16cbc-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16cbc-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="16cbc-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16cbc-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="16cbc-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16cbc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="16cbc-109">O cmdlet Remove-AzSqlElasticJobAgent remove um agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="16cbc-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="16cbc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="16cbc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="16cbc-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="16cbc-112">Remove um agente de trabalho elástico</span><span class="sxs-lookup"><span data-stu-id="16cbc-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="16cbc-113">OS</span><span class="sxs-lookup"><span data-stu-id="16cbc-113">PARAMETERS</span></span>

### <span data-ttu-id="16cbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16cbc-114">-DefaultProfile</span></span>
<span data-ttu-id="16cbc-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16cbc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16cbc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="16cbc-116">-Force</span></span>
<span data-ttu-id="16cbc-117">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="16cbc-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="16cbc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16cbc-118">-InputObject</span></span>
<span data-ttu-id="16cbc-119">O objeto agente</span><span class="sxs-lookup"><span data-stu-id="16cbc-119">The agent object</span></span>

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

### <span data-ttu-id="16cbc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="16cbc-120">-Name</span></span>
<span data-ttu-id="16cbc-121">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="16cbc-121">The agent name</span></span>

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

### <span data-ttu-id="16cbc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16cbc-122">-ResourceGroupName</span></span>
<span data-ttu-id="16cbc-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="16cbc-123">The resource group name</span></span>

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

### <span data-ttu-id="16cbc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16cbc-124">-ResourceId</span></span>
<span data-ttu-id="16cbc-125">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="16cbc-125">The agent resource id</span></span>

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

### <span data-ttu-id="16cbc-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="16cbc-126">-ServerName</span></span>
<span data-ttu-id="16cbc-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="16cbc-127">The server name</span></span>

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

### <span data-ttu-id="16cbc-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16cbc-128">-Confirm</span></span>
<span data-ttu-id="16cbc-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16cbc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16cbc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16cbc-130">-WhatIf</span></span>
<span data-ttu-id="16cbc-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16cbc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16cbc-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16cbc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16cbc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16cbc-133">CommonParameters</span></span>
<span data-ttu-id="16cbc-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16cbc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16cbc-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16cbc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16cbc-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16cbc-136">INPUTS</span></span>

### <span data-ttu-id="16cbc-137">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="16cbc-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="16cbc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16cbc-138">OUTPUTS</span></span>

### <span data-ttu-id="16cbc-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="16cbc-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="16cbc-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16cbc-140">NOTES</span></span>

## <span data-ttu-id="16cbc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16cbc-141">RELATED LINKS</span></span>
