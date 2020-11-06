---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzMetricAlertRuleV2.md
ms.openlocfilehash: 698f05840df6578d8595e2ca8e31c9f0a11bc722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600791"
---
# <span data-ttu-id="cd697-101">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd697-101">Remove-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="cd697-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd697-102">SYNOPSIS</span></span>
<span data-ttu-id="cd697-103">Remove uma regra de alerta de métrica v2 (não clássico).</span><span class="sxs-lookup"><span data-stu-id="cd697-103">Removes a V2 (non-classic) metric alert rule.</span></span>

## <span data-ttu-id="cd697-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd697-104">SYNTAX</span></span>

### <span data-ttu-id="cd697-105">ByMetricRuleResourceName</span><span class="sxs-lookup"><span data-stu-id="cd697-105">ByMetricRuleResourceName</span></span>
```
Remove-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd697-106">ByMetricRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="cd697-106">ByMetricRuleResourceId</span></span>
```
Remove-AzMetricAlertRuleV2 -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd697-107">ByRuleObject</span><span class="sxs-lookup"><span data-stu-id="cd697-107">ByRuleObject</span></span>
```
Remove-AzMetricAlertRuleV2 -InputObject <PSMetricAlertRuleV2> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd697-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd697-108">DESCRIPTION</span></span>
<span data-ttu-id="cd697-109">O cmdlet **Remove-AzMetricAlertRuleV2** remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="cd697-109">The **Remove-AzMetricAlertRuleV2** cmdlet removes an alert rule.</span></span> <span data-ttu-id="cd697-110">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="cd697-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="cd697-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd697-111">EXAMPLES</span></span>

### <span data-ttu-id="cd697-112">Exemplo 1: remover uma regra de alerta por nome</span><span class="sxs-lookup"><span data-stu-id="cd697-112">Example 1: Remove an alert rule by name</span></span>

```powershell
PS C:\> Remove-AzMetricAlertRuleV2 -ResourceGroupName xxxxRG -Name PsSdk -PassThru
True
```

<span data-ttu-id="cd697-113">Esse comando Remove a regra de alerta chamada PsSdk</span><span class="sxs-lookup"><span data-stu-id="cd697-113">This command removes the alert rule named PsSdk</span></span>

### <span data-ttu-id="cd697-114">Exemplo 2: remover uma regra de alerta por ID</span><span class="sxs-lookup"><span data-stu-id="cd697-114">Example 2: Remove an alert rule by ID</span></span>

```powershell
PS C:\>Remove-AzMetricAlertRuleV2 -ResourceId /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule
```

<span data-ttu-id="cd697-115">Este comando Remove a regra de alerta com ID do recurso `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span><span class="sxs-lookup"><span data-stu-id="cd697-115">This command removes the alert rule with resource ID `/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/metricAlertRG/providers/microsoft.insights/metricAlerts/myAlertRule`</span></span>
### <span data-ttu-id="cd697-116">Exemplo 3: obter um alerta e removê-lo</span><span class="sxs-lookup"><span data-stu-id="cd697-116">Example 3: Get an alert and remove it</span></span>

```powershell
PS c:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest -Name sampleAlertRule |Remove-AzMetricAlertRuleV2
```

<span data-ttu-id="cd697-117">Este comando obtém um alerta e o Remove.</span><span class="sxs-lookup"><span data-stu-id="cd697-117">This command gets an alert and removes it.</span></span>

## <span data-ttu-id="cd697-118">OS</span><span class="sxs-lookup"><span data-stu-id="cd697-118">PARAMETERS</span></span>

### <span data-ttu-id="cd697-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd697-119">-AsJob</span></span>
<span data-ttu-id="cd697-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cd697-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd697-121">-Confirm</span></span>
<span data-ttu-id="cd697-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd697-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd697-123">-DefaultProfile</span></span>
<span data-ttu-id="cd697-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd697-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd697-125">-InputObject</span></span>
<span data-ttu-id="cd697-126">O objeto de regra métrica</span><span class="sxs-lookup"><span data-stu-id="cd697-126">The Metric rule object</span></span>

```yaml
Type: PSMetricAlertRuleV2
Parameter Sets: ByRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd697-127">-Name</span></span>
<span data-ttu-id="cd697-128">O nome da regra de alerta de métrica</span><span class="sxs-lookup"><span data-stu-id="cd697-128">The name of metric alert rule</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd697-129">-PassThru</span></span>
<span data-ttu-id="cd697-130">Retornar true após a exclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cd697-130">Return true upon successful deletion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd697-131">-ResourceGroupName</span></span>
<span data-ttu-id="cd697-132">O ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd697-132">The ResourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceName
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd697-133">-ResourceId</span></span>
<span data-ttu-id="cd697-134">O RuleResourceId</span><span class="sxs-lookup"><span data-stu-id="cd697-134">The RuleResourceId</span></span>

```yaml
Type: String
Parameter Sets: ByMetricRuleResourceId
Aliases: RuleResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd697-135">-WhatIf</span></span>
<span data-ttu-id="cd697-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd697-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd697-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd697-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd697-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd697-138">CommonParameters</span></span>
<span data-ttu-id="cd697-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd697-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cd697-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd697-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd697-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd697-141">INPUTS</span></span>

### <span data-ttu-id="cd697-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cd697-142">System.String</span></span>

### <span data-ttu-id="cd697-143">Microsoft. Azure. Commands. insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd697-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="cd697-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd697-144">OUTPUTS</span></span>

### <span data-ttu-id="cd697-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd697-145">System.Boolean</span></span>

## <span data-ttu-id="cd697-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd697-146">NOTES</span></span>

## <span data-ttu-id="cd697-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd697-147">RELATED LINKS</span></span>
