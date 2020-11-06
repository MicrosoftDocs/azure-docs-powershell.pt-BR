---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441057"
---
# <span data-ttu-id="92cc6-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="92cc6-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="92cc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="92cc6-103">Adiciona ou atualiza uma regra de alerta de WebTest.</span><span class="sxs-lookup"><span data-stu-id="92cc6-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92cc6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92cc6-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92cc6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="92cc6-106">O cmdlet **Add-AzureRmWebtestAlertRule** adiciona ou atualiza uma regra de alerta de tipo de métrica, evento ou WebTest.</span><span class="sxs-lookup"><span data-stu-id="92cc6-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="92cc6-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="92cc6-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="92cc6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92cc6-108">EXAMPLES</span></span>

### <span data-ttu-id="92cc6-109">Exemplo 1: adicionar uma regra de alerta de WebTest</span><span class="sxs-lookup"><span data-stu-id="92cc6-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="92cc6-110">Esse comando adiciona ou atualiza uma regra de alerta de WebTest.</span><span class="sxs-lookup"><span data-stu-id="92cc6-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="92cc6-111">OS</span><span class="sxs-lookup"><span data-stu-id="92cc6-111">PARAMETERS</span></span>

### <span data-ttu-id="92cc6-112">-Ações</span><span class="sxs-lookup"><span data-stu-id="92cc6-112">-Actions</span></span>
<span data-ttu-id="92cc6-113">Especifica uma lista de ações separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="92cc6-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="92cc6-114">-Descrição</span><span class="sxs-lookup"><span data-stu-id="92cc6-114">-Description</span></span>
<span data-ttu-id="92cc6-115">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="92cc6-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="92cc6-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="92cc6-116">-DisableRule</span></span>
<span data-ttu-id="92cc6-117">Desabilita a regra.</span><span class="sxs-lookup"><span data-stu-id="92cc6-117">Disables the rule.</span></span>
<span data-ttu-id="92cc6-118">Se você não especificar esse parâmetro, a regra estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="92cc6-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="92cc6-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="92cc6-119">-FailedLocationCount</span></span>
<span data-ttu-id="92cc6-120">Especifica a contagem de locais com falha para as regras WebTest.</span><span class="sxs-lookup"><span data-stu-id="92cc6-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="92cc6-121">Isso é semelhante ao limiar nos outros tipos de regras.</span><span class="sxs-lookup"><span data-stu-id="92cc6-121">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92cc6-122">-Local</span><span class="sxs-lookup"><span data-stu-id="92cc6-122">-Location</span></span>
<span data-ttu-id="92cc6-123">Especifica o local onde a regra é definida.</span><span class="sxs-lookup"><span data-stu-id="92cc6-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="92cc6-124">-Metricname</span><span class="sxs-lookup"><span data-stu-id="92cc6-124">-MetricName</span></span>
<span data-ttu-id="92cc6-125">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="92cc6-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="92cc6-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="92cc6-126">-MetricNamespace</span></span>
<span data-ttu-id="92cc6-127">Especifica o namespace de métrica para a regra.</span><span class="sxs-lookup"><span data-stu-id="92cc6-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="92cc6-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="92cc6-128">-Name</span></span>
<span data-ttu-id="92cc6-129">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="92cc6-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="92cc6-130">-Resource</span><span class="sxs-lookup"><span data-stu-id="92cc6-130">-ResourceGroup</span></span>
<span data-ttu-id="92cc6-131">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92cc6-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="92cc6-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="92cc6-132">-TargetResourceUri</span></span>
<span data-ttu-id="92cc6-133">Especifica a ID do recurso do WebTest.</span><span class="sxs-lookup"><span data-stu-id="92cc6-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="92cc6-134">-WindowS</span><span class="sxs-lookup"><span data-stu-id="92cc6-134">-WindowSize</span></span>
<span data-ttu-id="92cc6-135">Especifica o tamanho da janela de tempo para a regra calcular seus dados.</span><span class="sxs-lookup"><span data-stu-id="92cc6-135">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="92cc6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92cc6-136">-DefaultProfile</span></span>
<span data-ttu-id="92cc6-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92cc6-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92cc6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92cc6-138">CommonParameters</span></span>
<span data-ttu-id="92cc6-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92cc6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92cc6-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92cc6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92cc6-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92cc6-141">INPUTS</span></span>

## <span data-ttu-id="92cc6-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92cc6-142">OUTPUTS</span></span>

### <span data-ttu-id="92cc6-143">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="92cc6-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="92cc6-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92cc6-144">NOTES</span></span>

## <span data-ttu-id="92cc6-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92cc6-145">RELATED LINKS</span></span>

[<span data-ttu-id="92cc6-146">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="92cc6-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="92cc6-147">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="92cc6-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="92cc6-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="92cc6-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="92cc6-149">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="92cc6-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


