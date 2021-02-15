---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116189"
---
# <span data-ttu-id="d1209-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="d1209-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="d1209-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1209-102">SYNOPSIS</span></span>
<span data-ttu-id="d1209-103">Obtém uma Análise (Regra de Alerta).</span><span class="sxs-lookup"><span data-stu-id="d1209-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="d1209-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1209-104">SYNTAX</span></span>

### <span data-ttu-id="d1209-105">WorkspaceScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d1209-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1209-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="d1209-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1209-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="d1209-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1209-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1209-108">DESCRIPTION</span></span>
<span data-ttu-id="d1209-109">O cmdlet **Get-AzSentinelAlertRule** obtém uma Analytic (Regra de Alerta) do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="d1209-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="d1209-110">Se você especificar o parâmetro *AlertRuleId,* um único objeto **AlertRule** será retornado.</span><span class="sxs-lookup"><span data-stu-id="d1209-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="d1209-111">Se você não especificar o parâmetro *AlertRuleId,* uma matriz contendo todas as Regras de Alerta no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="d1209-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="d1209-112">Você pode usar o objeto **AlertRule** para atualizar o AlertRule, por exemplo, você pode desabilitar **o AlertRule.**</span><span class="sxs-lookup"><span data-stu-id="d1209-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="d1209-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1209-113">EXAMPLES</span></span>

### <span data-ttu-id="d1209-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1209-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="d1209-115">Este exemplo obtém todos os **AlertRules** no espaço de trabalho especificado e, em seguida, o armazena na variável $AlertRules dados.</span><span class="sxs-lookup"><span data-stu-id="d1209-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="d1209-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d1209-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="d1209-117">Este exemplo obtém **um AlertRule** no espaço de trabalho especificado e o armazena na variável $AlertRule dados.</span><span class="sxs-lookup"><span data-stu-id="d1209-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="d1209-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1209-118">PARAMETERS</span></span>

### <span data-ttu-id="d1209-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="d1209-119">-AlertRuleId</span></span>
<span data-ttu-id="d1209-120">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="d1209-120">Alert Rule Id.</span></span>

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

### <span data-ttu-id="d1209-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1209-121">-DefaultProfile</span></span>
<span data-ttu-id="d1209-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1209-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1209-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1209-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1209-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1209-124">Resource group name.</span></span>

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

### <span data-ttu-id="d1209-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1209-125">-ResourceId</span></span>
<span data-ttu-id="d1209-126">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="d1209-126">Resource Id.</span></span>

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

### <span data-ttu-id="d1209-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="d1209-127">-WorkspaceName</span></span>
<span data-ttu-id="d1209-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d1209-128">Workspace Name.</span></span>

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

### <span data-ttu-id="d1209-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1209-129">CommonParameters</span></span>
<span data-ttu-id="d1209-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1209-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1209-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1209-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1209-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="d1209-132">INPUTS</span></span>

### <span data-ttu-id="d1209-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d1209-133">System.String</span></span>
## <span data-ttu-id="d1209-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="d1209-134">OUTPUTS</span></span>

### <span data-ttu-id="d1209-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="d1209-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="d1209-136">Notas</span><span class="sxs-lookup"><span data-stu-id="d1209-136">NOTES</span></span>

## <span data-ttu-id="d1209-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1209-137">RELATED LINKS</span></span>
