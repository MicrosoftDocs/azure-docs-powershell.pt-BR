---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433209"
---
# <span data-ttu-id="160d2-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="160d2-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="160d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="160d2-102">SYNOPSIS</span></span>
<span data-ttu-id="160d2-103">Adicionar uma resposta automática a um Analatic.</span><span class="sxs-lookup"><span data-stu-id="160d2-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="160d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="160d2-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="160d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="160d2-105">DESCRIPTION</span></span>
<span data-ttu-id="160d2-106">O cmdlet **New-AzSentinelAlertRuleAction** cria uma resposta automática para uma regra de alerta no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="160d2-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="160d2-107">Você deve fornecer a ID Resorce do aplicativo lógico e o URI Trigger que podem ser encontrados usando o módulo do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="160d2-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="160d2-108">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="160d2-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="160d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="160d2-109">EXAMPLES</span></span>

### <span data-ttu-id="160d2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="160d2-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="160d2-111">Este exemplo cria um **AlertRuleAction** para a regra de alerta especificada usando propriedades do aplicativo lógico e, em seguida, armazena-o na variável $AlertRuleAction.</span><span class="sxs-lookup"><span data-stu-id="160d2-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="160d2-112">OS</span><span class="sxs-lookup"><span data-stu-id="160d2-112">PARAMETERS</span></span>

### <span data-ttu-id="160d2-113">-ActionID</span><span class="sxs-lookup"><span data-stu-id="160d2-113">-ActionId</span></span>
<span data-ttu-id="160d2-114">ID da ação.</span><span class="sxs-lookup"><span data-stu-id="160d2-114">Action Id.</span></span>

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

### <span data-ttu-id="160d2-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="160d2-115">-AlertRuleId</span></span>
<span data-ttu-id="160d2-116">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="160d2-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="160d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160d2-117">-DefaultProfile</span></span>
<span data-ttu-id="160d2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="160d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160d2-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="160d2-119">-LogicAppResourceId</span></span>
<span data-ttu-id="160d2-120">ID do recurso de aplicativo lógica da ação.</span><span class="sxs-lookup"><span data-stu-id="160d2-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="160d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="160d2-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="160d2-122">Resource group name.</span></span>

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

### <span data-ttu-id="160d2-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="160d2-123">-TriggerUri</span></span>
<span data-ttu-id="160d2-124">URI de gatilho do aplicativo lógica da ação.</span><span class="sxs-lookup"><span data-stu-id="160d2-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="160d2-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="160d2-125">-WorkspaceName</span></span>
<span data-ttu-id="160d2-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="160d2-126">Workspace Name.</span></span>

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

### <span data-ttu-id="160d2-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="160d2-127">-Confirm</span></span>
<span data-ttu-id="160d2-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="160d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160d2-129">-WhatIf</span></span>
<span data-ttu-id="160d2-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="160d2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="160d2-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="160d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160d2-132">CommonParameters</span></span>
<span data-ttu-id="160d2-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="160d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160d2-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="160d2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160d2-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="160d2-135">INPUTS</span></span>

### <span data-ttu-id="160d2-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="160d2-136">None</span></span>
## <span data-ttu-id="160d2-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="160d2-137">OUTPUTS</span></span>

### <span data-ttu-id="160d2-138">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="160d2-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="160d2-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="160d2-139">NOTES</span></span>

## <span data-ttu-id="160d2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="160d2-140">RELATED LINKS</span></span>
