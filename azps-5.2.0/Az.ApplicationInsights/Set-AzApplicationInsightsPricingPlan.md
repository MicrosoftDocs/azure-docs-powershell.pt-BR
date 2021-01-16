---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261614"
---
# <span data-ttu-id="0718f-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="0718f-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="0718f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0718f-102">SYNOPSIS</span></span>
<span data-ttu-id="0718f-103">Definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0718f-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="0718f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0718f-104">SYNTAX</span></span>

### <span data-ttu-id="0718f-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0718f-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0718f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0718f-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0718f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0718f-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0718f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0718f-108">DESCRIPTION</span></span>
<span data-ttu-id="0718f-109">Defina o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0718f-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="0718f-110">O plano de preços do Application insights criado após o 2018 de abril não pode ser definido por este cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="0718f-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="0718f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0718f-111">EXAMPLES</span></span>

### <span data-ttu-id="0718f-112">Exemplo 1 definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0718f-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="0718f-113">Defina o plano de preços como "básico", defina a Cap do volume de dados diariamente como 400 GB por dia e pare enviar notificação quando a tampa do recurso for "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="0718f-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="0718f-114">OS</span><span class="sxs-lookup"><span data-stu-id="0718f-114">PARAMETERS</span></span>

### <span data-ttu-id="0718f-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0718f-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0718f-116">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0718f-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0718f-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="0718f-117">-DailyCapGB</span></span>
<span data-ttu-id="0718f-118">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="0718f-118">Daily Cap.</span></span>

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

### <span data-ttu-id="0718f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0718f-119">-DefaultProfile</span></span>
<span data-ttu-id="0718f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0718f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0718f-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="0718f-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="0718f-122">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="0718f-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="0718f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0718f-123">-Name</span></span>
<span data-ttu-id="0718f-124">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0718f-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="0718f-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="0718f-125">-PricingPlan</span></span>
<span data-ttu-id="0718f-126">Nome do plano de preços.</span><span class="sxs-lookup"><span data-stu-id="0718f-126">Pricing plan name.</span></span>

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

### <span data-ttu-id="0718f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0718f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0718f-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0718f-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="0718f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0718f-129">-ResourceId</span></span>
<span data-ttu-id="0718f-130">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0718f-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0718f-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0718f-131">-Confirm</span></span>
<span data-ttu-id="0718f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0718f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0718f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0718f-133">-WhatIf</span></span>
<span data-ttu-id="0718f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0718f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0718f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0718f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0718f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0718f-136">CommonParameters</span></span>
<span data-ttu-id="0718f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0718f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0718f-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0718f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0718f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0718f-139">INPUTS</span></span>

### <span data-ttu-id="0718f-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0718f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0718f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0718f-141">System.String</span></span>

## <span data-ttu-id="0718f-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0718f-142">OUTPUTS</span></span>

### <span data-ttu-id="0718f-143">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="0718f-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="0718f-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0718f-144">NOTES</span></span>

## <span data-ttu-id="0718f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0718f-145">RELATED LINKS</span></span>
