---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262934"
---
# <span data-ttu-id="64a90-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="64a90-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="64a90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64a90-102">SYNOPSIS</span></span>
<span data-ttu-id="64a90-103">Cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="64a90-103">Creates a new target group</span></span>

## <span data-ttu-id="64a90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64a90-104">SYNTAX</span></span>

### <span data-ttu-id="64a90-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="64a90-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a90-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="64a90-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a90-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="64a90-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a90-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64a90-108">DESCRIPTION</span></span>
<span data-ttu-id="64a90-109">O cmdlet New-AzSqlElasticJobTargetGroup cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="64a90-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="64a90-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64a90-110">EXAMPLES</span></span>

### <span data-ttu-id="64a90-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64a90-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="64a90-112">Cria um grupo de destino vazio</span><span class="sxs-lookup"><span data-stu-id="64a90-112">Creates an empty target group</span></span>

## <span data-ttu-id="64a90-113">OS</span><span class="sxs-lookup"><span data-stu-id="64a90-113">PARAMETERS</span></span>

### <span data-ttu-id="64a90-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="64a90-114">-AgentName</span></span>
<span data-ttu-id="64a90-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="64a90-115">The agent name</span></span>

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

### <span data-ttu-id="64a90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a90-116">-DefaultProfile</span></span>
<span data-ttu-id="64a90-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64a90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a90-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="64a90-118">-Name</span></span>
<span data-ttu-id="64a90-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="64a90-119">The target group name</span></span>

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

### <span data-ttu-id="64a90-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="64a90-120">-ParentObject</span></span>
<span data-ttu-id="64a90-121">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="64a90-121">The agent input object</span></span>

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

### <span data-ttu-id="64a90-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="64a90-122">-ParentResourceId</span></span>
<span data-ttu-id="64a90-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="64a90-123">The agent resource id</span></span>

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

### <span data-ttu-id="64a90-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a90-124">-ResourceGroupName</span></span>
<span data-ttu-id="64a90-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="64a90-125">The resource group name</span></span>

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

### <span data-ttu-id="64a90-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="64a90-126">-ServerName</span></span>
<span data-ttu-id="64a90-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="64a90-127">The server name</span></span>

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

### <span data-ttu-id="64a90-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64a90-128">-Confirm</span></span>
<span data-ttu-id="64a90-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a90-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a90-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a90-130">-WhatIf</span></span>
<span data-ttu-id="64a90-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64a90-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a90-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64a90-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a90-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a90-133">CommonParameters</span></span>
<span data-ttu-id="64a90-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a90-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a90-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a90-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a90-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64a90-136">INPUTS</span></span>

### <span data-ttu-id="64a90-137">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="64a90-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="64a90-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64a90-138">OUTPUTS</span></span>

### <span data-ttu-id="64a90-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="64a90-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="64a90-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64a90-140">NOTES</span></span>

## <span data-ttu-id="64a90-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64a90-141">RELATED LINKS</span></span>
