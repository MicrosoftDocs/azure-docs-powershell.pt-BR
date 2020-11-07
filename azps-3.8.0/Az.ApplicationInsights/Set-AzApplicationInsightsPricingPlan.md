---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942743"
---
# <span data-ttu-id="41b19-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="41b19-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="41b19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41b19-102">SYNOPSIS</span></span>
<span data-ttu-id="41b19-103">Definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="41b19-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="41b19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41b19-104">SYNTAX</span></span>

### <span data-ttu-id="41b19-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="41b19-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b19-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41b19-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b19-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41b19-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41b19-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41b19-108">DESCRIPTION</span></span>
<span data-ttu-id="41b19-109">Definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="41b19-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="41b19-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41b19-110">EXAMPLES</span></span>

### <span data-ttu-id="41b19-111">Exemplo 1 definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="41b19-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="41b19-112">Defina o plano de preços como "básico", defina a Cap do volume de dados diariamente como 400 GB por dia e pare enviar notificação quando a tampa do recurso for "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="41b19-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="41b19-113">OS</span><span class="sxs-lookup"><span data-stu-id="41b19-113">PARAMETERS</span></span>

### <span data-ttu-id="41b19-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="41b19-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="41b19-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="41b19-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="41b19-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="41b19-116">-DailyCapGB</span></span>
<span data-ttu-id="41b19-117">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="41b19-117">Daily Cap.</span></span>

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

### <span data-ttu-id="41b19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b19-118">-DefaultProfile</span></span>
<span data-ttu-id="41b19-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41b19-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b19-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="41b19-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="41b19-121">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="41b19-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="41b19-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="41b19-122">-Name</span></span>
<span data-ttu-id="41b19-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="41b19-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="41b19-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="41b19-124">-PricingPlan</span></span>
<span data-ttu-id="41b19-125">Nome do plano de preços.</span><span class="sxs-lookup"><span data-stu-id="41b19-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="41b19-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b19-126">-ResourceGroupName</span></span>
<span data-ttu-id="41b19-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41b19-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="41b19-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41b19-128">-ResourceId</span></span>
<span data-ttu-id="41b19-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="41b19-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="41b19-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41b19-130">-Confirm</span></span>
<span data-ttu-id="41b19-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41b19-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b19-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b19-132">-WhatIf</span></span>
<span data-ttu-id="41b19-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41b19-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41b19-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41b19-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b19-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b19-135">CommonParameters</span></span>
<span data-ttu-id="41b19-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b19-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b19-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b19-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b19-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41b19-138">INPUTS</span></span>

### <span data-ttu-id="41b19-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="41b19-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="41b19-140">System. String</span><span class="sxs-lookup"><span data-stu-id="41b19-140">System.String</span></span>

## <span data-ttu-id="41b19-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41b19-141">OUTPUTS</span></span>

### <span data-ttu-id="41b19-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="41b19-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="41b19-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41b19-143">NOTES</span></span>

## <span data-ttu-id="41b19-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41b19-144">RELATED LINKS</span></span>
