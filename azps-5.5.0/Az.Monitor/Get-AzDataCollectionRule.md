---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111765"
---
# <span data-ttu-id="4d528-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="4d528-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="4d528-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d528-102">SYNOPSIS</span></span>
<span data-ttu-id="4d528-103">Obtém regras de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="4d528-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="4d528-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d528-104">SYNTAX</span></span>

### <span data-ttu-id="4d528-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="4d528-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="4d528-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d528-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="4d528-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4d528-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="4d528-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d528-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="4d528-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d528-109">DESCRIPTION</span></span>
<span data-ttu-id="4d528-110">O **cmdlet Get-AzDataCollectionRule** recebe uma ou mais regras de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="4d528-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="4d528-111">As Regras de Coleta de Dados (DCR) definem os dados que vêm para o Monitor do Azure e especificam para onde esses dados devem ser enviados ou armazenados.</span><span class="sxs-lookup"><span data-stu-id="4d528-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="4d528-112">Este é o artigo completo [de visão geral do DCR.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="4d528-112">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="4d528-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d528-113">EXAMPLES</span></span>

### <span data-ttu-id="4d528-114">Exemplo 1: Obter regras de coleta de dados por ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="4d528-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="4d528-115">Esse comando lista todas as regras de coleta de dados para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="4d528-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="4d528-116">Exemplo 2: Obter regras de coleta de dados para determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4d528-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="4d528-117">Esse comando lista as regras de coleta de dados para o determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d528-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="4d528-118">Exemplo 3: Obter uma regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="4d528-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="4d528-119">Esse comando lista uma regra de coleta de dados (uma lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="4d528-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="4d528-120">Exemplo 4: Obter uma regra de coleta de dados por ID da Regra</span><span class="sxs-lookup"><span data-stu-id="4d528-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="4d528-121">Esse comando lista uma regra de coleta de dados (uma lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="4d528-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="4d528-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d528-122">PARAMETERS</span></span>

### <span data-ttu-id="4d528-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d528-123">-DefaultProfile</span></span>
<span data-ttu-id="4d528-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4d528-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d528-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d528-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d528-126">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4d528-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d528-127">-NomeDa Regra</span><span class="sxs-lookup"><span data-stu-id="4d528-127">-RuleName</span></span>
<span data-ttu-id="4d528-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4d528-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d528-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="4d528-129">-RuleId</span></span>
<span data-ttu-id="4d528-130">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4d528-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d528-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d528-131">CommonParameters</span></span>
<span data-ttu-id="4d528-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d528-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d528-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d528-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d528-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d528-134">INPUTS</span></span>

### <span data-ttu-id="4d528-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4d528-135">System.String</span></span>

## <span data-ttu-id="4d528-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d528-136">OUTPUTS</span></span>

### <span data-ttu-id="4d528-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="4d528-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="4d528-138">Notas</span><span class="sxs-lookup"><span data-stu-id="4d528-138">NOTES</span></span>

## <span data-ttu-id="4d528-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d528-139">RELATED LINKS</span></span>

<span data-ttu-id="4d528-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="4d528-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
