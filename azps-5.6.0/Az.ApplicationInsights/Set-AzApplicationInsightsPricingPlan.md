---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 7f730a59b740b061406f2ba14ccf76fe660aea14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889585"
---
# <span data-ttu-id="a8567-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="a8567-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="a8567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8567-102">SYNOPSIS</span></span>
<span data-ttu-id="a8567-103">Definir o plano de preços e as informações de volume de dados diários para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a8567-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="a8567-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a8567-104">SYNTAX</span></span>

### <span data-ttu-id="a8567-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a8567-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8567-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8567-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8567-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8567-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8567-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a8567-108">DESCRIPTION</span></span>
<span data-ttu-id="a8567-109">Definir o plano de preços e as informações de volume de dados diários para um recurso de insights de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a8567-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="a8567-110">O plano de preços das percepções do aplicativo criado após abril de 2018 não pode ser definido por este cmdlet: https://docs.microsoft.com/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="a8567-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="a8567-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8567-111">EXAMPLES</span></span>

### <span data-ttu-id="a8567-112">Exemplo 1 Definir o plano de preços e informações de volume de dados diários para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a8567-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="a8567-113">Definir o plano de preços como "Básico", definir o limite de volume de dados diário como 400 GB por dia e interromper a notificação de envio quando o limite de acerto do recurso "testar" no grupo de recursos "testgroup"</span><span class="sxs-lookup"><span data-stu-id="a8567-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="a8567-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a8567-114">PARAMETERS</span></span>

### <span data-ttu-id="a8567-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a8567-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="a8567-116">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="a8567-116">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8567-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="a8567-117">-DailyCapGB</span></span>
<span data-ttu-id="a8567-118">Daily Cap.</span><span class="sxs-lookup"><span data-stu-id="a8567-118">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8567-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8567-119">-DefaultProfile</span></span>
<span data-ttu-id="a8567-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a8567-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8567-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="a8567-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="a8567-122">Pare a notificação de envio ao atingir o limite.</span><span class="sxs-lookup"><span data-stu-id="a8567-122">Stop send notification when hit cap.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8567-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a8567-123">-Name</span></span>
<span data-ttu-id="a8567-124">Nome do componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a8567-124">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8567-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="a8567-125">-PricingPlan</span></span>
<span data-ttu-id="a8567-126">Nome do plano de preços.</span><span class="sxs-lookup"><span data-stu-id="a8567-126">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8567-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8567-127">-ResourceGroupName</span></span>
<span data-ttu-id="a8567-128">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a8567-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8567-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8567-129">-ResourceId</span></span>
<span data-ttu-id="a8567-130">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a8567-130">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8567-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8567-131">-Confirm</span></span>
<span data-ttu-id="a8567-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8567-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8567-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8567-133">-WhatIf</span></span>
<span data-ttu-id="a8567-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8567-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8567-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8567-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8567-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8567-136">CommonParameters</span></span>
<span data-ttu-id="a8567-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8567-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8567-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8567-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8567-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8567-139">INPUTS</span></span>

### <span data-ttu-id="a8567-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a8567-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="a8567-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a8567-141">System.String</span></span>

## <span data-ttu-id="a8567-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a8567-142">OUTPUTS</span></span>

### <span data-ttu-id="a8567-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="a8567-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="a8567-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a8567-144">NOTES</span></span>

## <span data-ttu-id="a8567-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8567-145">RELATED LINKS</span></span>
