---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429773"
---
# <span data-ttu-id="ff526-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ff526-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="ff526-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff526-102">SYNOPSIS</span></span>
<span data-ttu-id="ff526-103">Adiciona ou atualiza uma regra de alerta de WebTest.</span><span class="sxs-lookup"><span data-stu-id="ff526-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff526-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff526-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff526-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff526-105">DESCRIPTION</span></span>
<span data-ttu-id="ff526-106">O cmdlet **Add-AzureRmWebtestAlertRule** adiciona ou atualiza uma regra de alerta de tipo de métrica, evento ou WebTest.</span><span class="sxs-lookup"><span data-stu-id="ff526-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="ff526-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="ff526-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="ff526-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="ff526-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ff526-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff526-109">EXAMPLES</span></span>

### <span data-ttu-id="ff526-110">Exemplo 1: adicionar uma regra de alerta de WebTest</span><span class="sxs-lookup"><span data-stu-id="ff526-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="ff526-111">Esse comando adiciona ou atualiza uma regra de alerta de WebTest.</span><span class="sxs-lookup"><span data-stu-id="ff526-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="ff526-112">OS</span><span class="sxs-lookup"><span data-stu-id="ff526-112">PARAMETERS</span></span>

### <span data-ttu-id="ff526-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="ff526-113">-Action</span></span>
<span data-ttu-id="ff526-114">Especifica uma lista de ações separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="ff526-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="ff526-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff526-115">-DefaultProfile</span></span>
<span data-ttu-id="ff526-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ff526-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff526-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ff526-117">-Description</span></span>
<span data-ttu-id="ff526-118">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="ff526-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="ff526-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="ff526-119">-DisableRule</span></span>
<span data-ttu-id="ff526-120">Desabilita a regra.</span><span class="sxs-lookup"><span data-stu-id="ff526-120">Disables the rule.</span></span>
<span data-ttu-id="ff526-121">Se você não especificar esse parâmetro, a regra estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="ff526-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="ff526-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="ff526-122">-FailedLocationCount</span></span>
<span data-ttu-id="ff526-123">Especifica a contagem de locais com falha para as regras WebTest.</span><span class="sxs-lookup"><span data-stu-id="ff526-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="ff526-124">Isso é semelhante ao limiar nos outros tipos de regras.</span><span class="sxs-lookup"><span data-stu-id="ff526-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff526-125">-Local</span><span class="sxs-lookup"><span data-stu-id="ff526-125">-Location</span></span>
<span data-ttu-id="ff526-126">Especifica o local onde a regra é definida.</span><span class="sxs-lookup"><span data-stu-id="ff526-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="ff526-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="ff526-127">-MetricName</span></span>
<span data-ttu-id="ff526-128">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="ff526-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="ff526-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="ff526-129">-MetricNamespace</span></span>
<span data-ttu-id="ff526-130">Especifica o namespace de métrica para a regra.</span><span class="sxs-lookup"><span data-stu-id="ff526-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="ff526-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff526-131">-Name</span></span>
<span data-ttu-id="ff526-132">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="ff526-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="ff526-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff526-133">-ResourceGroupName</span></span>
<span data-ttu-id="ff526-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff526-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ff526-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="ff526-135">-TargetResourceUri</span></span>
<span data-ttu-id="ff526-136">Especifica a ID do recurso do WebTest.</span><span class="sxs-lookup"><span data-stu-id="ff526-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="ff526-137">-WindowS</span><span class="sxs-lookup"><span data-stu-id="ff526-137">-WindowSize</span></span>
<span data-ttu-id="ff526-138">Especifica o tamanho da janela de tempo para a regra calcular seus dados.</span><span class="sxs-lookup"><span data-stu-id="ff526-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="ff526-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff526-139">CommonParameters</span></span>
<span data-ttu-id="ff526-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff526-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff526-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff526-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff526-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff526-142">INPUTS</span></span>

### <span data-ttu-id="ff526-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ff526-143">None</span></span>
<span data-ttu-id="ff526-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ff526-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff526-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff526-145">OUTPUTS</span></span>

### <span data-ttu-id="ff526-146">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ff526-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="ff526-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff526-147">NOTES</span></span>

## <span data-ttu-id="ff526-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff526-148">RELATED LINKS</span></span>

[<span data-ttu-id="ff526-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ff526-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ff526-150">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ff526-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="ff526-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ff526-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="ff526-152">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ff526-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


