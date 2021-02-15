---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: d9ddfdb43db8e94d0dc65606f6c5f86f05db31d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112278"
---
# <span data-ttu-id="79189-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="79189-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="79189-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79189-102">SYNOPSIS</span></span>
<span data-ttu-id="79189-103">Definir o plano de preços e as informações de volume de dados diários para um recurso de informações de aplicativo</span><span class="sxs-lookup"><span data-stu-id="79189-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="79189-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79189-104">SYNTAX</span></span>

### <span data-ttu-id="79189-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="79189-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79189-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79189-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79189-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79189-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79189-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="79189-108">DESCRIPTION</span></span>
<span data-ttu-id="79189-109">De definir o plano de preços e as informações de volume de dados diários para um recurso de insights de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="79189-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="79189-110">O plano de preços de ideias de aplicativos criado após abril de 2018 não pode ser definido por este cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="79189-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/en-us/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="79189-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="79189-111">EXAMPLES</span></span>

### <span data-ttu-id="79189-112">Exemplo 1 Definir plano de preços e informações de volume de dados diários para um recurso de informações de aplicativo</span><span class="sxs-lookup"><span data-stu-id="79189-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="79189-113">Definir o plano de preços como "Básico", definir o limite de volume de dados diário para 400 GB por dia e interromper o envio de notificação quando atingir o limite do "teste" do recurso no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="79189-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="79189-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79189-114">PARAMETERS</span></span>

### <span data-ttu-id="79189-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="79189-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="79189-116">Objeto componente Do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79189-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="79189-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="79189-117">-DailyCapGB</span></span>
<span data-ttu-id="79189-118">Limite diário.</span><span class="sxs-lookup"><span data-stu-id="79189-118">Daily Cap.</span></span>

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

### <span data-ttu-id="79189-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79189-119">-DefaultProfile</span></span>
<span data-ttu-id="79189-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="79189-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79189-121">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="79189-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="79189-122">Interromper o envio de notificação quando atingir o limite.</span><span class="sxs-lookup"><span data-stu-id="79189-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="79189-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="79189-123">-Name</span></span>
<span data-ttu-id="79189-124">Nome do componente Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79189-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="79189-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="79189-125">-PricingPlan</span></span>
<span data-ttu-id="79189-126">Nome do plano de preços.</span><span class="sxs-lookup"><span data-stu-id="79189-126">Pricing plan name.</span></span>

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

### <span data-ttu-id="79189-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79189-127">-ResourceGroupName</span></span>
<span data-ttu-id="79189-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="79189-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="79189-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79189-129">-ResourceId</span></span>
<span data-ttu-id="79189-130">ID do Recurso de Componentes do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="79189-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="79189-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="79189-131">-Confirm</span></span>
<span data-ttu-id="79189-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79189-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79189-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79189-133">-WhatIf</span></span>
<span data-ttu-id="79189-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="79189-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79189-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79189-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79189-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79189-136">CommonParameters</span></span>
<span data-ttu-id="79189-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79189-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79189-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79189-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79189-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="79189-139">INPUTS</span></span>

### <span data-ttu-id="79189-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="79189-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="79189-141">System.String</span><span class="sxs-lookup"><span data-stu-id="79189-141">System.String</span></span>

## <span data-ttu-id="79189-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="79189-142">OUTPUTS</span></span>

### <span data-ttu-id="79189-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="79189-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="79189-144">Notas</span><span class="sxs-lookup"><span data-stu-id="79189-144">NOTES</span></span>

## <span data-ttu-id="79189-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79189-145">RELATED LINKS</span></span>
