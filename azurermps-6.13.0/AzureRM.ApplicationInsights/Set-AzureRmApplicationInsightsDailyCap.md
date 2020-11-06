---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 7b47576c0fd506831d8e48201d39bd66fec72032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428628"
---
# <span data-ttu-id="c4f98-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="c4f98-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="c4f98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4f98-102">SYNOPSIS</span></span>
<span data-ttu-id="c4f98-103">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="c4f98-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4f98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4f98-104">SYNTAX</span></span>

### <span data-ttu-id="c4f98-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4f98-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4f98-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4f98-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4f98-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4f98-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4f98-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4f98-108">DESCRIPTION</span></span>
<span data-ttu-id="c4f98-109">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="c4f98-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="c4f98-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4f98-110">EXAMPLES</span></span>

### <span data-ttu-id="c4f98-111">Exemplo 1 definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="c4f98-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="c4f98-112">Definir o limite de volume de dados diários para 400 GB por dia e interromper a notificação de envio quando o recurso de "teste" do recurso for definido no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="c4f98-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="c4f98-113">OS</span><span class="sxs-lookup"><span data-stu-id="c4f98-113">PARAMETERS</span></span>

### <span data-ttu-id="c4f98-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c4f98-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c4f98-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="c4f98-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c4f98-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="c4f98-116">-DailyCapGB</span></span>
<span data-ttu-id="c4f98-117">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="c4f98-117">Daily Cap.</span></span>

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

### <span data-ttu-id="c4f98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4f98-118">-DefaultProfile</span></span>
<span data-ttu-id="c4f98-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4f98-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4f98-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="c4f98-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="c4f98-121">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="c4f98-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="c4f98-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4f98-122">-Name</span></span>
<span data-ttu-id="c4f98-123">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="c4f98-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c4f98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4f98-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4f98-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c4f98-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4f98-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4f98-126">-ResourceId</span></span>
<span data-ttu-id="c4f98-127">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="c4f98-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c4f98-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4f98-128">-Confirm</span></span>
<span data-ttu-id="c4f98-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4f98-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4f98-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4f98-130">-WhatIf</span></span>
<span data-ttu-id="c4f98-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4f98-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4f98-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4f98-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4f98-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4f98-133">CommonParameters</span></span>
<span data-ttu-id="c4f98-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4f98-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4f98-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4f98-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4f98-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4f98-136">INPUTS</span></span>

### <span data-ttu-id="c4f98-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c4f98-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="c4f98-138">Parâmetros: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4f98-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="c4f98-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4f98-139">System.String</span></span>

## <span data-ttu-id="c4f98-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4f98-140">OUTPUTS</span></span>

### <span data-ttu-id="c4f98-141">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="c4f98-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="c4f98-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4f98-142">NOTES</span></span>

## <span data-ttu-id="c4f98-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4f98-143">RELATED LINKS</span></span>
