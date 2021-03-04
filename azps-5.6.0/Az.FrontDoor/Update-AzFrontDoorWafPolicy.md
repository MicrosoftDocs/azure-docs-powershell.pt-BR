---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: bc4aa72d202938b5727245386f3485fbc43a6ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887525"
---
# <span data-ttu-id="46aea-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="46aea-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="46aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46aea-102">SYNOPSIS</span></span>
<span data-ttu-id="46aea-103">Atualizar política WAF</span><span class="sxs-lookup"><span data-stu-id="46aea-103">Update WAF policy</span></span>

## <span data-ttu-id="46aea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="46aea-104">SYNTAX</span></span>

### <span data-ttu-id="46aea-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46aea-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46aea-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46aea-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46aea-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46aea-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46aea-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="46aea-108">DESCRIPTION</span></span>
<span data-ttu-id="46aea-109">O cmdlet **Update-AzFrontDoorWafPolicy** atualiza uma política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="46aea-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="46aea-110">Se os parâmetros de entrada não são fornecidos, parâmetros antigos da política WAF existente serão usados.</span><span class="sxs-lookup"><span data-stu-id="46aea-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="46aea-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46aea-111">EXAMPLES</span></span>

### <span data-ttu-id="46aea-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46aea-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="46aea-113">Atualize um código de status personalizado de política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="46aea-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="46aea-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="46aea-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="46aea-115">Atualize um modo de política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="46aea-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="46aea-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="46aea-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="46aea-117">Atualize um estado e modo de política WAF existentes.</span><span class="sxs-lookup"><span data-stu-id="46aea-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="46aea-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="46aea-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="46aea-119">Atualizar todas as políticas waf no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46aea-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="46aea-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="46aea-120">PARAMETERS</span></span>

### <span data-ttu-id="46aea-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="46aea-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="46aea-122">Corpo da Resposta Personalizado</span><span class="sxs-lookup"><span data-stu-id="46aea-122">Custom Response Body</span></span>

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

### <span data-ttu-id="46aea-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="46aea-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="46aea-124">Código de Status da Resposta Personalizado</span><span class="sxs-lookup"><span data-stu-id="46aea-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46aea-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="46aea-125">-Customrule</span></span>
<span data-ttu-id="46aea-126">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="46aea-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="46aea-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46aea-127">-DefaultProfile</span></span>
<span data-ttu-id="46aea-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46aea-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46aea-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="46aea-129">-EnabledState</span></span>
<span data-ttu-id="46aea-130">Se a política está em estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="46aea-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="46aea-131">Os valores possíveis incluem: 'Disabled', 'Enabled'</span><span class="sxs-lookup"><span data-stu-id="46aea-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="46aea-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46aea-132">-InputObject</span></span>
<span data-ttu-id="46aea-133">O objeto FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="46aea-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46aea-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="46aea-134">-ManagedRule</span></span>
<span data-ttu-id="46aea-135">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="46aea-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="46aea-136">-Mode</span><span class="sxs-lookup"><span data-stu-id="46aea-136">-Mode</span></span>
<span data-ttu-id="46aea-137">Descreve se ele está no modo de detecção ou no modo de prevenção no nível da política.</span><span class="sxs-lookup"><span data-stu-id="46aea-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="46aea-138">Os valores possíveis incluem:'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="46aea-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="46aea-139">-Name</span><span class="sxs-lookup"><span data-stu-id="46aea-139">-Name</span></span>
<span data-ttu-id="46aea-140">O nome do FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="46aea-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46aea-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="46aea-141">-RedirectUrl</span></span>
<span data-ttu-id="46aea-142">URL de redirecionamento</span><span class="sxs-lookup"><span data-stu-id="46aea-142">Redirect URL</span></span>

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

### <span data-ttu-id="46aea-143">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="46aea-143">-RequestBodyCheck</span></span>
<span data-ttu-id="46aea-144">Define se o corpo deve ser inspecionado por regras gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="46aea-144">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="46aea-145">Os valores possíveis incluem: 'Habilitado', 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="46aea-145">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="46aea-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46aea-146">-ResourceGroupName</span></span>
<span data-ttu-id="46aea-147">O grupo de recursos ao qual o FireWallPolicy pertence.</span><span class="sxs-lookup"><span data-stu-id="46aea-147">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46aea-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46aea-148">-ResourceId</span></span>
<span data-ttu-id="46aea-149">ID de recurso do FireWallPolicy a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="46aea-149">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46aea-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46aea-150">-Confirm</span></span>
<span data-ttu-id="46aea-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46aea-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46aea-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46aea-152">-WhatIf</span></span>
<span data-ttu-id="46aea-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46aea-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46aea-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46aea-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46aea-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46aea-155">CommonParameters</span></span>
<span data-ttu-id="46aea-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46aea-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46aea-157">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46aea-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46aea-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46aea-158">INPUTS</span></span>

### <span data-ttu-id="46aea-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="46aea-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="46aea-160">System.String</span><span class="sxs-lookup"><span data-stu-id="46aea-160">System.String</span></span>

## <span data-ttu-id="46aea-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="46aea-161">OUTPUTS</span></span>

### <span data-ttu-id="46aea-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="46aea-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="46aea-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="46aea-163">NOTES</span></span>

## <span data-ttu-id="46aea-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46aea-164">RELATED LINKS</span></span>

<span data-ttu-id="46aea-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="46aea-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
