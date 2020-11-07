---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 08f89698b54585127e957d68082975f8e8e9744f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773839"
---
# <span data-ttu-id="453b8-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="453b8-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="453b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="453b8-102">SYNOPSIS</span></span>
<span data-ttu-id="453b8-103">Cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="453b8-103">Creates a new target group</span></span>

## <span data-ttu-id="453b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="453b8-104">SYNTAX</span></span>

### <span data-ttu-id="453b8-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="453b8-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="453b8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="453b8-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="453b8-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="453b8-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="453b8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="453b8-108">DESCRIPTION</span></span>
<span data-ttu-id="453b8-109">O cmdlet New-AzSqlElasticJobTargetGroup cria um novo grupo de destino</span><span class="sxs-lookup"><span data-stu-id="453b8-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="453b8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="453b8-110">EXAMPLES</span></span>

### <span data-ttu-id="453b8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="453b8-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="453b8-112">Cria um grupo de destino vazio</span><span class="sxs-lookup"><span data-stu-id="453b8-112">Creates an empty target group</span></span>

## <span data-ttu-id="453b8-113">OS</span><span class="sxs-lookup"><span data-stu-id="453b8-113">PARAMETERS</span></span>

### <span data-ttu-id="453b8-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="453b8-114">-AgentName</span></span>
<span data-ttu-id="453b8-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="453b8-115">The agent name</span></span>

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

### <span data-ttu-id="453b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453b8-116">-DefaultProfile</span></span>
<span data-ttu-id="453b8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="453b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="453b8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="453b8-118">-Name</span></span>
<span data-ttu-id="453b8-119">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="453b8-119">The target group name</span></span>

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

### <span data-ttu-id="453b8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="453b8-120">-ParentObject</span></span>
<span data-ttu-id="453b8-121">O objeto de entrada do agente</span><span class="sxs-lookup"><span data-stu-id="453b8-121">The agent input object</span></span>

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

### <span data-ttu-id="453b8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="453b8-122">-ParentResourceId</span></span>
<span data-ttu-id="453b8-123">A ID do recurso do agente</span><span class="sxs-lookup"><span data-stu-id="453b8-123">The agent resource id</span></span>

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

### <span data-ttu-id="453b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="453b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="453b8-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="453b8-125">The resource group name</span></span>

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

### <span data-ttu-id="453b8-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="453b8-126">-ServerName</span></span>
<span data-ttu-id="453b8-127">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="453b8-127">The server name</span></span>

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

### <span data-ttu-id="453b8-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="453b8-128">-Confirm</span></span>
<span data-ttu-id="453b8-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="453b8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453b8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453b8-130">-WhatIf</span></span>
<span data-ttu-id="453b8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="453b8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="453b8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="453b8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453b8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453b8-133">CommonParameters</span></span>
<span data-ttu-id="453b8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="453b8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453b8-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="453b8-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453b8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="453b8-136">INPUTS</span></span>

### <span data-ttu-id="453b8-137">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="453b8-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="453b8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="453b8-138">OUTPUTS</span></span>

### <span data-ttu-id="453b8-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="453b8-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="453b8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="453b8-140">NOTES</span></span>

## <span data-ttu-id="453b8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="453b8-141">RELATED LINKS</span></span>
