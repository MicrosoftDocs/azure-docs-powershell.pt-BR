---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433223"
---
# <span data-ttu-id="83c3c-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="83c3c-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="83c3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="83c3c-103">Obter uma resposta automática (ação de regra de alerta).</span><span class="sxs-lookup"><span data-stu-id="83c3c-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="83c3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83c3c-104">SYNTAX</span></span>

### <span data-ttu-id="83c3c-105">AlertRuleId (padrão)</span><span class="sxs-lookup"><span data-stu-id="83c3c-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83c3c-106">ActionID</span><span class="sxs-lookup"><span data-stu-id="83c3c-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83c3c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83c3c-107">DESCRIPTION</span></span>
<span data-ttu-id="83c3c-108">O cmdlet **Get-AzSentinelAlertRuleAction** Obtém uma resposta automática (ação de regra de alerta) do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="83c3c-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="83c3c-109">Se você especificar os parâmetros *ActionID* e *AlertRuleId* , um único objeto **AlertRuleAction** será retornado.</span><span class="sxs-lookup"><span data-stu-id="83c3c-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="83c3c-110">Se você não especificar o parâmetro *ActionID* , uma matriz que contenha todas as ações para a regra de alerta específica no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="83c3c-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="83c3c-111">Você pode usar o objeto **Action** para atualizar a ação, por exemplo, você pode alterar a **ação** para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="83c3c-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="83c3c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83c3c-112">EXAMPLES</span></span>

### <span data-ttu-id="83c3c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="83c3c-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="83c3c-114">Este exemplo obtém todas as **ações** da regra de alerta especificada no espaço de trabalho especificado e a armazena na variável $AlertRuleActions.</span><span class="sxs-lookup"><span data-stu-id="83c3c-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="83c3c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="83c3c-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="83c3c-116">Este exemplo obtém um **AlertRuleAction** para a regra de alerta especificada no espaço de trabalho especificado e, em seguida, armazena-o na variável $AlertRuleAction.</span><span class="sxs-lookup"><span data-stu-id="83c3c-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="83c3c-117">OS</span><span class="sxs-lookup"><span data-stu-id="83c3c-117">PARAMETERS</span></span>

### <span data-ttu-id="83c3c-118">-ActionID</span><span class="sxs-lookup"><span data-stu-id="83c3c-118">-ActionId</span></span>
<span data-ttu-id="83c3c-119">ID da ação.</span><span class="sxs-lookup"><span data-stu-id="83c3c-119">Action Id.</span></span>

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

### <span data-ttu-id="83c3c-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="83c3c-120">-AlertRuleId</span></span>
<span data-ttu-id="83c3c-121">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="83c3c-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="83c3c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c3c-122">-DefaultProfile</span></span>
<span data-ttu-id="83c3c-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83c3c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83c3c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83c3c-124">-ResourceGroupName</span></span>
<span data-ttu-id="83c3c-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="83c3c-125">Resource group name.</span></span>

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

### <span data-ttu-id="83c3c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="83c3c-126">-WorkspaceName</span></span>
<span data-ttu-id="83c3c-127">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="83c3c-127">Workspace Name.</span></span>

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

### <span data-ttu-id="83c3c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c3c-128">CommonParameters</span></span>
<span data-ttu-id="83c3c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c3c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c3c-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83c3c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c3c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83c3c-131">INPUTS</span></span>

### <span data-ttu-id="83c3c-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="83c3c-132">None</span></span>
## <span data-ttu-id="83c3c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83c3c-133">OUTPUTS</span></span>

### <span data-ttu-id="83c3c-134">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="83c3c-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="83c3c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83c3c-135">NOTES</span></span>

## <span data-ttu-id="83c3c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83c3c-136">RELATED LINKS</span></span>
