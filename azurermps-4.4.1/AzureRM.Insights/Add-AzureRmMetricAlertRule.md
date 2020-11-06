---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610773"
---
# <span data-ttu-id="31fe4-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="31fe4-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="31fe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="31fe4-103">Adiciona ou atualiza uma regra de alerta baseada em métrica.</span><span class="sxs-lookup"><span data-stu-id="31fe4-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31fe4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31fe4-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31fe4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="31fe4-106">O cmdlet **Add-AzureRmMetricAlertRule** adiciona ou atualiza uma regra de alerta baseada em métrica.</span><span class="sxs-lookup"><span data-stu-id="31fe4-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="31fe4-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="31fe4-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="31fe4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31fe4-108">EXAMPLES</span></span>

### <span data-ttu-id="31fe4-109">Exemplo 1: adicionar uma regra de alerta de métrica a um site</span><span class="sxs-lookup"><span data-stu-id="31fe4-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="31fe4-110">Esse comando cria uma regra de alerta métrica para um site.</span><span class="sxs-lookup"><span data-stu-id="31fe4-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="31fe4-111">Exemplo 2: desabilitar uma regra</span><span class="sxs-lookup"><span data-stu-id="31fe4-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="31fe4-112">Esse comando desabilita uma regra.</span><span class="sxs-lookup"><span data-stu-id="31fe4-112">This command disables a rule.</span></span>
<span data-ttu-id="31fe4-113">Se a regra não existir, será criada para ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="31fe4-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="31fe4-114">Se a regra existir, basta desfazê-la.</span><span class="sxs-lookup"><span data-stu-id="31fe4-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="31fe4-115">Exemplo 3: adicionar uma regra com ações</span><span class="sxs-lookup"><span data-stu-id="31fe4-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="31fe4-116">Esse comando cria uma regra de alerta métrica para um site.</span><span class="sxs-lookup"><span data-stu-id="31fe4-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="31fe4-117">OS</span><span class="sxs-lookup"><span data-stu-id="31fe4-117">PARAMETERS</span></span>

### <span data-ttu-id="31fe4-118">-Ações</span><span class="sxs-lookup"><span data-stu-id="31fe4-118">-Actions</span></span>
<span data-ttu-id="31fe4-119">Especifica uma lista de ações separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="31fe4-119">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="31fe4-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="31fe4-120">-Description</span></span>
<span data-ttu-id="31fe4-121">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="31fe4-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="31fe4-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="31fe4-122">-DisableRule</span></span>
<span data-ttu-id="31fe4-123">Desabilita a regra.</span><span class="sxs-lookup"><span data-stu-id="31fe4-123">Disables the rule.</span></span>
<span data-ttu-id="31fe4-124">Se você não especificar esse parâmetro, a regra estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="31fe4-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="31fe4-125">-Local</span><span class="sxs-lookup"><span data-stu-id="31fe4-125">-Location</span></span>
<span data-ttu-id="31fe4-126">Especifica o local onde a regra é definida.</span><span class="sxs-lookup"><span data-stu-id="31fe4-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="31fe4-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="31fe4-127">-MetricName</span></span>
<span data-ttu-id="31fe4-128">Especifica o nome da métrica que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="31fe4-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="31fe4-129">Especifique esse parâmetro somente para regras com base em métricas.</span><span class="sxs-lookup"><span data-stu-id="31fe4-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="31fe4-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="31fe4-130">-Name</span></span>
<span data-ttu-id="31fe4-131">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="31fe4-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="31fe4-132">-Operador</span><span class="sxs-lookup"><span data-stu-id="31fe4-132">-Operator</span></span>
<span data-ttu-id="31fe4-133">Especifica o operador relacional para a condição da regra.</span><span class="sxs-lookup"><span data-stu-id="31fe4-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="31fe4-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="31fe4-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31fe4-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="31fe4-135">GreaterThan</span></span>
- <span data-ttu-id="31fe4-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="31fe4-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="31fe4-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="31fe4-137">LessThan</span></span>
- <span data-ttu-id="31fe4-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="31fe4-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="31fe4-139">-Resource</span><span class="sxs-lookup"><span data-stu-id="31fe4-139">-ResourceGroup</span></span>
<span data-ttu-id="31fe4-140">Especifica o nome do grupo de recursos para a regra.</span><span class="sxs-lookup"><span data-stu-id="31fe4-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="31fe4-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="31fe4-141">-TargetResourceId</span></span>
<span data-ttu-id="31fe4-142">Especifica a ID do recurso que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="31fe4-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="31fe4-143">Observação: esta propriedade não pode ser atualizada para uma regra de alerta existente.</span><span class="sxs-lookup"><span data-stu-id="31fe4-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="31fe4-144">-Threshold</span><span class="sxs-lookup"><span data-stu-id="31fe4-144">-Threshold</span></span>
<span data-ttu-id="31fe4-145">Especifica o limite da regra.</span><span class="sxs-lookup"><span data-stu-id="31fe4-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="31fe4-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="31fe4-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="31fe4-147">Especifica o operador de agregação a ser aplicado à janela de tempo quando a regra está sendo avaliada.</span><span class="sxs-lookup"><span data-stu-id="31fe4-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="31fe4-148">-WindowS</span><span class="sxs-lookup"><span data-stu-id="31fe4-148">-WindowSize</span></span>
<span data-ttu-id="31fe4-149">Especifica o tamanho da janela de tempo para a regra calcular seus dados.</span><span class="sxs-lookup"><span data-stu-id="31fe4-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="31fe4-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31fe4-150">-DefaultProfile</span></span>
<span data-ttu-id="31fe4-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31fe4-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31fe4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31fe4-152">CommonParameters</span></span>
<span data-ttu-id="31fe4-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31fe4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31fe4-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31fe4-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31fe4-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31fe4-155">INPUTS</span></span>

## <span data-ttu-id="31fe4-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31fe4-156">OUTPUTS</span></span>

### <span data-ttu-id="31fe4-157">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="31fe4-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="31fe4-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31fe4-158">NOTES</span></span>

## <span data-ttu-id="31fe4-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31fe4-159">RELATED LINKS</span></span>

[<span data-ttu-id="31fe4-160">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="31fe4-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="31fe4-161">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="31fe4-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="31fe4-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="31fe4-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="31fe4-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="31fe4-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="31fe4-164">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="31fe4-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="31fe4-165">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="31fe4-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="31fe4-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="31fe4-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


