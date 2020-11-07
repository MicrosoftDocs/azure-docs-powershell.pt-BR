---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: a20de2c2431e1ab6aea5da4d6dd61e6c745a3c56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942463"
---
# <span data-ttu-id="ecea5-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="ecea5-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="ecea5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecea5-102">SYNOPSIS</span></span>
<span data-ttu-id="ecea5-103">Remove o grupo de destino</span><span class="sxs-lookup"><span data-stu-id="ecea5-103">Removes the target group</span></span>

## <span data-ttu-id="ecea5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecea5-104">SYNTAX</span></span>

### <span data-ttu-id="ecea5-105">Defaultset (padrão)</span><span class="sxs-lookup"><span data-stu-id="ecea5-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecea5-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ecea5-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecea5-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="ecea5-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecea5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecea5-108">DESCRIPTION</span></span>
<span data-ttu-id="ecea5-109">O cmdlet Remove-AzSqlElasticJobTargetGroup remove um grupo de destino e seus destinos</span><span class="sxs-lookup"><span data-stu-id="ecea5-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="ecea5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecea5-110">EXAMPLES</span></span>

### <span data-ttu-id="ecea5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ecea5-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="ecea5-112">Remove um grupo de destino e os alvos</span><span class="sxs-lookup"><span data-stu-id="ecea5-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="ecea5-113">OS</span><span class="sxs-lookup"><span data-stu-id="ecea5-113">PARAMETERS</span></span>

### <span data-ttu-id="ecea5-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ecea5-114">-AgentName</span></span>
<span data-ttu-id="ecea5-115">O nome do agente</span><span class="sxs-lookup"><span data-stu-id="ecea5-115">The agent name</span></span>

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

### <span data-ttu-id="ecea5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecea5-116">-DefaultProfile</span></span>
<span data-ttu-id="ecea5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecea5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecea5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ecea5-118">-Force</span></span>
<span data-ttu-id="ecea5-119">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="ecea5-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ecea5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecea5-120">-InputObject</span></span>
<span data-ttu-id="ecea5-121">O objeto do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="ecea5-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecea5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecea5-122">-Name</span></span>
<span data-ttu-id="ecea5-123">O nome do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="ecea5-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecea5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecea5-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecea5-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ecea5-125">The resource group name</span></span>

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

### <span data-ttu-id="ecea5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecea5-126">-ResourceId</span></span>
<span data-ttu-id="ecea5-127">A ID do recurso do grupo de destino</span><span class="sxs-lookup"><span data-stu-id="ecea5-127">The target group resource id</span></span>

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

### <span data-ttu-id="ecea5-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ecea5-128">-ServerName</span></span>
<span data-ttu-id="ecea5-129">O nome do servidor</span><span class="sxs-lookup"><span data-stu-id="ecea5-129">The server name</span></span>

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

### <span data-ttu-id="ecea5-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecea5-130">-Confirm</span></span>
<span data-ttu-id="ecea5-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecea5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecea5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecea5-132">-WhatIf</span></span>
<span data-ttu-id="ecea5-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecea5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecea5-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecea5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecea5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecea5-135">CommonParameters</span></span>
<span data-ttu-id="ecea5-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecea5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecea5-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecea5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecea5-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecea5-138">INPUTS</span></span>

### <span data-ttu-id="ecea5-139">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="ecea5-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="ecea5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecea5-140">OUTPUTS</span></span>

### <span data-ttu-id="ecea5-141">Microsoft. Azure. Commands. Sql. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="ecea5-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="ecea5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecea5-142">NOTES</span></span>

## <span data-ttu-id="ecea5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecea5-143">RELATED LINKS</span></span>
