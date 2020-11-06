---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 4785abb883c262273d8d3b0798067e76092511fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439901"
---
# <span data-ttu-id="7653d-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="7653d-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="7653d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7653d-102">SYNOPSIS</span></span>
<span data-ttu-id="7653d-103">Definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="7653d-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7653d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7653d-104">SYNTAX</span></span>

### <span data-ttu-id="7653d-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7653d-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7653d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7653d-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7653d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7653d-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7653d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7653d-108">DESCRIPTION</span></span>
<span data-ttu-id="7653d-109">Definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="7653d-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="7653d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7653d-110">EXAMPLES</span></span>

### <span data-ttu-id="7653d-111">Exemplo 1 definir o plano de preços e as informações de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="7653d-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="7653d-112">Defina o plano de preços como "básico", defina o limite de volume de dados diários para 400 GB por dia e pare enviar notificação quando a tampa do recurso for "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="7653d-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7653d-113">OS</span><span class="sxs-lookup"><span data-stu-id="7653d-113">PARAMETERS</span></span>

### <span data-ttu-id="7653d-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7653d-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7653d-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="7653d-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7653d-116">-Confirm</span></span>
<span data-ttu-id="7653d-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7653d-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="7653d-118">-DailyCapGB</span></span>
<span data-ttu-id="7653d-119">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="7653d-119">Daily Cap.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7653d-120">-DefaultProfile</span></span>
<span data-ttu-id="7653d-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7653d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7653d-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="7653d-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="7653d-123">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="7653d-123">Stop send notification when hit cap.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7653d-124">-Name</span></span>
<span data-ttu-id="7653d-125">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="7653d-125">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-126">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="7653d-126">-PricingPlan</span></span>
<span data-ttu-id="7653d-127">Nome do plano de preços.</span><span class="sxs-lookup"><span data-stu-id="7653d-127">Pricing plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7653d-128">-ResourceGroupName</span></span>
<span data-ttu-id="7653d-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7653d-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7653d-130">-ResourceId</span></span>
<span data-ttu-id="7653d-131">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="7653d-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7653d-132">-WhatIf</span></span>
<span data-ttu-id="7653d-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7653d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7653d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7653d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7653d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7653d-135">CommonParameters</span></span>
<span data-ttu-id="7653d-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7653d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7653d-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7653d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7653d-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7653d-138">INPUTS</span></span>

### <span data-ttu-id="7653d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7653d-139">System.String</span></span>
<span data-ttu-id="7653d-140">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7653d-140">System.Double System.Boolean</span></span>

## <span data-ttu-id="7653d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7653d-141">OUTPUTS</span></span>

### <span data-ttu-id="7653d-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="7653d-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="7653d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7653d-143">NOTES</span></span>

## <span data-ttu-id="7653d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7653d-144">RELATED LINKS</span></span>

