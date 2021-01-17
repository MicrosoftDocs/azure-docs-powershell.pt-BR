---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433226"
---
# <span data-ttu-id="0fe84-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fe84-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="0fe84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0fe84-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe84-103">Obtém um analítico (regra de alerta).</span><span class="sxs-lookup"><span data-stu-id="0fe84-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="0fe84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fe84-104">SYNTAX</span></span>

### <span data-ttu-id="0fe84-105">WorkspaceScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="0fe84-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe84-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0fe84-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe84-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="0fe84-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fe84-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0fe84-108">DESCRIPTION</span></span>
<span data-ttu-id="0fe84-109">O cmdlet **Get-AzSentinelAlertRule** Obtém uma análise (regra de alerta) do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="0fe84-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="0fe84-110">Se você especificar o parâmetro *AlertRuleId* , um único objeto **AlertRule** será retornado.</span><span class="sxs-lookup"><span data-stu-id="0fe84-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="0fe84-111">Se você não especificar o parâmetro *AlertRuleId* , uma matriz contendo todas as regras de alerta no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="0fe84-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="0fe84-112">Você pode usar o objeto **AlertRule** para atualizar o AlertRule, por exemplo, você pode desabilitar o **AlertRule**.</span><span class="sxs-lookup"><span data-stu-id="0fe84-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="0fe84-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fe84-113">EXAMPLES</span></span>

### <span data-ttu-id="0fe84-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0fe84-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="0fe84-115">Este exemplo obtém todos os **AlertRules** no espaço de trabalho especificado e, em seguida, armazena-os na variável $AlertRules.</span><span class="sxs-lookup"><span data-stu-id="0fe84-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="0fe84-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0fe84-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="0fe84-117">Este exemplo obtém um **AlertRule** no espaço de trabalho especificado e, em seguida, armazena-o na variável $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="0fe84-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="0fe84-118">OS</span><span class="sxs-lookup"><span data-stu-id="0fe84-118">PARAMETERS</span></span>

### <span data-ttu-id="0fe84-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0fe84-119">-AlertRuleId</span></span>
<span data-ttu-id="0fe84-120">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="0fe84-120">Alert Rule Id.</span></span>

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

### <span data-ttu-id="0fe84-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe84-121">-DefaultProfile</span></span>
<span data-ttu-id="0fe84-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe84-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe84-123">-ResourceGroupName</span></span>
<span data-ttu-id="0fe84-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0fe84-124">Resource group name.</span></span>

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

### <span data-ttu-id="0fe84-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fe84-125">-ResourceId</span></span>
<span data-ttu-id="0fe84-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0fe84-126">Resource Id.</span></span>

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

### <span data-ttu-id="0fe84-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0fe84-127">-WorkspaceName</span></span>
<span data-ttu-id="0fe84-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0fe84-128">Workspace Name.</span></span>

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

### <span data-ttu-id="0fe84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe84-129">CommonParameters</span></span>
<span data-ttu-id="0fe84-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe84-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fe84-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe84-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0fe84-132">INPUTS</span></span>

### <span data-ttu-id="0fe84-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0fe84-133">System.String</span></span>
## <span data-ttu-id="0fe84-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0fe84-134">OUTPUTS</span></span>

### <span data-ttu-id="0fe84-135">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fe84-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="0fe84-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0fe84-136">NOTES</span></span>

## <span data-ttu-id="0fe84-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fe84-137">RELATED LINKS</span></span>
