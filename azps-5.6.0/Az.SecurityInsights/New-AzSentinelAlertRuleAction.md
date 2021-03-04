---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: ed4d1b5d833ce73a9b0a19e38a05192d11a0d8f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888431"
---
# <span data-ttu-id="b154e-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="b154e-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="b154e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b154e-102">SYNOPSIS</span></span>
<span data-ttu-id="b154e-103">Adicione uma Resposta Automatizada a um Analatic.</span><span class="sxs-lookup"><span data-stu-id="b154e-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="b154e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b154e-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b154e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b154e-105">DESCRIPTION</span></span>
<span data-ttu-id="b154e-106">O cmdlet **New-AzSentinelAlertRuleAction** cria uma Resposta Automatizada para uma Regra de Alerta no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="b154e-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="b154e-107">Você deve fornecer o Logic App Resorce Id e o Uri de Gatilho que podem ser encontrados usando o módulo Aplicativo Lógico.</span><span class="sxs-lookup"><span data-stu-id="b154e-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="b154e-108">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="b154e-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="b154e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b154e-109">EXAMPLES</span></span>

### <span data-ttu-id="b154e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b154e-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="b154e-111">Este exemplo cria um **AlertRuleAction** para a Regra de Alerta especificada usando propriedades do Aplicativo Lógico e a armazena na variável $AlertRuleAction.</span><span class="sxs-lookup"><span data-stu-id="b154e-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="b154e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b154e-112">PARAMETERS</span></span>

### <span data-ttu-id="b154e-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="b154e-113">-ActionId</span></span>
<span data-ttu-id="b154e-114">Id de ação.</span><span class="sxs-lookup"><span data-stu-id="b154e-114">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154e-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="b154e-115">-AlertRuleId</span></span>
<span data-ttu-id="b154e-116">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="b154e-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b154e-117">-DefaultProfile</span></span>
<span data-ttu-id="b154e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b154e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b154e-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="b154e-119">-LogicAppResourceId</span></span>
<span data-ttu-id="b154e-120">ID do Recurso do Aplicativo Lógica de Ação.</span><span class="sxs-lookup"><span data-stu-id="b154e-120">Action Logic App Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b154e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b154e-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b154e-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154e-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="b154e-123">-TriggerUri</span></span>
<span data-ttu-id="b154e-124">Action Logic App Trigger Uri.</span><span class="sxs-lookup"><span data-stu-id="b154e-124">Action Logic App Trigger Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154e-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b154e-125">-WorkspaceName</span></span>
<span data-ttu-id="b154e-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b154e-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b154e-127">-Confirm</span></span>
<span data-ttu-id="b154e-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b154e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b154e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b154e-129">-WhatIf</span></span>
<span data-ttu-id="b154e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b154e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b154e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b154e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b154e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b154e-132">CommonParameters</span></span>
<span data-ttu-id="b154e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b154e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b154e-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b154e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b154e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b154e-135">INPUTS</span></span>

### <span data-ttu-id="b154e-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b154e-136">None</span></span>
## <span data-ttu-id="b154e-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b154e-137">OUTPUTS</span></span>

### <span data-ttu-id="b154e-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="b154e-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="b154e-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="b154e-139">NOTES</span></span>

## <span data-ttu-id="b154e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b154e-140">RELATED LINKS</span></span>
