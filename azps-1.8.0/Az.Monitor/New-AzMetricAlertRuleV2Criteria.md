---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770296"
---
# New-AzMetricAlertRuleV2Criteria

## Sinopse
Cria um objeto de critério local que pode ser usado para criar um novo alerta de métrica

## SYNTAX

### StaticThresholdParameterSet
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DynamicThresholdParameterSet
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzMetricAlertRuleV2Criteria** cria um objeto de critérios métrico local a ser usado como um cmdlet Add-AzMetricAlertRuleV2 de entrada, que cria uma nova regra de alerta de métrica.

## EXEMPLOS

### Exemplo 1: criar um critério simples de alerta de métrica

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

Esse comando cria um critério simples de alerta de métrica que pode ser usado em uma regra de alerta de métrica

### Exemplo 2: criar um critério de alerta métrico mais complexo

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

Esse conjunto de comandos cria um critério de alerta métrico mais complexo que inclui a seleção de dimensão

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -DimensionSelection
Lista de condições de dimensão

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DynamicThreshold
O limite dinâmico para a condição da regra

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailingPeriod
O período de falha para a condição da regra

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreDataBefore
O parâmetro IgnoreDataBefore

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metricname
O nome da métrica para a regra

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetricNamespace
O namespace da métrica

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operador
O operador de condição da regra

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sensibilidade
A sensibilidade para a condição da regra

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Threshold
O limite para a condição da regra

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Agregação de TimeSerial
A operação de agregação usada para acumular vários valores métricos ao longo do intervalo de janela

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TotalPeriod
O período total para a condição de regra

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.
Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. insights. OutputClasses. PSMetricDimension []

## EXIBE

### Microsoft. Azure. Commands. insights. OutputClasses. PSMetricCriteria

## INFORMA

## LINKS RELACIONADOS
