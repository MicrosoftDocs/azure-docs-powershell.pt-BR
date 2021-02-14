---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117145"
---
# <span data-ttu-id="bbfce-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbfce-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="bbfce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbfce-102">SYNOPSIS</span></span>
<span data-ttu-id="bbfce-103">Excluir um análtico.</span><span class="sxs-lookup"><span data-stu-id="bbfce-103">Delete an Analytic.</span></span>

## <span data-ttu-id="bbfce-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbfce-104">SYNTAX</span></span>

### <span data-ttu-id="bbfce-105">AlertRuleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bbfce-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbfce-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="bbfce-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbfce-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bbfce-107">DESCRIPTION</span></span>
<span data-ttu-id="bbfce-108">O cmdlet **Remove-AzSentinelAlertRule** exclui permanentemente uma Regra de Alerta de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="bbfce-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="bbfce-109">Você pode passar um objeto **AlertRule** usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="bbfce-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="bbfce-110">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="bbfce-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="bbfce-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbfce-111">EXAMPLES</span></span>

### <span data-ttu-id="bbfce-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bbfce-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="bbfce-113">Esse comando remove a Regra de Alerta do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bbfce-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="bbfce-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbfce-114">PARAMETERS</span></span>

### <span data-ttu-id="bbfce-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="bbfce-115">-AlertRuleId</span></span>
<span data-ttu-id="bbfce-116">ID da Regra de Alerta.</span><span class="sxs-lookup"><span data-stu-id="bbfce-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="bbfce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfce-117">-DefaultProfile</span></span>
<span data-ttu-id="bbfce-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbfce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbfce-119">-InputObject</span></span>
<span data-ttu-id="bbfce-120">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="bbfce-120">InputObject.</span></span>

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

### <span data-ttu-id="bbfce-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbfce-121">-PassThru</span></span>
<span data-ttu-id="bbfce-122">Passthru</span><span class="sxs-lookup"><span data-stu-id="bbfce-122">PassThru</span></span>

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

### <span data-ttu-id="bbfce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbfce-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbfce-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbfce-124">Resource group name.</span></span>

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

### <span data-ttu-id="bbfce-125">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="bbfce-125">-WorkspaceName</span></span>
<span data-ttu-id="bbfce-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bbfce-126">Workspace Name.</span></span>

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

### <span data-ttu-id="bbfce-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bbfce-127">-Confirm</span></span>
<span data-ttu-id="bbfce-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbfce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbfce-129">-WhatIf</span></span>
<span data-ttu-id="bbfce-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bbfce-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbfce-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbfce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbfce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbfce-132">CommonParameters</span></span>
<span data-ttu-id="bbfce-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbfce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbfce-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbfce-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbfce-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="bbfce-135">INPUTS</span></span>

### <span data-ttu-id="bbfce-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bbfce-136">System.String</span></span>
### <span data-ttu-id="bbfce-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbfce-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="bbfce-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="bbfce-138">OUTPUTS</span></span>

### <span data-ttu-id="bbfce-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="bbfce-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="bbfce-140">Notas</span><span class="sxs-lookup"><span data-stu-id="bbfce-140">NOTES</span></span>

## <span data-ttu-id="bbfce-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbfce-141">RELATED LINKS</span></span>
