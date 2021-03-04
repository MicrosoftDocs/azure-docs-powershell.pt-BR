---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 022ef6979ddac4fa31c0a1dae42ae04c044498dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891604"
---
# <span data-ttu-id="fd918-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="fd918-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="fd918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd918-102">SYNOPSIS</span></span>
<span data-ttu-id="fd918-103">Obtém um ou mais grupos de destino de trabalho</span><span class="sxs-lookup"><span data-stu-id="fd918-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="fd918-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fd918-104">SYNTAX</span></span>

### <span data-ttu-id="fd918-105">DefaultSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fd918-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd918-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd918-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd918-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd918-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd918-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fd918-108">DESCRIPTION</span></span>
<span data-ttu-id="fd918-109">O Get-AzSqlElasticJobTargetGroup cmdlet obtém um grupo de destino e seus destinos</span><span class="sxs-lookup"><span data-stu-id="fd918-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="fd918-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd918-110">EXAMPLES</span></span>

### <span data-ttu-id="fd918-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd918-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="fd918-112">Obtém um grupo de destino e seus destinos</span><span class="sxs-lookup"><span data-stu-id="fd918-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="fd918-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fd918-113">PARAMETERS</span></span>

### <span data-ttu-id="fd918-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fd918-114">-AgentName</span></span>
<span data-ttu-id="fd918-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="fd918-115">The agent name</span></span>

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

### <span data-ttu-id="fd918-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd918-116">-DefaultProfile</span></span>
<span data-ttu-id="fd918-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd918-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd918-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fd918-118">-Name</span></span>
<span data-ttu-id="fd918-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="fd918-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd918-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fd918-120">-ParentObject</span></span>
<span data-ttu-id="fd918-121">O objeto agent</span><span class="sxs-lookup"><span data-stu-id="fd918-121">The agent object</span></span>

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

### <span data-ttu-id="fd918-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fd918-122">-ParentResourceId</span></span>
<span data-ttu-id="fd918-123">A ID de recurso do agente</span><span class="sxs-lookup"><span data-stu-id="fd918-123">The agent resource id</span></span>

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

### <span data-ttu-id="fd918-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd918-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd918-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fd918-125">The resource group name</span></span>

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

### <span data-ttu-id="fd918-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fd918-126">-ServerName</span></span>
<span data-ttu-id="fd918-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="fd918-127">The server name</span></span>

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

### <span data-ttu-id="fd918-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd918-128">CommonParameters</span></span>
<span data-ttu-id="fd918-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd918-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd918-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd918-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd918-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd918-131">INPUTS</span></span>

### <span data-ttu-id="fd918-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="fd918-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="fd918-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fd918-133">OUTPUTS</span></span>

### <span data-ttu-id="fd918-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="fd918-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="fd918-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="fd918-135">NOTES</span></span>

## <span data-ttu-id="fd918-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd918-136">RELATED LINKS</span></span>
