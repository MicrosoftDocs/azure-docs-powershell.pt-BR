---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 0828961a534a6f98d52cdf8c4e2a134cc2975df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886840"
---
# <span data-ttu-id="ed256-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="ed256-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="ed256-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed256-102">SYNOPSIS</span></span>
<span data-ttu-id="ed256-103">Remova uma Resposta Automatizada de um Analytic.</span><span class="sxs-lookup"><span data-stu-id="ed256-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="ed256-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ed256-104">SYNTAX</span></span>

### <span data-ttu-id="ed256-105">ActionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ed256-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed256-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed256-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed256-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ed256-107">DESCRIPTION</span></span>
<span data-ttu-id="ed256-108">O cmdlet **Remove-AzSentinelAlertRuleAction** exclui permanentemente uma Resposta Automatizada da Regra de Alerta em um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="ed256-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="ed256-109">Você pode passar um **objeto AlertRuleAction** usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="ed256-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="ed256-110">Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="ed256-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ed256-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed256-111">EXAMPLES</span></span>

### <span data-ttu-id="ed256-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed256-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="ed256-113">Este comando remove a Regra de Alerta do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ed256-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="ed256-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ed256-114">PARAMETERS</span></span>

### <span data-ttu-id="ed256-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="ed256-115">-ActionId</span></span>
<span data-ttu-id="ed256-116">Id de ação.</span><span class="sxs-lookup"><span data-stu-id="ed256-116">Action Id.</span></span>

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

### <span data-ttu-id="ed256-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="ed256-117">-AlertRuleId</span></span>
<span data-ttu-id="ed256-118">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="ed256-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed256-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed256-119">-DefaultProfile</span></span>
<span data-ttu-id="ed256-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed256-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed256-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed256-121">-InputObject</span></span>
<span data-ttu-id="ed256-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="ed256-122">InputObject.</span></span>

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

### <span data-ttu-id="ed256-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed256-123">-PassThru</span></span>
<span data-ttu-id="ed256-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="ed256-124">PassThru</span></span>

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

### <span data-ttu-id="ed256-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed256-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed256-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed256-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed256-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed256-127">-WorkspaceName</span></span>
<span data-ttu-id="ed256-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ed256-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed256-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed256-129">-Confirm</span></span>
<span data-ttu-id="ed256-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed256-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed256-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed256-131">-WhatIf</span></span>
<span data-ttu-id="ed256-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed256-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed256-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed256-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed256-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed256-134">CommonParameters</span></span>
<span data-ttu-id="ed256-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed256-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed256-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed256-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed256-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed256-137">INPUTS</span></span>

### <span data-ttu-id="ed256-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ed256-138">System.String</span></span>
### <span data-ttu-id="ed256-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ed256-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="ed256-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ed256-140">OUTPUTS</span></span>

### <span data-ttu-id="ed256-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ed256-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="ed256-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="ed256-142">NOTES</span></span>

## <span data-ttu-id="ed256-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed256-143">RELATED LINKS</span></span>
