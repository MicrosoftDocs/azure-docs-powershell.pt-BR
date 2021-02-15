---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112603"
---
# <span data-ttu-id="c9813-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="c9813-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="c9813-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9813-102">SYNOPSIS</span></span>
<span data-ttu-id="c9813-103">Obter modelo de regra para análise.</span><span class="sxs-lookup"><span data-stu-id="c9813-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="c9813-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9813-104">SYNTAX</span></span>

### <span data-ttu-id="c9813-105">WorkspaceScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c9813-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9813-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="c9813-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9813-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="c9813-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9813-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9813-108">DESCRIPTION</span></span>
<span data-ttu-id="c9813-109">O cmdlet **Get-AzSentinelAlertRuleTemplate obtém** um Modelo de Regra de Alerta do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="c9813-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="c9813-110">Se você especificar o parâmetro *AlertRuleTemplateId,* um único objeto **AlertRuleTemplate** será retornado.</span><span class="sxs-lookup"><span data-stu-id="c9813-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="c9813-111">Se você não especificar o parâmetro *AlertRuleTemplateId,* uma matriz que contém todos os Modelos de Regra de Alerta no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="c9813-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="c9813-112">Você pode usar o **objeto AlertRuleTemplate** para criar uma nova Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="c9813-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="c9813-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9813-113">EXAMPLES</span></span>

### <span data-ttu-id="c9813-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c9813-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="c9813-115">Este exemplo obtém todos os **AlertRuleTemplates** no espaço de trabalho especificado e, em seguida, o armazena na variável $AlertRuleTemplates dados.</span><span class="sxs-lookup"><span data-stu-id="c9813-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="c9813-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c9813-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="c9813-117">Este exemplo obtém **um AlertRuleTemplate** no espaço de trabalho especificado e, em seguida, o armazena na variável $AlertRuleTemplate dados.</span><span class="sxs-lookup"><span data-stu-id="c9813-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="c9813-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9813-118">PARAMETERS</span></span>

### <span data-ttu-id="c9813-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="c9813-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="c9813-120">ID da Regra de Alerta do Modelo.</span><span class="sxs-lookup"><span data-stu-id="c9813-120">Template Alert Rule Id.</span></span>

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

### <span data-ttu-id="c9813-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9813-121">-DefaultProfile</span></span>
<span data-ttu-id="c9813-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9813-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9813-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9813-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9813-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9813-124">Resource group name.</span></span>

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

### <span data-ttu-id="c9813-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9813-125">-ResourceId</span></span>
<span data-ttu-id="c9813-126">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="c9813-126">Resource Id.</span></span>

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

### <span data-ttu-id="c9813-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c9813-127">-WorkspaceName</span></span>
<span data-ttu-id="c9813-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9813-128">Workspace Name.</span></span>

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

### <span data-ttu-id="c9813-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9813-129">CommonParameters</span></span>
<span data-ttu-id="c9813-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9813-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9813-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9813-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9813-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="c9813-132">INPUTS</span></span>

### <span data-ttu-id="c9813-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c9813-133">System.String</span></span>
## <span data-ttu-id="c9813-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="c9813-134">OUTPUTS</span></span>

### <span data-ttu-id="c9813-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="c9813-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="c9813-136">Notas</span><span class="sxs-lookup"><span data-stu-id="c9813-136">NOTES</span></span>

## <span data-ttu-id="c9813-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9813-137">RELATED LINKS</span></span>
