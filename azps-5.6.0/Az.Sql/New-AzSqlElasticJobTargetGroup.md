---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 9a80504f1b3aff814d50b5b4aba98b488d1e55b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887663"
---
# <span data-ttu-id="897b4-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="897b4-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="897b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="897b4-102">SYNOPSIS</span></span>
<span data-ttu-id="897b4-103">Cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="897b4-103">Creates a new target group</span></span>

## <span data-ttu-id="897b4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="897b4-104">SYNTAX</span></span>

### <span data-ttu-id="897b4-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="897b4-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897b4-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="897b4-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="897b4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="897b4-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="897b4-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="897b4-108">DESCRIPTION</span></span>
<span data-ttu-id="897b4-109">O New-AzSqlElasticJobTargetGroup cmdlet cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="897b4-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="897b4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="897b4-110">EXAMPLES</span></span>

### <span data-ttu-id="897b4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="897b4-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="897b4-112">Cria um grupo de destino vazio</span><span class="sxs-lookup"><span data-stu-id="897b4-112">Creates an empty target group</span></span>

## <span data-ttu-id="897b4-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="897b4-113">PARAMETERS</span></span>

### <span data-ttu-id="897b4-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="897b4-114">-AgentName</span></span>
<span data-ttu-id="897b4-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="897b4-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897b4-116">-DefaultProfile</span></span>
<span data-ttu-id="897b4-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="897b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="897b4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="897b4-118">-Name</span></span>
<span data-ttu-id="897b4-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="897b4-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="897b4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="897b4-120">-ParentObject</span></span>
<span data-ttu-id="897b4-121">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="897b4-121">The agent input object</span></span>

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

### <span data-ttu-id="897b4-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="897b4-122">-ParentResourceId</span></span>
<span data-ttu-id="897b4-123">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="897b4-123">The agent resource id</span></span>

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

### <span data-ttu-id="897b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="897b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="897b4-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="897b4-125">The resource group name</span></span>

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

### <span data-ttu-id="897b4-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="897b4-126">-ServerName</span></span>
<span data-ttu-id="897b4-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="897b4-127">The server name</span></span>

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

### <span data-ttu-id="897b4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="897b4-128">-Confirm</span></span>
<span data-ttu-id="897b4-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="897b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="897b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="897b4-130">-WhatIf</span></span>
<span data-ttu-id="897b4-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="897b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="897b4-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="897b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="897b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897b4-133">CommonParameters</span></span>
<span data-ttu-id="897b4-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="897b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897b4-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="897b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897b4-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="897b4-136">INPUTS</span></span>

### <span data-ttu-id="897b4-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="897b4-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="897b4-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="897b4-138">OUTPUTS</span></span>

### <span data-ttu-id="897b4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="897b4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="897b4-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="897b4-140">NOTES</span></span>

## <span data-ttu-id="897b4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="897b4-141">RELATED LINKS</span></span>
