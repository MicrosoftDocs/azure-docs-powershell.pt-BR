---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: e51e43d2555decaa3f37509a89ebe9d55ba2ac96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886926"
---
# <span data-ttu-id="36238-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="36238-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="36238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36238-102">SYNOPSIS</span></span>
<span data-ttu-id="36238-103">Atualizações (substituição completa) uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="36238-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="36238-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="36238-104">SYNTAX</span></span>

### <span data-ttu-id="36238-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36238-105">ByName (Default)</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="36238-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36238-106">ByResourceId</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -RuleId <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="36238-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="36238-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="36238-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="36238-108">DESCRIPTION</span></span>
<span data-ttu-id="36238-109">O cmdlet **Set-AzDataCollectionRule** substitui uma regra de coleta de dados existente.</span><span class="sxs-lookup"><span data-stu-id="36238-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="36238-110">As Regras de Coleta de Dados (DCR) definem os dados que vêm para o Monitor do Azure e especificam para onde esses dados devem ser enviados ou armazenados.</span><span class="sxs-lookup"><span data-stu-id="36238-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="36238-111">Aqui está o artigo completo [de visão geral do DCR](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span><span class="sxs-lookup"><span data-stu-id="36238-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="36238-112">Para usar o parâmetro -RuleFile, construa um arquivo json contendo três propriedades: dataSources, destinos, dataFlows (consulte Example #1).</span><span class="sxs-lookup"><span data-stu-id="36238-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="36238-113">Você pode encontrar aqui o detalhe [do esquema](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span><span class="sxs-lookup"><span data-stu-id="36238-113">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="36238-114">A saída de um DCR serializado com o cmdlet ConvertTo-Json também é suportada (Exemplo #2).</span><span class="sxs-lookup"><span data-stu-id="36238-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="36238-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36238-115">EXAMPLES</span></span>

### <span data-ttu-id="36238-116">Exemplo 1: Atualizar a regra de coleta de dados, JSON da API Rest</span><span class="sxs-lookup"><span data-stu-id="36238-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -ResourceGroupName 'testdcr' 
                                -RuleName 'newDcr' 
                                -RuleFile 'C:\samples\dcr1.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="36238-117">Esse comando substitui uma regra de coleta de dados existente para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="36238-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="36238-118">Exemplo 2: Atualizar regra de coleta de dados, JSON de PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="36238-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr' 
                                -RuleFile 'C:\samples\dcr2.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="36238-119">Esse comando substitui uma regra de coleta de dados existente para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="36238-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="36238-120">Exemplo 3: Atualizar a regra de coleta de dados do objeto</span><span class="sxs-lookup"><span data-stu-id="36238-120">Example 3: Update data collection rule from object</span></span>
```powershell
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr.Description = 'This is a test'
PS C:\>$dcr | Set-AzDataCollectionRule

Description       : This is a test
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

## <span data-ttu-id="36238-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="36238-121">PARAMETERS</span></span>

### <span data-ttu-id="36238-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36238-122">-DefaultProfile</span></span>
<span data-ttu-id="36238-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="36238-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36238-124">-Location</span><span class="sxs-lookup"><span data-stu-id="36238-124">-Location</span></span>
<span data-ttu-id="36238-125">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="36238-125">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36238-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="36238-126">-RuleFile</span></span>
<span data-ttu-id="36238-127">O caminho do arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="36238-127">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36238-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36238-128">-ResourceGroupName</span></span>
<span data-ttu-id="36238-129">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="36238-129">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36238-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="36238-130">-RuleName</span></span>
<span data-ttu-id="36238-131">O nome do recurso</span><span class="sxs-lookup"><span data-stu-id="36238-131">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36238-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="36238-132">-RuleId</span></span>
<span data-ttu-id="36238-133">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="36238-133">The resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36238-134">-Description</span><span class="sxs-lookup"><span data-stu-id="36238-134">-Description</span></span>
<span data-ttu-id="36238-135">A descrição do recurso</span><span class="sxs-lookup"><span data-stu-id="36238-135">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36238-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="36238-136">-Tag</span></span>
<span data-ttu-id="36238-137">As marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="36238-137">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36238-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36238-138">-InputObject</span></span>
<span data-ttu-id="36238-139">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="36238-139">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="36238-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36238-140">-Confirm</span></span>
<span data-ttu-id="36238-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36238-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36238-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36238-142">-WhatIf</span></span>
<span data-ttu-id="36238-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36238-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36238-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36238-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36238-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36238-145">CommonParameters</span></span>
<span data-ttu-id="36238-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36238-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36238-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36238-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36238-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36238-148">INPUTS</span></span>

### <span data-ttu-id="36238-149">System.String</span><span class="sxs-lookup"><span data-stu-id="36238-149">System.String</span></span>

## <span data-ttu-id="36238-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="36238-150">OUTPUTS</span></span>

### <span data-ttu-id="36238-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="36238-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="36238-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="36238-152">NOTES</span></span>

## <span data-ttu-id="36238-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36238-153">RELATED LINKS</span></span>

<span data-ttu-id="36238-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="36238-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>