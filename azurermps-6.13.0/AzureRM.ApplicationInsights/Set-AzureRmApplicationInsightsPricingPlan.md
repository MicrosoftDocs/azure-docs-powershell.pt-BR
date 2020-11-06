---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 03c1a556f6b3fc207fbbb612f31d172705e4f42b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428626"
---
# <span data-ttu-id="4d910-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="4d910-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="4d910-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d910-102">SYNOPSIS</span></span>
<span data-ttu-id="4d910-103">Definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="4d910-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d910-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d910-104">SYNTAX</span></span>

### <span data-ttu-id="4d910-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4d910-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d910-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d910-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d910-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d910-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d910-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d910-108">DESCRIPTION</span></span>
<span data-ttu-id="4d910-109">Definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="4d910-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="4d910-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d910-110">EXAMPLES</span></span>

### <span data-ttu-id="4d910-111">Exemplo 1 definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="4d910-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="4d910-112">Defina o plano de preços como "básico", defina o limite de volume de dados diários para 400 GB por dia e pare enviar notificação quando a tampa do recurso for "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="4d910-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="4d910-113">OS</span><span class="sxs-lookup"><span data-stu-id="4d910-113">PARAMETERS</span></span>

### <span data-ttu-id="4d910-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4d910-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4d910-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="4d910-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4d910-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="4d910-116">-DailyCapGB</span></span>
<span data-ttu-id="4d910-117">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="4d910-117">Daily Cap.</span></span>

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

### <span data-ttu-id="4d910-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d910-118">-DefaultProfile</span></span>
<span data-ttu-id="4d910-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d910-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d910-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="4d910-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="4d910-121">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="4d910-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="4d910-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d910-122">-Name</span></span>
<span data-ttu-id="4d910-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="4d910-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="4d910-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="4d910-124">-PricingPlan</span></span>
<span data-ttu-id="4d910-125">Nome do plano de preços.</span><span class="sxs-lookup"><span data-stu-id="4d910-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="4d910-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d910-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d910-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d910-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="4d910-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d910-128">-ResourceId</span></span>
<span data-ttu-id="4d910-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="4d910-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4d910-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d910-130">-Confirm</span></span>
<span data-ttu-id="4d910-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d910-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d910-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d910-132">-WhatIf</span></span>
<span data-ttu-id="4d910-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d910-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d910-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d910-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d910-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d910-135">CommonParameters</span></span>
<span data-ttu-id="4d910-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d910-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d910-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d910-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d910-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d910-138">INPUTS</span></span>

### <span data-ttu-id="4d910-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4d910-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="4d910-140">Parâmetros: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d910-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="4d910-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4d910-141">System.String</span></span>

## <span data-ttu-id="4d910-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d910-142">OUTPUTS</span></span>

### <span data-ttu-id="4d910-143">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="4d910-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="4d910-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d910-144">NOTES</span></span>

## <span data-ttu-id="4d910-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d910-145">RELATED LINKS</span></span>
