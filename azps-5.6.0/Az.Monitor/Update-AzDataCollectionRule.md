---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: 2e4aba9a2572b5612070d860dcbe20cda2366a02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890826"
---
# <span data-ttu-id="402a7-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="402a7-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="402a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="402a7-102">SYNOPSIS</span></span>
<span data-ttu-id="402a7-103">Atualiza uma propriedade de marcas de regra de conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="402a7-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="402a7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="402a7-104">SYNTAX</span></span>

### <span data-ttu-id="402a7-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="402a7-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="402a7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="402a7-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="402a7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="402a7-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="402a7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="402a7-108">DESCRIPTION</span></span>
<span data-ttu-id="402a7-109">O cmdlet **Update-AzDataCollectionRule** atualiza uma propriedade tags de regra de conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="402a7-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="402a7-110">As Regras de Coleta de Dados (DCR) definem os dados que vêm para o Monitor do Azure e especificam para onde esses dados devem ser enviados ou armazenados.</span><span class="sxs-lookup"><span data-stu-id="402a7-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="402a7-111">Aqui está o artigo completo [de visão geral do DCR](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span><span class="sxs-lookup"><span data-stu-id="402a7-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="402a7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="402a7-112">EXAMPLES</span></span>

### <span data-ttu-id="402a7-113">Exemplo 1: Atualizar marcas de regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="402a7-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="402a7-114">Este comando atualiza a propriedade tags para a regra de coleta de dados determinada.</span><span class="sxs-lookup"><span data-stu-id="402a7-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="402a7-115">Exemplo 2: Atualizar marcas de regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="402a7-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="402a7-116">Este comando atualiza a propriedade tags para a regra de coleta de dados determinada.</span><span class="sxs-lookup"><span data-stu-id="402a7-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="402a7-117">Exemplo 3: Atualizar marcas de regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="402a7-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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

<span data-ttu-id="402a7-118">Este comando atualiza a propriedade tags para a regra de coleta de dados determinada.</span><span class="sxs-lookup"><span data-stu-id="402a7-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="402a7-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="402a7-119">PARAMETERS</span></span>

### <span data-ttu-id="402a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402a7-120">-DefaultProfile</span></span>
<span data-ttu-id="402a7-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="402a7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="402a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="402a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="402a7-123">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="402a7-123">The resource group name</span></span>

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

### <span data-ttu-id="402a7-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="402a7-124">-RuleName</span></span>
<span data-ttu-id="402a7-125">O nome do recurso</span><span class="sxs-lookup"><span data-stu-id="402a7-125">The resource name</span></span>

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

### <span data-ttu-id="402a7-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="402a7-126">-RuleId</span></span>
<span data-ttu-id="402a7-127">A ID do recurso da regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="402a7-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="402a7-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="402a7-128">-InputObject</span></span>
<span data-ttu-id="402a7-129">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="402a7-129">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="402a7-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="402a7-130">-Tag</span></span>
<span data-ttu-id="402a7-131">A propriedade tags da regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="402a7-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="402a7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="402a7-132">-Confirm</span></span>
<span data-ttu-id="402a7-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="402a7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="402a7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="402a7-134">-WhatIf</span></span>
<span data-ttu-id="402a7-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="402a7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="402a7-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="402a7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="402a7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402a7-137">CommonParameters</span></span>
<span data-ttu-id="402a7-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402a7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402a7-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="402a7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402a7-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="402a7-140">INPUTS</span></span>

### <span data-ttu-id="402a7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="402a7-141">System.String</span></span>

## <span data-ttu-id="402a7-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="402a7-142">OUTPUTS</span></span>

### <span data-ttu-id="402a7-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="402a7-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="402a7-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="402a7-144">NOTES</span></span>

## <span data-ttu-id="402a7-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="402a7-145">RELATED LINKS</span></span>

<span data-ttu-id="402a7-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="402a7-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>