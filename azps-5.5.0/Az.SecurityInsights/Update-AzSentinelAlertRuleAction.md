---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113997"
---
# <span data-ttu-id="bb683-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="bb683-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="bb683-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb683-102">SYNOPSIS</span></span>
<span data-ttu-id="bb683-103">Atualizar uma Resposta Automatizada (Ação de Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="bb683-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="bb683-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb683-104">SYNTAX</span></span>

### <span data-ttu-id="bb683-105">ActionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb683-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb683-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb683-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb683-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="bb683-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb683-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb683-108">DESCRIPTION</span></span>
<span data-ttu-id="bb683-109">O cmdlet **Update-AzSentinelAlertRuleAction** atualiza o indicador no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="bb683-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="bb683-110">Você pode passar um objeto **AlertRuleAction** como um parâmetro ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros *AlertRuleId* e *ActionId.*</span><span class="sxs-lookup"><span data-stu-id="bb683-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="bb683-111">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="bb683-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="bb683-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bb683-112">EXAMPLES</span></span>

### <span data-ttu-id="bb683-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb683-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="bb683-114">Este exemplo atualiza uma **Ação AlertRuleAction** substituindo uma *Ação existente* por novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb683-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="bb683-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bb683-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="bb683-116">Este exemplo atualiza uma **AlertRuleAction** usando um InputObject substituindo uma *Ação existente* por novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb683-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="bb683-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb683-117">PARAMETERS</span></span>

### <span data-ttu-id="bb683-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="bb683-118">-ActionId</span></span>
<span data-ttu-id="bb683-119">ID da Ação.</span><span class="sxs-lookup"><span data-stu-id="bb683-119">Action Id.</span></span>

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

### <span data-ttu-id="bb683-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="bb683-120">-AlertRuleId</span></span>
<span data-ttu-id="bb683-121">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="bb683-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="bb683-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb683-122">-DefaultProfile</span></span>
<span data-ttu-id="bb683-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb683-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb683-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb683-124">-InputObject</span></span>
<span data-ttu-id="bb683-125">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="bb683-125">InputObject.</span></span>

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

### <span data-ttu-id="bb683-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="bb683-126">-LogicAppResourceId</span></span>
<span data-ttu-id="bb683-127">ID do Recurso do Aplicativo Lógica de Ação.</span><span class="sxs-lookup"><span data-stu-id="bb683-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="bb683-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb683-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb683-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb683-129">Resource group name.</span></span>

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

### <span data-ttu-id="bb683-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb683-130">-ResourceId</span></span>
<span data-ttu-id="bb683-131">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="bb683-131">Resource Id.</span></span>

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

### <span data-ttu-id="bb683-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="bb683-132">-TriggerUri</span></span>
<span data-ttu-id="bb683-133">Uri de acionador do aplicativo Action Logic.</span><span class="sxs-lookup"><span data-stu-id="bb683-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="bb683-134">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="bb683-134">-WorkspaceName</span></span>
<span data-ttu-id="bb683-135">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb683-135">Workspace Name.</span></span>

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

### <span data-ttu-id="bb683-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bb683-136">-Confirm</span></span>
<span data-ttu-id="bb683-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb683-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb683-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb683-138">-WhatIf</span></span>
<span data-ttu-id="bb683-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bb683-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb683-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb683-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb683-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb683-141">CommonParameters</span></span>
<span data-ttu-id="bb683-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb683-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb683-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb683-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb683-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="bb683-144">INPUTS</span></span>

### <span data-ttu-id="bb683-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="bb683-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="bb683-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="bb683-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="bb683-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bb683-147">System.String</span></span>

## <span data-ttu-id="bb683-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="bb683-148">OUTPUTS</span></span>

### <span data-ttu-id="bb683-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="bb683-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="bb683-150">Notas</span><span class="sxs-lookup"><span data-stu-id="bb683-150">NOTES</span></span>

## <span data-ttu-id="bb683-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb683-151">RELATED LINKS</span></span>
