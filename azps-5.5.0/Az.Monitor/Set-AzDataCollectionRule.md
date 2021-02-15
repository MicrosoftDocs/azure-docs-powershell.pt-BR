---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: 864b3c8abe2411316edf155c49757c1082a863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114239"
---
# <span data-ttu-id="3aa2c-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="3aa2c-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="3aa2c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3aa2c-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa2c-103">Atualizações (substituição total) uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="3aa2c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aa2c-104">SYNTAX</span></span>

### <span data-ttu-id="3aa2c-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="3aa2c-105">ByName (Default)</span></span>
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

### <span data-ttu-id="3aa2c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa2c-106">ByResourceId</span></span>
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

### <span data-ttu-id="3aa2c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3aa2c-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="3aa2c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aa2c-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa2c-109">O cmdlet **Set-AzDataCollectionRule** substitui uma regra de coleta de dados existente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="3aa2c-110">As Regras de Coleta de Dados (DCR) definem os dados que vêm para o Monitor do Azure e especificam para onde esses dados devem ser enviados ou armazenados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="3aa2c-111">Este é o artigo completo [de visão geral do DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="3aa2c-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="3aa2c-112">Para usar o parâmetro -RuleFile, construa um arquivo json contendo três propriedades: dataSources, destinos, dataFlows (consulte Exemplo #1).</span><span class="sxs-lookup"><span data-stu-id="3aa2c-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="3aa2c-113">Você pode encontrar aqui os detalhes [do esquema.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="3aa2c-113">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="3aa2c-114">A saída de um DCR serializado com o cmdlet ConvertTo-Json também é suportada (exemplo #2).</span><span class="sxs-lookup"><span data-stu-id="3aa2c-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="3aa2c-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3aa2c-115">EXAMPLES</span></span>

### <span data-ttu-id="3aa2c-116">Exemplo 1: Atualizar regra de coleta de dados, JSON da API rest</span><span class="sxs-lookup"><span data-stu-id="3aa2c-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
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

<span data-ttu-id="3aa2c-117">Esse comando substitui uma regra de coleta de dados existente para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="3aa2c-118">Exemplo 2: Atualizar regra de coleta de dados, JSON da PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="3aa2c-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
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

<span data-ttu-id="3aa2c-119">Esse comando substitui uma regra de coleta de dados existente para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="3aa2c-120">Exemplo 3: Atualizar a regra de coleta de dados do objeto</span><span class="sxs-lookup"><span data-stu-id="3aa2c-120">Example 3: Update data collection rule from object</span></span>
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

## <span data-ttu-id="3aa2c-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3aa2c-121">PARAMETERS</span></span>

### <span data-ttu-id="3aa2c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa2c-122">-DefaultProfile</span></span>
<span data-ttu-id="3aa2c-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3aa2c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aa2c-124">-Local</span><span class="sxs-lookup"><span data-stu-id="3aa2c-124">-Location</span></span>
<span data-ttu-id="3aa2c-125">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="3aa2c-125">The resource location</span></span>

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

### <span data-ttu-id="3aa2c-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="3aa2c-126">-RuleFile</span></span>
<span data-ttu-id="3aa2c-127">O caminho do arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="3aa2c-127">The JSON file path</span></span>

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

### <span data-ttu-id="3aa2c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa2c-128">-ResourceGroupName</span></span>
<span data-ttu-id="3aa2c-129">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3aa2c-129">The resource group name</span></span>

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

### <span data-ttu-id="3aa2c-130">-NomeDa Regra</span><span class="sxs-lookup"><span data-stu-id="3aa2c-130">-RuleName</span></span>
<span data-ttu-id="3aa2c-131">O nome do recurso</span><span class="sxs-lookup"><span data-stu-id="3aa2c-131">The resource name</span></span>

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

### <span data-ttu-id="3aa2c-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="3aa2c-132">-RuleId</span></span>
<span data-ttu-id="3aa2c-133">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="3aa2c-133">The resource ID</span></span>

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

### <span data-ttu-id="3aa2c-134">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3aa2c-134">-Description</span></span>
<span data-ttu-id="3aa2c-135">A descrição do recurso</span><span class="sxs-lookup"><span data-stu-id="3aa2c-135">The resource description</span></span>

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

### <span data-ttu-id="3aa2c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="3aa2c-136">-Tag</span></span>
<span data-ttu-id="3aa2c-137">As marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="3aa2c-137">The resource tags</span></span>

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

### <span data-ttu-id="3aa2c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aa2c-138">-InputObject</span></span>
<span data-ttu-id="3aa2c-139">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="3aa2c-139">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="3aa2c-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3aa2c-140">-Confirm</span></span>
<span data-ttu-id="3aa2c-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa2c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa2c-142">-WhatIf</span></span>
<span data-ttu-id="3aa2c-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3aa2c-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa2c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa2c-145">CommonParameters</span></span>
<span data-ttu-id="3aa2c-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa2c-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3aa2c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa2c-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="3aa2c-148">INPUTS</span></span>

### <span data-ttu-id="3aa2c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3aa2c-149">System.String</span></span>

## <span data-ttu-id="3aa2c-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="3aa2c-150">OUTPUTS</span></span>

### <span data-ttu-id="3aa2c-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="3aa2c-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="3aa2c-152">Notas</span><span class="sxs-lookup"><span data-stu-id="3aa2c-152">NOTES</span></span>

## <span data-ttu-id="3aa2c-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3aa2c-153">RELATED LINKS</span></span>

<span data-ttu-id="3aa2c-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="3aa2c-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>