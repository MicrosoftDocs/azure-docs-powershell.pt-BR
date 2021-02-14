---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117144"
---
# <span data-ttu-id="900fb-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="900fb-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="900fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="900fb-102">SYNOPSIS</span></span>
<span data-ttu-id="900fb-103">Remover uma Resposta Automatizada de um Análtico.</span><span class="sxs-lookup"><span data-stu-id="900fb-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="900fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="900fb-104">SYNTAX</span></span>

### <span data-ttu-id="900fb-105">ActionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="900fb-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="900fb-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="900fb-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="900fb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="900fb-107">DESCRIPTION</span></span>
<span data-ttu-id="900fb-108">O cmdlet **Remove-AzSentinelAlertRuleAction** exclui permanentemente uma Resposta Automatizada da Regra de Alerta em um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="900fb-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="900fb-109">Você pode passar um **objeto AlertRuleAction** usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="900fb-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="900fb-110">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="900fb-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="900fb-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="900fb-111">EXAMPLES</span></span>

### <span data-ttu-id="900fb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="900fb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="900fb-113">Esse comando remove a Regra de Alerta do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="900fb-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="900fb-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="900fb-114">PARAMETERS</span></span>

### <span data-ttu-id="900fb-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="900fb-115">-ActionId</span></span>
<span data-ttu-id="900fb-116">ID da Ação.</span><span class="sxs-lookup"><span data-stu-id="900fb-116">Action Id.</span></span>

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

### <span data-ttu-id="900fb-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="900fb-117">-AlertRuleId</span></span>
<span data-ttu-id="900fb-118">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="900fb-118">Alert Rule Id.</span></span>

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

### <span data-ttu-id="900fb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900fb-119">-DefaultProfile</span></span>
<span data-ttu-id="900fb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="900fb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="900fb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="900fb-121">-InputObject</span></span>
<span data-ttu-id="900fb-122">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="900fb-122">InputObject.</span></span>

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

### <span data-ttu-id="900fb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="900fb-123">-PassThru</span></span>
<span data-ttu-id="900fb-124">Passthru</span><span class="sxs-lookup"><span data-stu-id="900fb-124">PassThru</span></span>

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

### <span data-ttu-id="900fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="900fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="900fb-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="900fb-126">Resource group name.</span></span>

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

### <span data-ttu-id="900fb-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="900fb-127">-WorkspaceName</span></span>
<span data-ttu-id="900fb-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="900fb-128">Workspace Name.</span></span>

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

### <span data-ttu-id="900fb-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="900fb-129">-Confirm</span></span>
<span data-ttu-id="900fb-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="900fb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="900fb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="900fb-131">-WhatIf</span></span>
<span data-ttu-id="900fb-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="900fb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="900fb-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="900fb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="900fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900fb-134">CommonParameters</span></span>
<span data-ttu-id="900fb-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="900fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900fb-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="900fb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900fb-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="900fb-137">INPUTS</span></span>

### <span data-ttu-id="900fb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="900fb-138">System.String</span></span>
### <span data-ttu-id="900fb-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="900fb-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="900fb-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="900fb-140">OUTPUTS</span></span>

### <span data-ttu-id="900fb-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="900fb-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="900fb-142">Notas</span><span class="sxs-lookup"><span data-stu-id="900fb-142">NOTES</span></span>

## <span data-ttu-id="900fb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="900fb-143">RELATED LINKS</span></span>
