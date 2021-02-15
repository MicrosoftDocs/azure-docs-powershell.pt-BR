---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114521"
---
# <span data-ttu-id="a036f-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="a036f-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="a036f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a036f-102">SYNOPSIS</span></span>
<span data-ttu-id="a036f-103">Obter uma Resposta Automatizada (Ação de Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="a036f-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="a036f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a036f-104">SYNTAX</span></span>

### <span data-ttu-id="a036f-105">AlertRuleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a036f-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a036f-106">Actionid</span><span class="sxs-lookup"><span data-stu-id="a036f-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a036f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a036f-107">DESCRIPTION</span></span>
<span data-ttu-id="a036f-108">O cmdlet **Get-AzSentinelAlertRuleAction** obtém uma Resposta Automatizada (Ação de Regra de Alerta) do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="a036f-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="a036f-109">Se você especificar os parâmetros *ActionId* e *AlertRuleId,* um único objeto **AlertRuleAction** será retornado.</span><span class="sxs-lookup"><span data-stu-id="a036f-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="a036f-110">Se você não especificar o parâmetro *ActionId,* uma matriz contendo todas as Ações para a Regra de Alerta específica no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="a036f-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="a036f-111">Você pode usar o **objeto Ação** para atualizar a Ação, por exemplo, você pode alterar a **Ação de** uma Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="a036f-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="a036f-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a036f-112">EXAMPLES</span></span>

### <span data-ttu-id="a036f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a036f-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="a036f-114">Este exemplo obtém  todas as Ações da Regra de Alerta especificada no espaço de trabalho especificado e a armazena na variável $AlertRuleActions dados.</span><span class="sxs-lookup"><span data-stu-id="a036f-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="a036f-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a036f-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="a036f-116">Este exemplo obtém **uma AlertRuleAction** para a Regra de Alerta especificada no espaço de trabalho especificado e a armazena na variável $AlertRuleAction dados.</span><span class="sxs-lookup"><span data-stu-id="a036f-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="a036f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a036f-117">PARAMETERS</span></span>

### <span data-ttu-id="a036f-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="a036f-118">-ActionId</span></span>
<span data-ttu-id="a036f-119">ID da Ação.</span><span class="sxs-lookup"><span data-stu-id="a036f-119">Action Id.</span></span>

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

### <span data-ttu-id="a036f-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a036f-120">-AlertRuleId</span></span>
<span data-ttu-id="a036f-121">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="a036f-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="a036f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a036f-122">-DefaultProfile</span></span>
<span data-ttu-id="a036f-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a036f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a036f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a036f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a036f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a036f-125">Resource group name.</span></span>

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

### <span data-ttu-id="a036f-126">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="a036f-126">-WorkspaceName</span></span>
<span data-ttu-id="a036f-127">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a036f-127">Workspace Name.</span></span>

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

### <span data-ttu-id="a036f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a036f-128">CommonParameters</span></span>
<span data-ttu-id="a036f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a036f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a036f-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a036f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a036f-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="a036f-131">INPUTS</span></span>

### <span data-ttu-id="a036f-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a036f-132">None</span></span>
## <span data-ttu-id="a036f-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="a036f-133">OUTPUTS</span></span>

### <span data-ttu-id="a036f-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="a036f-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="a036f-135">Notas</span><span class="sxs-lookup"><span data-stu-id="a036f-135">NOTES</span></span>

## <span data-ttu-id="a036f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a036f-136">RELATED LINKS</span></span>
