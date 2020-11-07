---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942988"
---
# <span data-ttu-id="e6c57-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e6c57-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="e6c57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6c57-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c57-103">Adiciona ou atualiza uma regra de alerta baseada em métrica.</span><span class="sxs-lookup"><span data-stu-id="e6c57-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="e6c57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6c57-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6c57-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6c57-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c57-106">O cmdlet **Add-AzMetricAlertRule** adiciona ou atualiza uma regra de alerta baseada em métrica.</span><span class="sxs-lookup"><span data-stu-id="e6c57-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="e6c57-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="e6c57-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="e6c57-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="e6c57-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e6c57-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6c57-109">EXAMPLES</span></span>

### <span data-ttu-id="e6c57-110">Exemplo 1: adicionar uma regra de alerta de métrica a um site</span><span class="sxs-lookup"><span data-stu-id="e6c57-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="e6c57-111">Esse comando cria uma regra de alerta métrica para um site.</span><span class="sxs-lookup"><span data-stu-id="e6c57-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="e6c57-112">Exemplo 2: desabilitar uma regra</span><span class="sxs-lookup"><span data-stu-id="e6c57-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="e6c57-113">Esse comando desabilita uma regra.</span><span class="sxs-lookup"><span data-stu-id="e6c57-113">This command disables a rule.</span></span>
<span data-ttu-id="e6c57-114">Se a regra não existir, será criada para ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e6c57-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="e6c57-115">Se a regra existir, basta desfazê-la.</span><span class="sxs-lookup"><span data-stu-id="e6c57-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="e6c57-116">Exemplo 3: adicionar uma regra com ações</span><span class="sxs-lookup"><span data-stu-id="e6c57-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e6c57-117">Esse comando cria uma regra de alerta métrica para um site.</span><span class="sxs-lookup"><span data-stu-id="e6c57-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="e6c57-118">OS</span><span class="sxs-lookup"><span data-stu-id="e6c57-118">PARAMETERS</span></span>

### <span data-ttu-id="e6c57-119">-Ação</span><span class="sxs-lookup"><span data-stu-id="e6c57-119">-Action</span></span>
<span data-ttu-id="e6c57-120">Especifica uma lista de ações separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="e6c57-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c57-121">-DefaultProfile</span></span>
<span data-ttu-id="e6c57-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e6c57-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6c57-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e6c57-123">-Description</span></span>
<span data-ttu-id="e6c57-124">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="e6c57-124">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e6c57-125">-DisableRule</span></span>
<span data-ttu-id="e6c57-126">Desabilita a regra.</span><span class="sxs-lookup"><span data-stu-id="e6c57-126">Disables the rule.</span></span>
<span data-ttu-id="e6c57-127">Se você não especificar esse parâmetro, a regra estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="e6c57-127">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-128">-Local</span><span class="sxs-lookup"><span data-stu-id="e6c57-128">-Location</span></span>
<span data-ttu-id="e6c57-129">Especifica o local onde a regra é definida.</span><span class="sxs-lookup"><span data-stu-id="e6c57-129">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="e6c57-130">-MetricName</span></span>
<span data-ttu-id="e6c57-131">Especifica o nome da métrica que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="e6c57-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="e6c57-132">Especifique esse parâmetro somente para regras com base em métricas.</span><span class="sxs-lookup"><span data-stu-id="e6c57-132">Specify this parameter only for metric-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6c57-133">-Name</span></span>
<span data-ttu-id="e6c57-134">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="e6c57-134">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-135">-Operador</span><span class="sxs-lookup"><span data-stu-id="e6c57-135">-Operator</span></span>
<span data-ttu-id="e6c57-136">Especifica o operador relacional para a condição da regra.</span><span class="sxs-lookup"><span data-stu-id="e6c57-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="e6c57-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e6c57-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6c57-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="e6c57-138">GreaterThan</span></span>
- <span data-ttu-id="e6c57-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e6c57-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="e6c57-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="e6c57-140">LessThan</span></span>
- <span data-ttu-id="e6c57-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e6c57-141">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c57-142">-ResourceGroupName</span></span>
<span data-ttu-id="e6c57-143">Especifica o nome do grupo de recursos para a regra.</span><span class="sxs-lookup"><span data-stu-id="e6c57-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e6c57-144">-TargetResourceId</span></span>
<span data-ttu-id="e6c57-145">Especifica a ID do recurso que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="e6c57-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="e6c57-146">Observação: esta propriedade não pode ser atualizada para uma regra de alerta existente.</span><span class="sxs-lookup"><span data-stu-id="e6c57-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="e6c57-147">-Threshold</span></span>
<span data-ttu-id="e6c57-148">Especifica o limite da regra.</span><span class="sxs-lookup"><span data-stu-id="e6c57-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="e6c57-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="e6c57-150">Especifica o operador de agregação a ser aplicado à janela de tempo quando a regra está sendo avaliada.</span><span class="sxs-lookup"><span data-stu-id="e6c57-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-151">-WindowS</span><span class="sxs-lookup"><span data-stu-id="e6c57-151">-WindowSize</span></span>
<span data-ttu-id="e6c57-152">Especifica o tamanho da janela de tempo para a regra calcular seus dados.</span><span class="sxs-lookup"><span data-stu-id="e6c57-152">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c57-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6c57-153">-Confirm</span></span>
<span data-ttu-id="e6c57-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6c57-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6c57-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6c57-155">-WhatIf</span></span>
<span data-ttu-id="e6c57-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6c57-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6c57-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6c57-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6c57-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c57-158">CommonParameters</span></span>
<span data-ttu-id="e6c57-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c57-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c57-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6c57-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c57-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6c57-161">INPUTS</span></span>

### <span data-ttu-id="e6c57-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="e6c57-162">System.TimeSpan</span></span>

### <span data-ttu-id="e6c57-163">Microsoft. Azure. Management. monitor. Management. Models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="e6c57-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="e6c57-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="e6c57-164">System.Double</span></span>

### <span data-ttu-id="e6c57-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e6c57-165">System.String</span></span>

### <span data-ttu-id="e6c57-166">System. Nullable ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. TimeAggregationOperator, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e6c57-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e6c57-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6c57-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e6c57-168">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. RuleAction, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e6c57-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6c57-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6c57-169">OUTPUTS</span></span>

### <span data-ttu-id="e6c57-170">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e6c57-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e6c57-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6c57-171">NOTES</span></span>

## <span data-ttu-id="e6c57-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6c57-172">RELATED LINKS</span></span>

[<span data-ttu-id="e6c57-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e6c57-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e6c57-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e6c57-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="e6c57-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e6c57-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="e6c57-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e6c57-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="e6c57-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e6c57-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="e6c57-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e6c57-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="e6c57-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="e6c57-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


