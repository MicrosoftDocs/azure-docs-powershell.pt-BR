---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: ce4c9d8fd297b53eb628ffcc32ad9479e0647dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901367"
---
# <span data-ttu-id="576b1-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="576b1-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="576b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576b1-102">SYNOPSIS</span></span>
<span data-ttu-id="576b1-103">Definir o limite de volume de dados diários para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="576b1-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="576b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="576b1-104">SYNTAX</span></span>

### <span data-ttu-id="576b1-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="576b1-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="576b1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="576b1-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576b1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="576b1-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="576b1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="576b1-108">DESCRIPTION</span></span>
<span data-ttu-id="576b1-109">Definir o limite de volume de dados diários para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="576b1-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="576b1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="576b1-110">EXAMPLES</span></span>

### <span data-ttu-id="576b1-111">Exemplo 1 Definir o limite de volume de dados diário para um recurso de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="576b1-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="576b1-112">Definir o limite de volume de dados diário como 400 GB por dia e interromper a notificação de envio quando o limite de acerto para o recurso "test" no grupo de recursos "testgroup"</span><span class="sxs-lookup"><span data-stu-id="576b1-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="576b1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="576b1-113">PARAMETERS</span></span>

### <span data-ttu-id="576b1-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="576b1-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="576b1-115">Objeto Application Insights Component.</span><span class="sxs-lookup"><span data-stu-id="576b1-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="576b1-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="576b1-116">-DailyCapGB</span></span>
<span data-ttu-id="576b1-117">Daily Cap.</span><span class="sxs-lookup"><span data-stu-id="576b1-117">Daily Cap.</span></span>

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

### <span data-ttu-id="576b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576b1-118">-DefaultProfile</span></span>
<span data-ttu-id="576b1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="576b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="576b1-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="576b1-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="576b1-121">Pare a notificação de envio ao atingir o limite.</span><span class="sxs-lookup"><span data-stu-id="576b1-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="576b1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="576b1-122">-Name</span></span>
<span data-ttu-id="576b1-123">Nome do componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="576b1-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="576b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="576b1-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="576b1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="576b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="576b1-126">-ResourceId</span></span>
<span data-ttu-id="576b1-127">ID do Recurso de Componente do Application Insights.</span><span class="sxs-lookup"><span data-stu-id="576b1-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="576b1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="576b1-128">-Confirm</span></span>
<span data-ttu-id="576b1-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="576b1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576b1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576b1-130">-WhatIf</span></span>
<span data-ttu-id="576b1-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="576b1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="576b1-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="576b1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576b1-133">CommonParameters</span></span>
<span data-ttu-id="576b1-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576b1-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="576b1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576b1-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="576b1-136">INPUTS</span></span>

### <span data-ttu-id="576b1-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="576b1-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="576b1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="576b1-138">System.String</span></span>

## <span data-ttu-id="576b1-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="576b1-139">OUTPUTS</span></span>

### <span data-ttu-id="576b1-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="576b1-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="576b1-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="576b1-141">NOTES</span></span>

## <span data-ttu-id="576b1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="576b1-142">RELATED LINKS</span></span>
