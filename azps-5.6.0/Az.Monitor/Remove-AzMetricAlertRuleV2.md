---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: c8085f4f760ff3f2c4c1fa7310eef2c2f2bb33bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885426"
---
# <span data-ttu-id="47b3a-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="47b3a-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="47b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="47b3a-103">Remove uma regra de alerta métrica V2 (não clássica).</span><span class="sxs-lookup"><span data-stu-id="47b3a-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="47b3a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47b3a-104">SYNTAX</span></span>

### <span data-ttu-id="47b3a-105">ByMetricRuleResourceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="47b3a-105">ByMetricRuleResourceName (Default)</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b3a-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="47b3a-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47b3a-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="47b3a-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b3a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47b3a-108">DESCRIPTION</span></span>
<span data-ttu-id="47b3a-109">O cmdlet **Remove-AzMetricAlertRuleV2** remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="47b3a-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="47b3a-110">Este cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="47b3a-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="47b3a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47b3a-111">EXAMPLES</span></span>

### <span data-ttu-id="47b3a-112">Exemplo 1: Remover uma regra de alerta pelo nome</span><span class="sxs-lookup"><span data-stu-id="47b3a-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="47b3a-113">Este comando remove a regra de alerta chamada PsSdk</span><span class="sxs-lookup"><span data-stu-id="47b3a-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="47b3a-114">Exemplo 2: Remover uma regra de alerta por ID</span><span class="sxs-lookup"><span data-stu-id="47b3a-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="47b3a-115">Este comando remove a regra de alerta com a ID do recurso `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="47b3a-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>

### <span data-ttu-id="47b3a-116">Exemplo 3: Obter um alerta e removê-lo</span><span class="sxs-lookup"><span data-stu-id="47b3a-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="47b3a-117">Esse comando recebe um alerta e o remove.</span><span class="sxs-lookup"><span data-stu-id="47b3a-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="47b3a-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47b3a-118">PARAMETERS</span></span>

### <span data-ttu-id="47b3a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47b3a-119">-AsJob</span></span>
<span data-ttu-id="47b3a-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="47b3a-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b3a-121">-DefaultProfile</span></span>
<span data-ttu-id="47b3a-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47b3a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b3a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47b3a-123">-InputObject</span></span>
<span data-ttu-id="47b3a-124">O objeto de regra Metric</span><span class="sxs-lookup"><span data-stu-id="47b3a-124">The Metric rule object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="47b3a-125">-Name</span></span>
<span data-ttu-id="47b3a-126">O nome da regra de alerta métrica</span><span class="sxs-lookup"><span data-stu-id="47b3a-126">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47b3a-127">-PassThru</span></span>
<span data-ttu-id="47b3a-128">Retornar true após a exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="47b3a-128">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b3a-129">-ResourceGroupName</span></span>
<span data-ttu-id="47b3a-130">The ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b3a-130">The ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47b3a-131">-ResourceId</span></span>
<span data-ttu-id="47b3a-132">The RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="47b3a-132">The RuleResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b3a-133">-Confirm</span></span>
<span data-ttu-id="47b3a-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b3a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b3a-135">-WhatIf</span></span>
<span data-ttu-id="47b3a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47b3a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b3a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47b3a-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47b3a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b3a-138">CommonParameters</span></span>
<span data-ttu-id="47b3a-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b3a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b3a-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47b3a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b3a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47b3a-141">INPUTS</span></span>

### <span data-ttu-id="47b3a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="47b3a-142">System.String</span></span>

### <span data-ttu-id="47b3a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="47b3a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="47b3a-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47b3a-144">OUTPUTS</span></span>

### <span data-ttu-id="47b3a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47b3a-145">System.Boolean</span></span>

## <span data-ttu-id="47b3a-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="47b3a-146">NOTES</span></span>

## <span data-ttu-id="47b3a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47b3a-147">RELATED LINKS</span></span>
