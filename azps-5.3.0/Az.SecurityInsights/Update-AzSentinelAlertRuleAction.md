---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433184"
---
# <span data-ttu-id="29db7-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="29db7-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="29db7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29db7-102">SYNOPSIS</span></span>
<span data-ttu-id="29db7-103">Atualizar uma resposta automática (ação de regra de alerta).</span><span class="sxs-lookup"><span data-stu-id="29db7-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="29db7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29db7-104">SYNTAX</span></span>

### <span data-ttu-id="29db7-105">ActionID (padrão)</span><span class="sxs-lookup"><span data-stu-id="29db7-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29db7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="29db7-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29db7-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="29db7-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29db7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29db7-108">DESCRIPTION</span></span>
<span data-ttu-id="29db7-109">O cmdlet **Update-AzSentinelAlertRuleAction** atualiza o indicador no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="29db7-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="29db7-110">Você pode passar um objeto **AlertRuleAction** como um parâmetro ou usando o operador pipeline ou, como alternativa, pode especificar os parâmetros *AlertRuleId* e *ActionID* .</span><span class="sxs-lookup"><span data-stu-id="29db7-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="29db7-111">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="29db7-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="29db7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29db7-112">EXAMPLES</span></span>

### <span data-ttu-id="29db7-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29db7-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="29db7-114">Este exemplo atualiza um **AlertRuleAction** que substitui uma *ação* existente por novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="29db7-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="29db7-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29db7-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="29db7-116">Este exemplo atualiza um **AlertRuleAction** usando um InputObject substituindo uma *ação* existente por novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="29db7-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="29db7-117">OS</span><span class="sxs-lookup"><span data-stu-id="29db7-117">PARAMETERS</span></span>

### <span data-ttu-id="29db7-118">-ActionID</span><span class="sxs-lookup"><span data-stu-id="29db7-118">-ActionId</span></span>
<span data-ttu-id="29db7-119">ID da ação.</span><span class="sxs-lookup"><span data-stu-id="29db7-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29db7-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="29db7-120">-AlertRuleId</span></span>
<span data-ttu-id="29db7-121">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="29db7-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29db7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29db7-122">-DefaultProfile</span></span>
<span data-ttu-id="29db7-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29db7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29db7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29db7-124">-InputObject</span></span>
<span data-ttu-id="29db7-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="29db7-125">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29db7-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="29db7-126">-LogicAppResourceId</span></span>
<span data-ttu-id="29db7-127">ID do recurso de aplicativo lógica da ação.</span><span class="sxs-lookup"><span data-stu-id="29db7-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="29db7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29db7-128">-ResourceGroupName</span></span>
<span data-ttu-id="29db7-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29db7-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29db7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29db7-130">-ResourceId</span></span>
<span data-ttu-id="29db7-131">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="29db7-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29db7-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="29db7-132">-TriggerUri</span></span>
<span data-ttu-id="29db7-133">URI de gatilho do aplicativo lógica da ação.</span><span class="sxs-lookup"><span data-stu-id="29db7-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="29db7-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="29db7-134">-WorkspaceName</span></span>
<span data-ttu-id="29db7-135">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="29db7-135">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29db7-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29db7-136">-Confirm</span></span>
<span data-ttu-id="29db7-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29db7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29db7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29db7-138">-WhatIf</span></span>
<span data-ttu-id="29db7-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29db7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29db7-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29db7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29db7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29db7-141">CommonParameters</span></span>
<span data-ttu-id="29db7-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29db7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29db7-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29db7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29db7-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29db7-144">INPUTS</span></span>

### <span data-ttu-id="29db7-145">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="29db7-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="29db7-146">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="29db7-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="29db7-147">System. String</span><span class="sxs-lookup"><span data-stu-id="29db7-147">System.String</span></span>

## <span data-ttu-id="29db7-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29db7-148">OUTPUTS</span></span>

### <span data-ttu-id="29db7-149">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="29db7-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="29db7-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29db7-150">NOTES</span></span>

## <span data-ttu-id="29db7-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29db7-151">RELATED LINKS</span></span>
