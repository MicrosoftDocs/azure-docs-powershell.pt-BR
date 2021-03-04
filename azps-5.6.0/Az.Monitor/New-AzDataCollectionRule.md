---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: b14d834e005f8a81666fd98b40d276825f04c0e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889461"
---
# <span data-ttu-id="ae17b-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="ae17b-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="ae17b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae17b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae17b-103">Criar uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="ae17b-103">Create a data collection rule.</span></span>

## <span data-ttu-id="ae17b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae17b-104">SYNTAX</span></span>

### <span data-ttu-id="ae17b-105">ByFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae17b-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
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

## <span data-ttu-id="ae17b-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae17b-106">DESCRIPTION</span></span>
<span data-ttu-id="ae17b-107">O cmdlet **New-AzDataCollectionRule** cria uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="ae17b-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="ae17b-108">As Regras de Coleta de Dados (DCR) definem os dados que vêm para o Monitor do Azure e especificam para onde esses dados devem ser enviados ou armazenados.</span><span class="sxs-lookup"><span data-stu-id="ae17b-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="ae17b-109">Aqui está o artigo completo [de visão geral do DCR](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span><span class="sxs-lookup"><span data-stu-id="ae17b-109">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="ae17b-110">Para usar o parâmetro -RuleFile, construa um arquivo json contendo três propriedades: dataSources, destinos, dataFlows (consulte Example #1)</span><span class="sxs-lookup"><span data-stu-id="ae17b-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="ae17b-111">Você pode encontrar aqui o detalhe [do esquema](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span><span class="sxs-lookup"><span data-stu-id="ae17b-111">You may find here the [schema detail](https://docs.microsoft.com/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="ae17b-112">A saída de um DCR serializado com o cmdlet ConvertTo-Json também é suportada (consulte Example #2).</span><span class="sxs-lookup"><span data-stu-id="ae17b-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="ae17b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae17b-113">EXAMPLES</span></span>

### <span data-ttu-id="ae17b-114">Exemplo 1: Criar regra de coleta de dados, JSON da API Rest</span><span class="sxs-lookup"><span data-stu-id="ae17b-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
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

<span data-ttu-id="ae17b-115">Este comando cria uma regra de coleta de dados para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ae17b-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="ae17b-116">Exemplo 2: Criar regra de coleta de dados, JSON de PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="ae17b-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
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

<span data-ttu-id="ae17b-117">Este comando cria uma regra de coleta de dados para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ae17b-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="ae17b-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae17b-118">PARAMETERS</span></span>

### <span data-ttu-id="ae17b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae17b-119">-DefaultProfile</span></span>
<span data-ttu-id="ae17b-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ae17b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae17b-121">-Location</span><span class="sxs-lookup"><span data-stu-id="ae17b-121">-Location</span></span>
<span data-ttu-id="ae17b-122">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="ae17b-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae17b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae17b-123">-ResourceGroupName</span></span>
<span data-ttu-id="ae17b-124">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ae17b-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae17b-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ae17b-125">-RuleName</span></span>
<span data-ttu-id="ae17b-126">O nome do recurso</span><span class="sxs-lookup"><span data-stu-id="ae17b-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae17b-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="ae17b-127">-RuleFile</span></span>
<span data-ttu-id="ae17b-128">O caminho do arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="ae17b-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae17b-129">-Description</span><span class="sxs-lookup"><span data-stu-id="ae17b-129">-Description</span></span>
<span data-ttu-id="ae17b-130">A descrição do recurso</span><span class="sxs-lookup"><span data-stu-id="ae17b-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae17b-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae17b-131">-Tag</span></span>
<span data-ttu-id="ae17b-132">As marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="ae17b-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae17b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae17b-133">-Confirm</span></span>
<span data-ttu-id="ae17b-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae17b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae17b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae17b-135">-WhatIf</span></span>
<span data-ttu-id="ae17b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae17b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae17b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae17b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae17b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae17b-138">CommonParameters</span></span>
<span data-ttu-id="ae17b-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae17b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae17b-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae17b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae17b-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae17b-141">INPUTS</span></span>

### <span data-ttu-id="ae17b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ae17b-142">System.String</span></span>

## <span data-ttu-id="ae17b-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae17b-143">OUTPUTS</span></span>

### <span data-ttu-id="ae17b-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="ae17b-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="ae17b-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae17b-145">NOTES</span></span>

## <span data-ttu-id="ae17b-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae17b-146">RELATED LINKS</span></span>

<span data-ttu-id="ae17b-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="ae17b-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>