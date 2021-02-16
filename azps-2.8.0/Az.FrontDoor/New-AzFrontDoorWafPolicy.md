---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 0612f8bddf69e36fe8084bf27dbb44635059ee1a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408909"
---
# <span data-ttu-id="ec3a7-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="ec3a7-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="ec3a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3a7-103">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="ec3a7-103">Create WAF policy</span></span>

## <span data-ttu-id="ec3a7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec3a7-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec3a7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec3a7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec3a7-106">O cmdlet **New-AzFrontDoorWafPolicy** cria uma nova política WAF do Azure no grupo de recursos especificado sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="ec3a7-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="ec3a7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ec3a7-107">EXAMPLES</span></span>

### <span data-ttu-id="ec3a7-108">Exemplo 1: Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="ec3a7-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="ec3a7-109">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="ec3a7-109">Create WAF policy</span></span>

## <span data-ttu-id="ec3a7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec3a7-110">PARAMETERS</span></span>

### <span data-ttu-id="ec3a7-111">-CustomBlockResponseBlock</span><span class="sxs-lookup"><span data-stu-id="ec3a7-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="ec3a7-112">Corpo de Resposta Personalizado</span><span class="sxs-lookup"><span data-stu-id="ec3a7-112">Custom Response Body</span></span>

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

### <span data-ttu-id="ec3a7-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="ec3a7-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="ec3a7-114">Código de Status de Resposta Personalizado</span><span class="sxs-lookup"><span data-stu-id="ec3a7-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="ec3a7-115">-Regras personalizadas</span><span class="sxs-lookup"><span data-stu-id="ec3a7-115">-Customrule</span></span>
<span data-ttu-id="ec3a7-116">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="ec3a7-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="ec3a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec3a7-117">-DefaultProfile</span></span>
<span data-ttu-id="ec3a7-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec3a7-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ec3a7-119">-EnabledState</span></span>
<span data-ttu-id="ec3a7-120">Se a política está em estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="ec3a7-121">Os valores possíveis incluem: 'Desabilitado', 'Habilitado'</span><span class="sxs-lookup"><span data-stu-id="ec3a7-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="ec3a7-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="ec3a7-122">-ManagedRule</span></span>
<span data-ttu-id="ec3a7-123">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="ec3a7-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="ec3a7-124">-Modo</span><span class="sxs-lookup"><span data-stu-id="ec3a7-124">-Mode</span></span>
<span data-ttu-id="ec3a7-125">Descreve se ele está no modo de detecção ou no modo de prevenção no nível da política.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="ec3a7-126">Os valores possíveis incluem:'Prevenção', 'Detecção'</span><span class="sxs-lookup"><span data-stu-id="ec3a7-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="ec3a7-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec3a7-127">-Name</span></span>
<span data-ttu-id="ec3a7-128">Nome WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="ec3a7-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="ec3a7-129">-RedirectUrl</span></span>
<span data-ttu-id="ec3a7-130">Redirecionar URL</span><span class="sxs-lookup"><span data-stu-id="ec3a7-130">Redirect URL</span></span>

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

### <span data-ttu-id="ec3a7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec3a7-131">-ResourceGroupName</span></span>
<span data-ttu-id="ec3a7-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ec3a7-132">The resource group name</span></span>

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

### <span data-ttu-id="ec3a7-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ec3a7-133">-Confirm</span></span>
<span data-ttu-id="ec3a7-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec3a7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec3a7-135">-WhatIf</span></span>
<span data-ttu-id="ec3a7-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec3a7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec3a7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3a7-138">CommonParameters</span></span>
<span data-ttu-id="ec3a7-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec3a7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3a7-140">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec3a7-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3a7-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="ec3a7-141">INPUTS</span></span>

### <span data-ttu-id="ec3a7-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ec3a7-142">None</span></span>

## <span data-ttu-id="ec3a7-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="ec3a7-143">OUTPUTS</span></span>

### <span data-ttu-id="ec3a7-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ec3a7-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="ec3a7-145">Notas</span><span class="sxs-lookup"><span data-stu-id="ec3a7-145">NOTES</span></span>

## <span data-ttu-id="ec3a7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec3a7-146">RELATED LINKS</span></span>

<span data-ttu-id="ec3a7-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="ec3a7-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
