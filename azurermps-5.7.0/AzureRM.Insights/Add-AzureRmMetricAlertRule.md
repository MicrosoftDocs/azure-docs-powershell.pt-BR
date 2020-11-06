---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 097f3562ca326275c050054fd07d11d349cf98d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429775"
---
# <span data-ttu-id="6bcb5-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6bcb5-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="6bcb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6bcb5-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcb5-103">Adiciona ou atualiza uma regra de alerta baseada em métrica.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bcb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bcb5-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bcb5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6bcb5-105">DESCRIPTION</span></span>
<span data-ttu-id="6bcb5-106">O cmdlet **Add-AzureRmMetricAlertRule** adiciona ou atualiza uma regra de alerta baseada em métrica.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="6bcb5-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="6bcb5-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="6bcb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bcb5-109">EXAMPLES</span></span>

### <span data-ttu-id="6bcb5-110">Exemplo 1: adicionar uma regra de alerta de métrica a um site</span><span class="sxs-lookup"><span data-stu-id="6bcb5-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="6bcb5-111">Esse comando cria uma regra de alerta métrica para um site.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="6bcb5-112">Exemplo 2: desabilitar uma regra</span><span class="sxs-lookup"><span data-stu-id="6bcb5-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="6bcb5-113">Esse comando desabilita uma regra.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-113">This command disables a rule.</span></span>
<span data-ttu-id="6bcb5-114">Se a regra não existir, será criada para ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="6bcb5-115">Se a regra existir, basta desfazê-la.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="6bcb5-116">Exemplo 3: adicionar uma regra com ações</span><span class="sxs-lookup"><span data-stu-id="6bcb5-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="6bcb5-117">Esse comando cria uma regra de alerta métrica para um site.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="6bcb5-118">OS</span><span class="sxs-lookup"><span data-stu-id="6bcb5-118">PARAMETERS</span></span>

### <span data-ttu-id="6bcb5-119">-Ação</span><span class="sxs-lookup"><span data-stu-id="6bcb5-119">-Action</span></span>
<span data-ttu-id="6bcb5-120">Especifica uma lista de ações separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bcb5-121">-DefaultProfile</span></span>
<span data-ttu-id="6bcb5-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6bcb5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6bcb5-123">-Description</span></span>
<span data-ttu-id="6bcb5-124">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-124">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="6bcb5-125">-DisableRule</span></span>
<span data-ttu-id="6bcb5-126">Desabilita a regra.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-126">Disables the rule.</span></span>
<span data-ttu-id="6bcb5-127">Se você não especificar esse parâmetro, a regra estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-127">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-128">-Local</span><span class="sxs-lookup"><span data-stu-id="6bcb5-128">-Location</span></span>
<span data-ttu-id="6bcb5-129">Especifica o local onde a regra é definida.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-129">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-130">-Metricname</span><span class="sxs-lookup"><span data-stu-id="6bcb5-130">-MetricName</span></span>
<span data-ttu-id="6bcb5-131">Especifica o nome da métrica que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="6bcb5-132">Especifique esse parâmetro somente para regras com base em métricas.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-132">Specify this parameter only for metric-based rules.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="6bcb5-133">-Name</span></span>
<span data-ttu-id="6bcb5-134">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-134">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-135">-Operador</span><span class="sxs-lookup"><span data-stu-id="6bcb5-135">-Operator</span></span>
<span data-ttu-id="6bcb5-136">Especifica o operador relacional para a condição da regra.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="6bcb5-137">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6bcb5-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6bcb5-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="6bcb5-138">GreaterThan</span></span>
- <span data-ttu-id="6bcb5-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="6bcb5-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="6bcb5-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="6bcb5-140">LessThan</span></span>
- <span data-ttu-id="6bcb5-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="6bcb5-141">LessThanOrEqual</span></span>

```yaml
Type: ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bcb5-142">-ResourceGroupName</span></span>
<span data-ttu-id="6bcb5-143">Especifica o nome do grupo de recursos para a regra.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6bcb5-144">-TargetResourceId</span></span>
<span data-ttu-id="6bcb5-145">Especifica a ID do recurso que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="6bcb5-146">Observação: esta propriedade não pode ser atualizada para uma regra de alerta existente.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-147">-Threshold</span><span class="sxs-lookup"><span data-stu-id="6bcb5-147">-Threshold</span></span>
<span data-ttu-id="6bcb5-148">Especifica o limite da regra.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="6bcb5-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="6bcb5-150">Especifica o operador de agregação a ser aplicado à janela de tempo quando a regra está sendo avaliada.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: TimeAggregationOperator
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-151">-WindowS</span><span class="sxs-lookup"><span data-stu-id="6bcb5-151">-WindowSize</span></span>
<span data-ttu-id="6bcb5-152">Especifica o tamanho da janela de tempo para a regra calcular seus dados.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-152">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bcb5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcb5-153">CommonParameters</span></span>
<span data-ttu-id="6bcb5-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcb5-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bcb5-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcb5-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6bcb5-156">INPUTS</span></span>

### <span data-ttu-id="6bcb5-157">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6bcb5-157">None</span></span>
<span data-ttu-id="6bcb5-158">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6bcb5-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6bcb5-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6bcb5-159">OUTPUTS</span></span>

### <span data-ttu-id="6bcb5-160">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6bcb5-160">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="6bcb5-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6bcb5-161">NOTES</span></span>

## <span data-ttu-id="6bcb5-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bcb5-162">RELATED LINKS</span></span>

[<span data-ttu-id="6bcb5-163">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6bcb5-163">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6bcb5-164">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6bcb5-164">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="6bcb5-165">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6bcb5-165">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="6bcb5-166">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="6bcb5-166">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="6bcb5-167">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="6bcb5-167">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="6bcb5-168">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6bcb5-168">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="6bcb5-169">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="6bcb5-169">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


