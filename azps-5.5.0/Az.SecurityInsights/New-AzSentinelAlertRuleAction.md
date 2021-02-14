---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117153"
---
# <span data-ttu-id="a9766-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="a9766-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="a9766-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9766-102">SYNOPSIS</span></span>
<span data-ttu-id="a9766-103">Adicione uma Resposta Automatizada a um análtico.</span><span class="sxs-lookup"><span data-stu-id="a9766-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="a9766-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9766-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9766-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9766-105">DESCRIPTION</span></span>
<span data-ttu-id="a9766-106">O cmdlet **New-AzSentinelAlertRuleAction** cria uma Resposta Automatizada para uma Regra de Alerta no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="a9766-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="a9766-107">Você deve fornecer a ID do Aplicativo Logic Resorce e o Uri do Gatilho, que podem ser encontrados usando o módulo do Aplicativo Lógico.</span><span class="sxs-lookup"><span data-stu-id="a9766-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="a9766-108">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="a9766-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a9766-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a9766-109">EXAMPLES</span></span>

### <span data-ttu-id="a9766-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9766-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="a9766-111">Este exemplo cria uma **AlertRuleAction** para a Regra de Alerta especificada usando propriedades do aplicativo Logic e a armazena na variável $AlertRuleAction dados.</span><span class="sxs-lookup"><span data-stu-id="a9766-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="a9766-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9766-112">PARAMETERS</span></span>

### <span data-ttu-id="a9766-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="a9766-113">-ActionId</span></span>
<span data-ttu-id="a9766-114">ID da Ação.</span><span class="sxs-lookup"><span data-stu-id="a9766-114">Action Id.</span></span>

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

### <span data-ttu-id="a9766-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a9766-115">-AlertRuleId</span></span>
<span data-ttu-id="a9766-116">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="a9766-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="a9766-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9766-117">-DefaultProfile</span></span>
<span data-ttu-id="a9766-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9766-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9766-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="a9766-119">-LogicAppResourceId</span></span>
<span data-ttu-id="a9766-120">ID do Recurso do Aplicativo Lógica de Ação.</span><span class="sxs-lookup"><span data-stu-id="a9766-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="a9766-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9766-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9766-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9766-122">Resource group name.</span></span>

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

### <span data-ttu-id="a9766-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="a9766-123">-TriggerUri</span></span>
<span data-ttu-id="a9766-124">Uri de acionador do aplicativo Action Logic.</span><span class="sxs-lookup"><span data-stu-id="a9766-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="a9766-125">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="a9766-125">-WorkspaceName</span></span>
<span data-ttu-id="a9766-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a9766-126">Workspace Name.</span></span>

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

### <span data-ttu-id="a9766-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a9766-127">-Confirm</span></span>
<span data-ttu-id="a9766-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9766-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9766-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9766-129">-WhatIf</span></span>
<span data-ttu-id="a9766-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a9766-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9766-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9766-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9766-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9766-132">CommonParameters</span></span>
<span data-ttu-id="a9766-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9766-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9766-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9766-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9766-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="a9766-135">INPUTS</span></span>

### <span data-ttu-id="a9766-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a9766-136">None</span></span>
## <span data-ttu-id="a9766-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="a9766-137">OUTPUTS</span></span>

### <span data-ttu-id="a9766-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="a9766-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="a9766-139">Notas</span><span class="sxs-lookup"><span data-stu-id="a9766-139">NOTES</span></span>

## <span data-ttu-id="a9766-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9766-140">RELATED LINKS</span></span>
