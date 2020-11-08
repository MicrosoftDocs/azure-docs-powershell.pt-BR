---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125998"
---
# <span data-ttu-id="0b471-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0b471-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="0b471-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b471-102">SYNOPSIS</span></span>
<span data-ttu-id="0b471-103">Adiciona ou atualiza uma regra de alerta de WebTest.</span><span class="sxs-lookup"><span data-stu-id="0b471-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="0b471-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b471-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b471-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b471-105">DESCRIPTION</span></span>
<span data-ttu-id="0b471-106">O cmdlet **Add-AzWebtestAlertRule** adiciona ou atualiza uma regra de alerta de tipo de métrica, evento ou WebTest.</span><span class="sxs-lookup"><span data-stu-id="0b471-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="0b471-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="0b471-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="0b471-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="0b471-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0b471-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b471-109">EXAMPLES</span></span>

### <span data-ttu-id="0b471-110">Exemplo 1: adicionar uma regra de alerta de WebTest</span><span class="sxs-lookup"><span data-stu-id="0b471-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="0b471-111">Esse comando adiciona ou atualiza uma regra de alerta de WebTest.</span><span class="sxs-lookup"><span data-stu-id="0b471-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="0b471-112">OS</span><span class="sxs-lookup"><span data-stu-id="0b471-112">PARAMETERS</span></span>

### <span data-ttu-id="0b471-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="0b471-113">-Action</span></span>
<span data-ttu-id="0b471-114">Especifica uma lista de ações separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="0b471-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="0b471-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b471-115">-DefaultProfile</span></span>
<span data-ttu-id="0b471-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0b471-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b471-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0b471-117">-Description</span></span>
<span data-ttu-id="0b471-118">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="0b471-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="0b471-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="0b471-119">-DisableRule</span></span>
<span data-ttu-id="0b471-120">Desabilita a regra.</span><span class="sxs-lookup"><span data-stu-id="0b471-120">Disables the rule.</span></span>
<span data-ttu-id="0b471-121">Se você não especificar esse parâmetro, a regra estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="0b471-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="0b471-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="0b471-122">-FailedLocationCount</span></span>
<span data-ttu-id="0b471-123">Especifica a contagem de locais com falha para as regras WebTest.</span><span class="sxs-lookup"><span data-stu-id="0b471-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="0b471-124">Isso é semelhante ao limiar nos outros tipos de regras.</span><span class="sxs-lookup"><span data-stu-id="0b471-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="0b471-125">-Local</span><span class="sxs-lookup"><span data-stu-id="0b471-125">-Location</span></span>
<span data-ttu-id="0b471-126">Especifica o local onde a regra é definida.</span><span class="sxs-lookup"><span data-stu-id="0b471-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="0b471-127">-Metricname</span><span class="sxs-lookup"><span data-stu-id="0b471-127">-MetricName</span></span>
<span data-ttu-id="0b471-128">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="0b471-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="0b471-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="0b471-129">-MetricNamespace</span></span>
<span data-ttu-id="0b471-130">Especifica o namespace de métrica para a regra.</span><span class="sxs-lookup"><span data-stu-id="0b471-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="0b471-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b471-131">-Name</span></span>
<span data-ttu-id="0b471-132">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="0b471-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="0b471-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b471-133">-ResourceGroupName</span></span>
<span data-ttu-id="0b471-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b471-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b471-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="0b471-135">-TargetResourceUri</span></span>
<span data-ttu-id="0b471-136">Especifica a ID do recurso do WebTest.</span><span class="sxs-lookup"><span data-stu-id="0b471-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="0b471-137">-WindowS</span><span class="sxs-lookup"><span data-stu-id="0b471-137">-WindowSize</span></span>
<span data-ttu-id="0b471-138">Especifica o tamanho da janela de tempo para a regra calcular seus dados.</span><span class="sxs-lookup"><span data-stu-id="0b471-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="0b471-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b471-139">-Confirm</span></span>
<span data-ttu-id="0b471-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b471-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b471-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b471-141">-WhatIf</span></span>
<span data-ttu-id="0b471-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b471-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b471-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b471-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b471-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b471-144">CommonParameters</span></span>
<span data-ttu-id="0b471-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b471-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b471-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b471-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b471-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b471-147">INPUTS</span></span>

### <span data-ttu-id="0b471-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0b471-148">System.String</span></span>

### <span data-ttu-id="0b471-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="0b471-149">System.TimeSpan</span></span>

### <span data-ttu-id="0b471-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0b471-150">System.Int32</span></span>

### <span data-ttu-id="0b471-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0b471-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0b471-152">System. Collections. Generic. List ' 1 [Microsoft. Azure. Management. monitor. Management. Models. RuleAction, Microsoft. Azure. PowerShell. cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0b471-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0b471-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b471-153">OUTPUTS</span></span>

### <span data-ttu-id="0b471-154">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b471-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="0b471-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b471-155">NOTES</span></span>

## <span data-ttu-id="0b471-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b471-156">RELATED LINKS</span></span>

[<span data-ttu-id="0b471-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0b471-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="0b471-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0b471-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="0b471-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="0b471-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="0b471-160">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="0b471-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


