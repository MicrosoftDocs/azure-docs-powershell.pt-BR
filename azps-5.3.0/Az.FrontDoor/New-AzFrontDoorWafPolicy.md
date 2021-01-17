---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 441e47b4ef2a796fcdf5ee802cba83f0fce7e352
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426913"
---
# <span data-ttu-id="4c32c-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="4c32c-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="4c32c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c32c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c32c-103">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="4c32c-103">Create WAF policy</span></span>

## <span data-ttu-id="4c32c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c32c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c32c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c32c-105">DESCRIPTION</span></span>
<span data-ttu-id="4c32c-106">O cmdlet **New-AzFrontDoorWafPolicy** cria uma nova política do Azure WAF no grupo de recursos especificado na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="4c32c-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="4c32c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c32c-107">EXAMPLES</span></span>

### <span data-ttu-id="4c32c-108">Exemplo 1: criar uma política WAF</span><span class="sxs-lookup"><span data-stu-id="4c32c-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="4c32c-109">Criar política WAF</span><span class="sxs-lookup"><span data-stu-id="4c32c-109">Create WAF policy</span></span>

## <span data-ttu-id="4c32c-110">OS</span><span class="sxs-lookup"><span data-stu-id="4c32c-110">PARAMETERS</span></span>

### <span data-ttu-id="4c32c-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="4c32c-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="4c32c-112">Corpo de resposta personalizado</span><span class="sxs-lookup"><span data-stu-id="4c32c-112">Custom Response Body</span></span>

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

### <span data-ttu-id="4c32c-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="4c32c-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="4c32c-114">Código de status de resposta personalizado</span><span class="sxs-lookup"><span data-stu-id="4c32c-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="4c32c-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="4c32c-115">-Customrule</span></span>
<span data-ttu-id="4c32c-116">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="4c32c-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="4c32c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c32c-117">-DefaultProfile</span></span>
<span data-ttu-id="4c32c-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c32c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c32c-119">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="4c32c-119">-EnabledState</span></span>
<span data-ttu-id="4c32c-120">Se a política está no estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4c32c-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="4c32c-121">Os valores possíveis incluem: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="4c32c-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="4c32c-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="4c32c-122">-ManagedRule</span></span>
<span data-ttu-id="4c32c-123">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="4c32c-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="4c32c-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="4c32c-124">-Mode</span></span>
<span data-ttu-id="4c32c-125">Descreve se ele está no modo de detecção ou no modo de prevenção em nível de política.</span><span class="sxs-lookup"><span data-stu-id="4c32c-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="4c32c-126">Os valores possíveis incluem: ' Prevention ', ' detecção '</span><span class="sxs-lookup"><span data-stu-id="4c32c-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="4c32c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c32c-127">-Name</span></span>
<span data-ttu-id="4c32c-128">Nome do WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="4c32c-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="4c32c-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="4c32c-129">-RedirectUrl</span></span>
<span data-ttu-id="4c32c-130">Redirecionar URL</span><span class="sxs-lookup"><span data-stu-id="4c32c-130">Redirect URL</span></span>

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

### <span data-ttu-id="4c32c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c32c-131">-ResourceGroupName</span></span>
<span data-ttu-id="4c32c-132">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4c32c-132">The resource group name</span></span>

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

### <span data-ttu-id="4c32c-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c32c-133">-Confirm</span></span>
<span data-ttu-id="4c32c-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c32c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c32c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c32c-135">-WhatIf</span></span>
<span data-ttu-id="4c32c-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c32c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c32c-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c32c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c32c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c32c-138">CommonParameters</span></span>
<span data-ttu-id="4c32c-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c32c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c32c-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c32c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c32c-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c32c-141">INPUTS</span></span>

### <span data-ttu-id="4c32c-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4c32c-142">None</span></span>

## <span data-ttu-id="4c32c-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c32c-143">OUTPUTS</span></span>

### <span data-ttu-id="4c32c-144">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="4c32c-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="4c32c-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c32c-145">NOTES</span></span>

## <span data-ttu-id="4c32c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c32c-146">RELATED LINKS</span></span>

<span data-ttu-id="4c32c-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="4c32c-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
