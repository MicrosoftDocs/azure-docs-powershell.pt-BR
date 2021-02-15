---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117542"
---
# <span data-ttu-id="0ab48-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0ab48-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="0ab48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0ab48-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab48-103">Adiciona ou atualiza uma regra de alerta de teste da Web.</span><span class="sxs-lookup"><span data-stu-id="0ab48-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="0ab48-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ab48-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab48-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ab48-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab48-106">O cmdlet **Add-AzWebtestAlertRule** adiciona ou atualiza uma regra de alerta do tipo métrica, evento ou teste da Web.</span><span class="sxs-lookup"><span data-stu-id="0ab48-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="0ab48-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="0ab48-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="0ab48-108">Esse cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.</span><span class="sxs-lookup"><span data-stu-id="0ab48-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0ab48-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0ab48-109">EXAMPLES</span></span>

### <span data-ttu-id="0ab48-110">Exemplo 1: Adicionar uma regra de alerta de teste na Web</span><span class="sxs-lookup"><span data-stu-id="0ab48-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="0ab48-111">Esse comando adiciona ou atualiza uma regra de alerta de teste da Web.</span><span class="sxs-lookup"><span data-stu-id="0ab48-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="0ab48-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ab48-112">PARAMETERS</span></span>

### <span data-ttu-id="0ab48-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="0ab48-113">-Action</span></span>
<span data-ttu-id="0ab48-114">Especifica uma lista de ações separada por vírgula.</span><span class="sxs-lookup"><span data-stu-id="0ab48-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="0ab48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab48-115">-DefaultProfile</span></span>
<span data-ttu-id="0ab48-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0ab48-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ab48-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="0ab48-117">-Description</span></span>
<span data-ttu-id="0ab48-118">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="0ab48-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="0ab48-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="0ab48-119">-DisableRule</span></span>
<span data-ttu-id="0ab48-120">Desabilita a regra.</span><span class="sxs-lookup"><span data-stu-id="0ab48-120">Disables the rule.</span></span>
<span data-ttu-id="0ab48-121">Se você não especificar esse parâmetro, a regra será habilitada.</span><span class="sxs-lookup"><span data-stu-id="0ab48-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="0ab48-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="0ab48-122">-FailedLocationCount</span></span>
<span data-ttu-id="0ab48-123">Especifica a contagem de locais com falha para as regras de teste da Web.</span><span class="sxs-lookup"><span data-stu-id="0ab48-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="0ab48-124">Isso é semelhante ao limite nos outros tipos de regras.</span><span class="sxs-lookup"><span data-stu-id="0ab48-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="0ab48-125">-Local</span><span class="sxs-lookup"><span data-stu-id="0ab48-125">-Location</span></span>
<span data-ttu-id="0ab48-126">Especifica o local onde a regra é definida.</span><span class="sxs-lookup"><span data-stu-id="0ab48-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="0ab48-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="0ab48-127">-MetricName</span></span>
<span data-ttu-id="0ab48-128">Especifica o nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="0ab48-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="0ab48-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="0ab48-129">-MetricNamespace</span></span>
<span data-ttu-id="0ab48-130">Especifica o namespace métrico da regra.</span><span class="sxs-lookup"><span data-stu-id="0ab48-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="0ab48-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ab48-131">-Name</span></span>
<span data-ttu-id="0ab48-132">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="0ab48-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="0ab48-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ab48-133">-ResourceGroupName</span></span>
<span data-ttu-id="0ab48-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0ab48-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0ab48-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="0ab48-135">-TargetResourceUri</span></span>
<span data-ttu-id="0ab48-136">Especifica a ID de recurso do teste da Web.</span><span class="sxs-lookup"><span data-stu-id="0ab48-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="0ab48-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="0ab48-137">-WindowSize</span></span>
<span data-ttu-id="0ab48-138">Especifica o tamanho da janela de tempo para que a regra calcule seus dados.</span><span class="sxs-lookup"><span data-stu-id="0ab48-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="0ab48-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0ab48-139">-Confirm</span></span>
<span data-ttu-id="0ab48-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ab48-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ab48-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab48-141">-WhatIf</span></span>
<span data-ttu-id="0ab48-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0ab48-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ab48-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0ab48-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ab48-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab48-144">CommonParameters</span></span>
<span data-ttu-id="0ab48-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab48-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab48-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ab48-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab48-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="0ab48-147">INPUTS</span></span>

### <span data-ttu-id="0ab48-148">System.String</span><span class="sxs-lookup"><span data-stu-id="0ab48-148">System.String</span></span>

### <span data-ttu-id="0ab48-149">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="0ab48-149">System.TimeSpan</span></span>

### <span data-ttu-id="0ab48-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0ab48-150">System.Int32</span></span>

### <span data-ttu-id="0ab48-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0ab48-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0ab48-152">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0ab48-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0ab48-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="0ab48-153">OUTPUTS</span></span>

### <span data-ttu-id="0ab48-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0ab48-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="0ab48-155">Notas</span><span class="sxs-lookup"><span data-stu-id="0ab48-155">NOTES</span></span>

## <span data-ttu-id="0ab48-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ab48-156">RELATED LINKS</span></span>

[<span data-ttu-id="0ab48-157">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0ab48-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="0ab48-158">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0ab48-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="0ab48-159">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="0ab48-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="0ab48-160">New-AzAlertRuleWebweb</span><span class="sxs-lookup"><span data-stu-id="0ab48-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


