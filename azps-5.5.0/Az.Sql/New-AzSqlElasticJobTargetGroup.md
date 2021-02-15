---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112537"
---
# <span data-ttu-id="63e50-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="63e50-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="63e50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63e50-102">SYNOPSIS</span></span>
<span data-ttu-id="63e50-103">Cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="63e50-103">Creates a new target group</span></span>

## <span data-ttu-id="63e50-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63e50-104">SYNTAX</span></span>

### <span data-ttu-id="63e50-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63e50-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e50-106">Objectset</span><span class="sxs-lookup"><span data-stu-id="63e50-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e50-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="63e50-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e50-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="63e50-108">DESCRIPTION</span></span>
<span data-ttu-id="63e50-109">O New-AzSqlElasticJobTargetGroup cmdlet cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="63e50-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="63e50-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="63e50-110">EXAMPLES</span></span>

### <span data-ttu-id="63e50-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63e50-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="63e50-112">Cria um grupo de destino vazio</span><span class="sxs-lookup"><span data-stu-id="63e50-112">Creates an empty target group</span></span>

## <span data-ttu-id="63e50-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63e50-113">PARAMETERS</span></span>

### <span data-ttu-id="63e50-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="63e50-114">-AgentName</span></span>
<span data-ttu-id="63e50-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="63e50-115">The agent name</span></span>

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

### <span data-ttu-id="63e50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e50-116">-DefaultProfile</span></span>
<span data-ttu-id="63e50-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63e50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e50-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="63e50-118">-Name</span></span>
<span data-ttu-id="63e50-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="63e50-119">The target group name</span></span>

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

### <span data-ttu-id="63e50-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="63e50-120">-ParentObject</span></span>
<span data-ttu-id="63e50-121">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="63e50-121">The agent input object</span></span>

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

### <span data-ttu-id="63e50-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="63e50-122">-ParentResourceId</span></span>
<span data-ttu-id="63e50-123">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="63e50-123">The agent resource id</span></span>

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

### <span data-ttu-id="63e50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e50-124">-ResourceGroupName</span></span>
<span data-ttu-id="63e50-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="63e50-125">The resource group name</span></span>

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

### <span data-ttu-id="63e50-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="63e50-126">-ServerName</span></span>
<span data-ttu-id="63e50-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="63e50-127">The server name</span></span>

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

### <span data-ttu-id="63e50-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="63e50-128">-Confirm</span></span>
<span data-ttu-id="63e50-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e50-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e50-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e50-130">-WhatIf</span></span>
<span data-ttu-id="63e50-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="63e50-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63e50-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63e50-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e50-133">CommonParameters</span></span>
<span data-ttu-id="63e50-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e50-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63e50-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e50-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="63e50-136">INPUTS</span></span>

### <span data-ttu-id="63e50-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="63e50-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="63e50-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="63e50-138">OUTPUTS</span></span>

### <span data-ttu-id="63e50-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="63e50-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="63e50-140">Notas</span><span class="sxs-lookup"><span data-stu-id="63e50-140">NOTES</span></span>

## <span data-ttu-id="63e50-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63e50-141">RELATED LINKS</span></span>
