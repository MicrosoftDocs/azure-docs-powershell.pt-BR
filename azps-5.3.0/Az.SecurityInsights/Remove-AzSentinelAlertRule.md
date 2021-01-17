---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433195"
---
# <span data-ttu-id="358e0-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="358e0-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="358e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="358e0-102">SYNOPSIS</span></span>
<span data-ttu-id="358e0-103">Excluir um analítico.</span><span class="sxs-lookup"><span data-stu-id="358e0-103">Delete an Analytic.</span></span>

## <span data-ttu-id="358e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="358e0-104">SYNTAX</span></span>

### <span data-ttu-id="358e0-105">AlertRuleId (padrão)</span><span class="sxs-lookup"><span data-stu-id="358e0-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358e0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="358e0-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="358e0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="358e0-107">DESCRIPTION</span></span>
<span data-ttu-id="358e0-108">O cmdlet **Remove-AzSentinelAlertRule** exclui permanentemente uma regra de alerta de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="358e0-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="358e0-109">Você pode passar um objeto **AlertRule** usando o operador pipeline ou, como alternativa, pode especificar os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="358e0-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="358e0-110">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="358e0-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="358e0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="358e0-111">EXAMPLES</span></span>

### <span data-ttu-id="358e0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="358e0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="358e0-113">Esse comando Remove a regra de alerta do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="358e0-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="358e0-114">OS</span><span class="sxs-lookup"><span data-stu-id="358e0-114">PARAMETERS</span></span>

### <span data-ttu-id="358e0-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="358e0-115">-AlertRuleId</span></span>
<span data-ttu-id="358e0-116">ID da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="358e0-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="358e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358e0-117">-DefaultProfile</span></span>
<span data-ttu-id="358e0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="358e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="358e0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="358e0-119">-InputObject</span></span>
<span data-ttu-id="358e0-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="358e0-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="358e0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="358e0-121">-PassThru</span></span>
<span data-ttu-id="358e0-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="358e0-122">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="358e0-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="358e0-124">Resource group name.</span></span>

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

### <span data-ttu-id="358e0-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="358e0-125">-WorkspaceName</span></span>
<span data-ttu-id="358e0-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="358e0-126">Workspace Name.</span></span>

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

### <span data-ttu-id="358e0-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="358e0-127">-Confirm</span></span>
<span data-ttu-id="358e0-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="358e0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358e0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358e0-129">-WhatIf</span></span>
<span data-ttu-id="358e0-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="358e0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="358e0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="358e0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358e0-132">CommonParameters</span></span>
<span data-ttu-id="358e0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358e0-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="358e0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358e0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="358e0-135">INPUTS</span></span>

### <span data-ttu-id="358e0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="358e0-136">System.String</span></span>
### <span data-ttu-id="358e0-137">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="358e0-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="358e0-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="358e0-138">OUTPUTS</span></span>

### <span data-ttu-id="358e0-139">Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="358e0-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="358e0-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="358e0-140">NOTES</span></span>

## <span data-ttu-id="358e0-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="358e0-141">RELATED LINKS</span></span>
