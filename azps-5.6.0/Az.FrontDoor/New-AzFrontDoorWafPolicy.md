---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5c39a86b29ce27ea57d51e7e3bfb048560ef1ee6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887740"
---
# <span data-ttu-id="caf05-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="caf05-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="caf05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf05-102">SYNOPSIS</span></span>
<span data-ttu-id="caf05-103">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="caf05-103">Create WAF policy</span></span>

## <span data-ttu-id="caf05-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="caf05-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caf05-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="caf05-105">DESCRIPTION</span></span>
<span data-ttu-id="caf05-106">O cmdlet **New-AzFrontDoorWafPolicy** cria uma nova política waf do Azure no grupo de recursos especificado em assinatura atual</span><span class="sxs-lookup"><span data-stu-id="caf05-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="caf05-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="caf05-107">EXAMPLES</span></span>

### <span data-ttu-id="caf05-108">Exemplo 1: Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="caf05-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="caf05-109">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="caf05-109">Create WAF policy</span></span>

## <span data-ttu-id="caf05-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="caf05-110">PARAMETERS</span></span>

### <span data-ttu-id="caf05-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="caf05-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="caf05-112">Corpo da Resposta Personalizado</span><span class="sxs-lookup"><span data-stu-id="caf05-112">Custom Response Body</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="caf05-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="caf05-114">Código de Status da Resposta Personalizado</span><span class="sxs-lookup"><span data-stu-id="caf05-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="caf05-115">-Customrule</span></span>
<span data-ttu-id="caf05-116">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="caf05-116">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf05-117">-DefaultProfile</span></span>
<span data-ttu-id="caf05-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="caf05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caf05-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="caf05-119">-EnabledState</span></span>
<span data-ttu-id="caf05-120">Se a política está em estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="caf05-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="caf05-121">Os valores possíveis incluem: 'Disabled', 'Enabled'</span><span class="sxs-lookup"><span data-stu-id="caf05-121">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="caf05-122">-ManagedRule</span></span>
<span data-ttu-id="caf05-123">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="caf05-123">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="caf05-124">-Mode</span></span>
<span data-ttu-id="caf05-125">Descreve se ele está no modo de detecção ou no modo de prevenção no nível da política.</span><span class="sxs-lookup"><span data-stu-id="caf05-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="caf05-126">Os valores possíveis incluem:'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="caf05-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-127">-Name</span><span class="sxs-lookup"><span data-stu-id="caf05-127">-Name</span></span>
<span data-ttu-id="caf05-128">Nome WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="caf05-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="caf05-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="caf05-129">-RedirectUrl</span></span>
<span data-ttu-id="caf05-130">URL de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="caf05-130">Redirect URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-131">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="caf05-131">-RequestBodyCheck</span></span>
<span data-ttu-id="caf05-132">Define se o corpo deve ser inspecionado por regras gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="caf05-132">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="caf05-133">Os valores possíveis incluem: 'Habilitado', 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="caf05-133">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf05-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf05-134">-ResourceGroupName</span></span>
<span data-ttu-id="caf05-135">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="caf05-135">The resource group name</span></span>

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

### <span data-ttu-id="caf05-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caf05-136">-Confirm</span></span>
<span data-ttu-id="caf05-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caf05-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caf05-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf05-138">-WhatIf</span></span>
<span data-ttu-id="caf05-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="caf05-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caf05-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="caf05-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caf05-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf05-141">CommonParameters</span></span>
<span data-ttu-id="caf05-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf05-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf05-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="caf05-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf05-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="caf05-144">INPUTS</span></span>

### <span data-ttu-id="caf05-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="caf05-145">None</span></span>

## <span data-ttu-id="caf05-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="caf05-146">OUTPUTS</span></span>

### <span data-ttu-id="caf05-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="caf05-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="caf05-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="caf05-148">NOTES</span></span>

## <span data-ttu-id="caf05-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="caf05-149">RELATED LINKS</span></span>

<span data-ttu-id="caf05-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="caf05-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
