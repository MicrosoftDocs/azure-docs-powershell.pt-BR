---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 12e8e4f76f623391e6046f4f8b0bd424e7b9334d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602391"
---
# <span data-ttu-id="0d8d9-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="0d8d9-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="0d8d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8d9-103">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0d8d9-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d8d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d8d9-104">SYNTAX</span></span>

### <span data-ttu-id="0d8d9-105">ComponentNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0d8d9-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d8d9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d8d9-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d8d9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d8d9-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d8d9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d8d9-108">DESCRIPTION</span></span>
<span data-ttu-id="0d8d9-109">Definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0d8d9-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="0d8d9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d8d9-110">EXAMPLES</span></span>

### <span data-ttu-id="0d8d9-111">Exemplo 1 definir o limite de volume de dados diariamente para um recurso do Application insights</span><span class="sxs-lookup"><span data-stu-id="0d8d9-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="0d8d9-112">Definir o limite de volume de dados diários para 400 GB por dia e interromper a notificação de envio quando o recurso de "teste" do recurso for definido no grupo de recursos "grupo de teste"</span><span class="sxs-lookup"><span data-stu-id="0d8d9-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="0d8d9-113">OS</span><span class="sxs-lookup"><span data-stu-id="0d8d9-113">PARAMETERS</span></span>

### <span data-ttu-id="0d8d9-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0d8d9-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0d8d9-115">Objeto de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0d8d9-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0d8d9-116">-Confirm</span></span>
<span data-ttu-id="0d8d9-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d8d9-118">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="0d8d9-118">-DailyCapGB</span></span>
<span data-ttu-id="0d8d9-119">O limite diário.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-119">Daily Cap.</span></span>

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

### <span data-ttu-id="0d8d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8d9-120">-DefaultProfile</span></span>
<span data-ttu-id="0d8d9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d8d9-122">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="0d8d9-122">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="0d8d9-123">Parar enviar notificação quando a tampa da tecla.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-123">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="0d8d9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d8d9-124">-Name</span></span>
<span data-ttu-id="0d8d9-125">Nome do componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-125">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="0d8d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d8d9-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="0d8d9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d8d9-128">-ResourceId</span></span>
<span data-ttu-id="0d8d9-129">ID do recurso de componente do Application insights.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0d8d9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8d9-130">-WhatIf</span></span>
<span data-ttu-id="0d8d9-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d8d9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d8d9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8d9-133">CommonParameters</span></span>
<span data-ttu-id="0d8d9-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8d9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8d9-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d8d9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8d9-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d8d9-136">INPUTS</span></span>

### <span data-ttu-id="0d8d9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0d8d9-137">System.String</span></span>
<span data-ttu-id="0d8d9-138">System. Double System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d8d9-138">System.Double System.Boolean</span></span>

## <span data-ttu-id="0d8d9-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d8d9-139">OUTPUTS</span></span>

### <span data-ttu-id="0d8d9-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSPricingTier</span><span class="sxs-lookup"><span data-stu-id="0d8d9-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingTier</span></span>

## <span data-ttu-id="0d8d9-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d8d9-141">NOTES</span></span>

## <span data-ttu-id="0d8d9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d8d9-142">RELATED LINKS</span></span>

