---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117027"
---
# <span data-ttu-id="27984-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="27984-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="27984-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27984-102">SYNOPSIS</span></span>
<span data-ttu-id="27984-103">Definir o limite de volume de dados diários para um recurso de informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="27984-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="27984-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27984-104">SYNTAX</span></span>

### <span data-ttu-id="27984-105">ComponentNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="27984-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27984-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27984-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27984-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27984-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27984-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="27984-108">DESCRIPTION</span></span>
<span data-ttu-id="27984-109">Definir o limite de volume de dados diários para um recurso de informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="27984-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="27984-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="27984-110">EXAMPLES</span></span>

### <span data-ttu-id="27984-111">Exemplo 1 Definir o limite de volume de dados diários para um recurso de informações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="27984-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="27984-112">Definir o limite de volume de dados diários como 400 GB por dia e interromper o envio de notificação quando atingir o limite para o recurso "teste" no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="27984-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="27984-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27984-113">PARAMETERS</span></span>

### <span data-ttu-id="27984-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="27984-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="27984-115">Objeto componente Do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27984-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="27984-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="27984-116">-DailyCapGB</span></span>
<span data-ttu-id="27984-117">Limite diário.</span><span class="sxs-lookup"><span data-stu-id="27984-117">Daily Cap.</span></span>

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

### <span data-ttu-id="27984-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27984-118">-DefaultProfile</span></span>
<span data-ttu-id="27984-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="27984-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27984-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="27984-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="27984-121">Interromper o envio de notificação quando atingir o limite.</span><span class="sxs-lookup"><span data-stu-id="27984-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="27984-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="27984-122">-Name</span></span>
<span data-ttu-id="27984-123">Nome do componente Informações do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27984-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="27984-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27984-124">-ResourceGroupName</span></span>
<span data-ttu-id="27984-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27984-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="27984-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27984-126">-ResourceId</span></span>
<span data-ttu-id="27984-127">ID do Recurso de Componentes do Insights do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27984-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="27984-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="27984-128">-Confirm</span></span>
<span data-ttu-id="27984-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27984-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27984-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27984-130">-WhatIf</span></span>
<span data-ttu-id="27984-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="27984-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27984-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27984-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27984-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27984-133">CommonParameters</span></span>
<span data-ttu-id="27984-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27984-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27984-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27984-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27984-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="27984-136">INPUTS</span></span>

### <span data-ttu-id="27984-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="27984-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="27984-138">System.String</span><span class="sxs-lookup"><span data-stu-id="27984-138">System.String</span></span>

## <span data-ttu-id="27984-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="27984-139">OUTPUTS</span></span>

### <span data-ttu-id="27984-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="27984-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="27984-141">Notas</span><span class="sxs-lookup"><span data-stu-id="27984-141">NOTES</span></span>

## <span data-ttu-id="27984-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27984-142">RELATED LINKS</span></span>
