---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433216"
---
# <span data-ttu-id="e5865-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="e5865-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="e5865-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5865-102">SYNOPSIS</span></span>
<span data-ttu-id="e5865-103">Obter modelo de regra analítica.</span><span class="sxs-lookup"><span data-stu-id="e5865-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="e5865-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5865-104">SYNTAX</span></span>

### <span data-ttu-id="e5865-105">WorkspaceScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5865-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5865-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="e5865-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5865-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="e5865-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5865-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5865-108">DESCRIPTION</span></span>
<span data-ttu-id="e5865-109">O cmdlet **Get-AzSentinelAlertRuleTemplate** Obtém um modelo de regra de alerta do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="e5865-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="e5865-110">Se você especificar o parâmetro *AlertRuleTemplateId* , um único objeto **AlertRuleTemplate** será retornado.</span><span class="sxs-lookup"><span data-stu-id="e5865-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="e5865-111">Se você não especificar o parâmetro *AlertRuleTemplateId* , uma matriz que contenha todos os modelos de regra de alerta no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="e5865-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="e5865-112">Você pode usar o objeto **AlertRuleTemplate** para criar uma nova regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="e5865-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="e5865-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5865-113">EXAMPLES</span></span>

### <span data-ttu-id="e5865-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5865-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="e5865-115">Este exemplo obtém todos os **AlertRuleTemplates** no espaço de trabalho especificado e, em seguida, armazena-os na variável $AlertRuleTemplates.</span><span class="sxs-lookup"><span data-stu-id="e5865-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="e5865-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e5865-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="e5865-117">Este exemplo obtém um **AlertRuleTemplate** no espaço de trabalho especificado e, em seguida, armazena-o na variável $AlertRuleTemplate.</span><span class="sxs-lookup"><span data-stu-id="e5865-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="e5865-118">OS</span><span class="sxs-lookup"><span data-stu-id="e5865-118">PARAMETERS</span></span>

### <span data-ttu-id="e5865-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="e5865-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="e5865-120">ID da regra de alerta de modelo.</span><span class="sxs-lookup"><span data-stu-id="e5865-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5865-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5865-121">-DefaultProfile</span></span>
<span data-ttu-id="e5865-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5865-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5865-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5865-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5865-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5865-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5865-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5865-125">-ResourceId</span></span>
<span data-ttu-id="e5865-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="e5865-126">Resource Id.</span></span>

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

### <span data-ttu-id="e5865-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5865-127">-WorkspaceName</span></span>
<span data-ttu-id="e5865-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e5865-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5865-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5865-129">CommonParameters</span></span>
<span data-ttu-id="e5865-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5865-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5865-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5865-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5865-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5865-132">INPUTS</span></span>

### <span data-ttu-id="e5865-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e5865-133">System.String</span></span>
## <span data-ttu-id="e5865-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5865-134">OUTPUTS</span></span>

### <span data-ttu-id="e5865-135">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRuleTemplates. PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="e5865-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="e5865-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5865-136">NOTES</span></span>

## <span data-ttu-id="e5865-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5865-137">RELATED LINKS</span></span>
