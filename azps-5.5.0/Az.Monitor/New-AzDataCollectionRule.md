---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: cdde294c3af4684146d265e2024f6948660312bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117521"
---
# <span data-ttu-id="8c553-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="8c553-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="8c553-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c553-102">SYNOPSIS</span></span>
<span data-ttu-id="8c553-103">Criar uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="8c553-103">Create a data collection rule.</span></span>

## <span data-ttu-id="8c553-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c553-104">SYNTAX</span></span>

### <span data-ttu-id="8c553-105">ByFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8c553-105">ByFile (Default)</span></span>
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

## <span data-ttu-id="8c553-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c553-106">DESCRIPTION</span></span>
<span data-ttu-id="8c553-107">O **cmdlet New-AzDataCollectionRule** cria uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="8c553-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="8c553-108">As Regras de Coleta de Dados (DCR) definem os dados que vêm para o Monitor do Azure e especificam para onde esses dados devem ser enviados ou armazenados.</span><span class="sxs-lookup"><span data-stu-id="8c553-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="8c553-109">Este é o artigo completo [de visão geral do DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="8c553-109">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="8c553-110">Para usar o parâmetro -RuleFile, construa um arquivo json contendo três propriedades: dataSources, destinos, dataFlows (consulte Exemplo #1)</span><span class="sxs-lookup"><span data-stu-id="8c553-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="8c553-111">Você pode encontrar aqui os detalhes [do esquema.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="8c553-111">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="8c553-112">A saída de um DCR serializado com o cmdlet ConvertTo-Json também tem suporte (consulte Exemplo #2).</span><span class="sxs-lookup"><span data-stu-id="8c553-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="8c553-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c553-113">EXAMPLES</span></span>

### <span data-ttu-id="8c553-114">Exemplo 1: Criar regra de coleta de dados, JSON a partir da API rest</span><span class="sxs-lookup"><span data-stu-id="8c553-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
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

<span data-ttu-id="8c553-115">Esse comando cria regras de coleta de dados para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8c553-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="8c553-116">Exemplo 2: Criar regra de coleta de dados, JSON a partir de PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="8c553-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
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

<span data-ttu-id="8c553-117">Esse comando cria regras de coleta de dados para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8c553-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="8c553-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c553-118">PARAMETERS</span></span>

### <span data-ttu-id="8c553-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c553-119">-DefaultProfile</span></span>
<span data-ttu-id="8c553-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8c553-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c553-121">-Local</span><span class="sxs-lookup"><span data-stu-id="8c553-121">-Location</span></span>
<span data-ttu-id="8c553-122">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="8c553-122">The resource location</span></span>

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

### <span data-ttu-id="8c553-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c553-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c553-124">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8c553-124">The resource group name</span></span>

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

### <span data-ttu-id="8c553-125">-NomeDa Regra</span><span class="sxs-lookup"><span data-stu-id="8c553-125">-RuleName</span></span>
<span data-ttu-id="8c553-126">O nome do recurso</span><span class="sxs-lookup"><span data-stu-id="8c553-126">The resource name</span></span>

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

### <span data-ttu-id="8c553-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="8c553-127">-RuleFile</span></span>
<span data-ttu-id="8c553-128">O caminho do arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="8c553-128">The JSON file path</span></span>

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

### <span data-ttu-id="8c553-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8c553-129">-Description</span></span>
<span data-ttu-id="8c553-130">A descrição do recurso</span><span class="sxs-lookup"><span data-stu-id="8c553-130">The resource description</span></span>

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

### <span data-ttu-id="8c553-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c553-131">-Tag</span></span>
<span data-ttu-id="8c553-132">As marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="8c553-132">The resource tags</span></span>

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

### <span data-ttu-id="8c553-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8c553-133">-Confirm</span></span>
<span data-ttu-id="8c553-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c553-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c553-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c553-135">-WhatIf</span></span>
<span data-ttu-id="8c553-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8c553-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c553-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c553-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c553-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c553-138">CommonParameters</span></span>
<span data-ttu-id="8c553-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c553-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c553-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c553-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c553-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="8c553-141">INPUTS</span></span>

### <span data-ttu-id="8c553-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8c553-142">System.String</span></span>

## <span data-ttu-id="8c553-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="8c553-143">OUTPUTS</span></span>

### <span data-ttu-id="8c553-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="8c553-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="8c553-145">Notas</span><span class="sxs-lookup"><span data-stu-id="8c553-145">NOTES</span></span>

## <span data-ttu-id="8c553-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c553-146">RELATED LINKS</span></span>

<span data-ttu-id="8c553-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="8c553-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>