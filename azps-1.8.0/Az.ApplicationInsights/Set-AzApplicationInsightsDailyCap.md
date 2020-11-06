---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: 3f46445bbdf8f3b9e7a25f4ab5bda0fd11961e00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601652"
---
# <span data-ttu-id="4c41d-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="4c41d-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="4c41d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c41d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c41d-103">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="4c41d-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="4c41d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c41d-104">SYNTAX</span></span>

### <span data-ttu-id="4c41d-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c41d-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c41d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c41d-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c41d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c41d-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c41d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c41d-108">DESCRIPTION</span></span>
<span data-ttu-id="4c41d-109">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="4c41d-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="4c41d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c41d-110">EXAMPLES</span></span>

### <span data-ttu-id="4c41d-111">Exemplo 1 definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="4c41d-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="4c41d-112">Definir o limite de volume de dados diários para 400 GB por dia e interromper a notificação de envio quando o recurso de "teste" do recurso for definido no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="4c41d-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="4c41d-113">OS</span><span class="sxs-lookup"><span data-stu-id="4c41d-113">PARAMETERS</span></span>

### <span data-ttu-id="4c41d-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4c41d-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4c41d-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="4c41d-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4c41d-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="4c41d-116">-DailyCapGB</span></span>
<span data-ttu-id="4c41d-117">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="4c41d-117">Daily Cap.</span></span>

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

### <span data-ttu-id="4c41d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c41d-118">-DefaultProfile</span></span>
<span data-ttu-id="4c41d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c41d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c41d-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="4c41d-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="4c41d-121">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="4c41d-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="4c41d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c41d-122">-Name</span></span>
<span data-ttu-id="4c41d-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="4c41d-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="4c41d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c41d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c41d-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c41d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="4c41d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c41d-126">-ResourceId</span></span>
<span data-ttu-id="4c41d-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="4c41d-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4c41d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c41d-128">-Confirm</span></span>
<span data-ttu-id="4c41d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c41d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c41d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c41d-130">-WhatIf</span></span>
<span data-ttu-id="4c41d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c41d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c41d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c41d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c41d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c41d-133">CommonParameters</span></span>
<span data-ttu-id="4c41d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c41d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c41d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c41d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c41d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c41d-136">INPUTS</span></span>

### <span data-ttu-id="4c41d-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4c41d-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="4c41d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4c41d-138">System.String</span></span>

## <span data-ttu-id="4c41d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c41d-139">OUTPUTS</span></span>

### <span data-ttu-id="4c41d-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="4c41d-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="4c41d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c41d-141">NOTES</span></span>

## <span data-ttu-id="4c41d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c41d-142">RELATED LINKS</span></span>
