---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: 0283bfcc0c3eecf3ca7f97a8f5bb2b8813c4ae78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597888"
---
# <span data-ttu-id="dcbaa-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="dcbaa-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="dcbaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbaa-103">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="dcbaa-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="dcbaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcbaa-104">SYNTAX</span></span>

### <span data-ttu-id="dcbaa-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dcbaa-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcbaa-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcbaa-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcbaa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcbaa-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcbaa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcbaa-108">DESCRIPTION</span></span>
<span data-ttu-id="dcbaa-109">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="dcbaa-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="dcbaa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcbaa-110">EXAMPLES</span></span>

### <span data-ttu-id="dcbaa-111">Exemplo 1 definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="dcbaa-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="dcbaa-112">Definir a porcentagem de volume de dados diariamente para 400 GB por dia e interromper a notificação de envio quando o recurso de "teste" do recurso estiver no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="dcbaa-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="dcbaa-113">OS</span><span class="sxs-lookup"><span data-stu-id="dcbaa-113">PARAMETERS</span></span>

### <span data-ttu-id="dcbaa-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="dcbaa-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="dcbaa-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="dcbaa-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="dcbaa-116">-DailyCapGB</span></span>
<span data-ttu-id="dcbaa-117">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-117">Daily Cap.</span></span>

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

### <span data-ttu-id="dcbaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbaa-118">-DefaultProfile</span></span>
<span data-ttu-id="dcbaa-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcbaa-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="dcbaa-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="dcbaa-121">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="dcbaa-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcbaa-122">-Name</span></span>
<span data-ttu-id="dcbaa-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="dcbaa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbaa-124">-ResourceGroupName</span></span>
<span data-ttu-id="dcbaa-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="dcbaa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcbaa-126">-ResourceId</span></span>
<span data-ttu-id="dcbaa-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="dcbaa-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dcbaa-128">-Confirm</span></span>
<span data-ttu-id="dcbaa-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcbaa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcbaa-130">-WhatIf</span></span>
<span data-ttu-id="dcbaa-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcbaa-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcbaa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbaa-133">CommonParameters</span></span>
<span data-ttu-id="dcbaa-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcbaa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbaa-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcbaa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbaa-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcbaa-136">INPUTS</span></span>

### <span data-ttu-id="dcbaa-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="dcbaa-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="dcbaa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dcbaa-138">System.String</span></span>

## <span data-ttu-id="dcbaa-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcbaa-139">OUTPUTS</span></span>

### <span data-ttu-id="dcbaa-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="dcbaa-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="dcbaa-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcbaa-141">NOTES</span></span>

## <span data-ttu-id="dcbaa-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcbaa-142">RELATED LINKS</span></span>
