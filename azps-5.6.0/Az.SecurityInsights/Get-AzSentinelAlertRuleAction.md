---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 37cc56714712d71ab34adee14a8b758cd9dd1113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889731"
---
# <span data-ttu-id="e2e8b-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="e2e8b-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="e2e8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e8b-103">Obter uma Resposta Automatizada (Ação de Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="e2e8b-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="e2e8b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e2e8b-104">SYNTAX</span></span>

### <span data-ttu-id="e2e8b-105">AlertRuleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e2e8b-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2e8b-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="e2e8b-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e8b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e2e8b-107">DESCRIPTION</span></span>
<span data-ttu-id="e2e8b-108">O cmdlet **Get-AzSentinelAlertRuleAction** obtém uma Resposta Automatizada (Ação de Regra de Alerta) do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="e2e8b-109">Se você especificar os *parâmetros ActionId* e *AlertRuleId,* um único **objeto AlertRuleAction** será retornado.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="e2e8b-110">Se você não especificar o parâmetro *ActionId,* uma matriz contendo todas as Ações da Regra de Alerta específica no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="e2e8b-111">Você pode usar o **objeto Action** para atualizar a Ação, por exemplo, você pode alterar a **Ação** de uma Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="e2e8b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2e8b-112">EXAMPLES</span></span>

### <span data-ttu-id="e2e8b-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e2e8b-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="e2e8b-114">Este exemplo obtém todas as **Ações** da Regra de Alerta especificada no espaço de trabalho especificado e a armazena na variável $AlertRuleActions.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="e2e8b-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e2e8b-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="e2e8b-116">Este exemplo obtém **um AlertRuleAction** para a Regra de Alerta especificada no espaço de trabalho especificado e a armazena na variável $AlertRuleAction.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="e2e8b-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e2e8b-117">PARAMETERS</span></span>

### <span data-ttu-id="e2e8b-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="e2e8b-118">-ActionId</span></span>
<span data-ttu-id="e2e8b-119">Id de ação.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-119">Action Id.</span></span>

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

### <span data-ttu-id="e2e8b-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e2e8b-120">-AlertRuleId</span></span>
<span data-ttu-id="e2e8b-121">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="e2e8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e8b-122">-DefaultProfile</span></span>
<span data-ttu-id="e2e8b-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e8b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e8b-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2e8b-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-125">Resource group name.</span></span>

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

### <span data-ttu-id="e2e8b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2e8b-126">-WorkspaceName</span></span>
<span data-ttu-id="e2e8b-127">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-127">Workspace Name.</span></span>

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

### <span data-ttu-id="e2e8b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e8b-128">CommonParameters</span></span>
<span data-ttu-id="e2e8b-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e8b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e8b-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2e8b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e8b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2e8b-131">INPUTS</span></span>

### <span data-ttu-id="e2e8b-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e2e8b-132">None</span></span>
## <span data-ttu-id="e2e8b-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e2e8b-133">OUTPUTS</span></span>

### <span data-ttu-id="e2e8b-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="e2e8b-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="e2e8b-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="e2e8b-135">NOTES</span></span>

## <span data-ttu-id="e2e8b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2e8b-136">RELATED LINKS</span></span>
