---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 836d566c9e75fdce825542ebb13520933c071cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889730"
---
# <span data-ttu-id="e1367-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1367-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="e1367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1367-102">SYNOPSIS</span></span>
<span data-ttu-id="e1367-103">Obtém uma Análise (Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="e1367-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="e1367-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e1367-104">SYNTAX</span></span>

### <span data-ttu-id="e1367-105">WorkspaceScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e1367-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1367-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e1367-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1367-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1367-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1367-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e1367-108">DESCRIPTION</span></span>
<span data-ttu-id="e1367-109">O cmdlet **Get-AzSentinelAlertRule** obtém um Analytic (Regra de Alerta) do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="e1367-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="e1367-110">Se você especificar o *parâmetro AlertRuleId,* um único **objeto AlertRule** será retornado.</span><span class="sxs-lookup"><span data-stu-id="e1367-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="e1367-111">Se você não especificar o parâmetro *AlertRuleId,* uma matriz contendo todas as Regras de Alerta no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="e1367-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="e1367-112">Você pode usar o **objeto AlertRule** para atualizar o AlertRule, por exemplo, você pode desabilitar **AlertRule**.</span><span class="sxs-lookup"><span data-stu-id="e1367-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="e1367-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1367-113">EXAMPLES</span></span>

### <span data-ttu-id="e1367-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1367-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="e1367-115">Este exemplo obtém todos os **AlertRules** no espaço de trabalho especificado e o armazena na variável $AlertRules.</span><span class="sxs-lookup"><span data-stu-id="e1367-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="e1367-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e1367-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="e1367-117">Este exemplo obtém **um AlertRule** no espaço de trabalho especificado e o armazena na variável $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="e1367-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="e1367-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e1367-118">PARAMETERS</span></span>

### <span data-ttu-id="e1367-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e1367-119">-AlertRuleId</span></span>
<span data-ttu-id="e1367-120">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="e1367-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1367-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1367-121">-DefaultProfile</span></span>
<span data-ttu-id="e1367-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1367-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1367-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1367-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1367-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1367-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1367-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1367-125">-ResourceId</span></span>
<span data-ttu-id="e1367-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e1367-126">Resource Id.</span></span>

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

### <span data-ttu-id="e1367-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e1367-127">-WorkspaceName</span></span>
<span data-ttu-id="e1367-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1367-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1367-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1367-129">CommonParameters</span></span>
<span data-ttu-id="e1367-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1367-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1367-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1367-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1367-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1367-132">INPUTS</span></span>

### <span data-ttu-id="e1367-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e1367-133">System.String</span></span>
## <span data-ttu-id="e1367-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e1367-134">OUTPUTS</span></span>

### <span data-ttu-id="e1367-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1367-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="e1367-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="e1367-136">NOTES</span></span>

## <span data-ttu-id="e1367-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1367-137">RELATED LINKS</span></span>
